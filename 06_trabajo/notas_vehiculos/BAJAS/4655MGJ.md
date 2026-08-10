---
matricula: "4655MGJ"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.5d Dt 74kw (100cv) Edition"
bastidor: "VXKUBYHTKP4108353"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448557"
conductor_habitual: "David Sequera"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-03"
fecha_fin: "2023-12-05"
dias_arrendamiento: 63
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 63d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 4655MGJ (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.5d Dt 74kw (100cv) Edition | Origen: PDF: [[4655MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[4655MGJ ACTA DEVOLUCION.md]]
- Bastidor: VXKUBYHTKP4108353 | Origen: PDF: [[4655MGJ CONTRATO.doc]] | Markdown: [[4655MGJ CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[4655MGJ CONTRATO.doc]] | Markdown: [[4655MGJ CONTRATO.md]]
- Conductor: David Sequera (DNI: NO_CONSTA) | Origen: PDF: [[4655MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[4655MGJ ACTA DEVOLUCION.md]]
- Número Contrato: 448557 | Origen: PDF: [[4655MGJ CONTRATO.doc]] | Markdown: [[4655MGJ CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[4655MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[4655MGJ ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-03 | Origen: PDF: [[4655MGJ CONTRATO.doc]] | Markdown: [[4655MGJ CONTRATO.md]]
- Fecha Fin: 2023-12-05 | Origen: PDF: [[4655MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[4655MGJ ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 63 días (Calculado entre 2023-10-03 y 2023-12-05)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[4655MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[4655MGJ ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[4655MGJ CONTRATO.doc]] | Markdown: [[4655MGJ CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA4655MGJ (1).pdf]] | Markdown: [[MA4655MGJ (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[4655MGJ CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificados todos los documentos del expediente (CONTRATO, ACTA DEVOLUCION, MA4655MGJ). fecha_inicio (2023-10-03) procede de "Fecha Inicio Contrato" del CONTRATO. fecha_fin (2023-12-05) procede de la ACTA DEVOLUCION (no hay campo "Fecha hasta real" separado en este formulario). Sin cambios en fechas.
- Resto de campos (bastidor, marca/modelo, titular, conductor, número de contrato) verificados y coherentes con los documentos fuente. Sin cambios.
- dias_arrendamiento = 63 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 63d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
