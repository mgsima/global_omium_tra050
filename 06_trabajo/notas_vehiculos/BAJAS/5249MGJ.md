---
matricula: "5249MGJ"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.5d Dt 74kw (100cv) Edition"
bastidor: "VXKUBYHTKP4108390"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448560"
conductor_habitual: "Diego Gonzalez"
conductor_dni: "41702070B"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-03"
fecha_fin: "2023-12-22"
dias_arrendamiento: 80
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 80d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5249MGJ (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.5d Dt 74kw (100cv) Edition | Origen: PDF: [[5249MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5249MGJ ACTA DEVOLUCION.md]]
- Bastidor: VXKUBYHTKP4108390 | Origen: PDF: [[5249MGJ CONTRATO.doc]] | Markdown: [[5249MGJ CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[5249MGJ CONTRATO.doc]] | Markdown: [[5249MGJ CONTRATO.md]]
- Conductor: Diego Gonzalez (DNI: 41702070B) | Origen: PDF: [[5249MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5249MGJ ACTA DEVOLUCION.md]]
- Número Contrato: 448560 | Origen: PDF: [[5249MGJ CONTRATO.doc]] | Markdown: [[5249MGJ CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[5249MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5249MGJ ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-03 | Origen: PDF: [[5249MGJ CONTRATO.doc]] | Markdown: [[5249MGJ CONTRATO.md]]
- Fecha Fin: 2023-12-22 | Origen: PDF: [[5249MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5249MGJ ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 80 días (Calculado entre 2023-10-03 y 2023-12-22)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[5249MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5249MGJ ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5249MGJ CONTRATO.doc]] | Markdown: [[5249MGJ CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA5249MGJ (1).pdf]] | Markdown: [[MA5249MGJ (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[5249MGJ CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2023-10-03) y fecha_fin (2023-12-22) verificadas: ya estaban correctamente tomadas de [[5249MGJ CONTRATO.md]] (fecha de entrega del propio contrato) y [[5249MGJ ACTA DEVOLUCION.md]] respectivamente. Sin cambios en fechas ni en días de arrendamiento (80 días).
- conductor_dni: de NO_CONSTA a "41702070B", legible junto a la firma del conductor en [[5249MGJ ACTA DEVOLUCION.md]].
- fecha_matriculacion permanece NO_CONSTA: la ficha técnica [[MA5249MGJ (1).md]] está muy degradada por OCR y no contiene un bloque de permiso de circulación con los campos I / I.1 legibles.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 80d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
