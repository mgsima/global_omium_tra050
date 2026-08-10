---
matricula: "3483KWB"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT Clio Sport Tou. Zen En. Dci 66kw"
bastidor: "VF1R9800462262448"
combustible: "Diesel"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "MEDICION AVANZADA DE CONTADORES SA"
titular_cif: "A96674460"
numero_contrato: "452463"
conductor_habitual: "Miguel Angel Fernández de la fe"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Sevilla"
comunidad_autonoma: "Andalucía"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-12-22"
fecha_fin: "2024-04-11"
dias_arrendamiento: 111
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 111d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 3483KWB (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT Clio Sport Tou. Zen En. Dci 66kw | Origen: PDF: [[3483KWB ACTA DEVOLUCION.pdf]] | Markdown: [[3483KWB ACTA DEVOLUCION.md]]
- Bastidor: VF1R9800462262448 | Origen: PDF: [[3483KWB FICHA Y PERMISO.pdf]] | Markdown: [[3483KWB FICHA Y PERMISO.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: MEDICION AVANZADA DE CONTADORES SA (CIF: A96674460) | Origen: [[Condiciones Particulares.pdf]]
- Conductor: Miguel Angel Fernández de la fe (DNI: NO_CONSTA) | Origen: PDF: [[3483KWB ACTA DEVOLUCION.pdf]] | Markdown: [[3483KWB ACTA DEVOLUCION.md]]
- Número Contrato: 452463 | Origen: [[Condiciones Particulares.pdf]]
- Base / Ubicación: Sevilla | Origen: PDF: [[3483KWB ACTA DEVOLUCION.pdf]] | Markdown: [[3483KWB ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Andalucía | Derivada de `base_ubicacion` ("Sevilla"), provincia de Sevilla.
- Fecha Inicio: 2023-12-22 | Origen: [[Acta Entrega, Condiciones Particulares.pdf]]
- Fecha Fin: 2024-04-11 | Origen: PDF: [[3483KWB ACTA DEVOLUCION.pdf]] | Markdown: [[3483KWB ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 111 días (Calculado entre 2023-12-22 y 2024-04-11)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[3483KWB ACTA DEVOLUCION.pdf]] | Markdown: [[3483KWB ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3483KWB ACTA ENTREGA.pdf]] | Markdown: [[3483KWB ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3483KWB FICHA Y PERMISO.pdf]] | Markdown: [[3483KWB FICHA Y PERMISO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3483KWBCondicionesparticulares_20251021092238.412_X.doc]] | Markdown: [[3483KWBCondicionesparticulares_20251021092238.412_X.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)

- Alerta Formato: WORD_DETECTADO en [[3483KWBCondicionesparticulares_20251021092238.412_X.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Verificado contra todos los documentos del expediente en la revisión de tenencias <730 días. `fecha_inicio` procede del contrato/acta de entrega y `fecha_fin` del acta de devolución: **la extracción era correcta**, no ha sido necesario modificar las fechas.
- El periodo de tenencia acreditado es de **111 días**, muy por debajo de los **730 días** exigidos en régimen de RENTING. Se etiqueta `elegibilidad_dudosa`: el periodo corto es real, no un error de extracción.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 111d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
