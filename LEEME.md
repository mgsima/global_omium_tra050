# Global Omnium TRA050 — mapa de la carpeta

Repositorio de la campaña de actuaciones TRA050 del grupo **Global Omnium** (`git@github.com:mgsima/global_omium_tra050.git`). Contiene **toda** la documentación de la campaña: lo que entrega el cliente, lo que genera el programa y los análisis. El repositorio de código (`tra050`) no guarda material de esta campaña de ningún tipo.

**La raíz es el flujo.** El número dice en qué orden te encuentras cada cosa, de lo que entra a lo que sale, y después lo que se produce por el camino. Cada zona tiene un ciclo de vida distinto, y por eso son zonas y no subcarpetas de un cajón común.

## Qué hay en cada sitio

| Carpeta | Qué contiene | Quién escribe |
| :--- | :--- | :--- |
| `01_entrada/_flota/` | Los dos Excel: el de cálculo CAE, que es **la fuente de datos de la campaña**, y el listado de solicitud de facturas | El cliente. **Nunca un script** |
| `01_entrada/ALTAS\|BAJAS/<MATRICULA>/` | **Lo que llega.** Una carpeta por vehículo con sus documentos tal y como los entregó el cliente. 156 altas, 161 bajas, 745 documentos | El cliente. **Nunca un script** |
| `02_verificacion/<EJERCICIO>/<ALTA>_<BAJA>/` | **Lo que sale al verificador**: el expediente de la pareja montado. Vacía todavía | El generador |
| `03_expedientes/<SOCIEDAD>/<ALTA>_<BAJA>.md` | **Una nota por pareja.** Es la unidad de negocio de esta campaña **y la fuente de verdad de la auditoría**. 69 expedientes en 13 sociedades | El auditor, a mano; el script sólo recalcula lo derivado |
| `03_expedientes/_VEHICULOS/<MATRICULA>.md` | Ficha de cada vehículo **documentado**: 317, una por carpeta de entrada | `fusionar_expedientes.py`, conservando lo escrito a mano |
| `03_expedientes/_*.md` | Los cuatro índices: `_SOLO_EXCEL`, `_SIN_PAREJA`, `_NO_ELEGIBLES`, `_SOCIEDADES` | El script |
| `04_extraido/ALTAS\|BAJAS/<MATRICULA>/` | Conversión a Markdown de cada documento, **1:1 con el original**. 744 ficheros | `convert_all_to_markdown.py` |
| `04_extraido/_datos/<MATRICULA>.json` | Datos extraídos por LLM, **uno por vehículo**, no por documento. 317 | `extract_vehicle_json_deepseek.py` |
| `04_extraido/_flota/` | El Excel volcado: 10 CSV, 10 JSON, `global_omium.db` y su índice | El extractor |
| `05_planes/` | Planes de trabajo de la campaña | A mano |
| `06_reportes/<EJERCICIO>/` | Informes y cartas al cliente, por ejercicio. Hoy sólo `2023/` | Los scripts |
| `07_experimentos/<fecha>_<nombre>/` | Pruebas fechadas y autocontenidas | A mano |
| `08_generado/` | Datos de relleno de los documentos que redactamos nosotros | Los scripts |
| `0bsoleto/` | Material retirado, con la fecha en el nombre y el motivo en su `LEEME.md` | Se mueve a mano |
| `Consideraciones.md` | Requisitos de la campaña y las seis reglas de emparejamiento | A mano |
| `global_omnium.base` | Base de Obsidian sobre `03_expedientes/` | A mano |

## La unidad de negocio es la pareja, no el vehículo

En particulares hay una persona por expediente y el broker lo entrega montado. Aquí no: llegan 317 carpetas sueltas y **las parejas son el resultado de un análisis**. Un vehículo por su cuenta no acredita nada; lo que se presenta a verificación es que un vehículo eléctrico nuevo **sustituye** a uno de combustión concreto.

De ahí que el expediente sea `<ALTA>_<BAJA>.md` y que los vehículos vivan en un índice, `_VEHICULOS/`, con el nombre desnudo de la matrícula para que los `[[5875KPY]]` de toda la campaña sigan resolviendo.

## La sociedad es la carpeta; el ejercicio, una propiedad

La regla R1 exige que alta y baja sean de la misma sociedad del grupo. Con la sociedad como carpeta, **R1 deja de ser una comprobación y pasa a ser una imposibilidad física**: no se puede emparejar a través de una frontera de carpeta. Y el techo estructural de cada sociedad —cuántas parejas caben ahí dentro como máximo— se lee mirando la tabla de `_SOCIEDADES.md`.

El **ejercicio** (2023, 2024, 2025) no es carpeta en `03_expedientes/` porque no restringe nada: es una propiedad del expediente y una vista de la base. Sí manda donde se entrega, que es `02_verificacion/` y `06_reportes/`.

## El Excel es fuente de datos y no es prueba documental

Es la distinción más importante de la campaña, y es la que produjo el único riesgo real del lote 2023: tres expedientes cuyo periodo de posesión sólo consta en el histórico del Excel, que no vale ante la verificación.

Por eso están separados físicamente —`01_entrada/_flota/` frente a las carpetas de documentos— **y también en el vocabulario**: en las fichas de vehículo, todo dato que venga del Excel lleva prefijo `excel_` y el que venga de un documento conserva su nombre. Así se ven los dos uno al lado del otro y se nota cuándo discrepan. En `5875KPY`, por ejemplo, el documento dice `regimen: RENTING` y el Excel dice `excel_regimen: ALQUILER_CORTA_DURACION`, que es justo el campo en disputa de su R2.

Hasta el 2026-08-19 esas dos vistas vivían en dos juegos de notas separados que usaban los mismos nombres de clave, y por eso hacían falta dos bases de Obsidian que no se podían juntar.

## Dos universos, y sólo uno es auditable

* **El Excel: 490 vehículos** (245 altas y 245 bajas). Es el universo del emparejador.
* **Los documentos: 317 vehículos**, uno por carpeta de `01_entrada/`.

Los **174 que sólo están en el Excel** no tienen ni un papel detrás, así que no son expedientes ni merecen carpeta: están listados en `_SOLO_EXCEL.md` para que el cliente los localice o los descarte.

## La caché no es desechable

`04_extraido/` es la superficie de lectura de cada nota. El par «documento en `01_entrada/` ↔ conversión aquí» es lo que da la trazabilidad dato a dato: de qué documento salió cada matrícula, cada bastidor y cada fecha.

De ahí la regla: **los ficheros de la caché no se renombran nunca.** El 1:1 con el original *es* el mecanismo. La organización va en la carpeta de encima y en el frontmatter, jamás en el nombre. Y regenerarla cuesta tokens de APIs externas, así que se versiona a propósito: quien clone la campaña debe recibirla hecha.

## Reglas de esta carpeta

1. **No se borra nada.** Lo superado se mueve a `0bsoleto/` con la fecha por delante en el nombre y una entrada en su `LEEME.md`.
2. **Los documentos fuente son de solo lectura.** No se reescriben ni se renombran los documentos de `01_entrada/`, ni sus conversiones en `04_extraido/`.
3. **La nota del expediente es la fuente de verdad de la auditoría.** El script valida y recalcula lo derivado; el juicio se escribe a mano y el script lo conserva.
4. **Ningún script escribe fuera de esta carpeta.**
5. **Nunca commit ni push sin que el usuario lo pida** en esa conversación: este remoto lo ve el equipo.

## Historial

* **2026-08-19** — **Reorganización de la campaña**, siguiendo la filosofía de `data/particulares/`. Detalle y motivos en `05_planes/2026-08-19_reorganizacion.md`.
    * Desaparece `06_trabajo/` como cajón: la entrada y la salida ganan carpeta explícita (`01_entrada/`, `02_verificacion/`), lo derivado se queda con nombre propio (`04_extraido/`) y lo que tiene lectores humanos sube a la raíz (`03_expedientes/`, `05_planes/`, `06_reportes/`).
    * **Se fusionan los dos juegos de notas.** Las 491 fichas de emparejamiento y las 317 notas de vehículo pasan a 69 expedientes por pareja y 317 fichas de vehículo, con los datos del Excel prefijados `excel_`. Antes de fusionar se comprobó que los dos juegos **no discrepaban en ningún veredicto** de emparejamiento. Las 68 secciones `## REVISIÓN MANUAL` escritas a mano se copiaron íntegras.
    * **Se corrige un defecto de nombre en cinco vehículos.** `3154MXJ FACTURA NUEVO`, `3178MXJ`, `3186MXJ`, `3214MXJ` y `8711MXK` llevaban el sufijo pegado a la matrícula, y por eso el generador los declaró «fuera del universo del Excel». Están en las ocho hojas del Excel: la afirmación era falsa y venía del nombre de la carpeta. Corregido en entrada, caché, JSON y notas.
    * **Dos duplicados exactos se retiran**, verificados por MD5: `datos_extraidos/` entero y la caché suelta del prototipo `0696MWT`.
    * `requisitos_campana.md` sube a `Consideraciones.md`, y la tabla de las seis reglas de emparejamiento se traslada allí desde el índice de las fichas.
    * Las dos bases de Obsidian se unifican en `global_omnium.base`, con una vista nueva —**Excel contra documento**— que sólo es posible desde que las claves dejaron de colisionar.
