---
matricula: "4295MRH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "CITROEN C3 Bluehdi 75kw (1 00cv) Plus"
bastidor: "VF7SXYHTURT066261"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "AGUAS DE VALENCIA SA"
titular_cif: "A46000477"
numero_contrato: "461125"
conductor_habitual: "CARLOS SOLER SANCHIS"
conductor_dni: "45912951Y"
base_ubicacion: "Valencia"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-06-07"
fecha_fin: "2025-03-07"
dias_arrendamiento: 273
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 273d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 4295MRH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: CITROEN C3 Bluehdi 75kw (1 00cv) Plus | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Bastidor: VF7SXYHTURT066261 | Origen: PDF: [[4295MRH FICHA Y PERMISO.pdf]] | Markdown: [[4295MRH FICHA Y PERMISO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: AGUAS DE VALENCIA SA (CIF: A46000477) | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Conductor: CARLOS SOLER SANCHIS (DNI: 45912951Y) | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Número Contrato: 461125 | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Base / Ubicación: Valencia | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Valencia"), provincia de Valencia.
- Fecha Inicio: 2024-06-07 | Origen: PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]]
- Fecha Fin: 2025-03-07 | Origen: PDF: [[4295MRH ACTA DEVOLUCION.pdf]] | Markdown: [[4295MRH ACTA DEVOLUCION.md]] (Tipo: ACTA_DEVOLUCION)
- Días Arrendamiento / Tenencia: 273 días (Calculado entre 2024-06-07 y 2025-03-07)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[4295MRH ACTA DEVOLUCION.pdf]] | Markdown: [[4295MRH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[4295MRH CONTRATO.doc]] | Markdown: [[4295MRH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[4295MRH FICHA Y PERMISO.pdf]] | Markdown: [[4295MRH FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[4295MRH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2024-06-07) verificado contra el contrato ("Fecha salida"/"Fecha Entrega" del propio contrato, coincidente con el inicio efectivo de la posesión): correcto, sin cambios.
- fecha_fin: "2025-03-07"Fecha de Devolución (Día/mes/año)" está ilegible/no cumplimentado de forma reconocible en el OCR. No se ha podido localizar el origen real de la fecha 2024-07-10 en ningún documento del vehículo.
- dias_arrendamiento: 273
- fecha_matriculacion: corregido de 2024-05-10 a NO_CONSTA. El valor procedía de "[[4295MRH FICHA Y PERMISO.md]]" ("Primera expedición: 10/05/2024" de la tarjeta ITV / inspección técnica), no de los campos I/I.1 del permiso de circulación, que no son legibles en el documento.
- Discrepancia sin resolver: no se ha podido determinar si el acta de devolución está realmente cumplimentada (contiene restos de datos ilegibles) o es una plantilla en blanco; se mantiene tiene_acta_devolucion: true por precaución, pero se recomienda revisión del documento original en mejor calidad.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 273d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
