---
matricula: "0041LWY"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT 208 Bluehdi 73kw (100cv) Active"
bastidor: "VR3UBYHTKN5815957"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448564"
conductor_habitual: "joan muños"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-02"
fecha_fin: "2023-11-29"
dias_arrendamiento: 58
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 58d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 0041LWY (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT 208 Bluehdi 73kw (100cv) Active | Origen: PDF: [[0041LWY ACTA DEVOLUCION.pdf]] | Markdown: [[0041LWY ACTA DEVOLUCION.md]]
- Bastidor: VR3UBYHTKN5815957 | Origen: PDF: [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]] | Markdown: [[0041LWYCondicionesparticulares_20251021093304.863_X.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]] | Markdown: [[0041LWYCondicionesparticulares_20251021093304.863_X.md]]
- Conductor: joan muños (DNI: NO_CONSTA) | Origen: PDF: [[0041LWY ACTA DEVOLUCION.pdf]] | Markdown: [[0041LWY ACTA DEVOLUCION.md]]
- Número Contrato: 448564 | Origen: PDF: [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]] | Markdown: [[0041LWYCondicionesparticulares_20251021093304.863_X.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[0041LWY ACTA DEVOLUCION.pdf]] | Markdown: [[0041LWY ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-02 | Origen: PDF: [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]] | Markdown: [[0041LWYCondicionesparticulares_20251021093304.863_X.md]]
- Fecha Fin: 2023-11-29 | Origen: PDF: [[0041LWY ACTA DEVOLUCION.pdf]] | Markdown: [[0041LWY ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 58 días (Calculado entre 2023-10-02 y 2023-11-29)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[0041LWY ACTA DEVOLUCION.pdf]] | Markdown: [[0041LWY ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[0041LWY FICHA TECNICA Y PERMISO.pdf]] | Markdown: [[0041LWY FICHA TECNICA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]] | Markdown: [[0041LWYCondicionesparticulares_20251021093304.863_X.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)

- Alerta Formato: WORD_DETECTADO en [[0041LWYCondicionesparticulares_20251021093304.863_X.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificados todos los documentos del expediente (Condiciones Particulares, ACTA DEVOLUCION, FICHA TECNICA Y PERMISO). fecha_inicio (2023-10-02) coincide con la "Fecha Entrega" registrada en las Condiciones Particulares. fecha_fin (2023-11-29) procede de la ACTA DEVOLUCION (no hay campo "Fecha hasta real" separado en este formulario). Sin cambios en fechas.
- Resto de campos (bastidor, marca/modelo, titular, conductor, número de contrato) verificados y coherentes con los documentos fuente. Sin cambios.
- dias_arrendamiento = 58 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 58d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
