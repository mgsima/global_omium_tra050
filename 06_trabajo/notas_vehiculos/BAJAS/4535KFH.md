---
matricula: "4535KFH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT PARTNER 1.6 BLUEHDI 55KW L1 CONFORT (75CV)"
bastidor: "VF37ABHW6HJ860569"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA"
titular_cif: "A60401585"
numero_contrato: "CE/0820-2023-00393"
conductor_habitual: "A DESIGNAR POR LA EMPRESA"
conductor_dni: "12345678"
base_ubicacion: "BARCELONA (EL PRAT)"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-02-01"
fecha_fin: "2023-09-19"
dias_arrendamiento: 230
fecha_matriculacion: "2017-11-14"
tiene_acta_devolucion: true
coche_emparejado: "[[2120MFK]]"
emparejamiento_nivel: "C_CONDICIONADO"
emparejamiento_pendiente: "posesion solo defendible por antiguedad: aportar contratos previos; REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 230d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 2135d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante; la fecha de alta del Excel contradice a la factura: decidir cual vale"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 4535KFH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: [[2120MFK]]
- Marca / Modelo: PEUGEOT PARTNER 1.6 BLUEHDI 55KW L1 CONFORT (75CV) | Origen: PDF: [[4535KFH CONTRATO ANEXO.pdf]] | Markdown: [[4535KFH CONTRATO ANEXO.md]]
- Bastidor: VF37ABHW6HJ860569 | Origen: PDF: [[- 4535KFH FT.pdf]] | Markdown: [[- 4535KFH FT.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular / Arrendatario: COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA (CIF: A60401585) | Origen: PDF: [[4535KFH CONTRATO.pdf]] | Markdown: [[4535KFH CONTRATO.md]]
- Arrendador (titular registral DGT): NORTHGATE ESPAÑA RENTING FLEXIBLE SA (CIF: A28659423)
- Conductor: A DESIGNAR POR LA EMPRESA (DNI: 12345678) | Origen: [[ACTA_ENTREGA.pdf]]
- Número Contrato: CE/0820-2023-00393 | Origen: PDF: [[4535KFH ACTA DEVOLUCION.pdf]] | Markdown: [[4535KFH ACTA DEVOLUCION.md]]
- Base / Ubicación: BARCELONA (EL PRAT) | Origen: PDF: [[4535KFH ACTA DEVOLUCION.pdf]] | Markdown: [[4535KFH ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("BARCELONA (EL PRAT)"), provincia de Barcelona.
- Fecha Inicio: 2023-02-01 | Origen: [[ACTA_ENTREGA.pdf]]
- Fecha Fin: 2023-09-19 | Origen: PDF: [[4535KFH ACTA DEVOLUCION.pdf]] | Markdown: [[4535KFH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 230 días (Calculado entre 2023-02-01 y 2023-09-19)
- Fecha Matriculación: 2017-11-14 | Origen: PDF: [[- 4535KFH PC.pdf]] | Markdown: [[- 4535KFH PC.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[- 4535KFH FT.pdf]] | Markdown: [[- 4535KFH FT.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[- 4535KFH PC.pdf]] | Markdown: [[- 4535KFH PC.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)
- PDF: [[4535KFH ACTA DEVOLUCION.pdf]] | Markdown: [[4535KFH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[4535KFH ACTA ENTREGA.pdf]] | Markdown: [[4535KFH ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[4535KFH CONTRATO ANEXO.pdf]] | Markdown: [[4535KFH CONTRATO ANEXO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[4535KFH CONTRATO.pdf]] | Markdown: [[4535KFH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **230 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.
- titular_empresa corregido de "NORTHGATE ESPAÑA RENTING FLEXIBLE SA" a "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA" (CIF A28659423 → A60401585). El valor anterior era el ARRENDADOR (empresa de alquiler / titular registral en DGT), no el arrendatario. Se sigue el criterio mayoritario del lote, donde `titular_empresa` recoge la sociedad del grupo Global Omnium que posee y usa el vehículo. El arrendador queda registrado en el cuerpo para no perder el dato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 230d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 2135d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
