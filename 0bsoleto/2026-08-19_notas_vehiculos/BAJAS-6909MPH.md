---
matricula: "6909MPH"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "RENAULT INDUST. Express Advance 1.5 Blu e Dci 70"
bastidor: "VF1RJK00772667404"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "460660"
conductor_habitual: "Jordi ríos"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Barcelona"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2024-06-03"
fecha_fin: "2024-08-12"
dias_arrendamiento: 70
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 70d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 6909MPH (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: RENAULT INDUST. Express Advance 1.5 Blu e Dci 70 | Origen: PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]]
- Bastidor: VF1RJK00772667404 | Origen: PDF: [[6909MPH CONTRATO.doc]] | Markdown: [[6909MPH CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL | Origen: PDF: [[6909MPH CONTRATO.doc]] | Markdown: [[6909MPH CONTRATO.md]]
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]]
- Conductor: Jordi ríos (DNI: NO_CONSTA) | Origen: PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]]
- Número Contrato: 460660 | Origen: PDF: [[6909MPH CONTRATO.doc]] | Markdown: [[6909MPH CONTRATO.md]]
- Base / Ubicación: Barcelona | Origen: PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("Barcelona"), provincia de Barcelona.
- Fecha Inicio: 2024-06-03 | Origen: PDF: [[6909MPH ACTA ENTREGA.pdf]] | Markdown: [[6909MPH ACTA ENTREGA.md]]
- Fecha Fin: 2024-08-12 | Origen: PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 70 días (Calculado entre 2024-06-03 y 2024-08-12)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[6909MPH ACTA DEVOLUCION.pdf]] | Markdown: [[6909MPH ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[6909MPH ACTA ENTREGA.pdf]] | Markdown: [[6909MPH ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[6909MPH CONTRATO.doc]] | Markdown: [[6909MPH CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)
- PDF: [[MA6909MPH.pdf]] | Markdown: [[MA6909MPH.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)

- Alerta Formato: WORD_DETECTADO en [[6909MPH CONTRATO.doc]]

## REVISIÓN MANUAL (2026-07-23)
- Combustible corregido de "Gasolina" a "DIESEL": la marca/modelo (RENAULT Express Advance 1.5 Blue dCi 70, en CONTRATO, ACTA ENTREGA y ACTA DEVOLUCION) es un motor diésel ("dCi" = Diesel Common Rail Injection), y el propio campo `tipo_vehiculo` ya estaba correctamente marcado como COMBUSTION_DIESEL. El valor "Gasolina" del OCR corresponde a la etiqueta fija del indicador de nivel de depósito de los formularios ACTA ENTREGA/DEVOLUCION (escala 0 a Lleno), no a una selección de tipo de combustible, y contradecía el resto del expediente.
- fecha_inicio (2024-06-03) y fecha_fin (2024-08-12) verificadas: proceden de la ACTA ENTREGA (coincide con "Fecha Entrega" del CONTRATO) y de la ACTA DEVOLUCION respectivamente (sin campo "Fecha hasta real" en el formulario). Sin cambios en fechas.
- Resto de campos (bastidor, titular, número de contrato) verificados y coherentes con los documentos fuente. conductor_dni permanece NO_CONSTA: el DNI que aparece al pie de la ACTA DEVOLUCION (90002118J) no está inequívocamente atribuido al conductor declarado (Jordi ríos), por lo que no se ha inventado la atribución.
- dias_arrendamiento = 70 días, muy por debajo de los 730 días exigibles en RENTING. Se marca `elegibilidad_dudosa`.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 70d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
