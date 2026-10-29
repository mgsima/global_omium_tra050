---
doc_type: reglas
aplica_a: "emparejador v4"
estado: "BORRADOR"
actualizado: 2026-10-22
---
# Reglas de emparejamiento activas

Deciden si alta y baja forman pareja. Emparejador las aplica como **filtros duros**: pareja que incumple regla no entra en grafo, aunque sea buena en lo demás. Entre parejas que entran, busca máximo y desempata según «Cómo se elige entre parejas válidas».

Fuentes normativas: ficha TRA050 v1.1 y criterio 25-11.01 (`docs/conocimiento/`). Decisiones del usuario llevan fecha.

## Las reglas, por número

Cada regla: código + nombre corto, citar siempre ambos: «R5 Ventana», nunca «R5» solo.


- **R1 Sociedad · Misma sociedad del grupo.** `cod_sociedad` alta = baja. Nunca CIF del titular registral (en renting = arrendadora).
- **R2 Posesión · Posesión mínima de la baja.** >365 días en propiedad; ≥730 si por contrato, sea cual sea su nombre.
    - Se cuentan los días reales de posesión del solicitante: del inicio del contrato a la devolución en renting, y de la fecha en que el permiso de circulación pone el coche a nombre de la sociedad a la de salida en propiedad (decisión del usuario del 2026-10-22).
    - Si la sociedad compró el coche nuevo, esa fecha coincide con la matriculación y vale.
    - Fuera de ese caso, contar desde la matriculación no vale nunca: prueba la edad del coche y no quién lo tuvo (criterio del usuario del 2026-08-19).
    - La etiqueta del contrato en el Excel no descarta por sí sola. Descarta el tiempo real.
- **R3 Propulsión.**
    - R3a Alta eléctrica: el alta es eléctrica pura. Híbridos, PHEV y de autonomía extendida no valen como vehículo nuevo.
    - R3b Baja de combustión: la baja es de combustión, híbridos incluidos. Solo se excluye el eléctrico puro como sustituido.
- **R4 Categoría.**
    - R4a Categoría admitida: los dos coches son de categoría M, N o L según la homologación. Remolques, maquinaria y matrículas que no son vehículos quedan fuera.
    - R4b Misma subcategoría: alta y baja tienen la misma subcategoría de homologación: M1 con M1, N1 con N1, N2 con N2, L3e con L3e (decisión del usuario del 2026-10-22, por ahora).
    - Se lee de la ficha técnica o del permiso (campo J), no de la categoría interna del Excel («Turismo», «Furgoneta», «Camión»). El Excel solo sirve de indicio cuando no hay documento.
- **R5 Ventana · Ventana temporal.** Salida de baja entre 3 meses antes y 6 meses después de adquisición del alta, extremos incluidos.
    - Fecha de adquisición del alta: **la de la factura** (decisión del usuario del 2026-10-22). La matriculación se anota al lado, y si discrepa de la factura va a reparos.
    - Fecha de salida de la baja: la del documento de R9 Salida (acta de entrega, desguace, compraventa o cambio de titularidad).
- **R6 Año · Año de ejecución 2024 o posterior.** Factura del alta desde 1 enero 2024.
    - La ficha admite desde el 25/01/2023, pero las compras de 2023 ya no son susceptibles de CAE (decisión del usuario del 2026-09-24, confirmada el 2026-10-22).
- **R7 Alta nueva · El alta es nueva**, o segunda mano con primera matriculación anterior a 25/01/2023 sin CAE generado.
    - En Global Omnium todas las altas son nuevas. Si apareciera una de segunda mano, va a `REVISAR`.
- **R8 Titularidad · El alta está matriculada a nombre de la sociedad**, o de empresa de renting si alta en renting.
- **R9 Salida · La baja ya no está en poder del solicitante**, y consta fecha de salida.
    - Renting: acta de entrega firmada en conformidad.
    - Propiedad: certificado de desguace, cambio de titularidad en la DGT, contrato de compraventa, factura del concesionario que recoja el coche viejo o nuevo permiso a nombre de otro.
    - Desde el 1 de julio de 2026, compraventa y nuevo permiso van con declaración responsable de no conviviente.
    - M2, M3 y N que quedan en depósito para piezas: basta la documentación oficial de que están inmovilizados y sin permiso de circulación.

## Dónde se evalúa cada una

- **En la ficha del coche** (`03_coches/`): solo dependen de ese coche. Coche que falla una no entra en ninguna pareja.
    - Alta: R3a Alta eléctrica, R4a Categoría admitida, R6 Año, R7 Alta nueva y R8 Titularidad.
    - Baja: R2 Posesión, R3b Baja de combustión, R4a Categoría admitida y R9 Salida.
- **En la pareja**, por cada combinación alta × baja que pasó reglas del coche: R1 Sociedad, R4b Misma subcategoría y R5 Ventana.

## Cómo se aplica cada regla

- Cada regla da uno de tres resultados:
    - `OK`: se cumple.
    - `FALLA`: no se cumple. La pareja no existe.
    - `SIN_DATOS`: falta el dato para decidir. La pareja no entra en el grafo, pero se apunta como **arista potencial** con el dato que falta, para pedírselo al cliente.
- Dato viene de documento o solo de Excel:
    - Con documento, la regla queda **acreditada**.
    - Con Excel, la regla queda **indiciaria**: la pareja entra en el grafo y el dato queda en `pendientes` de su nota, para pedir el documento.
    - Si el documento y el Excel discrepan, manda el documento y la discrepancia queda anotada.
- Dato corregido a mano (`_fuente: "MANUAL"`) manda.

## Lo que no es regla de emparejamiento

Se exige al expediente, no cambia qué parejas existen. Se comprueba en nota de pareja, en auditoría.

- Contraprestación económica explícita en cesión.
- Firma manuscrita con DNI del firmante.
- NIF, matrícula y bastidor coherentes en todos los documentos.
- Cálculo del ahorro coincide con ficha.

## Cómo se elige entre parejas válidas

- **1 · Máximo número de parejas.** Emparejamiento de máxima cardinalidad sobre grafo de parejas que pasan todas las reglas, resuelto por separado por sociedad (R1 Sociedad ya las separa).
    - **Certificado**: para cada sociedad y categoría se calcula también la cobertura mínima de vértices. Por el teorema de König, si coincide con el número de parejas, está demostrado que no cabe ni una más con los datos actuales.
- **2 · Entre los máximos, más ahorro.** Combinación con más kWh/año. Empate: pareja ya propuesta en agosto.
- **Parejas fijadas.** Pareja en `estado_pareja: FIJADA` no se recalcula: sus dos coches salen del grafo antes de empezar. Emparejador solo reparte lo libre.

## Sin niveles

Parejas sin nivel de documentación: usuario los quitó 2026-10-22. Nota de cada pareja anota, sin clasificar, dos listas:

- `pendientes`: reglas cumplidas solo con Excel o ficha de agosto; falta documento.
- `reparos`: lo que pide decisión o documento especial: siniestro, factura y matriculación discrepan, o contrato con etiqueta dudosa.

Pareja que incumple regla sin arreglo **no se queda marcada: se retira** a `_0bsoleto/` (criterio usuario 2026-08-19).

## Cambios respecto al emparejador v3 (agosto de 2026)

- R6 Año: de 25/01/2023 a 1/1/2024.
- R4 Categoría: deja categoría del Excel, usa subcategoría de homologación.
- R5 Ventana: fecha de factura del documento, no del Excel. Factura y matriculación discrepan → reparo.
- Desaparece posesión `DEFENDIBLE` contada desde matriculación, que v3 admitía.
- Desaparecen niveles de pareja v3 (A, B, C).
- Datos faltantes ya no descartan en silencio: generan aristas potenciales.
- Nuevas reglas explícitas: R7 Alta nueva, R8 Titularidad, R9 Salida.
- Se añaden certificado de máximo y parejas fijadas.