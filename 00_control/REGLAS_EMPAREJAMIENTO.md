---
doc_type: reglas
aplica_a: "emparejador v4"
estado: "BORRADOR"
actualizado: 2026-10-22
---

# Reglas de emparejamiento activas

Lo que decide si un alta y una baja pueden formar pareja. El emparejador las aplica como **filtros duros**: una pareja que incumple una regla no entra en el grafo, por buena que sea en lo demás. Entre las parejas que sí entran, el emparejador busca el máximo y desempata como dice el apartado «Cómo se elige entre parejas válidas».

Fuentes normativas: ficha TRA050 v1.1 y criterio 25-11.01 (`docs/conocimiento/`). Las decisiones del usuario llevan su fecha.

## Las reglas, por número

Cada regla tiene código y nombre corto, y se cita siempre con los dos: «R5 Ventana», nunca «R5» a secas.


- **R1 Sociedad · Misma sociedad del grupo.** `cod_sociedad` del alta igual al de la baja. Nunca el CIF del titular registral, que en renting es la arrendadora.
- **R2 Posesión · Posesión mínima de la baja.** Más de 365 días en propiedad; 730 o más si se tuvo por contrato, sea cual sea su nombre.
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
- **R5 Ventana · Ventana temporal.** La salida de la baja cae entre 3 meses antes y 6 meses después de la adquisición del alta, con los dos extremos incluidos.
    - Fecha de adquisición del alta: **la de la factura** (decisión del usuario del 2026-10-22). La matriculación se anota al lado, y si discrepa de la factura va a reparos.
    - Fecha de salida de la baja: la del documento de R9 Salida (acta de entrega, desguace, compraventa o cambio de titularidad).
- **R6 Año · Año de ejecución 2024 o posterior.** La factura del alta es del 1 de enero de 2024 en adelante.
    - La ficha admite desde el 25/01/2023, pero las compras de 2023 ya no son susceptibles de CAE (decisión del usuario del 2026-09-24, confirmada el 2026-10-22).
- **R7 Alta nueva · El alta es nueva**, o de segunda mano con primera matriculación anterior al 25/01/2023 que no haya generado CAE.
    - En Global Omnium todas las altas son nuevas. Si apareciera una de segunda mano, va a `REVISAR`.
- **R8 Titularidad · El alta está matriculada a nombre de la sociedad**, o de la empresa de renting si el alta es en renting.
- **R9 Salida · La baja ya no está en poder del solicitante**, y consta la fecha de salida.
    - Renting: acta de entrega firmada en conformidad.
    - Propiedad: certificado de desguace, cambio de titularidad en la DGT, contrato de compraventa, factura del concesionario que recoja el coche viejo o nuevo permiso a nombre de otro.
    - Desde el 1 de julio de 2026, compraventa y nuevo permiso van con declaración responsable de no conviviente.
    - M2, M3 y N que quedan en depósito para piezas: basta la documentación oficial de que están inmovilizados y sin permiso de circulación.

## Dónde se evalúa cada una

- **En la ficha del coche** (`03_coches/`), porque solo dependen de ese coche. Si un coche falla una, no entra en ninguna pareja.
    - Alta: R3a Alta eléctrica, R4a Categoría admitida, R6 Año, R7 Alta nueva y R8 Titularidad.
    - Baja: R2 Posesión, R3b Baja de combustión, R4a Categoría admitida y R9 Salida.
- **En la pareja**, para cada combinación alta × baja que ha pasado las reglas del coche: R1 Sociedad, R4b Misma subcategoría y R5 Ventana.

## Cómo se aplica cada regla

- Cada regla da uno de tres resultados:
    - `OK`: se cumple.
    - `FALLA`: no se cumple. La pareja no existe.
    - `SIN_DATOS`: falta el dato para decidir. La pareja no entra en el grafo, pero se apunta como **arista potencial** con el dato que falta, para pedírselo al cliente.
- El dato puede venir de un documento o solo del Excel:
    - Con documento, la regla queda **acreditada**.
    - Con Excel, la regla queda **indiciaria**: la pareja entra en el grafo y el dato queda en `pendientes` de su nota, para pedir el documento.
    - Si el documento y el Excel discrepan, manda el documento y la discrepancia queda anotada.
- Si una persona corrigió un dato a mano (`_fuente: "MANUAL"`), manda ese dato.

## Lo que no es regla de emparejamiento

Se exige al expediente, pero no cambia qué parejas existen. Se comprueba en la nota de la pareja, en la auditoría.

- Contraprestación económica explícita en la cesión.
- Firma manuscrita con DNI del firmante.
- NIF, matrícula y bastidor coherentes en todos los documentos.
- Que el cálculo del ahorro coincida con la ficha.

## Cómo se elige entre parejas válidas

- **1 · Máximo número de parejas.** Emparejamiento de máxima cardinalidad sobre el grafo de parejas que pasan todas las reglas, resuelto por separado en cada sociedad (R1 Sociedad ya las separa).
    - **Certificado**: para cada sociedad y categoría se calcula también la cobertura mínima de vértices. Por el teorema de König, si coincide con el número de parejas, está demostrado que no cabe ni una más con los datos actuales.
- **2 · Entre los máximos, más ahorro.** La combinación que suma más kWh/año. A igual ahorro, la pareja que ya se propuso en agosto.
- **Parejas fijadas.** Una pareja en `estado_pareja: FIJADA` no se vuelve a calcular: sus dos coches salen del grafo antes de empezar. El emparejador solo reparte lo que queda libre.

## Sin niveles

Las parejas no llevan nivel de documentación: el usuario los quitó el 2026-10-22. La nota de cada pareja anota, sin clasificarla, dos listas:

- `pendientes`: reglas que se cumplen solo con el Excel o la ficha de agosto; falta el documento.
- `reparos`: lo que pide una decisión o un documento especial: siniestro, factura y matriculación que discrepan, o contrato con etiqueta dudosa.

Una pareja que incumple una regla y no tiene arreglo **no se queda marcada: se retira** a `_0bsoleto/` (criterio del usuario del 2026-08-19).

## Cambios respecto al emparejador v3 (agosto de 2026)

- R6 Año pasa del 25/01/2023 al 1/1/2024.
- R4 Categoría deja de usar la categoría del Excel y pasa a la subcategoría de homologación.
- R5 Ventana toma la fecha de la factura del documento, no la del Excel. Si la factura y la matriculación discrepan, queda anotado como reparo.
- Desaparece la posesión `DEFENDIBLE` contada desde la matriculación, que el v3 seguía admitiendo.
- Desaparecen los niveles de pareja del v3 (A, B y C).
- Los datos que faltan dejan de descartar en silencio: generan aristas potenciales.
- Nuevas como reglas explícitas: R7 Alta nueva, R8 Titularidad y R9 Salida.
- Se añaden el certificado de máximo y las parejas fijadas.
