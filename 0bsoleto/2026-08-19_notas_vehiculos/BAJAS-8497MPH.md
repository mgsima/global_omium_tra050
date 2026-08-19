---
matricula: "8497MPH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 Kw (95 Cv)"
bastidor: "VF1RJK00772667354"
combustible: "Diesel"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "464354"
conductor_habitual: "Úrsula Cárdenas moreno"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-08-01"
fecha_fin: "2025-03-24"
dias_arrendamiento: 235
fecha_matriculacion: "2024-03-26"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 235d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 8497MPH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 Kw (95 Cv) | Origen: PDF: [[8497MPH ACTA DEVOLUCION.pdf]] | Markdown: [[8497MPH ACTA DEVOLUCION.md]]
- Bastidor: VF1RJK00772667354 | Origen: PDF: [[8497MPH CONTRATO.doc]] | Markdown: [[8497MPH CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[8497MPH CONTRATO.doc]] | Markdown: [[8497MPH CONTRATO.md]]
- Conductor: Úrsula Cárdenas moreno (DNI: NO_CONSTA) | Origen: PDF: [[8497MPH ACTA DEVOLUCION.pdf]] | Markdown: [[8497MPH ACTA DEVOLUCION.md]]
- Número Contrato: 464354 | Origen: PDF: [[8497MPH CONTRATO.doc]] | Markdown: [[8497MPH CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[8497MPH ACTA DEVOLUCION.pdf]] | Markdown: [[8497MPH ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-08-01 | Origen: PDF: [[8497MPH CONTRATO.doc]] | Markdown: [[8497MPH CONTRATO.md]]
- Fecha Fin: 2025-03-24 | Origen: PDF: [[8497MPH ACTA DEVOLUCION.pdf]] | Markdown: [[8497MPH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 235 días (Calculado entre 2024-08-01 y 2025-03-24)
- Fecha Matriculación: 2024-03-26 | Origen: PDF: [[MA8497MPH (1).pdf]] | Markdown: [[MA8497MPH (1).md]]

## INVENTARIO DOCUMENTAL
- PDF: [[8497MPH ACTA DEVOLUCION.pdf]] | Markdown: [[8497MPH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[8497MPH CONTRATO.doc]] | Markdown: [[8497MPH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA8497MPH (1).pdf]] | Markdown: [[MA8497MPH (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[8497MPH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **235 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 235d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 363d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
