---
matricula: "1947LMM"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "NISSAN NV250 1.5 DCI 70KW L1H1 2 SEATS OPTIMA (95CV) FURGÓN DERIVADO DE TURISMO"
bastidor: "VF1WF000464825533"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA"
titular_cif: "A60401585"
numero_contrato: "CE/0820-2023-01726"
conductor_habitual: "A DESIGNAR POR"
conductor_dni: "12345678"
base_ubicacion: "BARCELONA (EL PRAT)"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-09-01"
fecha_fin: "2024-09-07"
dias_arrendamiento: 372
fecha_matriculacion: "2021-02-04"
tiene_acta_devolucion: true
coche_emparejado: "[[1066MWL]]"
emparejamiento_nivel: "C_CONDICIONADO"
emparejamiento_pendiente: "posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 372d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 1311d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante; la fecha de alta del Excel contradice a la factura: decidir cual vale"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 1947LMM (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: [[1066MWL]]
- Marca / Modelo: NISSAN NV250 1.5 DCI 70KW L1H1 2 SEATS OPTIMA (95CV) FURGÓN DERIVADO DE TURISMO | Origen: PDF: [[1947LMM CONTRATO ACUERDO.pdf]] | Markdown: [[1947LMM CONTRATO ACUERDO.md]]
- Bastidor: VF1WF000464825533 | Origen: PDF: [[1947LMM PC.pdf]] | Markdown: [[1947LMM PC.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular / Arrendatario: COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA (CIF: A60401585) | Origen: PDF: [[1947LMM CONTRATO ACUERDO.pdf]] | Markdown: [[1947LMM CONTRATO ACUERDO.md]]
- Arrendador (titular registral DGT): NORTHGATE ESPAÑA RENTING FLEXIBLE SA (CIF: A28659423)
- Conductor: A DESIGNAR POR (DNI: 12345678) | Origen: PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]]
- Número Contrato: CE/0820-2023-01726 | Origen: PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]]
- Base / Ubicación: BARCELONA (EL PRAT) | Origen: PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("BARCELONA (EL PRAT)"), provincia de Barcelona.
- Fecha Inicio: 2023-09-01 | Origen: PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]]
- Fecha Fin: 2024-09-07 (PREVISTA) | Origen: PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]]
- Días Arrendamiento / Tenencia: 372 días (Calculado entre 2023-09-01 y 2024-09-07)
- Fecha Matriculación: 2021-02-04 | Origen: PDF: [[1947LMM PC.pdf]] | Markdown: [[1947LMM PC.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[1947LMM ACTA DEVOLUCION.pdf]] | Markdown: [[1947LMM ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM CONTRATO ACUERDO.pdf]] | Markdown: [[1947LMM CONTRATO ACUERDO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM CONTRATO.pdf]] | Markdown: [[1947LMM CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM FT.pdf]] | Markdown: [[1947LMM FT.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM PC.pdf]] | Markdown: [[1947LMM PC.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM seguro.pdf]] | Markdown: [[1947LMM seguro.md]] (Tipo: DNI, Formato: PDF, Estado: VALIDO)
- PDF: [[1947LMM-ACTA DE ENTREGA.pdf]] | Markdown: [[1947LMM-ACTA DE ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)
- fecha_fin: corregido de 2024-09-06 a 2024-09-07. El valor anterior procedía en realidad del campo "FECHA FIN CONTRATO" de la Solicitud de Arrendamiento ([[1947LMM CONTRATO ACUERDO.md]]), mal etiquetado como si viniera del Acta de Devolución. El Acta de Devolución real ([[1947LMM ACTA DEVOLUCION.md]]) tiene el OCR completamente ilegible (sin ningún dato reconocible), por lo que no se puede leer una fecha de devolución real. Se aplica el criterio de última instancia: "Fecha Fin Prevista" (2024-09-07), tomada del Acta de Entrega, y se marca explícitamente como PREVISTA.
- dias_arrendamiento: 372
- Periodo de tenencia (372 días) por debajo de los 730 días de renting; se añade tag `elegibilidad_dudosa`.
- Discrepancia sin resolver (no corregida): el Certificado de Seguro ([[1947LMM seguro.md]]) identifica el vehículo como "NISSAN NV300 COMBI 6 L1H1", mientras que Contrato, Acta de Entrega y Ficha Técnica indican "NISSAN NV250 1.5 DCI 70KW L1H1 2 SEATS OPTIMA (95CV)". No se modifica marca_modelo por ser el dato mayoritario y coincidente con la mayoría de documentos.
- titular_empresa corregido de "NORTHGATE ESPAÑA RENTING FLEXIBLE SA" a "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA" (CIF A28659423 → A60401585). El valor anterior era el ARRENDADOR (empresa de alquiler / titular registral en DGT), no el arrendatario. Se sigue el criterio mayoritario del lote, donde `titular_empresa` recoge la sociedad del grupo Global Omnium que posee y usa el vehículo. El arrendador queda registrado en el cuerpo para no perder el dato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 372d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 1311d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
