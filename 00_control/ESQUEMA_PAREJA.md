---
doc_type: esquema
aplica_a: "04_parejas/<SOCIEDAD>/<ALTA>_<BAJA>.md"
estado: "BORRADOR"
actualizado: 2026-10-22
---

# Esquema de la nota de pareja

Una nota por pareja alta ↔ baja. Es la unidad que se presenta a verificación y la fuente de verdad **de la sustitución**. Los datos de cada coche viven en su ficha (`03_coches/`, ver [[ESQUEMA_COCHE]]). La pareja los copia solo para que la base de Obsidian los vea, y el script los refresca desde la ficha en cada pasada.

- Carpeta: la sociedad (`04_parejas/CGAC/`), para que la R1 Sociedad no se pueda saltar.
- Nombre: `<ALTA>_<BAJA>.md`, matrículas desnudas.
- Reglas que se comprueban: [[REGLAS_EMPAREJAMIENTO]].

## Ciclo de vida

- **`propuesta`**: la crea el emparejador. Mientras está así, la siguiente pasada puede deshacerla y proponer otra mejor. La nota vieja va a `_0bsoleto/` y no se pisa.
- **`fijada`**: una persona la da por buena, o empieza a pedirle papeles al cliente. El emparejador ya no la toca y sus dos coches salen del grafo.
- **Retirada**: incumple una regla sin arreglo. La nota se mueve a `_0bsoleto/<fecha>_<motivo>/` y los dos coches vuelven al grafo.

`estado_pareja` dice si la pareja se mueve. `estado` dice cómo va la auditoría, con el mismo vocabulario que KnowCapital y particulares.

## YAML

```yaml
# --- Identidad ---
expediente: "6439MWV_0246LLK"
alta: "[[6439MWV]]"
baja: "[[0246LLK]]"
sociedad: "G.O.MEDIOAMBIENTE S.L."
cod_sociedad: "1004"
ejercicio: "2024"                # año de ejecución: factura del alta, o la salida de la baja si fue después
categoria: "M1"

# --- Ciclo de vida ---
estado_pareja: "propuesta"       # propuesta | dudosa | fijada
fecha_propuesta: "2026-10-23"
emparejador: "v4"
fijada_por: null                 # quién la fijó
fecha_fijada: null

# --- Fechas que deciden R5 Ventana (copiadas de las fichas) ---
fecha_adquisicion_alta: "2024-02-14"   # factura del VE
fecha_adquisicion_alta_fuente: "DOCUMENTO"
fecha_salida_baja: "2024-03-01"
fecha_salida_baja_fuente: "DOCUMENTO"
desfase_dias: 16                 # salida − adquisición; dentro si está entre −3 y +6 meses
dias_posesion_baja: 1102
umbral_posesion: 730

# --- Reglas: ok | falla | sin_datos, y con qué se acreditan ---
r1_sociedad: "ok"
r2_posesion: "ok"
r2_fuente: "DOCUMENTO"
r3_propulsion: "ok"
r3_fuente: "DOCUMENTO"
r4_categoria: "ok"
r4_fuente: "EXCEL"               # regla solo por Excel -> va a pendientes
r5_ventana: "ok"
r5_fuente: "DOCUMENTO"
r6_anio: "ok"
r7_alta_nueva: "ok"
r8_titularidad: "ok"
r9_salida: "ok"
reparos: []                      # lo que pide una decisión
pendientes:                      # papel ordinario que falta
    - "categoria de la baja solo por Excel: ficha tecnica de 0246LLK"

# --- Por qué esta pareja y no otra ---
alternativas_alta: 3             # cuántas bajas admisibles tenía el alta
alternativas_baja: 2             # cuántas altas admisibles tenía la baja
peso: 1450000                    # el desempate del emparejador, para auditar la elección

# --- Ahorro ---
cva: 7.89                        # consumo del antiguo, Anexo II por combustible
factor_conversion: 9.19
cvn: 16.9                        # consumo del nuevo, ficha IDAE
cvn_fuente: "FICHA_IDAE"         # FICHA_IDAE | FICHA_IDAE_APROXIMADA | DEFECTO
ficha_idae: "575365"
km_anuales: 13073
ahorro_anual_kwh: 7269.78

# --- Documentos del expediente ---
# Se deciden aquí (auditar_documentos.py o a mano) y se copian a la ficha de cada coche.
# Una pareja nueva arranca con los de las fichas.
doc_01_cesion: "faltan_datos"    # faltan_datos = sin generar; falta = generado sin firmar
doc_02_anexo_i: "faltan_datos"
doc_03_factura: "ok"
doc_04_permiso_ve: "ok"
doc_05_ft_ve: "ok"
doc_06_consumo_idae: "ok"
doc_07_propiedad: "ok"
doc_08_ft_antiguo: "falta"
doc_09_entrega: "ok"
doc_20_ficha: "faltan_datos"
docs_ok: 6
docs_pendientes: 4
docs_pide_cliente:
    - "8 · Ficha técnica del antiguo (0246LLK)"
fichero_09_entrega:              # una pareja fichero_*/motivo_* por carpeta, derivadas, para revision_documentos.base
    - "[[tra050/data/global_omium_tra050/01_entrada/BAJAS/0246LLK/0246LLK ACTA DEVOLUCION.pdf|0246LLK ACTA DEVOLUCION.pdf]]"
motivo_09_entrega: ""            # qué revisar: lo que dijo la IA o, si no opinó, las reglas
auditoria_docs:                  # lo escribe auditar_documentos.py: estado y motivo de cada fase
    - "doc_03_factura: ok · reglas: R6 Año ok con fecha_adquisicion de «Factura»: factura del 2024-12-18 · ia: factura a nombre de la sociedad"

# --- Auditoría ---
estado: "sin_auditar"            # sin_auditar | ok | pendiente_subsanacion | revisar | rechazado
num_incidencias: 0
verificado_manualmente: false
fecha_verificacion: null

tags:
    - pareja
    - global_omnium
    - tra050
```

## Cuerpo de la nota

Las secciones marcadas (script) se regeneran en cada pasada. Las demás se escriben a mano y el script las conserva intactas.

- `## Resumen` (script): qué coche sustituye a cuál y qué falta, en tres líneas.
- `## Documentos` (script): los diez documentos del expediente con su estado y enlace.
- `## Cálculo del ahorro` (script): la fórmula con los valores y su fuente.
- `## Por qué esta pareja` (script): las otras bajas que tenía el alta y las otras altas que tenía la baja, y por qué el emparejador eligió esta.
- `## Reglas` (script): una línea por regla con el valor comprobado y el documento que lo acredita, o «Excel» si solo hay indicio.
- `## Notas de auditoría` (a mano).
- `## Instrucciones al cliente` (a mano): lo que se le pide, en su lenguaje.
- `## Incidencias` (a mano).
- `## Historial` (a mano): propuesta, fijada, cambios.

## Qué cambia respecto a las notas de agosto

- Desaparecen `CANDIDATAS ALTERNATIVAS` e `INVENTARIO DOCUMENTAL` como secciones propias. El inventario es de cada coche y vive en su ficha. Las alternativas se resumen en `## Por qué esta pareja`.
- Nuevos `estado_pareja`, `fijada_por` y `fecha_fijada`, para que una pareja con trabajo encima no se recalcule.
- Una clave por regla (`r1_sociedad` … `r9_salida`) con su fuente, en vez de una tabla en el cuerpo. Así la base puede filtrar «parejas con R4 Categoría solo por Excel».
- Los documentos se nombran igual que en KnowCapital.
