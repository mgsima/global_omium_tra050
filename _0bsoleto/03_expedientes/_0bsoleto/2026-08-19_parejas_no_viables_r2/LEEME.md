---
doc_type: leeme_obsoleto
retirado: 2026-08-19
motivo: R2 incumplida (posesion real por contrato < 730d) y sin baja sustituta
origen: 03_expedientes/<sociedad>/
---

# Cuatro parejas retiradas: la baja no acredita la posesion

Estas cuatro **no son expedientes y no deben volver a contarse como tales**. Eran emparejamientos propuestos por `emparejar_tra050_v3.py` que no se sostienen: en las cuatro, el vehiculo sustituido estuvo en poder del solicitante **menos de los 730 dias** que exige la tenencia por contrato.

| Pareja | Ejercicio | Sociedad | Posesion real | Arrendadora |
| :--- | :-: | :--- | ---: | :--- |
| `0767MJM ← 5875KPY` | 2023 | CGAC | 149d | NORTHGATE |
| `2120MFK ← 4535KFH` | 2023 | CGAC | 230d | NORTHGATE |
| `1066MWL ← 1947LMM` | 2024 | CGAC | 372d | NORTHGATE |
| `1108KHK ← 2653LTG` | 2024 | G.O. Medioambiente | 30d | AYVENS |

## Por que se retiran y no se dejan marcadas

**Criterio del usuario del 2026-08-19: un expediente es una cosa real.** Una pareja que no se puede presentar no es un expediente en mal estado, es una pareja que no existe. Dejarla en `03_expedientes/` con una etiqueta de «no viable» ensuciaba todos los recuentos y obligaba a filtrar en cada consulta. Se retira entera.

El criterio de fondo que las tumba, tambien del 2026-08-19: **la posesion se mide por los dias reales acreditados por contrato.** No la salva la denominacion del contrato —eso solo era un sintoma— ni contar desde la matriculacion, que prueba la edad del coche y no que lo tuviera el solicitante.

## Se busco sustituta para las cuatro. No hay

Barrido de las bajas de cada sociedad con R2 estricta mas R3, R4 y R5:

| Alta | Bajas que si cumplen las seis reglas | Situacion |
| :--- | :--- | :--- |
| `0767MJM` y `2120MFK` | `6586KPD` (1870d) | asignada a `2076MJP` |
| `1066MWL` | `0019LLR` (1544d), `9413LKC` (1542d) | asignadas a `6398MWV` y `6445MWV` |
| `1108KHK` | `9019LBN` (1818d) | asignada a `6559MWV` |

En los tres casos la alternativa existe pero **ya esta ocupada por otra alta**. Las tres altas electricas de CGAC de 2023 (`0767MJM`, `2076MJP`, `2120MFK`) competian por una unica baja valida.

## Donde ha quedado cada vehiculo

* **Las cuatro altas** (`0767MJM`, `2120MFK`, `1066MWL`, `1108KHK`) vuelven a `_SIN_PAREJA.md`: son elegibles y siguen buscando vehiculo sustituido. Si el cliente localiza uno que cumpla las seis reglas, se rehace el expediente.
* **Las cuatro bajas** (`5875KPY`, `4535KFH`, `1947LMM`, `2653LTG`) pasan a `_NO_ELEGIBLES.md`, con el mismo motivo que ya llevaban alli otras bajas de arrendamiento corto. **No sirven para ninguna pareja**, no solo para esta.

> Detalle util para entender el fallo: `_NO_ELEGIBLES.md` ya descartaba por este mismo motivo a bajas como `0041LWY` (58d). El filtro de elegibilidad existia y era correcto; lo que fallaba es que el emparejador no lo aplicaba a las bajas que ya habia emparejado. Si se vuelve a tocar `emparejar_tra050_v3.py`, ese es el bug a corregir.

## Si hubiera que revivirlas

Solo con documentacion nueva: contratos anteriores encadenados **sin interrupcion** que lleven la posesion real por encima de 730 dias hasta la fecha de baja. La carta al cliente del 2026-08-19 ya no los pide, porque el usuario dio por hecho que ese tiempo no existe.
