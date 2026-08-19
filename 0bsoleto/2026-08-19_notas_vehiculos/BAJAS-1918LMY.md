---
matricula: "1918LMY"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.5d Dt 74kw (1 00cv) Edition"
bastidor: "VXKUBYHTKM4076895"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454460"
conductor_habitual: "EULÀLIA MASS PONTE"
conductor_dni: "46988025Z"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-02-01"
fecha_fin: "2024-03-08"
dias_arrendamiento: 36
fecha_matriculacion: "2021-03-02"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Elegible pero sin alta compatible (sociedad/categoria/ventana)"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 1918LMY (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.5d Dt 74kw (1 00cv) Edition | Origen: PDF: [[1918LMY ACTA DEVOLUCION.pdf]] | Markdown: [[1918LMY ACTA DEVOLUCION.md]]
- Bastidor: VXKUBYHTKM4076895 | Origen: PDF: [[1918LMY CONTRATO.doc]] | Markdown: [[1918LMY CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[1918LMY CONTRATO.doc]] | Markdown: [[1918LMY CONTRATO.md]]
- Conductor: EULÀLIA MASS PONTE (DNI: 46988025Z) | Origen: PDF: [[1918LMY ACTA ENTREGA.pdf]] | Markdown: [[1918LMY ACTA ENTREGA.md]]
- Número Contrato: 454460 | Origen: PDF: [[1918LMY CONTRATO.doc]] | Markdown: [[1918LMY CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[1918LMY ACTA ENTREGA.pdf]] | Markdown: [[1918LMY ACTA ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-02-01 | Origen: PDF: [[1918LMY ACTA ENTREGA.pdf]] | Markdown: [[1918LMY ACTA ENTREGA.md]]
- Fecha Fin: 2024-03-08 | Origen: PDF: [[1918LMY ACTA DEVOLUCION.pdf]] | Markdown: [[1918LMY ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 36 días (Calculado entre 2024-02-01 y 2024-03-08)
- Fecha Matriculación: 2021-03-02 (APROXIMADA: "Primera expedición" de la ficha técnica, NO campo I/I.1 del permiso de circulación) | Origen: PDF: [[MA1918LMY (1).pdf]] | Markdown: [[MA1918LMY (1).md]]

## INVENTARIO DOCUMENTAL
- PDF: [[1918LMY ACTA DEVOLUCION.pdf]] | Markdown: [[1918LMY ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[1918LMY ACTA ENTREGA.pdf]] | Markdown: [[1918LMY ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[1918LMY CONTRATO.doc]] | Markdown: [[1918LMY CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA1918LMY (1).pdf]] | Markdown: [[MA1918LMY (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[1918LMY CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio: corregido de 2024-01-31 a 2024-02-01. El valor anterior era la "Fecha Salida" (31/01/2024, Barcelona), es decir, la fecha en que el vehículo salió de la base logística, no la fecha de entrega efectiva al cliente. La entrega real ("Fecha Entrada" en Vilanova i la Geltrú) fue el 01/02/2024, coincidente con "Fecha Entrega" y "Fecha Inicio Contrato" (01/02/2024) en [[1918LMY CONTRATO.md]].
- dias_arrendamiento: 36
- fecha_matriculacion: se mantiene 2021-03-02, pero marcada como APROXIMADA. El valor procede de "[[MA1918LMY (1).md]]" ("Primera expedición: 02/03/2021 17:52:28"), NO de los campos I/I.1 del permiso de circulación, que no son legibles en el documento. La marca de hora indica sello de emisión del documento, no fecha registral.
- CRITERIO PENDIENTE: mismo campo tratado con criterio distinto en otros vehículos del lote (ver [[2653LTG]]). Debe unificarse antes de cerrar el lote.
- fecha_fin (2024-03-08) verificado contra el acta de devolución: correcto, sin cambios.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 36d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 1102d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
