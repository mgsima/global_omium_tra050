---
matricula: "5262MGK"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT Clio Techno Blue Dci 74kw (100cv)"
bastidor: "VF1RJA00470805275"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448562"
conductor_habitual: "Victor mora"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-03"
fecha_fin: "2023-11-29"
dias_arrendamiento: 57
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 57d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5262MGK (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT Clio Techno Blue Dci 74kw (100cv) | Origen: PDF: [[5262MGK ACTA DEVOLUCION.pdf]] | Markdown: [[5262MGK ACTA DEVOLUCION.md]]
- Bastidor: VF1RJA00470805275 | Origen: PDF: [[5262MGK CONTRATO.doc]] | Markdown: [[5262MGK CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[5262MGK CONTRATO.doc]] | Markdown: [[5262MGK CONTRATO.md]]
- Conductor: Victor mora (DNI: NO_CONSTA) | Origen: PDF: [[5262MGK ACTA DEVOLUCION.pdf]] | Markdown: [[5262MGK ACTA DEVOLUCION.md]]
- Número Contrato: 448562 | Origen: PDF: [[5262MGK CONTRATO.doc]] | Markdown: [[5262MGK CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[5262MGK ACTA DEVOLUCION.pdf]] | Markdown: [[5262MGK ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-03 | Origen: PDF: [[5262MGK CONTRATO.doc]] | Markdown: [[5262MGK CONTRATO.md]]
- Fecha Fin: 2023-11-29 | Origen: PDF: [[5262MGK ACTA DEVOLUCION.pdf]] | Markdown: [[5262MGK ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 57 días (Calculado entre 2023-10-03 y 2023-11-29)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[5262MGK ACTA DEVOLUCION.pdf]] | Markdown: [[5262MGK ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5262MGK CONTRATO.doc]] | Markdown: [[5262MGK CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[5262MGK FICHA Y PERMISO.pdf]] | Markdown: [[5262MGK FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[5262MGK CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificados todos los documentos del expediente (CONTRATO, ACTA DEVOLUCION, FICHA Y PERMISO). fecha_inicio (2023-10-03) y fecha_fin (2023-11-29) ya estaban correctamente extraídas: fecha_inicio procede de "Fecha Inicio Contrato" del CONTRATO y fecha_fin de la fecha de salida/entrada de la ACTA DEVOLUCION (no existe campo "Fecha hasta real" separado en este formulario). Sin cambios en fechas.
- Resto de campos (bastidor, marca/modelo, titular, conductor, número de contrato) verificados y coherentes con los documentos fuente. Sin cambios.
- dias_arrendamiento = 57 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 57d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
