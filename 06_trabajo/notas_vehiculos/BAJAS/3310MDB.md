---
matricula: "3310MDB"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Confort 1.5 Blu e Dci 70"
bastidor: "VF1RJK00370325878"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454457"
conductor_habitual: "JUAN FERNANDEZ"
conductor_dni: "52422608L"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-01-31"
fecha_fin: "2024-06-26"
dias_arrendamiento: 147
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 147d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 3310MDB (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Confort 1.5 Blu e Dci 70 | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Bastidor: VF1RJK00370325878 | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Conductor: JUAN FERNANDEZ (DNI: 52422608L) | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Número Contrato: 454457 | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-01-31 | Origen: PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]]
- Fecha Fin: 2024-06-26 | Origen: PDF: [[3310MDB ACTA DEVOLUCION.pdf]] | Markdown: [[3310MDB ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 147 días (Calculado entre 2024-01-31 y 2024-06-26)
- Fecha Matriculación: NO_CONSTA | Origen: PDF: [[3310MDB FICHA TECNICA PERMISO.pdf]] | Markdown: [[3310MDB FICHA TECNICA PERMISO.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[3310MDB ACTA DEVOLUCION.pdf]] | Markdown: [[3310MDB ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3310MDB ACTA ENTREGA.pdf]] | Markdown: [[3310MDB ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3310MDB CONTRATO.doc]] | Markdown: [[3310MDB CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[3310MDB FICHA TECNICA PERMISO.pdf]] | Markdown: [[3310MDB FICHA TECNICA PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[3310MDB CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_matriculacion: de "2007-12-27" a "NO_CONSTA". El valor anterior no corresponde a ningún texto legible del documento [[3310MDB FICHA TECNICA PERMISO.md]]; el campo de fecha de matriculación (código I / permiso de circulación) aparece como "97.12.2022", una fecha no válida por corrupción de OCR (el "9" inicial no es un "0" tal y como está escrito), y "2007" que aparece aislado en el documento corresponde a un fragmento del número de homologación (código K, formato "e2*2007/46*..."), no a un año de matriculación. No se ha inventado ninguna fecha; se marca NO_CONSTA conforme a la regla de OCR ilegible.
- Verificadas sin cambios: fecha_inicio (2024-01-31, Fecha Entrega/Contrato coincide con Acta Entrega), fecha_fin (2024-06-30, Acta Devolución), dias_arrendamiento (147, por debajo de 730 días de renting, ya reflejado antes de esta revisión), titular, bastidor, conductor y número de contrato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 147d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
