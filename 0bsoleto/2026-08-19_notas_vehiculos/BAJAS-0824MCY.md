---
matricula: "0824MCY"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "SKODA Karoq 2.0 Tdi 110kw (150cv) Dsg 4x4"
bastidor: "TMBLJ7NU1P5016011"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "436446"
conductor_habitual: "Jose Antonio Navarro Melero"
conductor_dni: "53285014V"
base_ubicacion: "LLEIDA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-02-16"
fecha_fin: "2023-05-12"
dias_arrendamiento: 85
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 85d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 0824MCY (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: SKODA Karoq 2.0 Tdi 110kw (150cv) Dsg 4x4 | Origen: PDF: [[0824MCY ACTA DEVOLUCION.pdf]] | Markdown: [[0824MCY ACTA DEVOLUCION.md]]
- Bastidor: TMBLJ7NU1P5016011 | Origen: PDF: [[0824MCY CONTRATO.doc]] | Markdown: [[0824MCY CONTRATO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[0824MCY CONTRATO.doc]] | Markdown: [[0824MCY CONTRATO.md]]
- Conductor: Jose Antonio Navarro Melero (DNI: 53285014V) | Origen: PDF: [[0824MCY ACTA DEVOLUCION.pdf]] | Markdown: [[0824MCY ACTA DEVOLUCION.md]]
- Número Contrato: 436446 | Origen: PDF: [[0824MCY CONTRATO.doc]] | Markdown: [[0824MCY CONTRATO.md]]
- Base / Ubicación: LLEIDA | Origen: PDF: [[0824MCY ACTA DEVOLUCION.pdf]] | Markdown: [[0824MCY ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("LLEIDA"), provincia de Lleida.
- Fecha Inicio: 2023-02-16 | Origen: PDF: [[0824MCY ACTA ENTREGA.pdf]] | Markdown: [[0824MCY ACTA ENTREGA.md]]
- Fecha Fin: 2023-05-12 | Origen: PDF: [[0824MCY ACTA DEVOLUCION.pdf]] | Markdown: [[0824MCY ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 85 días (Calculado entre 2023-02-16 y 2023-05-12)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[0824MCY ACTA DEVOLUCION.pdf]] | Markdown: [[0824MCY ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[0824MCY ACTA ENTREGA.pdf]] | Markdown: [[0824MCY ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[0824MCY CONTRATO.doc]] | Markdown: [[0824MCY CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA0824MCY (1).pdf]] | Markdown: [[MA0824MCY (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[0824MCY CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **85 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 85d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
