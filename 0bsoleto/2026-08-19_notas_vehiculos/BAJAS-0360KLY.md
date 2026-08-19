---
matricula: "0360KLY"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Kangoo Furgón"
bastidor: "VF1FW51J160372775"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "MEDICION AVANZADA DE CONTADORES SA"
titular_cif: "A96674460"
numero_contrato: "452465"
conductor_habitual: "Miguel Angel fernandez"
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

# FICHA VEHÍCULO: 0360KLY (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Kangoo Furgón | Origen: PDF: [[0360KLY ACTA DEVOLUCION.pdf]] | Markdown: [[0360KLY ACTA DEVOLUCION.md]]
- Bastidor: VF1FW51J160372775 | Origen: PDF: [[0360KLY CONTRATO.doc]] | Markdown: [[0360KLY CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: MEDICION AVANZADA DE CONTADORES SA (CIF: A96674460) | Origen: PDF: [[0360KLY CONTRATO.doc]] | Markdown: [[0360KLY CONTRATO.md]]
- Conductor: Miguel Angel fernandez (DNI: NO_CONSTA) | Origen: PDF: [[0360KLY ACTA DEVOLUCION.pdf]] | Markdown: [[0360KLY ACTA DEVOLUCION.md]]
- Número Contrato: 452465 | Origen: PDF: [[0360KLY CONTRATO.doc]] | Markdown: [[0360KLY CONTRATO.md]]
- Base / Ubicación: Sevilla | Origen: PDF: [[0360KLY ACTA DEVOLUCION.pdf]] | Markdown: [[0360KLY ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Andalucía | Derivada de `base_ubicacion` ("Sevilla"), provincia de Sevilla.
- Fecha Inicio: 2023-12-22 | Origen: PDF: [[0360KLY CONTRATO.doc]] | Markdown: [[0360KLY CONTRATO.md]]
- Fecha Fin: 2024-01-30 | Origen: PDF: [[0360KLY ACTA DEVOLUCION.pdf]] | Markdown: [[0360KLY ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 39 días (Calculado entre 2023-12-22 y 2024-01-30)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[0360KLY ACTA DEVOLUCION.pdf]] | Markdown: [[0360KLY ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[0360KLY ACTA ENTREGA.pdf]] | Markdown: [[0360KLY ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[0360KLY CONTRATO.doc]] | Markdown: [[0360KLY CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA0360KLY (1).pdf]] | Markdown: [[MA0360KLY (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[0360KLY CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2023-12-22) y fecha_fin (2024-01-30) verificados contra el contrato de alta y el acta de devolución respectivamente: correctos, sin cambios.
- combustible: corregido de "Gasolina" a "DIESEL". El valor anterior procedía de la casilla marcada en las actas de entrega/devolución, pero contradice tipo_vehiculo (COMBUSTION_DIESEL) y la propia denominación del vehículo en [[0360KLY CONTRATO.md]]: "RENAULT INDUST. Kangoo Furgón Profesional Dci 66kw (90cv)" — "Dci" (dCi) es la denominación comercial del motor diésel de Renault, lo que indica que la casilla del acta fue mal leída por el OCR.
- fecha_matriculacion (NO_CONSTA) verificado: correcto, no consta un permiso de circulación legible ni campos I/I.1 identificables; se mantiene sin cambios.
- dias_arrendamiento (39 días) queda muy por debajo de los 730 días de referencia para RENTING: elegibilidad dudosa.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 39d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
