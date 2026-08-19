---
matricula: "6742MGH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.5d Dt 74kw (100cv) Edition"
bastidor: "VXKUBYHTKP4107231"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448556"
conductor_habitual: "angel"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-04"
fecha_fin: "2023-11-29"
dias_arrendamiento: 56
fecha_matriculacion: "2023-04-24"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 56d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 6742MGH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.5d Dt 74kw (100cv) Edition | Origen: PDF: [[6742MGH ACTA DEVOLUCION.pdf]] | Markdown: [[6742MGH ACTA DEVOLUCION.md]]
- Bastidor: VXKUBYHTKP4107231 | Origen: PDF: [[6742MGH CONTRATO.doc]] | Markdown: [[6742MGH CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[6742MGH CONTRATO.doc]] | Markdown: [[6742MGH CONTRATO.md]]
- Conductor: angel (DNI: NO_CONSTA) | Origen: PDF: [[6742MGH ACTA DEVOLUCION.pdf]] | Markdown: [[6742MGH ACTA DEVOLUCION.md]]
- Número Contrato: 448556 | Origen: PDF: [[6742MGH CONTRATO.doc]] | Markdown: [[6742MGH CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[6742MGH ACTA DEVOLUCION.pdf]] | Markdown: [[6742MGH ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-04 | Origen: PDF: [[6742MGH CONTRATO.doc]] | Markdown: [[6742MGH CONTRATO.md]]
- Fecha Fin: 2023-11-29 | Origen: PDF: [[6742MGH ACTA DEVOLUCION.pdf]] | Markdown: [[6742MGH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 56 días (Calculado entre 2023-10-04 y 2023-11-29)
- Fecha Matriculación: 2023-04-24 | Origen: PDF: [[MA6742MGH (1).pdf]] | Markdown: [[MA6742MGH (1).md]]

## INVENTARIO DOCUMENTAL
- PDF: [[6742MGH ACTA DEVOLUCION.pdf]] | Markdown: [[6742MGH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[6742MGH CONTRATO.doc]] | Markdown: [[6742MGH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA6742MGH (1).pdf]] | Markdown: [[MA6742MGH (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[6742MGH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Fecha Matriculación corregida de NO_CONSTA a 2023-04-24: el campo "Primera expedición" de la Tarjeta ITV expedida por DGT (dato I/I.1 de matriculación) es legible en [[MA6742MGH (1).md]] ("Primera expedición: 24/04/2023 17:21:07"), coherente con la primera inspección ITV el 24/04/2023. Se había dejado NO_CONSTA por error de extracción.
- Verificado: fecha_inicio (2023-10-04, del campo "Fecha Entrega" en [[6742MGH CONTRATO.md]]) y fecha_fin (2023-11-29, del acta de devolución marcada DEVOLUCIÓN) son correctas; no proceden del documento de baja el inicio. dias_arrendamiento = 56 días, no se modifica.
- El periodo de tenencia (56 días) no alcanza los 730 días exigibles en un régimen RENTING; se marca elegibilidad_dudosa.
- Discrepancia sin resolver: la persona que retira el vehículo según el contrato ("JORDI BATLLOSERA", DNI 45540545Q) no coincide con el conductor habitual registrado ("angel", del acta de devolución). No se modifica el campo por tratarse de un posible cambio de conductor durante el periodo de alquiler.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 56d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 219d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
