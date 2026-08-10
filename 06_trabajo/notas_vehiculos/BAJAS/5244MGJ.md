---
matricula: "5244MGJ"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.5d Dt 74kw (100cv) Edition"
bastidor: "VXKUBYHTKP4108389"
combustible: "DIESEL"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448559"
conductor_habitual: "Cristina saldarriaga"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-03"
fecha_fin: "2023-11-29"
dias_arrendamiento: 57
fecha_matriculacion: "2023-04-25"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 57d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5244MGJ (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.5d Dt 74kw (100cv) Edition | Origen: PDF: [[5244MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5244MGJ ACTA DEVOLUCION.md]]
- Bastidor: VXKUBYHTKP4108389 | Origen: PDF: [[5244MGJ CONTRATO.doc]] | Markdown: [[5244MGJ CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[5244MGJ CONTRATO.doc]] | Markdown: [[5244MGJ CONTRATO.md]]
- Conductor: Cristina saldarriaga (DNI: NO_CONSTA) | Origen: PDF: [[5244MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5244MGJ ACTA DEVOLUCION.md]]
- Número Contrato: 448559 | Origen: PDF: [[5244MGJ CONTRATO.doc]] | Markdown: [[5244MGJ CONTRATO.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[5244MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5244MGJ ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-03 | Origen: PDF: [[5244MGJ CONTRATO.doc]] | Markdown: [[5244MGJ CONTRATO.md]]
- Fecha Fin: 2023-11-29 | Origen: PDF: [[5244MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5244MGJ ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 57 días (Calculado entre 2023-10-03 y 2023-11-29)
- Fecha Matriculación: 2023-04-25 | Origen: PDF: [[MA5244MGJ (1).pdf]] | Markdown: [[MA5244MGJ (1).md]]

## INVENTARIO DOCUMENTAL
- PDF: [[5244MGJ ACTA DEVOLUCION.pdf]] | Markdown: [[5244MGJ ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5244MGJ CONTRATO.doc]] | Markdown: [[5244MGJ CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA5244MGJ (1).pdf]] | Markdown: [[MA5244MGJ (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[5244MGJ CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **57 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 57d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 218d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
