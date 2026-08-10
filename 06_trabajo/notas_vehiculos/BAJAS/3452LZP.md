---
matricula: "3452LZP"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT MASTER"
bastidor: "VF1VB000069113190"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "CANALIZACIONES CIVILES, S.A."
titular_cif: "A12013561"
numero_contrato: "23013"
conductor_habitual: "NO_CONSTA"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Beniparrell (Valencia)"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2022-10-27"
fecha_fin: "2023-01-01"
dias_arrendamiento: 66
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 66d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 3452LZP (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT MASTER | Origen: PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]]
- Bastidor: VF1VB000069113190 | Origen: PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular / Arrendatario: CANALIZACIONES CIVILES, S.A. (CIF: A12013561) | Origen: PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]]
- Arrendador (titular registral DGT): Transportes y Líneas del Mediterráneo, S.L. (CIF: B-46244554)
- Conductor: NO_CONSTA (DNI: NO_CONSTA)
- Número Contrato: 23013 | Origen: PDF: [[3452LZP ACTA DEVOLUCION.pdf]] | Markdown: [[3452LZP ACTA DEVOLUCION.md]]
- Base / Ubicación: Beniparrell (Valencia) | Origen: PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Beniparrell (Valencia)"), provincia de Valencia.
- Fecha Inicio: 2022-10-27 | Origen: PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]]
- Fecha Fin: 2023-01-01 | Origen: PDF: [[3452LZP ACTA DEVOLUCION.pdf]] | Markdown: [[3452LZP ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 66 días (Calculado entre 2022-10-27 y 2023-01-01)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[3452LZP ACTA DEVOLUCION.pdf]] | Markdown: [[3452LZP ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3452LZP CONTRATO.pdf]] | Markdown: [[3452LZP CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3452LZP FICHA TECNICA.pdf]] | Markdown: [[3452LZP FICHA TECNICA.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[3452LZP PERMISO CIRCULACION.pdf]] | Markdown: [[3452LZP PERMISO CIRCULACION.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)
- Verificados todos los documentos del expediente (CONTRATO, ACTA DEVOLUCION "3. Baja Alquiler", FICHA TECNICA, PERMISO CIRCULACION). fecha_inicio (2022-10-27) procede correctamente del campo "Fecha desde" del CONTRATO (entrega del vehículo), no del acta de baja. Sin cambios.
- fecha_fin (2023-01-01) procede de la ACTA DEVOLUCION: el campo "Fecha hasta real" está en blanco, por lo que se usa la fecha de cabecera/"Fecha desde" del propio evento de baja (domingo, 1 de enero de 2023), conforme a la prioridad (b) del método de revisión. No se ha usado la "Fecha hasta prevista" (7 de febrero de 2023). Sin cambios respecto al valor ya registrado.
- Resto de campos (bastidor, marca/modelo, titular, número de contrato) verificados y coherentes con los documentos fuente. Sin cambios.
- dias_arrendamiento = 66 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.
- titular_empresa corregido de "Transportes y Líneas del Mediterráneo, S.L." a "CANALIZACIONES CIVILES, S.A." (CIF B-46244554 → A12013561). El valor anterior era el ARRENDADOR (empresa de alquiler / titular registral en DGT), no el arrendatario. Se sigue el criterio mayoritario del lote, donde `titular_empresa` recoge la sociedad del grupo Global Omnium que posee y usa el vehículo. El arrendador queda registrado en el cuerpo para no perder el dato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con TLM. El contrato solo cubre 66d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
