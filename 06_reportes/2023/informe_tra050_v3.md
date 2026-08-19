---
doc_type: emparejamiento_tra050_v3
normativa: TRA050_v1.1 + criterio 25-11.01
fecha_ejecucion: 2026-08-07 14:58
parejas: 69
---

# Emparejamiento TRA050 v3 - Global Omnium

## Que hace distinto a las versiones anteriores

Las seis reglas se aplican como **filtros duros**: una pareja que incumple cualquiera de ellas no llega a existir en el grafo. El peso solo desempata entre parejas ya admisibles.

La identidad de empresa se comprueba con `Cod.Sociedad` del Excel, no con el `titular_cif` de los documentos: en renting ese titular es la arrendadora (Ayvens, Arval, LeasePlan), no la empresa del grupo. Global Omnium es un grupo, asi que no se exige una sociedad concreta sino que **alta y baja compartan la misma**.

## Reglas aplicadas

| # | Regla | Umbral |
| :- | :--- | :--- |
| R1 | Misma sociedad del grupo | `Cod.Sociedad` alta == baja |
| R2 | Posesion minima del sustituido | 365d en propiedad / 730d si se tuvo por contrato de arrendamiento, con independencia de como se llame ese contrato en el Excel |
| R3 | Alta electrica pura; baja de combustion, **hibrido incluido** (solo se excluye el electrico puro) | combustible |
| R4 | Misma categoria | `Categoría Veh.` alta == baja |
| R5 | Ventana de sincronia | -3 meses / +6 meses |
| R6 | Ambito temporal CAE | adquisicion posterior al 2023-01-25 |

## Resultado

- Altas evaluadas: **245** | Bajas evaluadas: **245**
- Altas elegibles: 232 | Bajas elegibles: 184
- **Parejas formadas: 69**

| Nivel | Parejas | Significado |
| :--- | :-: | :--- |
| `A_ACREDITADO` | 37 | Carpeta documental en ambos y reglas verificadas con documento |
| `B_INDICIO` | 11 | Cumple con datos de Excel; falta la carpeta |
| `C_CONDICIONADO` | 21 | Cumple pero con una salvedad que hay que resolver |

> Solo el nivel A puede presentarse como verificado. B y C son propuestas solidas que requieren pedir documentacion antes de cerrarlas.

## Parejas

| # | Alta | Sociedad | Cat | F. adq. | Baja | Regimen | F. baja | Desf. | Posesion | Nivel | Pendiente |
| :-: | :--- | :--- | :-- | :--- | :--- | :--- | :--- | :-: | :-: | :--- | :--- |
| 1 | `0767MJM` | CGAC | Furgoneta/Furgón | 2023-07-19 | `5875KPY` | ALQUILER_CORTA_DURACION | 2023-06-30 | -19d | 1716d | C_CONDICIONADO | posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 149d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 1716d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante |
| 2 | `0971MXH` | MEDICION AVANZADA CONTAD. | Furgoneta/Furgón | 2024-12-19 | `7001LLV` | RENTING | 2025-04-04 | +106d | 1527d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 3 | `1066MWL` | CGAC | Turismo | 2024-10-23 | `1947LMM` | ALQUILER_CORTA_DURACION | 2024-09-07 | -46d | 1311d | C_CONDICIONADO | posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 372d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 1311d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante; la fecha de alta del Excel contradice a la factura: decidir cual vale |
| 4 | `1108KHK` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-06-14 | `2653LTG` | ALQUILER_CORTA_DURACION | 2024-06-07 | -7d | 973d | C_CONDICIONADO | posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 30d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 973d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante; la fecha de alta del Excel contradice a la factura: decidir cual vale |
| 5 | `1666MGR` | CGAC | Furgoneta/Furgón | 2023-04-27 | `T5455BB` | PROPIEDAD | 2023-03-09 | -49d | 8833d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 6 | `1667MGR` | CGAC | Furgoneta/Furgón | 2023-04-26 | `5949LLV` | RENTING | 2023-04-08 | -18d | 761d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 7 | `2076MJP` | CGAC | Furgoneta/Furgón | 2023-07-25 | `6586KPD` | RENTING | 2023-10-26 | +93d | 1870d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 8 | `2120MFK` | CGAC | Furgoneta/Furgón | 2023-07-25 | `4535KFH` | ALQUILER_CORTA_DURACION | 2023-09-19 | +56d | 2135d | C_CONDICIONADO | posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 230d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 2135d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante; la fecha de alta del Excel contradice a la factura: decidir cual vale |
| 9 | `2704MXG` | AVSA | Furgoneta/Furgón | 2024-12-18 | `9377LMG` | RENTING | 2025-03-05 | +77d | 1461d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 10 | `2705MXG` | AVSA | Furgoneta/Furgón | 2024-12-18 | `4926LMS` | RENTING | 2024-10-29 | -50d | 1303d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 11 | `2720MWP` | AVSA | Turismo | 2024-11-21 | `9428LKC` | RENTING | 2024-10-29 | -23d | 1461d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta; aportar acta de devolucion firmada |
| 12 | `2722MXG` | AVSA | Furgoneta/Furgón | 2024-12-18 | `3598LKS` | RENTING | 2024-10-16 | -63d | 1420d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 13 | `2737MXG` | AVSA | Furgoneta/Furgón | 2024-12-18 | `5937LLV` | RENTING | 2024-10-18 | -61d | 1313d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 14 | `3103MXJ` | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | 2024-12-17 | `6736LLV` | RENTING | 2025-04-25 | +129d | 1551d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 15 | `3105MWZ` | EMIVASA | Turismo | 2024-11-28 | `7970LKX` | RENTING | 2025-01-10 | +43d | 1519d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 16 | `3111MWZ` | EMIVASA | Turismo | 2024-11-29 | `0383LKK` | RENTING | 2025-04-29 | +151d | 1658d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 17 | `3116MXJ` | G.O.MEDIOAMBIENTE S.L. | Furgoneta/Furgón | 2024-12-23 | `8767LLW` | RENTING | 2025-02-11 | +50d | 1453d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada |
| 18 | `3121MWZ` | EMIVASA | Turismo | 2024-11-29 | `3904LLT` | RENTING | 2025-01-14 | +46d | 1447d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 19 | `3122MWZ` | EMIVASA | Turismo | 2024-11-29 | `8066LKY` | RENTING | 2024-12-01 | +2d | 1461d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 20 | `3133MWZ` | EMIVASA | Turismo | 2024-11-29 | `4170LKY` | RENTING | 2024-12-01 | +2d | 1461d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 21 | `3143MWZ` | EMIVASA | Turismo | 2024-11-29 | `9417LKC` | RENTING | 2025-01-15 | +47d | 1539d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 22 | `3147MXJ` | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | 2024-12-17 | `6741LLV` | RENTING | 2025-02-08 | +53d | 1461d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 23 | `3154MXJ` | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | 2024-12-17 | `7015LLV` | RENTING | 2024-10-29 | -49d | 1366d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 24 | `3157MXJ` | EGEVASA | Furgoneta/Furgón | 2024-12-19 | `6844LLV` | RENTING | 2025-02-08 | +51d | 1461d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 25 | `3178MXJ` | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | 2024-12-17 | `6987LLV` | RENTING | 2024-12-27 | +10d | 1421d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 26 | `3191MXJ` | EGEVASA | Furgoneta/Furgón | 2024-12-19 | `8313LLZ` | RENTING | 2025-02-08 | +51d | 1461d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 27 | `3246MXJ` | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | 2024-12-23 | `7055LLV` | RENTING | 2025-03-31 | +98d | 1481d | B_INDICIO | confirmar fecha de adquisicion con factura o permiso de circulacion; confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo nuevo; solicitar carpeta documental del vehiculo sustituido |
| 28 | `4073MXK` | CGAC | Furgoneta/Furgón | 2024-12-20 | `5932LLV` | RENTING | 2025-03-27 | +97d | 1515d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 29 | `4597LGC` | ISG | Furgoneta/Furgón | 2024-05-10 | `9305LMG` | RENTING | 2024-05-07 | -3d | 1156d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta; confirmar fecha de adquisicion con factura o permiso de circulacion; solicitar carpeta documental del vehiculo nuevo |
| 30 | `5020MWL` | CGAC | Furgoneta/Furgón | 2024-11-18 | `3569LKS` | RENTING | 2024-11-07 | -11d | 1414d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 31 | `5230MXL` | UTE CHIVA(AV/EG) | Furgoneta/Furgón | 2024-12-20 | `6794LLV` | RENTING | 2024-11-19 | -31d | 1365d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 32 | `5566KSD` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2023-12-22 | `6994KGK` | ALQUILER_CORTA_DURACION | 2023-12-01 | -21d | 815d | C_CONDICIONADO | REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. Se admite porque el propio contrato cubre 815d, por encima de los 730d exigidos: lo que decide es el periodo de posesion, no como se llame el contrato. COMPROBAR en el contrato que ese periodo es continuado y no una sucesion de alquileres con interrupciones; la fecha de alta del Excel contradice a la factura: decidir cual vale |
| 33 | `6007MWV` | AVSA | Turismo | 2024-11-26 | `7017KWW` | RENTING | 2025-01-24 | +59d | 2076d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 34 | `6015MWV` | AVSA | Turismo | 2024-11-26 | `7962LKX` | RENTING | 2024-12-20 | +24d | 1498d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 35 | `6029MWV` | AVSA | Turismo | 2024-11-26 | `5255LKX` | RENTING | 2025-01-20 | +55d | 1462d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 36 | `6033MWV` | CANALIZ. CIVILES S.A. | Turismo | 2024-11-26 | `5243LKX` | RENTING | 2025-01-13 | +48d | 1504d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 37 | `6037MWV` | CANALIZ. CIVILES S.A. | Turismo | 2024-11-29 | `5996LKM` | RENTING | 2025-05-22 | +174d | 1659d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 38 | `6042MWV` | AVSA | Turismo | 2024-11-26 | `0269LLK` | RENTING | 2025-01-23 | +58d | 1501d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 39 | `6082MWV` | E.Mixta Metropolitana, SA | Turismo | 2024-11-25 | `5493LLD` | RENTING | 2024-12-11 | +16d | 1461d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 40 | `6083MWV` | AVSA | Turismo | 2024-11-28 | `5829LLX` | RENTING | 2025-01-14 | +47d | 1456d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 41 | `6084MWV` | AVSA | Turismo | 2024-11-26 | `9418LKC` | RENTING | 2025-01-22 | +57d | 1546d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 42 | `6089MWV` | AVSA | Turismo | 2024-11-28 | `9504LDD` | RENTING | 2025-05-21 | +174d | 1979d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 43 | `6094MWV` | AVSA | Turismo | 2024-11-27 | `9494LKC` | RENTING | 2025-01-14 | +48d | 1538d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 44 | `6097MWV` | AVSA | Turismo | 2024-11-28 | `1451LDY` | RENTING | 2025-05-21 | +174d | 1938d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 45 | `6124MWV` | ISG | Turismo | 2024-11-26 | `9276LMB` | RENTING | 2025-02-05 | +71d | 1478d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 46 | `6126MWV` | ISG | Turismo | 2024-11-26 | `3043KBJ` | RENTING | 2025-05-22 | +177d | 2876d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 47 | `6128MWV` | ISG | Turismo | 2024-11-28 | `0251LLK` | RENTING | 2024-10-29 | -30d | 1408d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 48 | `6209MWV` | EMP.AG.POTABL.MALGRAT SA | Turismo | 2024-11-29 | `4223LJV` | RENTING | 2024-12-09 | +10d | 1554d | B_INDICIO | confirmar fecha de adquisicion con factura o permiso de circulacion; solicitar carpeta documental del vehiculo nuevo |
| 49 | `6233MXY` | CGAC | Turismo | 2025-01-24 | `1192LPK` | RENTING | 2025-06-11 | +138d | 1461d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta; confirmar fecha de adquisicion con factura o permiso de circulacion; confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo nuevo; solicitar carpeta documental del vehiculo sustituido |
| 50 | `6245MWV` | E.Mixta Metropolitana, SA | Turismo | 2024-11-26 | `3931LLT` | RENTING | 2025-01-30 | +65d | 1463d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 51 | `6334MXF` | AVSA | Furgoneta/Furgón | 2024-12-18 | `6997LLV` | RENTING | 2025-02-08 | +52d | 1461d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 52 | `6398MWV` | CGAC | Turismo | 2024-11-21 | `0019LLR` | RENTING | 2025-04-01 | +131d | 1544d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 53 | `6439MWV` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-11-26 | `0246LLK` | RENTING | 2025-04-11 | +136d | 1572d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 54 | `6442MWV` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-11-26 | `3942LLT` | RENTING | 2025-03-14 | +108d | 1506d | B_INDICIO | aportar acta de devolucion firmada |
| 55 | `6444MWV` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-11-29 | `4988LLY` | RENTING | 2025-01-19 | +51d | 1461d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 56 | `6445MWV` | CGAC | Turismo | 2024-11-29 | `9413LKC` | RENTING | 2025-02-07 | +70d | 1542d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 57 | `6492MWV` | MEDICION AVANZADA CONTAD. | Turismo | 2024-11-29 | `0818LKK` | RENTING | 2025-01-10 | +42d | 1533d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 58 | `6493MWV` | MEDICION AVANZADA CONTAD. | Turismo | 2024-11-26 | `8030LKY` | RENTING | 2025-01-16 | +51d | 1507d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 59 | `6558MWV` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-11-28 | `9977LLM` | RENTING | 2025-04-24 | +147d | 1529d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 60 | `6559MWV` | G.O.MEDIOAMBIENTE S.L. | Turismo | 2024-11-25 | `9019LBN` | RENTING | 2024-10-02 | -54d | 1818d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
| 61 | `7775MXF` | GAMASER | Furgoneta/Furgón | 2024-12-18 | `5969LLV` | RENTING | 2024-11-06 | -42d | 1374d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 62 | `8349MXG` | ISG | Furgoneta/Furgón | 2024-12-19 | `5918LLV` | RENTING | 2025-02-05 | +48d | 1469d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 63 | `8597MWT` | CGAC | Furgoneta/Furgón | 2024-11-28 | `4938LMS` | RENTING | 2025-04-08 | +131d | 1461d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta; confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 64 | `8628MWT` | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | 2024-11-29 | `7399LLP` | RENTING | 2025-04-23 | +145d | 1461d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta; confirmar fecha de adquisicion con factura o permiso de circulacion; confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo nuevo; solicitar carpeta documental del vehiculo sustituido |
| 65 | `8634MWT` | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | 2024-11-28 | `9369LMG` | RENTING | 2025-03-31 | +123d | 1487d | B_INDICIO | confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo sustituido |
| 66 | `8662NDJ` | EMIVASA | Turismo | 2025-07-04 | `1485LSB` | RENTING | 2025-06-04 | -30d | 1398d | B_INDICIO | confirmar fecha de adquisicion con factura o permiso de circulacion; solicitar carpeta documental del vehiculo nuevo |
| 67 | `8873KDN` | GAMASER | Turismo | 2023-11-01 | `1751LHM` | RENTING | 2023-08-31 | -62d | 1155d | B_INDICIO | confirmar fecha de adquisicion con factura o permiso de circulacion; confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada; solicitar carpeta documental del vehiculo nuevo |
| 68 | `8994MSH` | CGAC | Furgoneta/Furgón | 2024-06-10 | `6756LLV` | RENTING | 2024-06-28 | +18d | 1201d | C_CONDICIONADO | baja por siniestro: acreditar con baja definitiva DGT, no con venta |
| 69 | `9050MWN` | AVSA | Turismo | 2024-11-21 | `8298KZS` | RENTING | 2024-09-10 | -72d | 1819d | A_ACREDITADO | Documentacion en carpeta y reglas verificadas con documento |
