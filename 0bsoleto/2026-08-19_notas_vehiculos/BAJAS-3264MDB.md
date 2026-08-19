---
matricula: "3264MDB"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Confort 1.5 Blu e Dci 70"
bastidor: "VF1RJK00170325877"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454456"
conductor_habitual: "MARC MARZABAL"
conductor_dni: "52422608L"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-01-31"
fecha_fin: "2024-05-13"
dias_arrendamiento: 103
fecha_matriculacion: "2022-12-27"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 103d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 3264MDB (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Confort 1.5 Blu e Dci 70 | Origen: PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]]
- Bastidor: VF1RJK00170325877 | Origen: PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]]
- Conductor: MARC MARZABAL (DNI: 52422608L) | Origen: PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]]
- Número Contrato: 454456 | Origen: PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[3264MDB ACTA ENTREGA.pdf]] | Markdown: [[3264MDB ACTA ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-01-31 | Origen: PDF: [[3264MDB ACTA ENTREGA.pdf]] | Markdown: [[3264MDB ACTA ENTREGA.md]]
- Fecha Fin: 2024-05-13 | Origen: PDF: [[3264MDB ACTA DEVOLUCION.pdf]] | Markdown: [[3264MDB ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 103 días (Calculado entre 2024-01-31 y 2024-05-13)
- Fecha Matriculación: 2022-12-27 | Origen: PDF: [[MA3264MDB.pdf]] | Markdown: [[MA3264MDB.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[3264MDB ACTA DEVOLUCION.pdf]] | Markdown: [[3264MDB ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3264MDB ACTA ENTREGA.pdf]] | Markdown: [[3264MDB ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3264MDB CONTRATO.doc]] | Markdown: [[3264MDB CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA3264MDB.pdf]] | Markdown: [[MA3264MDB.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[3264MDB CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2024-01-31) y fecha_fin (2024-05-13) verificadas: ya estaban correctamente tomadas de [[3264MDB ACTA ENTREGA.md]] y [[3264MDB ACTA DEVOLUCION.md]] respectivamente. Sin cambios en fechas ni en días de arrendamiento (103 días).
- fecha_matriculacion: de NO_CONSTA a "2022-12-27". El dato estaba disponible en el bloque de Permiso de Circulación de [[MA3264MDB.md]] (fecha 27-12-2022 repetida en los campos I / I.1), consistente con la próxima ITV (27-12-2024) citada también en el contrato, y no había sido extraído.
- Discrepancia sin resolver (no corregida): el conductor que figura en la entrega (MARC MARZABAL) difiere del que figura en la devolución (Eulalia Mas) en [[3264MDB ACTA DEVOLUCION.md]]; se mantiene el conductor de la entrega por ser el que coincide con el contrato, pero podría tratarse de un cambio de conductor habitual durante el periodo no reflejado en el YAML.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 103d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 503d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
