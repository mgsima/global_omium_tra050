---
matricula: "2502LZC"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Confort 1.5 Blu e Dci 70"
bastidor: "VF1RJK00669309894"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454314"
conductor_habitual: "HONORIO ROYO LLEIXA"
conductor_dni: "47629922G"
base_ubicacion: "TARRAGONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-02-01"
fecha_fin: "2024-03-21"
dias_arrendamiento: 49
fecha_matriculacion: "2022-07-07"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 49d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 2502LZC (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Confort 1.5 Blu e Dci 70 | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Bastidor: VF1RJK00669309894 | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Conductor: HONORIO ROYO LLEIXA (DNI: 47629922G) | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Número Contrato: 454314 | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Base / Ubicación: TARRAGONA | Origen: PDF: [[2502LZC ACTA DEVOLUCION.pdf]] | Markdown: [[2502LZC ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("TARRAGONA"), provincia de Tarragona.
- Fecha Inicio: 2024-02-01 | Origen: PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]]
- Fecha Fin: 2024-03-21 | Origen: PDF: [[2502LZC ACTA DEVOLUCION.pdf]] | Markdown: [[2502LZC ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 49 días (Calculado entre 2024-02-01 y 2024-03-21)
- Fecha Matriculación: 2022-07-07 | Origen: [[FICHA TECNICA.pdf]]

## INVENTARIO DOCUMENTAL
- PDF: [[2502LZC  CONTRATO.doc]] | Markdown: [[2502LZC  CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[2502LZC ACTA DEVOLUCION.pdf]] | Markdown: [[2502LZC ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[MA2502LZC.pdf]] | Markdown: [[MA2502LZC.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[2502LZC  CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **49 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 49d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 623d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
