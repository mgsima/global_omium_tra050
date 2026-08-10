---
matricula: "8677MGK"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Advance 1.5 Blu e Dci 70"
bastidor: "VF1RJK00170658578"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "454459"
conductor_habitual: "EULALIA MASS PONTE"
conductor_dni: "46988025Z"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-02-01"
fecha_fin: "2024-07-31"
dias_arrendamiento: 181
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 181d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 8677MGK (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 | Origen: PDF: [[8677MGK CONTRATO.doc]] | Markdown: [[8677MGK CONTRATO.md]]
- Bastidor: VF1RJK00170658578 | Origen: PDF: [[8677MGK CONTRATO.doc]] | Markdown: [[8677MGK CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[8677MGK CONTRATO.doc]] | Markdown: [[8677MGK CONTRATO.md]]
- Conductor: EULALIA MASS PONTE (DNI: 46988025Z) | Origen: PDF: [[8677MGK ACTA ENTREGA.pdf]] | Markdown: [[8677MGK ACTA ENTREGA.md]]
- Número Contrato: 454459 | Origen: PDF: [[8677MGK CONTRATO.doc]] | Markdown: [[8677MGK CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[8677MGK ACTA ENTREGA.pdf]] | Markdown: [[8677MGK ACTA ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-02-01 | Origen: PDF: [[8677MGK ACTA ENTREGA.pdf]] | Markdown: [[8677MGK ACTA ENTREGA.md]] (campo "Fecha Entrada"/"Fecha Entrega")
- Fecha Fin: 2024-07-31 | Origen: PDF: [[8677MGK ACTA DEVOLUCION.pdf]] | Markdown: [[8677MGK ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 181 días (Calculado entre 2024-02-01 y 2024-07-31)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[8677MGK ACTA DEVOLUCION.pdf]] | Markdown: [[8677MGK ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[8677MGK ACTA ENTREGA.pdf]] | Markdown: [[8677MGK ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[8677MGK CONTRATO.doc]] | Markdown: [[8677MGK CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA8677MGK.pdf]] | Markdown: [[MA8677MGK.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[8677MGK CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio: de "2024-01-31" a "2024-02-01". El valor anterior correspondía al campo "Fecha Salida" (salida del vehículo de la base de Barcelona) de [[8677MGK ACTA ENTREGA.md]]; el vehículo llegó a destino (Vilanova i la Geltrú) y quedó formalmente entregado el 01/02/2024 ("Fecha Entrada"/"Fecha Entrega"), dato que coincide con [[8677MGK CONTRATO.md]] ("Fecha Entrega: 01/02/2024").
- dias_arrendamiento: 181
- combustible: de "Gasolina" a "DIESEL". El valor anterior contradecía el propio campo tipo_vehiculo ("COMBUSTION_DIESEL") ya registrado en la nota y la denominación del vehículo en el contrato ("Express Advance 1.5 Blu e Dci 70"), donde "Dci" identifica el motor diésel Renault. El "Gasolina" que aparece en las actas de entrega/devolución corresponde a una etiqueta de plantilla mal reconocida por OCR junto al indicador de nivel de combustible, no a una selección real de tipo de combustible.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 181d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
