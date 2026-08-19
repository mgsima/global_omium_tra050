---
matricula: "1722MGL"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT EXPRESS Advance 1.5 Blu e Dci 70"
bastidor: "VF1RJK00270658461"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454458"
conductor_habitual: "Juan Fernandez León"
conductor_dni: "52422608L"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-01-31"
fecha_fin: "2024-05-21"
dias_arrendamiento: 111
fecha_matriculacion: "2023-04-27"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 111d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 1722MGL (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT EXPRESS Advance 1.5 Blu e Dci 70 | Origen: PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]]
- Bastidor: VF1RJK00270658461 | Origen: PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]]
- Conductor: Juan Fernandez León (DNI: 52422608L) | Origen: PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]]
- Número Contrato: 454458 | Origen: PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[1722MGL ACTA ENTREGA.pdf]] | Markdown: [[1722MGL ACTA ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-01-31 | Origen: PDF: [[1722MGL ACTA ENTREGA.pdf]] | Markdown: [[1722MGL ACTA ENTREGA.md]]
- Fecha Fin: 2024-05-21 | Origen: PDF: [[1722MGL ACTA DEVOLUCION.pdf]] | Markdown: [[1722MGL ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 111 días (Calculado entre 2024-01-31 y 2024-05-21)
- Fecha Matriculación: 2023-04-27 | Origen: PDF: [[MA1722MGL.pdf]] | Markdown: [[MA1722MGL.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[1722MGL ACTA DEVOLUCION.pdf]] | Markdown: [[1722MGL ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[1722MGL ACTA ENTREGA.pdf]] | Markdown: [[1722MGL ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[1722MGL CONTRATO.doc]] | Markdown: [[1722MGL CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA1722MGL.pdf]] | Markdown: [[MA1722MGL.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[1722MGL CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2024-01-31) y fecha_fin (2024-05-21) verificadas: ya estaban correctamente tomadas de [[1722MGL ACTA ENTREGA.md]] y [[1722MGL ACTA DEVOLUCION.md]] respectivamente. Sin cambios en fechas ni en días de arrendamiento (111 días).
- fecha_matriculacion: de NO_CONSTA a "2023-04-27". El dato estaba disponible y legible en el bloque de Permiso de Circulación de [[MA1722MGL.md]] (campo I: 27-04-2023, coincide con (I.1) Fecha de expedición), y no había sido extraído.
- Se corrige además el formato de los enlaces de Origen de "Base / Ubicación" y "Fecha Inicio" en la trazabilidad, que apuntaban a un nombre de archivo genérico inexistente ([[ACTA_ENTREGA.pdf]]) en lugar de al documento real ([[1722MGL ACTA ENTREGA.pdf]] / [[1722MGL ACTA ENTREGA.md]]).

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 111d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 390d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
