---
matricula: "1865LDL"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "CITROEN C3 Bluehdi 73kw (1 00cv) S&s Feel"
bastidor: "VF7SXYHYPKT719152"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "MEDICION AVANZADA DE CONTADORES SA"
titular_cif: "A96674460"
numero_contrato: "452464"
conductor_habitual: "susana cuevas"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Sevilla"
comunidad_autonoma: "Andalucía"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-12-22"
fecha_fin: "2024-01-30"
dias_arrendamiento: 39
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 39d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 1865LDL (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: CITROEN C3 Bluehdi 73kw (1 00cv) S&s Feel | Origen: PDF: [[1865LDL ACTA DEVOLUCION.pdf]] | Markdown: [[1865LDL ACTA DEVOLUCION.md]]
- Bastidor: VF7SXYHYPKT719152 | Origen: PDF: [[1865LDL CONTRATO.doc]] | Markdown: [[1865LDL CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: MEDICION AVANZADA DE CONTADORES SA (CIF: A96674460) | Origen: PDF: [[1865LDL CONTRATO.doc]] | Markdown: [[1865LDL CONTRATO.md]]
- Conductor: susana cuevas (DNI: NO_CONSTA) | Origen: PDF: [[1865LDL ACTA DEVOLUCION.pdf]] | Markdown: [[1865LDL ACTA DEVOLUCION.md]]
- Número Contrato: 452464 | Origen: PDF: [[1865LDL CONTRATO.doc]] | Markdown: [[1865LDL CONTRATO.md]]
- Base / Ubicación: Sevilla | Origen: PDF: [[1865LDL ACTA DEVOLUCION.pdf]] | Markdown: [[1865LDL ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Andalucía | Derivada de `base_ubicacion` ("Sevilla"), provincia de Sevilla.
- Fecha Inicio: 2023-12-22 | Origen: PDF: [[1865LDL CONTRATO.doc]] | Markdown: [[1865LDL CONTRATO.md]]
- Fecha Fin: 2024-01-30 | Origen: PDF: [[1865LDL ACTA DEVOLUCION.pdf]] | Markdown: [[1865LDL ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 39 días (Calculado entre 2023-12-22 y 2024-01-30)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[1865LDL ACTA DE ENTREGA.pdf]] | Markdown: [[1865LDL ACTA DE ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[1865LDL ACTA DEVOLUCION.pdf]] | Markdown: [[1865LDL ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[1865LDL CONTRATO.doc]] | Markdown: [[1865LDL CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[1865LDL FICHA Y PERMISO.pdf]] | Markdown: [[1865LDL FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[1865LDL CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2023-12-22) y fecha_fin (2024-01-30) verificados contra el contrato de alta y el acta de devolución respectivamente: correctos, sin cambios.
- combustible: corregido de "Gasolina" a "DIESEL". El valor anterior procedía de la casilla marcada en las actas de entrega/devolución, pero contradice tipo_vehiculo (COMBUSTION_DIESEL) y la denominación del vehículo "CITROEN C3 Bluehdi 73kw" — "BlueHDi" es la denominación comercial del motor diésel de PSA/Citroën, lo que indica que la casilla del acta fue mal leída por el OCR.
- fecha_matriculacion: corregido de 2019-12-10 a NO_CONSTA. El valor anterior era la "Fecha de emisión" (10/12/2019) del certificado de conformidad en [[1865LDL FICHA Y PERMISO.md]], fuente explícitamente excluida por el protocolo. Los campos I/I.1 del permiso de circulación no son legibles en el documento.
- dias_arrendamiento (39 días) queda muy por debajo de los 730 días de referencia para RENTING: elegibilidad dudosa.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 39d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
