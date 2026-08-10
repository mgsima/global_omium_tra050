---
matricula: "4836MGD"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT Clio Techno Blue Dci 74kw (100cv)"
bastidor: "VF1RJA00170805170"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448555"
conductor_habitual: "anna"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-02"
fecha_fin: "2023-12-18"
dias_arrendamiento: 77
fecha_matriculacion: "2023-04-17"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 77d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 4836MGD (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT Clio Techno Blue Dci 74kw (100cv) | Origen: PDF: [[4836MGD ACTA DEVOLUCION.pdf]] | Markdown: [[4836MGD ACTA DEVOLUCION.md]]
- Bastidor: VF1RJA00170805170 | Origen: PDF: [[4836MGD CONTRATO.doc]] | Markdown: [[4836MGD CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[4836MGD CONTRATO.doc]] | Markdown: [[4836MGD CONTRATO.md]]
- Conductor: anna (DNI: NO_CONSTA) | Origen: PDF: [[4836MGD ACTA DEVOLUCION.pdf]] | Markdown: [[4836MGD ACTA DEVOLUCION.md]]
- Número Contrato: 448555 | Origen: PDF: [[4836MGD CONTRATO.doc]] | Markdown: [[4836MGD CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[4836MGD ACTA DEVOLUCION.pdf]] | Markdown: [[4836MGD ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-02 | Origen: PDF: [[4836MGD CONTRATO.doc]] | Markdown: [[4836MGD CONTRATO.md]]
- Fecha Fin: 2023-12-18 | Origen: PDF: [[4836MGD ACTA DEVOLUCION.pdf]] | Markdown: [[4836MGD ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 77 días (Calculado entre 2023-10-02 y 2023-12-18)
- Fecha Matriculación: 2023-04-17 | Origen: PDF: [[4836MGD FICHA Y PERMISO.pdf]] | Markdown: [[4836MGD FICHA Y PERMISO.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[4836MGD ACTA DEVOLUCION.pdf]] | Markdown: [[4836MGD ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[4836MGD CONTRATO.doc]] | Markdown: [[4836MGD CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[4836MGD FICHA Y PERMISO.pdf]] | Markdown: [[4836MGD FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[4836MGD CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2023-10-02) y fecha_fin (2023-12-18) verificadas: ya estaban correctamente tomadas de [[4836MGD CONTRATO.md]] (fecha de entrega del propio contrato) y [[4836MGD ACTA DEVOLUCION.md]] respectivamente. Sin cambios en fechas ni en días de arrendamiento (77 días).
- fecha_matriculacion: de NO_CONSTA a "2023-04-17". El dato estaba disponible y legible en el bloque de Permiso de Circulación de [[4836MGD FICHA Y PERMISO.md]] (campo I: 17-04-2023, coincide con (I.1) Fecha de expedición), y no había sido extraído.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 77d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 245d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
