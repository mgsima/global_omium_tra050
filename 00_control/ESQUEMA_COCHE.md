---
doc_type: esquema
aplica_a: "03_coches/<MATRICULA>.md"
estado: "BORRADOR"
actualizado: 2026-10-22
---

# Esquema de la ficha de coche

Una ficha por vehículo del universo: los que tienen carpeta en `01_entrada/` y los que solo figuran en el Excel. El nombre del fichero es la matrícula desnuda (`5566KSD.md`), para que los `[[5566KSD]]` resuelvan desde cualquier nota.

La ficha es la fuente de verdad **del coche**. Lo que se decide sobre la sustitución vive en la pareja (`04_parejas/`), no aquí.

## Principios

- Un coche se audita una vez. La pareja solo combina dos coches ya auditados.
- Todo dato que decide una regla lleva al lado su fuente, en un campo `<dato>_fuente`:
    - `DOCUMENTO` con el nombre del fichero en `<dato>_doc`.
    - `EXCEL` si solo consta en la hoja de flota. Sirve para proponer parejas, no para acreditarlas.
    - `MANUAL` si lo fijó una persona revisando el documento. El script no lo pisa nunca.
- Los datos del Excel se conservan aparte con prefijo `excel_`, para ver cuándo discrepan del documento.
- Lo que el script no sabe va a `null`, nunca a un valor inventado.
- Vocabulario de documentos y estados igual que en particulares y KnowCapital: `doc_NN_<nombre>` con `ok`, `falta`, `rehacer`, `revisar`, `na`, `sin_auditar`.

## YAML

```yaml
# --- Identidad ---
matricula: "5566KSD"
rol: "ALTA"                      # ALTA (eléctrico nuevo) | BAJA (sustituido)
bastidor: "VF1AG000861226255"
marca_modelo: "RENAULT ZOE LIMITED 40 R110"
sociedad: "G.O.MEDIOAMBIENTE S.L."
cod_sociedad: "1004"             # R1 Sociedad compara este código, nunca el CIF del titular registral
titular_registral: "GLOBAL OMNIUM MEDIOAMBIENTE SL"   # en renting será la arrendadora
tiene_documentos: true           # false = solo está en el Excel
documentos_en_carpeta: 1

# --- Datos que deciden reglas (cada uno con su fuente) ---
categoria: "M1"                  # R4 Categoría: categoría de homologación (M1, N1, N2, L...), no la del Excel
categoria_fuente: "DOCUMENTO"
categoria_doc: "FICHA TECNICA.pdf"
combustible: "ELECTRICO"         # R3 Propulsión: ELECTRICO | GASOLINA | DIESEL | HIBRIDO_GASOLINA | HIBRIDO_DIESEL | GLP | GNC
combustible_fuente: "DOCUMENTO"
combustible_doc: "FICHA TECNICA.pdf"

# Solo ALTA
fecha_adquisicion: "2024-02-28"  # R5 Ventana y R6 Año: fecha de la factura
fecha_adquisicion_fuente: "DOCUMENTO"
fecha_adquisicion_doc: "FACTURA.pdf"
fecha_matriculacion: "2024-03-12" # se anota; si discrepa de la factura, la pareja va a reparos
anio_ejecucion: 2024             # derivado; 2023 o antes = no apto
cvn: 16.9                        # kWh/100km, de la ficha IDAE; null si no hay ficha asignada
ficha_idae: "575365"
ficha_idae_fuente: "FICHA_IDAE"  # FICHA_IDAE | FICHA_IDAE_APROXIMADA

# Solo BAJA
regimen: "RENTING"               # PROPIEDAD | RENTING | ALQUILER | ...; solo fija el umbral de R2 Posesión
regimen_fuente: "DOCUMENTO"
fecha_inicio_posesion: "2021-09-08"
fecha_inicio_posesion_fuente: "DOCUMENTO"
fecha_inicio_posesion_doc: "CONTRATO.pdf"
fecha_salida: "2023-12-01"       # venta, devolución o desguace: R5 Ventana
fecha_salida_fuente: "DOCUMENTO"
fecha_salida_doc: "ACTA DEVOLUCION.pdf"
salida_tipo: "DEVOLUCION"        # DEVOLUCION | VENTA | DESGUACE | SINIESTRO
dias_posesion: 815               # derivado de las dos fechas; nunca desde la matriculación
umbral_posesion: 730             # 365 en propiedad, 730 por contrato
estado_posesion: "acreditada"    # acreditada (documento) | indicio (Excel) | insuficiente | sin_datos

# --- Datos del Excel, tal cual ---
excel_categoria: "Turismo"
excel_combustible: "GASOLINA"
excel_regimen: "ALQUILER_CORTA_DURACION"
excel_fecha_alta: "2023-12-22"
excel_fecha_baja: "2023-12-01"
excel_arrendadora: "AYVENS"
excel_marca_modelo: "RENAULT ZOE 40"

# --- Elegibilidad del coche por sí solo ---
elegible: true                   # cumple todo lo que no depende de la pareja
motivos_no_elegible: []          # ej. "Posesion 58d < 730d"
datos_que_faltan: []             # ej. "fecha_salida": lo que lo sacaría de sin_datos

# --- Documentos (los de este coche; los de la pareja van en la pareja) ---
# ALTA
doc_03_factura: "ok"
doc_04_permiso_ve: "ok"
doc_05_ft_ve: "ok"
doc_06_consumo_idae: "ok"
# BAJA
doc_07_propiedad: "ok"           # contrato de renting o justificante de propiedad
doc_08_ft_antiguo: "ok"
doc_09_entrega: "ok"             # acta de devolución, compraventa o certificado de desguace

# --- Estado ---
estado: "sin_auditar"            # sin_auditar | auditado | revisar | no_elegible
verificado_manualmente: false
fecha_verificacion: null

# --- Emparejamiento (lo escribe el emparejador; no se toca a mano) ---
pareja: "[[5566KSD_6994KGK]]"    # null si no tiene
aristas_admisibles: 4            # con cuántos coches podría emparejarse
aristas_potenciales: 2           # cuántas más tendría si se documentara lo que falta

tags:
    - coche
    - global_omnium
    - alta
```

## Cuerpo de la nota

Secciones en este orden. Las que el script regenera llevan (script); las demás se escriben a mano y el script las conserva intactas al reescribir.

- `## Resumen` (script): dos o tres líneas, qué coche es y si es elegible.
- `## Documentos en carpeta` (script): cada fichero de `01_entrada/` con enlace al original y a su conversión en `02_extraido/`.
- `## Trazabilidad` (script): por cada dato que decide una regla, documento, página o campo y valor leído. Si el Excel dice otra cosa, se pone al lado.
- `## Notas de auditoría` (a mano): lo que ha visto la persona al revisar. Aquí entran las `REVISIÓN MANUAL` de las fichas viejas.
- `## Incidencias` (a mano): lo que hay que pedir o resolver.
- `## Historial` (a mano): fecha y qué cambió.

## Lo que se trae de las notas viejas

Origen: `_0bsoleto/03_expedientes/`.

- **Datos corregidos a mano en 45 fichas.** Su YAML difiere del JSON de extracción (sobre todo fechas de inicio y fin de contrato, combustible y matriculación). Se toman de la ficha vieja con `_fuente: "MANUAL"`, no del JSON, para no deshacer el trabajo.
- **Las secciones `## REVISIÓN MANUAL`** de 68 fichas (65 del 2026-07-23 y 3 del 2026-08-10, más un apéndice) pasan a `## Notas de auditoría` del mismo coche, íntegras y con su fecha. 43 llevan un «PENDIENTE DE COMPROBAR» que pasa además a `## Incidencias`.
- **Las asignaciones de ficha IDAE** (`_FICHAS_IDAE.md`) pasan a `ficha_idae` del coche. Las cinco que había eran de altas de 2023, así que hoy no aplican a ninguna pareja viva.
- **No se trae**:
    - Las notas de pareja: sus secciones `Notas de auditoria` e `Incidencias` estaban vacías en las 65 (`_Pendiente._`). La única con texto propio es la R2 Posesión de `5566KSD_6994KGK`, que es de 2023.
    - Los veredictos de emparejamiento (`coche_emparejado`, `estado_emparejamiento`, `altas_compatibles`): los recalcula el emparejador v4.
    - Los índices `_SIN_PAREJA`, `_NO_ELEGIBLES`, `_SOLO_EXCEL`, `_SOCIEDADES`: salen de las fichas como vistas de la base.
