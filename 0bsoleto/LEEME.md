# `0bsoleto/` — material retirado

Nada se borra. Lo que deja de valer se mueve aquí con la fecha por delante en el nombre y una entrada en esta lista explicando por qué dejó de valer.

## 2026-08-19 — la reorganización de la campaña

### `2026-08-19_fichas_emparejamiento/` — 491 fichas + índice

Una ficha por vehículo del **universo del Excel**, con la verificación regla a regla y las candidatas alternativas. Las escribía `scripts/global_omnium/generar_fichas_emparejamiento.py`.

Su contenido está íntegro en `03_expedientes/`: la verificación R1–R6 y las candidatas viajaron al expediente de la pareja, los datos del Excel a la ficha de vehículo con prefijo `excel_`, y la tabla de reglas del índice al apartado 5 de `Consideraciones.md`.

### `2026-08-19_notas_vehiculos/` — 317 notas

Una nota por vehículo del **universo documentado**, con los datos leídos de los PDF. Las escribía `scripts/global_omnium/generate_vehicle_notes.py`. Su contenido está en `03_expedientes/_VEHICULOS/`, incluidas las **68 secciones `## REVISIÓN MANUAL`** escritas a mano, que se copiaron íntegras.

El prefijo `ALTAS-` / `BAJAS-` del nombre viene de la carpeta en la que estaban; se conserva para no perder de cuál salía cada una.

### `2026-08-19_bases_separadas/` — las dos bases de Obsidian

`tra050-Dashboard.base` leía las fichas y `06_trabajo/global_omnium.base` leía las notas. **Eran dos y no una porque no se podían juntar**: las dos usaban `marca_modelo`, `categoria`, `combustible`, `conductor_habitual` y `regimen` para valores de procedencia distinta —el Excel en una, los documentos en la otra— y una tabla no puede tener dos columnas con el mismo nombre. Resuelto el choque con el prefijo `excel_`, las sustituye `global_omnium.base`.

### `2026-08-19_datos_extraidos_duplicado/` — 11 ficheros

`datos_extraidos/` era copia **byte a byte** de `global_omium_extraido/`, hoy `04_extraido/_flota/`. Verificado por MD5 en los diez CSV y en `global_omium.json`:

```
    e4afdd30714db9f1d74a8b8c9ab5404d  datos_extraidos/AE_GF_2.csv
    cc11d1cb3caffd143c45e553aa2a515f  datos_extraidos/AE_GF.csv
    59264c178cb191edbf9ed2bb15f4afc7  datos_extraidos/ALTA_20242025.csv
    062d17dfbe2f5ec4f3034e0842fc1d97  datos_extraidos/BAJA2022202320242025.csv
    9fa274a1ab39e3d36e4dd0c615b3e453  datos_extraidos/DATOS_Acuerdo_GF.csv
    9fa274a1ab39e3d36e4dd0c615b3e453  datos_extraidos/datos_anexos.csv
    89af728962cbf459bf641461513bf044  datos_extraidos/Hoja2.csv
    28b143773614990a3fb1da48e4ffa50a  datos_extraidos/RESUMEN_ACT.csv
    25a6dbabdc20940b3d43828f76636f88  datos_extraidos/SUSTITUCIONES.csv
    fbcecdbe5ca3cff01b44de6a285f0434  datos_extraidos/TABLA_SOC_CAE.csv
    0274299be52091c2d31d42e5478ff154  datos_extraidos/global_omium.json
```

### `2026-08-19_cache_0696MWT_duplicada/` — 4 ficheros

`06_trabajo/03_cache_markdown/0696MWT/` era una conversión suelta del expediente prototipo, fuera del árbol `ALTAS/`/`BAJAS/`. Las conversiones buenas están en `04_extraido/ALTAS/0696MWT/` y `04_extraido/BAJAS/9853KXP/`.

## 2026-08-07 — fichas duplicadas por un defecto de nombre

### `2026-08-07_fichas_duplicadas_por_sufijo/` — 5 fichas

Cinco carpetas de entrada llevaban un sufijo pegado a la matrícula —`3154MXJ FACTURA NUEVO` y cuatro más—, así que el generador buscó `"3154MXJ FACTURA NUEVO"` en el Excel, no lo encontró y emitió una ficha que afirmaba `estado_emparejamiento: FUERA_DEL_UNIVERSO` y «no figura en la hoja del Excel».

**Esa afirmación era falsa**: los cinco vehículos están en las ocho hojas del Excel. Las fichas buenas, con el nombre limpio, existían en paralelo y son las que sobreviven. Estas se conservan porque documentan el error, y **se dejan con el nombre sucio a propósito**: reescribir un archivo fechado falsearía lo que pasó.

El defecto de nombre se corrigió el 2026-08-19 en `01_entrada/`, `04_extraido/` y las notas.

## `2026-08-19_parejas_no_viables_r2/`

Cuatro parejas retiradas de `03_expedientes/` porque la baja no acreditaba los 730 dias de posesion que exige la tenencia por contrato: `0767MJM ← 5875KPY` (149d), `2120MFK ← 4535KFH` (230d), `1066MWL ← 1947LMM` (372d) y `1108KHK ← 2653LTG` (30d). Se busco baja sustituta para las cuatro y **no hay ninguna libre**. Las altas volvieron a `_SIN_PAREJA.md` y las bajas a `_NO_ELEGIBLES.md`. La campana pasa de 69 a 65 expedientes. Detalle completo en el `LEEME.md` de la carpeta.
