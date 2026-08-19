---
doc_type: plan
cliente: Global Omnium
campana: TRA050
fecha: 2026-08-19
estado: EJECUTADO
---

# Reorganización de la carpeta de Global Omnium

Llevar esta campaña a la misma filosofía que `data/particulares/`, teniendo en cuenta que el caso no es el mismo: aquí no hay una persona por expediente, hay un grupo de 31 sociedades y un universo de 490 vehículos entre los que hay que construir las parejas.

## 1. Qué hace que la estructura de particulares funcione

No es la numeración. Son cinco decisiones, y conviene nombrarlas antes de copiarlas:

1. **La raíz es el flujo, no un catálogo.** El número dice en qué orden te encuentras cada cosa: lo que entra, lo que sale, y después lo que se produce por el camino. No hay un cajón `06_trabajo/`; ese cajón existió en particulares y se disolvió el 2026-08-12 justamente porque mezclaba cosas con lectores y ciclos de vida distintos.
2. **Cada zona es una zona porque tiene un ciclo de vida propio.** `01_entrada/` no se escribe nunca, `02_verificacion/` se regenera entera por lote y viaja fuera, `03_expedientes/` se regenera conservando lo escrito a mano, `04_extraido/` es caro y derivado.
3. **Hay una nota por unidad de negocio, y esa nota es la fuente de verdad de la auditoría.** Los scripts validan y recalculan lo derivado; no poseen el juicio.
4. **La caché es 1:1 con el original y no se renombra jamás.** El par «documento en `01_entrada/` ↔ conversión en `04_extraido/`» es lo que da trazabilidad dato a dato.
5. **Lo público y común sale al repo de código; lo que identifica a alguien se queda.**

## 2. Inventario real de lo que hay

2.684 ficheros. Medido, no estimado.

| Zona actual | Contenido | Volumen |
| :--- | :--- | ---: |
| `00001 ALTAS/<MATRICULA>/` | Documentos de origen de las altas | 156 carpetas |
| `00002 BAJAS/<MATRICULA>/` | Documentos de origen de las bajas | 161 carpetas |
| — ambas juntas | PDF, DOC, DOCX, XLSX, JPEG | **745 documentos** |
| `00003 FICHAS EMPAREJAMIENTO/*.md` | Ficha por vehículo con verificación R1–R6 y candidatas | **491 fichas** + índice |
| `00003 FICHAS EMPAREJAMIENTO/0bsoleto/` | 5 fichas retiradas el 2026-08-07 | 5 |
| `06_trabajo/01_planes/` | ROADMAP, task, requisitos de campaña, modificaciones | 5 md + 1 json |
| `06_trabajo/02_documentacion/` | **vacía** | 0 |
| `06_trabajo/03_cache_markdown/ALTAS\|BAJAS/` | Conversión a Markdown, **1:1 con cada documento** | **744 md** |
| `06_trabajo/03_cache_markdown/0696MWT/` | Conversión suelta del expediente prototipo | 4 md |
| `06_trabajo/04_cache_json/ALTAS\|BAJAS/` | Datos extraídos por LLM, **uno por vehículo** | **317 json** |
| `06_trabajo/04_preparados_verificar/0696MWT/` | Expediente montado para el verificador | 4 pdf |
| `06_trabajo/05_reportes/` | Auditoría del prototipo + informe LlamaIndex | 2 md |
| `06_trabajo/notas_vehiculos/ALTAS\|BAJAS/` | Nota por vehículo con datos del documento | **317 md** |
| `global_omium_extraido/` | El Excel volcado: 10 CSV, 10 JSON, `.db`, índice | 22 ficheros |
| `datos_extraidos/` | **Copia byte a byte** de `global_omium_extraido/csv/` | 10 CSV |
| `analisis_2023/` | El lote 2023: informes, CSV, carta al cliente | 12 ficheros |
| `CALCULO CAE ... .xlsx` | El Excel de flota, en la raíz | 1 |
| `tra050-Dashboard.base`, `06_trabajo/global_omnium.base` | Dos bases distintas | 2 |

### Lo que el inventario aclara y yo había supuesto mal

**Los dos juegos de notas no son duplicados: cubren universos distintos.** Las 491 fichas de emparejamiento son el **universo del Excel** (245 altas + 245 bajas, tengan carpeta o no). Las 317 notas de vehículo son el **universo documentado**, y coinciden **exactamente, una a una**, con las 317 carpetas de entrada. Hay 179 fichas de vehículos que sólo existen en el Excel y no tienen ni un papel detrás.

**Donde sí chocan es en nueve claves de YAML, y ese choque es real.** `matricula`, `rol`, `tags`, `marca_modelo`, `categoria`, `combustible`, `conductor_habitual`, `coche_emparejado` y `emparejamiento_nivel` están en los dos ficheros — con el mismo nombre y **distinto significado**. En `0210MWZ`, la ficha dice `marca_modelo: PEUGEOT E-PARTNER PRO 100 KW` (del Excel) y la nota dice `Citroën ë-C3 Eléctrico Max` (de la factura); `categoria` es `Furgoneta/Furgón` en una y `M1` en la otra, porque una habla el vocabulario del Excel y la otra el de la DGT. **Por eso hay dos `.base` y no una**: no se pueden mezclar en una tabla. Y por eso el veredicto de emparejamiento, que vive en las dos, puede divergir sin que nadie se entere.

**Cinco carpetas de entrada llevan un sufijo pegado a la matrícula** — `3154MXJ FACTURA NUEVO`, `3178MXJ`, `3186MXJ`, `3214MXJ`, `8711MXK` — y esa clave sucia no casa con la del Excel. Al ejecutar el paso 4 se vio hasta dónde llegó el daño: el generador buscó `"3154MXJ FACTURA NUEVO"`, no lo encontró y emitió cinco fichas que afirmaban `estado_emparejamiento: FUERA_DEL_UNIVERSO` y «no figura en la hoja del Excel». **Es falso: los cinco están en las ocho hojas del Excel.** Las fichas buenas, con el nombre limpio, existían en paralelo, así que el error se apartó a `0bsoleto/` el 2026-08-07 sin que nadie viera la causa. Es un defecto de nombre, no de datos.

**El expediente montado para el verificador ya existe, prototipado.** `04_preparados_verificar/0696MWT/` reúne los 4 PDF del alta `0696MWT` y su baja `9853KXP`, **idénticos byte a byte** a los de la entrada, y `05_reportes/0696MWT.md` es su informe de auditoría (`RECHAZADO`, bastidor no coincide). Eso es `02_verificacion/` en miniatura, y valida la estructura. Le falta el `.docx` de condiciones particulares, que es justo el documento en formato no válido del lote 2023.

**Dos ficheros de flota están colocados como si fueran de un vehículo.** `LISTADO DE SOLICITUD DE FACTURAS DE VEHICULOS ELECTRICOS (1).xlsx` cuelga suelto de la raíz de `00001 ALTAS/` y es el único de los 745 documentos sin conversión a Markdown. Y `6586KPD ACTA DEVOLUCION.jpeg` es la única imagen: es el acta que el lote 2023 pide repetir en PDF.

**`datos_extraidos/` es duplicado exacto**, verificado por MD5 en los diez CSV.

## 3. En qué Global Omnium es otro caso

| | Particulares | Global Omnium |
| :--- | :--- | :--- |
| Unidad de negocio | La persona, una por expediente | **La pareja alta+baja**, que hay que construir |
| ¿Llega montado? | Sí, el broker lo entrega | **No.** Llegan 317 carpetas sueltas y 69 parejas son resultado de un análisis |
| Eje de agrupación | El lote del broker | **La sociedad del grupo**, 31 de ellas |
| Eje de entrega | El lote | **El ejercicio** (2023, 2024, 2025) |
| Fuente primaria | Los PDF del cliente | Un **Excel de flota** más las carpetas por matrícula |
| Universo | Cerrado: 17 | **Dos universos**: 490 en el Excel, 317 con papeles |

De ahí salen tres consecuencias que la estructura tiene que reflejar y hoy no refleja:

**La sociedad es el contenedor natural, no una etiqueta.** R1 exige que alta y baja sean de la misma sociedad, así que el emparejamiento sólo puede ocurrir dentro de una sociedad. Si la sociedad es la carpeta, R1 deja de ser una comprobación y pasa a ser una imposibilidad física, y el techo estructural de cada sociedad se lee mirando la carpeta. El ejercicio, en cambio, es propiedad del expediente y eje de entrega: gobierna `02_verificacion/` y `06_reportes/`, no `03_expedientes/`.

**El Excel es fuente de datos y no es prueba documental.** Es la distinción que produjo el único riesgo real del lote 2023. La estructura debe separarlos físicamente y **el vocabulario también**: todo dato que venga del Excel lleva prefijo `excel_` en el YAML, y así las nueve claves dejan de colisionar y una sola `.base` puede enseñar las dos columnas una al lado de la otra.

**Un vehículo sin papeles no es un expediente.** Los 179 que sólo están en el Excel no merecen carpeta: merecen una línea en un índice.

## 4. Estructura propuesta

```
LEEME.md                        mapa de la carpeta
Consideraciones.md              criterios de auditoría  ← requisitos_campana.md
global_omnium.base              una sola base, sobre 03_expedientes/

01_entrada/                     SOLO LECTURA
    _flota/                     CALCULO CAE ... .xlsx  +  LISTADO DE SOLICITUD ... .xlsx
    ALTAS/<MATRICULA>/          156 carpetas
    BAJAS/<MATRICULA>/          161 carpetas

02_verificacion/<EJERCICIO>/<ALTA>_<BAJA>/    lo que sale al verificador
                                              ← 04_preparados_verificar/0696MWT/

03_expedientes/
    <SOCIEDAD>/<ALTA>_<BAJA>.md    la pareja: fuente de verdad, 69 notas
    _VEHICULOS/<MATRICULA>.md      317 fichas de vehículo documentado
    _SOLO_EXCEL.md                 los 179 sin papeles
    _SIN_PAREJA.md                 las 278 elegibles sin pareja y sus criterios de búsqueda
    _NO_ELEGIBLES.md               las 74 descartadas, con motivo
    _SOCIEDADES.md                 las 31 sociedades, código y techo estructural

04_extraido/
    ALTAS|BAJAS/<MATRICULA>/       744 md, 1:1 con cada documento
    _datos/<MATRICULA>.json        317 json de extracción por vehículo
    _flota/                        10 CSV, 10 JSON, global_omium.db, índice

05_planes/                      ROADMAP, task, modificaciones, este plan
06_reportes/<EJERCICIO>/        2023/ ← analisis_2023/ entero
07_experimentos/                2026-07-22_llamaindex/, 2026-07-21_prototipo_0696MWT/
08_generado/                    fichas TRA050 y anexos que redactemos nosotros
0bsoleto/                       con su LEEME.md
```

### Las decisiones que hay dentro

**El expediente es la pareja y vive bajo su sociedad.** `03_expedientes/CGAC/0767MJM_5875KPY.md` reúne lo que hoy está partido en cuatro sitios: la ficha del alta, la de la baja y las dos notas de vehículo. Ahí van la verificación R1–R6, los estados documentales, el ejercicio, el nivel de confianza y las notas de auditoría, editables a mano; el script recalcula recuentos, tablas y listas de petición, nada más.

**La ficha por vehículo no desaparece, cambia de papel.** `_VEHICULOS/<MATRICULA>.md` guarda lo que es del vehículo y no de la pareja —titular, bastidor, régimen, fechas, inventario documental— y conserva el nombre desnudo de la matrícula, así que los `[[5875KPY]]` que ya existen siguen resolviendo. Las «candidatas alternativas», que hoy están en la ficha del alta, pasan al expediente, que es quien decide.

**Los ficheros con guion bajo delante son índices, no expedientes**, igual que `_FICHAS_IDAE.md` en particulares.

**`_datos/` sale de `_extraido/` por vehículo, no por documento.** Los 317 JSON no son conversión de un documento: son el resultado de la extracción por LLM sobre todos los documentos de un vehículo. Ciclo de vida distinto, y por eso subcarpeta propia con guion bajo.

## 5. Cómo se ejecuta

Todo con `git mv` dentro del repo del cliente, que está limpio y al día.

1. **Esqueleto y entrada.** `00001`/`00002` → `01_entrada/ALTAS|BAJAS/`; los dos XLSX a `01_entrada/_flota/`.
2. **Caché.** `03_cache_markdown/ALTAS|BAJAS` → `04_extraido/`; `04_cache_json/*` aplanado a `04_extraido/_datos/`; `global_omium_extraido/` → `04_extraido/_flota/`. `datos_extraidos/`, duplicado exacto, y `03_cache_markdown/0696MWT/`, copia suelta, se retiran a `0bsoleto/` con el MD5 anotado — no se borran.
3. **Notas y reportes.** `01_planes` → `05_planes/` (menos `requisitos_campana.md`, que sube a `Consideraciones.md`); `analisis_2023/` → `06_reportes/2023/`; los dos de `05_reportes` a `07_experimentos/`. Se borra `02_documentacion/`, vacía. Desaparece `06_trabajo/`.
4. **Los cinco nombres con sufijo.** Renombrar `3154MXJ FACTURA NUEVO` → `3154MXJ` y sus cuatro hermanas, en entrada y en caché, y recuperar sus fichas de `0bsoleto/`. Es la corrección de un defecto, y va antes del paso 5 para que la clave case.
5. **Fusión de notas** en expediente-por-pareja + ficha-por-vehículo, con los datos del Excel prefijados `excel_`. Único paso que necesita script nuevo y único con juicio dentro.
6. **Documentación y base.** `LEEME.md`, `Consideraciones.md`, `0bsoleto/LEEME.md`; unificar las dos `.base` en una.
7. **Repo de código.** 11 rutas duras en `scripts/global_omnium/` y `docs/organizacion_datos.md`.

Los pasos 1–3 y 6 son mecánicos. El 4 es acotado y verificable. El 5 conviene hacerlo aparte y revisarlo.

## Nota al margen

La carpeta y el remoto se llaman `global_omium`, sin la ene. El cliente es **Global Omnium**. No se toca: renombrar el remoto le rompe el clon a todo el equipo.


---

## Ejecutado el 2026-08-19

Los siete pasos, con `git mv` sobre un repo limpio: **2.672 renombrados, 11 renombrados con cambios y cero borrados**. De 2.684 ficheros a 3.079, y la diferencia son sólo altas: 390 notas nuevas en `03_expedientes/`, cuatro `LEEME.md` y la base unificada.

Lo que se aprendió por el camino y no estaba en la propuesta:

* **Los dos juegos de notas no discrepaban en ningún veredicto.** Se comprobó antes de fusionar, comparando `coche_emparejado` en los 317 vehículos comunes: cero divergencias. La fusión era segura.
* **El sufijo había producido una afirmación falsa**, no sólo una clave rota. Está contado arriba y en `0bsoleto/LEEME.md`.
* **`datos_extraidos/` tenía once ficheros duplicados, no diez.** Además de los diez CSV estaba `global_omium.json`, también byte a byte idéntico.
* **El prefijo `excel_` expone discrepancias que antes no se podían ver.** En `5875KPY`, el documento dice `regimen: RENTING` y el Excel `excel_regimen: ALQUILER_CORTA_DURACION` — y ése es justo el campo en disputa de su R2. La base lleva una vista nueva, **Excel contra documento**, que sólo es posible desde que las claves dejaron de colisionar.
* **El rol dejó de ser una carpeta.** `_VEHICULOS/` y `_datos/` son planos, así que el reparto ALTA/BAJA se resuelve leyendo la clave `rol`. Se centralizó en `scripts/global_omnium/rutas.py`, que además reúne todas las rutas de la campaña.
* **Dos generadores se retiran a `scripts/global_omnium/0bsoleto/`**: `generate_vehicle_notes.py` y `generar_fichas_emparejamiento.py`. Escribían las notas antiguas y ejecutarlos ahora pisaría la auditoría, que es exactamente lo que le pasó a particulares antes de la inversión de propiedad del 2026-08-13. `emparejar_tra050_v3.py` sigue vigente: se retira la capa que escribía las parejas, no la que las calcula.
* **`extraer_excel_global_omium.py` deja de escribir la copia de respaldo** en `datos_extraidos/`, que era el duplicado.

### Lo que queda pendiente

* Los **69 expedientes nacen con `estado: SIN_AUDITAR`**. La verificación R1–R6 viaja hecha, pero el juicio por expediente está por escribir, y a partir de ahora se escribe a mano en la nota.
* **Los ejercicios 2024 y 2025 siguen sin análisis propio.** Son 62 de las 69 parejas.
* Nada se ha commiteado ni empujado, aquí ni en el repo de código.
