---
doc_type: informe
tema: "Cómo se han elegido las parejas alta-baja: recorrido para una auditoría externa"
fecha: 2026-10-29
emparejador: v4
tags:
    - global_omnium
    - emparejamiento
---

# Cómo se han elegido las parejas: recorrido para auditar el proceso

Este documento explica, paso a paso, cómo se pasa de la flota de Global Omnium a las parejas alta-baja que se proponen para la ficha TRA050. Está pensado para que alguien ajeno al trabajo pueda comprobar cada paso y repetirlo.

- Foto a 2026-10-29. Las cifras salen de `emparejar_v4.py --seco` con las fichas de ese día.
- Una **alta** es el vehículo eléctrico nuevo; una **baja** es el vehículo de combustión al que sustituye. Una **pareja** es una alta y una baja que se presentan juntas como una actuación.
- Las reglas se citan con número y nombre («R5 Ventana»). Su texto completo está en [[REGLAS_EMPAREJAMIENTO]].

## Resultado en una línea

- 473 vehículos (244 altas y 229 bajas) → 66 parejas propuestas, con un ahorro estimado de 410.484 kWh/año.
    - 51 parejas sin reparos de fondo.
    - 15 parejas **dudosas**: la baja salió por siniestro según el Excel del cliente. En general no se pueden presentar.
- Está demostrado que, con los datos actuales, no caben más parejas en ninguna sociedad (certificado del paso 6).
- Si se consiguiera el único dato que falta (la fecha de salida de la baja 0894LKM), el techo sería 67.

## Historia: por qué hay un emparejamiento v4

- **Julio de 2026 (v2):** primer emparejador automático sobre el Excel de flota.
- **Agosto de 2026 (v3):** 69 parejas, con niveles de documentación A, B y C.
    - El 2026-08-19 se retiraron 4 parejas porque la baja no llegaba a los 730 días de posesión por contrato; no había bajas libres para sustituirlas. Quedaron 65.
    - v3 admitía una posesión «defendible» contada desde la matriculación del coche, que no prueba quién lo tuvo.
- **2026-10-22:** se decide rehacer el emparejamiento desde cero.
    - Las compras de 2023 dejan de ser susceptibles de CAE: los 5 expedientes del ejercicio 2023 pasan a `RECHAZADO`.
    - Se retira el emparejamiento de agosto entero a `_0bsoleto/03_expedientes/`. No se borra: lo escrito a mano en él (68 revisiones manuales y datos corregidos) se trae a las fichas nuevas.
    - Se fijan las reglas v4. Cambios respecto a v3:
        - R6 Año desde el 1/1/2024;
        - R4 por subcategoría de homologación y no por la categoría del Excel;
        - R5 con la fecha de la factura;
        - desaparecen la posesión «defendible» y los niveles A, B y C;
        - los datos que faltan ya no descartan en silencio.
- **2026-10-29:**
    - Revisión de las 54 bajas descartadas por R2 Posesión: 2 estaban mal descartadas (9244JFB y 0370LXS) y se corrigieron. Las parejas pasan de 63 a 64. Detalle en [[2026-10-29_revision_R2_posesion]].
    - Se da preferencia a las bajas sin siniestro (paso 5). El reparto pasa de 48 parejas limpias + 16 con siniestro a 49 + 15.
    - Auditoría integral del emparejamiento: se corrige en `coches.py` la prioridad entre `F.Devolución/Baja` y `F.Vig.Final` del Excel, la normalización de `"GAS-OIL"` y `"GAS LICUADO DE PETROLEO"` en `reglas_v4.py`, las categorías reales de 4 camiones pesados `N3`, 7 semirremolques `O4`, 1 tractor y 2 VW Caddy Kombi `M1` con ficha técnica girada (`5443LLD` y `5493LLD`), las fechas manuscritas de 8 actas de devolución verificadas en PDF (`5949LLV`, `9431LKC`, `4450LLV`, `5493LLD`, `6741LLV`, `4170LKY`, `8066LKY` y `4988LLY`) y el combustible de `1066MWL`, `0777MJM` y `2657KZK`. Se depuran 5 parejas inválidas y entran 7 parejas limpias válidas: el total pasa a **66 parejas (51 limpias y 15 dudosas · 410.484 kWh/año)** y se escriben las notas en `04_parejas/` y el registro en `00_control/emparejamiento/`.

## Paso 1 · Universo: una ficha por vehículo

- Fuentes:
    - el Excel de flota del cliente (`01_entrada/_flota/`);
    - las carpetas de documentos por matrícula (`01_entrada/ALTAS/` y `01_entrada/BAJAS/`): 156 altas y 161 bajas con documentos.
- `scripts/global_omnium/coches.py` escribe una ficha por vehículo en `03_coches/<MATRICULA>.md`: 473 en total, incluidos los que solo constan en el Excel (`tiene_documentos: false`).
- Cada dato que decide una regla lleva su fuente en un campo `<dato>_fuente`:
    - `DOCUMENTO`: leído del PDF;
    - `EXTRACCION`: extraído del PDF de forma automática;
    - `EXCEL`: solo lo dice el Excel;
    - `MANUAL`: corregido a mano después de revisar el original. Este valor manda sobre los demás.
- Si el documento y el Excel discrepan, manda el documento y la discrepancia queda anotada.

## Paso 2 · Reglas de cada vehículo por separado

- Se evalúan en la ficha, porque solo dependen de ese vehículo. Un vehículo que falla una no entra en ninguna pareja.
    - Altas: R3a Alta eléctrica, R4a Categoría admitida, R6 Año, R7 Alta nueva y R8 Titularidad.
    - Bajas: R2 Posesión, R3b Baja de combustión, R4a Categoría admitida y R9 Salida.
- Resultado:
    - 42 altas descartadas por R6 Año (factura anterior a 2024). Quedan 202.
    - 63 bajas descartadas: 54 por R2 Posesión y 9 por R4a Categoría admitida (8 remolques/semirremolques y 1 tractor). Quedan 166.

## Paso 3 · Reglas de cada combinación alta-baja

- Se prueban todas las combinaciones de las 202 altas con las 166 bajas: 33.532.
- R1 Sociedad: alta y baja deben ser de la misma sociedad del grupo (`cod_sociedad`). Quedan 2.646 combinaciones.
- Sobre esas se aplican R4b Misma subcategoría (M1 con M1, N1 con N1…) y R5 Ventana (la baja sale entre 3 meses antes y 6 meses después de la factura del alta):
    - 676 fallan solo R5 Ventana;
    - 667 fallan solo R4b Misma subcategoría;
    - 462 fallan las dos;
    - 18 no se pueden decidir porque falta un dato (todas de la baja 0894LKM, sin fecha de salida): son **potenciales**;
    - **823 son admisibles**: cumplen todas las reglas.
- Cada regla da `OK`, `FALLA` o `SIN_DATOS`. Una combinación con algún `FALLA` no existe; una con `SIN_DATOS` se apunta aparte con el dato que falta.

## Paso 4 · Cumplir con el Excel no es lo mismo que acreditar

- Si una regla se cumple solo con el dato del Excel, la pareja entra igual, pero la regla queda **indiciaria**: se apunta en `pendientes`, para pedir el documento.
- Lo que pide una decisión o un documento especial se apunta en `reparos`:
    - baja por siniestro: hace falta la baja definitiva en la DGT;
    - la factura y la matriculación del alta difieren en más de 31 días;
    - contrato con etiqueta dudosa en el Excel.
- Ni pendientes ni reparos cambian qué parejas existen; sirven para la auditoría de cada expediente.

## Paso 5 · Elegir las parejas entre las admisibles

- Con las 823 combinaciones admisibles se forma un grafo: cada vehículo es un nodo y cada combinación admisible, una arista. Cada alta y cada baja pueden estar como mucho en una pareja.
- La elección es un emparejamiento de grafo bipartito (librería `networkx`). Criterios, en orden estricto: cada uno pesa más que todos los siguientes juntos.
    - **0 · Más parejas sin siniestro.** Una baja que salió por siniestro (`salida_tipo: SINIESTRO`, del Excel: «CANCELADO POR SINIESTRO») en general no se puede presentar. Su pareja solo se elige si no hay otra baja sin siniestro que pueda ocupar ese hueco, y queda marcada `DUDOSA` (criterio del 2026-10-29).
    - **1 · Más parejas en total.**
    - **2 · Más ahorro estimado (kWh/año).**
    - **3 · A igualdad, la pareja que ya se propuso en agosto**, para no cambiar sin motivo parejas que daban igual.
- Las parejas `FIJADA` (con trabajo encima o papeles pedidos al cliente) no se recalculan: sus dos vehículos salen del grafo antes de empezar. Hoy no hay ninguna.
- Resultado: 66 parejas, 51 limpias y 15 dudosas.
    - De las 823 aristas, 136 tienen una baja por siniestro.
    - Las 15 parejas con siniestro restantes no tienen alternativa limpia admisible en su sociedad y categoría.

## Paso 6 · Certificado de que no caben más

- Para cada sociedad se calcula, además del emparejamiento, la **cobertura mínima de vértices**: el menor conjunto de vehículos que toca todas las aristas admisibles.
- Por el teorema de König, en un grafo bipartito el emparejamiento máximo y la cobertura mínima tienen el mismo tamaño. Si coinciden con el número de parejas elegidas, está demostrado que no cabe ni una más.
- Hoy coinciden en todas las sociedades («demostrado» en la salida del emparejador). Los criterios 0, 2 y 3 del paso 5 no han costado ninguna pareja.
- Las sociedades con más parejas:
    - 1001 AVSA: 28 altas y 31 bajas → 18 parejas.
    - 1505 CGAC: 20 altas y 15 bajas → 9 parejas.
    - 1200 EMIVASA: 57 altas y 10 bajas → 7 parejas.

## Por qué hay vehículos sin pareja

- **No elegible:** falla una regla propia del vehículo (paso 2): 42 altas y 63 bajas.
- **Sin pareja posible:** pasa sus reglas, pero ninguna combinación con la otra parte es admisible (casi siempre R4b o R5): 33 altas y 96 bajas.
- **Compite y pierde:** tiene combinaciones admisibles, pero todas sus posibles parejas ya están emparejadas con otros: 103 altas y 3 bajas. El emparejamiento es máximo, así que darle pareja a uno de estos quitaría la suya a otro.
    - Sobran altas: el cuello de botella son las bajas compatibles.
- **Falta un dato:** 1 baja (0894LKM), sin fecha de salida.
- Diagramas de estos flujos: [[2026-10-29_sankey_altas_bajas]].

## Cómo repetirlo y qué revisar

- Ejecución:
    - `python3 scripts/global_omnium/coches.py --todas` regenera las fichas sin pisar lo escrito a mano;
    - `python3 scripts/global_omnium/emparejar_v4.py --seco` cuenta y certifica sin escribir nada;
    - sin `--seco`, escribe el registro completo en `00_control/emparejamiento/` y las notas de pareja en `04_parejas/`.
- La pieza central para auditar en `00_control/emparejamiento/aristas.csv`:
    - las 823 combinaciones admisibles, no solo las elegidas;
    - el resultado y la fuente de cada regla;
    - si se eligió o no;
    - los kWh estimados, los reparos y los pendientes.
    - `potenciales.csv` lista las combinaciones a las que les falta un dato, y cuál.
- Comprobaciones sugeridas:
    - Coger parejas elegidas al azar y contrastar R1, R4b y R5 con los documentos originales de `01_entrada/`.
    - Coger vehículos «No elegible» y comprobar en su ficha la regla que los descarta y su fuente.
    - Revisar las reglas cumplidas solo con `EXCEL`: son las que más pueden cambiar al llegar el documento.
    - Revisar las 15 parejas dudosas: el siniestro solo consta en el Excel.

## Límites conocidos

- El Excel del cliente es la fuente de datos de la campaña, pero no es prueba documental. Las reglas que se cumplen solo con él quedan como pendientes.
- R4b por subcategoría es una decisión del 2026-10-22, «por ahora». Si se relajara, aparecerían más combinaciones admisibles.
- El siniestro se lee del Excel. Una baja por siniestro mal etiquetada en el Excel saldría como limpia, y al revés.
- Las 7 bajas de R2 Posesión que no se pudieron comprobar en la revisión del 2026-10-29 siguen descartadas con lo que hay.
