---
matricula: "3942LLT"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
tipo_vehiculo: "COMBUSTION_GASOLINA"
marca_modelo: "SEAT Arona 1.0 Tsi 85kw (115cv) Style GoEco"
bastidor: "VSSZZZKJZMR017640"
combustible: "Gasolina"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "383.283/5"
conductor_habitual: "JOSE M."
conductor_dni: "43789216 A"
base_ubicacion: "NO_CONSTA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "INFERIDA"
fecha_inicio: "2021-01-28"
fecha_fin: "2025-03-14"
dias_arrendamiento: 1506
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "[[6442MWV]]"
emparejamiento_nivel: "A_ACREDITADO"
emparejamiento_pendiente: "Documentacion en carpeta y reglas verificadas con documento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: false
---

# FICHA VEHÍCULO: 3942LLT (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: [[6442MWV]]
- Marca / Modelo: SEAT Arona 1.0 Tsi 85kw (115cv) Style GoEco | Origen: [[Condiciones Particulares.pdf]]
- Bastidor: VSSZZZKJZMR017640 | Origen: [[Condiciones Particulares.pdf]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_GASOLINA
- Combustible: Gasolina
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: [[Condiciones Particulares.pdf]]
- Conductor: JOSE M. (DNI: 43789216 A) | Origen: [[Acta Devolución.pdf]]
- Número Contrato: 383.283/5 | Origen: [[Condiciones Particulares.pdf]]
- Base / Ubicación: NO_CONSTA
- Comunidad Autónoma: Cataluña | INFERIDA: no consta la ubicación en el expediente. Los 10 vehículos del mismo titular (CIF A46615159) con ubicación documentada están todos en Cataluña.
- Fecha Inicio: 2021-01-28 | Origen: [[Condiciones Particulares.pdf]]
- Fecha Fin: 2025-03-14 | Origen: [[Acta Devolución.pdf]]
- Días Arrendamiento / Tenencia: 1506 días (Calculado entre 2021-01-28 y 2025-03-14)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[3942LLT ACTA DEVO.pdf]] | Markdown: [[3942LLT ACTA DEVO.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3942LLT Condiciones.pdf]] | Markdown: [[3942LLT Condiciones.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-08-10)
- `tiene_acta_devolucion` corregido de **false a true**. El acta está en carpeta y es válida: [[3942LLT ACTA DEVO.md]] es un ACTA DE DEVOLUCIÓN de LeasePlan con fecha **14/03/2025 a las 3:30**, recepciona LP SILLA, cliente EGUASA, conductor JOSE M. (DNI 43789216 A), 110.601 km, **firmada por el conductor** y con sello del Centro Logístico.
- Se le estaba pidiendo al cliente un acta que ya tenemos. Petición retirada y nivel subido de B_INDICIO a **A_ACREDITADO**, porque esa era la única acción pendiente de la pareja con [[6442MWV]].
- Causa del error: el clasificador etiquetó el documento como `Tipo: FACTURA_VE` en vez de `BAJA_VEHICULO`. Corregido arriba. La extracción sí había leído el acta —el JSON declara `origen_fecha_fin: "Acta Devolución"` y `origen_conductor: "Acta Devolución"`—, de modo que el fichero se contradecía a sí mismo.
- El PDF contiene **dos documentos**: el acta y, tras el separador, las indicaciones de devolución de LeasePlan.
