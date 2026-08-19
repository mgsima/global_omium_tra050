---
matricula: "2842LYK"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "CITROEN INDUST. Berlingo Talla M Bluehdi 100"
bastidor: "VR7EFYHT2NN525970"
combustible: "Diesel"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454313"
conductor_habitual: "Joel"
conductor_dni: "NO_CONSTA"
base_ubicacion: "TARRAGONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-02-01"
fecha_fin: "2024-03-21"
dias_arrendamiento: 49
fecha_matriculacion: "2022-06-03"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 49d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 2842LYK (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: CITROEN INDUST. Berlingo Talla M Bluehdi 100 | Origen: PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]]
- Bastidor: VR7EFYHT2NN525970 | Origen: PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]]
- Conductor: Joel (DNI: NO_CONSTA) | Origen: PDF: [[2842LYK ACTA DEVOLUCION.pdf]] | Markdown: [[2842LYK ACTA DEVOLUCION.md]]
- Número Contrato: 454313 | Origen: PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]]
- Base / Ubicación: TARRAGONA | Origen: PDF: [[2842LYK ACTA DEVOLUCION.pdf]] | Markdown: [[2842LYK ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("TARRAGONA"), provincia de Tarragona.
- Fecha Inicio: 2024-02-01 | Origen: PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]]
- Fecha Fin: 2024-03-21 | Origen: PDF: [[2842LYK ACTA DEVOLUCION.pdf]] | Markdown: [[2842LYK ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 49 días (Calculado entre 2024-02-01 y 2024-03-21)
- Fecha Matriculación: 2022-06-03 | Origen: PDF: [[MA2842LYK.pdf]] | Markdown: [[MA2842LYK.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[2842LYK ACTA DEVOLUCION.pdf]] | Markdown: [[2842LYK ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[2842LYK CONTRATO.doc]] | Markdown: [[2842LYK CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA2842LYK.pdf]] | Markdown: [[MA2842LYK.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[2842LYK CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Fecha Matriculación corregida de NO_CONSTA a 2022-06-03: el campo "Primera expedición" de la Tarjeta ITV expedida por DGT (dato I/I.1 de matriculación) es legible en [[MA2842LYK.md]] ("Primera expedición: 03/06/2022 16:56:34"), coherente con la primera inspección ITV el 03/06/2022. Se había dejado NO_CONSTA por error de extracción.
- Verificado: fecha_inicio (2024-02-01, del campo "Fecha Entrega" en [[2842LYK CONTRATO.md]]) y fecha_fin (2024-03-21, del acta de devolución marcada DEVOLUCIÓN) son correctas; no proceden del documento de baja el inicio. dias_arrendamiento = 49 días, no se modifica.
- El periodo de tenencia (49 días) no alcanza los 730 días exigibles en un régimen RENTING; se marca elegibilidad_dudosa.
- Discrepancia sin resolver: el conductor habitual registrado ("Joel", del acta de devolución) no coincide con la persona que retira el vehículo según el contrato ("HONORIO ROYO LLEIXA"). No se modifica el campo por tratarse de un posible cambio de conductor durante el periodo de alquiler.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 49d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 657d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
