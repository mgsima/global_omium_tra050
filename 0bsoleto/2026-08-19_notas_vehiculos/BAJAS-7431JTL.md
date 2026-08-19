---
matricula: "7431JTL"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL Corsa 1.4 Expression 90 Cv"
bastidor: "W0L0XEP68G4310572"
combustible: "Gas-oil"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "GLOBAL OMNIUM MEDIOAMBIENTE SL"
titular_cif: "B46017018"
numero_contrato: "434619"
conductor_habitual: "JESÚS LOPEZ MORALES"
conductor_dni: "B46017018"
base_ubicacion: "Gran Canaria"
comunidad_autonoma: "Canarias"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-02-21"
fecha_fin: "2024-08-27"
dias_arrendamiento: 553
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 553d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 7431JTL (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: OPEL Corsa 1.4 Expression 90 Cv | Origen: PDF: [[7431JTL ACTA DEVOLUCION.pdf]] | Markdown: [[7431JTL ACTA DEVOLUCION.md]]
- Bastidor: W0L0XEP68G4310572 | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Gas-oil
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: GLOBAL OMNIUM MEDIOAMBIENTE SL (CIF: B46017018) | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Conductor: JESÚS LOPEZ MORALES (DNI: B46017018) | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Número Contrato: 434619 | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Base / Ubicación: Gran Canaria | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Comunidad Autónoma: Canarias | Derivada de `base_ubicacion` ("Gran Canaria"), provincia de Las Palmas.
- Fecha Inicio: 2023-02-21 | Origen: PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]]
- Fecha Fin: 2024-08-27 | Origen: PDF: [[7431JTL ACTA DEVOLUCION.pdf]] | Markdown: [[7431JTL ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 553 días (Calculado entre 2023-02-21 y 2024-08-27)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[7431JTL ACTA DEVOLUCION.pdf]] | Markdown: [[7431JTL ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[7431JTL ACTA ENTREGA.pdf]] | Markdown: [[7431JTL ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[7431JTL CONTRATO.doc]] | Markdown: [[7431JTL CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)

- Alerta Formato: WORD_DETECTADO en [[7431JTL CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- tipo_vehiculo: corregido de COMBUSTION_GASOLINA a COMBUSTION_DIESEL, para ser coherente con el campo combustible ("Gas-oil"), tal como consta en el Acta de Entrega y el Acta de Devolución (campo "Combustible: Gas-oil"). El YAML original era contradictorio consigo mismo (combustible Gas-oil pero tipo_vehiculo Gasolina).
- fecha_inicio (2023-02-21, del Contrato) y fecha_fin (2024-08-27, del Acta de Devolución) ya estaban correctamente extraídas, verificado sin cambios. dias_arrendamiento (553) se mantiene.
- Periodo de tenencia (553 días) por debajo de los 730 días de renting; se añade tag `elegibilidad_dudosa`.
- Discrepancia sin resolver (no corregida): en el Contrato y el Acta de Entrega, el campo DNI del conductor (JESÚS LOPEZ MORALES) figura como "B46017018", que coincide con el CIF de GLOBAL OMNIUM MEDIOAMBIENTE SL, no con un DNI personal. Se mantiene el valor tal como consta en los documentos originales (no se ha inventado un DNI), pero se señala como probable error del documento fuente.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 553d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
