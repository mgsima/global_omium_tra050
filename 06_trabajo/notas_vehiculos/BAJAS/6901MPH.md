---
matricula: "6901MPH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Advance 1.5 Blu e Dci 70"
bastidor: "VF1RJK00572667403"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "460659"
conductor_habitual: "TONI BOIXADER"
conductor_dni: "90002606H"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-06-03"
fecha_fin: "2024-12-30"
dias_arrendamiento: 210
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 210d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 6901MPH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Bastidor: VF1RJK00572667403 | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Conductor: TONI BOIXADER (DNI: 90002606H) | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Número Contrato: 460659 | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-06-03 | Origen: PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]]
- Fecha Fin: 2024-12-30 | Origen: PDF: [[6901MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6901MPH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 210 días (Calculado entre 2024-06-03 y 2024-12-30)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[6901MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6901MPH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[6901MPH ACTA ENTREGA.pdf]] | Markdown: [[6901MPH ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[6901MPH CONTRATO.doc]] | Markdown: [[6901MPH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA6901MPH.pdf]] | Markdown: [[MA6901MPH.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[6901MPH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **210 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 210d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
