---
matricula: "6529LTJ"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT Mégane Life Blue Dci 8 5 Kw"
bastidor: "VF1RFB00367881003"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "GLOBAL OMNIUM MEDIOAMBIENTE SL"
titular_cif: "B46017018"
numero_contrato: "456030"
conductor_habitual: "DANIEL CABALLERO MEJIA"
conductor_dni: "1183148M"
base_ubicacion: "Valencia"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-02-27"
fecha_fin: "2024-04-24"
dias_arrendamiento: 57
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 57d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 6529LTJ (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT Mégane Life Blue Dci 8 5 Kw | Origen: PDF: [[6529LTJ ACTA DEVOLUCION.pdf]] | Markdown: [[6529LTJ ACTA DEVOLUCION.md]]
- Bastidor: VF1RFB00367881003 | Origen: PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: GLOBAL OMNIUM MEDIOAMBIENTE SL (CIF: B46017018) | Origen: PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]]
- Conductor: DANIEL CABALLERO MEJIA (DNI: 1183148M) | Origen: PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]]
- Número Contrato: 456030 | Origen: PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]]
- Base / Ubicación: Valencia | Origen: PDF: [[6529LTJ ACTA DEVOLUCION.pdf]] | Markdown: [[6529LTJ ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Valencia"), provincia de Valencia.
- Fecha Inicio: 2024-02-27 | Origen: PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]]
- Fecha Fin: 2024-04-24 | Origen: PDF: [[6529LTJ ACTA DEVOLUCION.pdf]] | Markdown: [[6529LTJ ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 57 días (Calculado entre 2024-02-27 y 2024-04-24)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[6529LTJ ACTA DEVOLUCION.pdf]] | Markdown: [[6529LTJ ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[6529LTJ ACTA ENTREGA.pdf]] | Markdown: [[6529LTJ ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[6529LTJ CONTRATO.doc]] | Markdown: [[6529LTJ CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA6529LTJ.pdf]] | Markdown: [[MA6529LTJ.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[6529LTJ CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificados todos los documentos del expediente (CONTRATO, ACTA ENTREGA, ACTA DEVOLUCION, MA6529LTJ). fecha_inicio (2024-02-27) coincide con la fecha de entrega registrada tanto en el CONTRATO ("Fecha Entrega") como en la ACTA ENTREGA. fecha_fin (2024-04-24) procede de la ACTA DEVOLUCION (no hay campo "Fecha hasta real" separado en este formulario). Sin cambios en fechas.
- Resto de campos (bastidor, marca/modelo, titular, conductor, número de contrato) verificados y coherentes con los documentos fuente. Sin cambios.
- dias_arrendamiento = 57 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 57d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
