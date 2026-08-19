---
matricula: "7017MPH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Advance 1.5 Blu e Dci 70"
bastidor: "VF1RJK00X72667395"
combustible: "Gas-oil"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "460662"
conductor_habitual: "gil Abel Figueras"
conductor_dni: "36983662F"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-06-03"
fecha_fin: "2024-08-12"
dias_arrendamiento: 70
fecha_matriculacion: "NO_EXISTE_DOCUMENTO"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 70d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 7017MPH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 | Origen: PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]]
- Bastidor: VF1RJK00X72667395 | Origen: PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Gas-oil
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]]
- Conductor: gil Abel Figueras (DNI: 36983662F) | Origen: PDF: [[7017MPH ACTA DEVOLUCION.pdf]] | Markdown: [[7017MPH ACTA DEVOLUCION.md]]
- Número Contrato: 460662 | Origen: PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[7017MPH ACTA DEVOLUCION.pdf]] | Markdown: [[7017MPH ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-06-03 | Origen: PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]]
- Fecha Fin: 2024-08-12 | Origen: PDF: [[7017MPH ACTA DEVOLUCION.pdf]] | Markdown: [[7017MPH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 70 días (Calculado entre 2024-06-03 y 2024-08-12)
- Fecha Matriculación: NO_EXISTE_DOCUMENTO (no hay permiso de circulación en el expediente; la ficha técnica solo aporta fecha del certificado de conformidad, que no es válida para este campo)

## INVENTARIO DOCUMENTAL
- PDF: [[7017MPH ACTA DEVOLUCION.pdf]] | Markdown: [[7017MPH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[7017MPH ACTA ENTREGA.pdf]] | Markdown: [[7017MPH ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[7017MPH CONTRATO.doc]] | Markdown: [[7017MPH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA7017MPH.pdf]] | Markdown: [[MA7017MPH.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[7017MPH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio (2024-06-03) y fecha_fin (2024-08-12) verificadas: ya estaban correctamente tomadas de [[7017MPH ACTA ENTREGA.md]] y [[7017MPH ACTA DEVOLUCION.md]] respectivamente, no de un documento de baja mal identificado. Sin cambios en fechas ni en días de arrendamiento (70 días).
- fecha_matriculacion: de "2024-03-12" a NO_EXISTE_DOCUMENTO. El valor anterior procedía de la "Fecha de emisión" del certificado de conformidad en [[MA7017MPH.md]], que la normativa excluye expresamente como fuente. No existe en el expediente un permiso de circulación con los campos I / I.1 legibles.
- conductor_dni: de NO_CONSTA a "36983662F", legible junto a la firma del conductor en [[7017MPH ACTA DEVOLUCION.md]].

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 70d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
