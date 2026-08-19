---
matricula: "4161FVT"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "NISSAN CABSTAR"
bastidor: "VWADHFF2471021944"
combustible: "GASOIL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "CANALIZACIONES CIVILES, S.A."
titular_cif: "A12013561"
numero_contrato: "23231"
conductor_habitual: "NO_CONSTA"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Beniparrell (Valencia)"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2022-01-31"
fecha_fin: "2023-05-29"
dias_arrendamiento: 483
fecha_matriculacion: "2007-09-20"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Elegible pero sin alta compatible (sociedad/categoria/ventana)"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 4161FVT (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: NISSAN CABSTAR | Origen: PDF: [[4161FVT FICHA TECNICA.pdf]] | Markdown: [[4161FVT FICHA TECNICA.md]]
- Bastidor: VWADHFF2471021944 | Origen: PDF: [[4161FVT ALTA ALQUILER.pdf]] | Markdown: [[4161FVT ALTA ALQUILER.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: GASOIL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular / Arrendatario: CANALIZACIONES CIVILES, S.A. (CIF: A12013561) | Origen: PDF: [[4161FVT ALTA ALQUILER.pdf]] | Markdown: [[4161FVT ALTA ALQUILER.md]]
- Arrendador (titular registral DGT): TRANSPORTES Y LINEAS DEL MEDITERRANEO S.L (CIF: B-46244554)
- Conductor: NO_CONSTA (DNI: NO_CONSTA)
- Número Contrato: 23231 | Origen: PDF: [[4161FVT DEVOLUCION ALQUILER.pdf]] | Markdown: [[4161FVT DEVOLUCION ALQUILER.md]]
- Base / Ubicación: Beniparrell (Valencia) | Origen: PDF: [[4161FVT ALTA ALQUILER.pdf]] | Markdown: [[4161FVT ALTA ALQUILER.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Beniparrell (Valencia)"), provincia de Valencia.
- Fecha Inicio: 2022-01-31 | Origen: PDF: [[4161FVT ALTA ALQUILER.pdf]] | Markdown: [[4161FVT ALTA ALQUILER.md]]
- Fecha Fin: 2023-05-29 | Origen: PDF: [[4161FVT DEVOLUCION ALQUILER.pdf]] | Markdown: [[4161FVT DEVOLUCION ALQUILER.md]]
- Días Arrendamiento / Tenencia: 483 días (Calculado entre 2022-01-31 y 2023-05-29)
- Fecha Matriculación: 2007-09-20 | Origen: PDF: [[4161FVT PERMISO CIRCULACION.pdf]] | Markdown: [[4161FVT PERMISO CIRCULACION.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[4161FVT ALTA ALQUILER.pdf]] | Markdown: [[4161FVT ALTA ALQUILER.md]] (Tipo: FACTURA_VE, Formato: PDF, Estado: VALIDO)
- PDF: [[4161FVT DEVOLUCION ALQUILER.pdf]] | Markdown: [[4161FVT DEVOLUCION ALQUILER.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[4161FVT FICHA TECNICA.pdf]] | Markdown: [[4161FVT FICHA TECNICA.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[4161FVT PERMISO CIRCULACION.pdf]] | Markdown: [[4161FVT PERMISO CIRCULACION.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)
## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **483 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.
- titular_empresa corregido de "TRANSPORTES Y LINEAS DEL MEDITERRANEO S.L" a "CANALIZACIONES CIVILES, S.A." (CIF B-46244554 → A12013561). El valor anterior era el ARRENDADOR (empresa de alquiler / titular registral en DGT), no el arrendatario. Se sigue el criterio mayoritario del lote, donde `titular_empresa` recoge la sociedad del grupo Global Omnium que posee y usa el vehículo. El arrendador queda registrado en el cuerpo para no perder el dato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con TLM. El contrato solo cubre 483d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 5730d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
