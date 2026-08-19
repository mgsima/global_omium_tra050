---
matricula: "5351MGK"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT Clio Techno Blue Dci 74kw (100cv)"
bastidor: "VF1RJA00770805240"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448561"
conductor_habitual: "MANUEL RARO"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-03"
fecha_fin: "2024-03-21"
dias_arrendamiento: 170
fecha_matriculacion: "2023-04-26"
tiene_acta_devolucion: false
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 170d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5351MGK (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT Clio Techno Blue Dci 74kw (100cv) | Origen: PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]]
- Bastidor: VF1RJA00770805240 | Origen: PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]]
- Conductor: MANUEL RARO (DNI: NO_CONSTA) | Origen: PDF: [[5351MGK ACTA ENTREGA.pdf]] | Markdown: [[5351MGK ACTA ENTREGA.md]]
- Número Contrato: 448561 | Origen: PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[5351MGK ACTA ENTREGA.pdf]] | Markdown: [[5351MGK ACTA ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2023-10-03 | Origen: PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]] (campo "Fecha Entrega")
- Fecha Fin: 2024-03-21 | Origen: PDF: [[5351MGK DEVOLUCION.pdf]] | Markdown: [[5351MGK DEVOLUCION.md]] (sin acta formal; confirmación por correo electrónico y factura de alquiler)
- Días Arrendamiento / Tenencia: 170 días (Calculado entre 2023-10-03 y 2024-03-21)
- Fecha Matriculación: 2023-04-26 | Origen: PDF: [[5351MGK FICHA Y PERMISO.pdf]] | Markdown: [[5351MGK FICHA Y PERMISO.md]] (campo I, permiso de circulación)

## INVENTARIO DOCUMENTAL
- PDF: [[5351MGK ACTA ENTREGA.pdf]] | Markdown: [[5351MGK ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[5351MGK CONTRATO.doc]] | Markdown: [[5351MGK CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[5351MGK DEVOLUCION.pdf]] | Markdown: [[5351MGK DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5351MGK FICHA Y PERMISO.pdf]] | Markdown: [[5351MGK FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[5351MGK CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- titular_empresa/titular_cif: de "LEASEPLAN SERVICIOS S.A." (CIF A-78007473) a "EMPRESA GENERAL VALENCIANA DEL AGUA" (CIF A46615159). El valor anterior era el ARRENDADOR (la propia LeasePlan), no el arrendatario/titular. [[5351MGK CONTRATO.md]] identifica expresamente "arrendatario EMPRESA GENERAL VALENCIANA DEL AGUA CIF: A46615159". Discrepancia sin resolver: el Acta de Entrega identifica como "Cliente: 407699 - COMPANYIA GENERAL D AIGUES CATALUNY", distinto del arrendatario que figura en el contrato; se mantiene el dato del contrato (que es la fuente explícita de "arrendatario") y se deja constancia de la discrepancia.
- fecha_inicio: de "2023-10-02" a "2023-10-03". El valor anterior correspondía al campo "Fecha salida" (salida del vehículo de la base de LeasePlan) de [[5351MGK CONTRATO.md]]; el dato correcto de inicio de posesión efectiva es el campo "Fecha Entrega: 03/10/2023" del mismo documento.
- dias_arrendamiento: 170
- fecha_matriculacion: de "NO_CONSTA" a "2023-04-26", tomado del campo "I" (Fecha de matriculación) de [[5351MGK FICHA Y PERMISO.md]], legible y correctamente identificado según la tabla de códigos del propio documento.
- tiene_acta_devolucion: de true a false. [[5351MGK DEVOLUCION.md]] NO es un acta de devolución cumplimentada, sino un hilo de correo electrónico ("¿devuelto el 21 de marzo de 2024?" / "Sí, es va retornar el 21 de març... no ens van fer arribar l'acta") junto con una factura cuyo periodo de facturación termina el 2024-03-21. La fecha_fin se mantiene (corroborada por correo + factura) pero no existe acta de devolución como tal.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 170d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 330d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
