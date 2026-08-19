---
matricula: "5056LWD"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT 208 Bluehdi 73kw (1 00cv) Active"
bastidor: "VR3UBYHTKN5801464"
combustible: "Gas-oil"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "AGUAS DE VALENCIA SA"
titular_cif: "A46000477"
numero_contrato: "458455"
conductor_habitual: "Leonardo v"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Valencia"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-04-15"
fecha_fin: "2024-05-02"
dias_arrendamiento: 17
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 17d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5056LWD (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT 208 Bluehdi 73kw (1 00cv) Active | Origen: PDF: [[5056LWD ACTA DEVOLUCION.pdf]] | Markdown: [[5056LWD ACTA DEVOLUCION.md]]
- Bastidor: VR3UBYHTKN5801464 | Origen: PDF: [[5056LWD FICHA Y PERMISO.pdf]] | Markdown: [[5056LWD FICHA Y PERMISO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Gas-oil
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: AGUAS DE VALENCIA SA (CIF: A46000477) | Origen: PDF: [[5056LWDCondicionesparticulares_20251021094053.804_X.doc]] | Markdown: [[5056LWDCondicionesparticulares_20251021094053.804_X.md]]
- Conductor: Leonardo v (DNI: NO_CONSTA) | Origen: PDF: [[5056LWD ACTA DEVOLUCION.pdf]] | Markdown: [[5056LWD ACTA DEVOLUCION.md]]
- Número Contrato: 458455 | Origen: PDF: [[5056LWDCondicionesparticulares_20251021094053.804_X.doc]] | Markdown: [[5056LWDCondicionesparticulares_20251021094053.804_X.md]]
- Base / Ubicación: Valencia | Origen: PDF: [[5056LWD ACTA DEVOLUCION.pdf]] | Markdown: [[5056LWD ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Valencia"), provincia de Valencia.
- Fecha Inicio: 2024-04-15 | Origen: PDF: [[5056LWDCondicionesparticulares_20251021094053.804_X.doc]] | Markdown: [[5056LWDCondicionesparticulares_20251021094053.804_X.md]]
- Fecha Fin: 2024-05-02 | Origen: PDF: [[5056LWD ACTA DEVOLUCION.pdf]] | Markdown: [[5056LWD ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 17 días (Calculado entre 2024-04-15 y 2024-05-02)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[5056LWD ACTA DEVOLUCION.pdf]] | Markdown: [[5056LWD ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5056LWD FICHA Y PERMISO.pdf]] | Markdown: [[5056LWD FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[5056LWDCondicionesparticulares_20251021094053.804_X.doc]] | Markdown: [[5056LWDCondicionesparticulares_20251021094053.804_X.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)

- Alerta Formato: WORD_DETECTADO en [[5056LWDCondicionesparticulares_20251021094053.804_X.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2024-04-15) y fecha_fin (2024-05-02) verificados contra las condiciones particulares (contrato de alta) y el acta de devolución respectivamente: correctos, sin cambios.
- fecha_matriculacion: corregido de 2022-01-31 a NO_CONSTA. El valor procedía de "[[5056LWD FICHA Y PERMISO.md]]", pero la fecha 31/01/2022 se encuentra dentro de la tabla de "INSPECCIONES TÉCNICAS" (ITV), no en los campos I/I.1 del permiso de circulación, que no son legibles en el documento (OCR muy degradado). No se puede confirmar una fecha de matriculación fiable.
- dias_arrendamiento (17 días) queda muy por debajo de los 730 días de referencia para RENTING: elegibilidad dudosa.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 17d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
