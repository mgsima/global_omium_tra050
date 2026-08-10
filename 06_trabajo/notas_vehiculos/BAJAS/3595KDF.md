---
matricula: "3595KDF"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT PARTNER CONFORT L1 1.6 BLUEHDI 75"
bastidor: "VF37ABHW6HJ696032"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA"
titular_cif: "A60401585"
numero_contrato: "CE/0820-2023-00391"
conductor_habitual: "A DESIGNAR POR"
conductor_dni: "12345678"
base_ubicacion: "BARCELONA (EL PRAT)"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-02-01"
fecha_fin: "2024-02-20"
dias_arrendamiento: 384
fecha_matriculacion: "2017-09-26"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Elegible pero sin alta compatible (sociedad/categoria/ventana)"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 3595KDF (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT PARTNER CONFORT L1 1.6 BLUEHDI 75 | Origen: [[Permiso de Circulación (D.3).pdf]]
- Bastidor: VF37ABHW6HJ696032 | Origen: [[Permiso de Circulación (E).pdf]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular / Arrendatario: COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA (CIF: A60401585) | Origen: PDF: [[3595KDF CONTRATO ANEXO.pdf]] | Markdown: [[3595KDF CONTRATO ANEXO.md]]
- Arrendador (titular registral DGT): NORTHGATE ESPAÑA RENTING FLEXIBLE SA (CIF: A28659423)
- Conductor: A DESIGNAR POR (DNI: 12345678) | Origen: PDF: [[3595KDF-ACTA DE ENTREGA.pdf]] | Markdown: [[3595KDF-ACTA DE ENTREGA.md]]
- Número Contrato: CE/0820-2023-00391 | Origen: PDF: [[3595KDF-ACTA DE ENTREGA.pdf]] | Markdown: [[3595KDF-ACTA DE ENTREGA.md]]
- Base / Ubicación: BARCELONA (EL PRAT) | Origen: PDF: [[3595KDF-ACTA DE ENTREGA.pdf]] | Markdown: [[3595KDF-ACTA DE ENTREGA.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("BARCELONA (EL PRAT)"), provincia de Barcelona.
- Fecha Inicio: 2023-02-01 | Origen: PDF: [[3595KDF-ACTA DE ENTREGA.pdf]] | Markdown: [[3595KDF-ACTA DE ENTREGA.md]]
- Fecha Fin: 2024-02-20 | Origen: [[Acta de Entrega (fecha fin prevista).pdf]]
- Días Arrendamiento / Tenencia: 384 días (Calculado entre 2023-02-01 y 2024-02-20)
- Fecha Matriculación: 2017-09-26 | Origen: [[Permiso de Circulación (I).pdf]]

## INVENTARIO DOCUMENTAL
- PDF: [[- 3595KDF PC.pdf]] | Markdown: [[- 3595KDF PC.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)
- PDF: [[- 3595KDF seguro (002).pdf]] | Markdown: [[- 3595KDF seguro (002).md]] (Tipo: DNI, Formato: PDF, Estado: VALIDO)
- PDF: [[3595KDF ACTA DEVOLUCION.pdf]] | Markdown: [[3595KDF ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[3595KDF CONTRATO ANEXO.pdf]] | Markdown: [[3595KDF CONTRATO ANEXO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3595KDF CONTRATO.pdf]] | Markdown: [[3595KDF CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[3595KDF FT.pdf]] | Markdown: [[3595KDF FT.md]] (Tipo: REVISION_MANUAL, Formato: PDF, Estado: VALIDO)
- PDF: [[3595KDF-ACTA DE ENTREGA.pdf]] | Markdown: [[3595KDF-ACTA DE ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)
- numero_contrato: corregido de "0811/202380026820/1/1" (número de Solicitud de Arrendamiento/SV, tomado de [[3595KDF CONTRATO ANEXO.md]]) a "CE/0820-2023-00391" (número real del Contrato de Alquiler individual), tomado del Acta de Entrega. El valor anterior era el identificador de la solicitud, no el del contrato de alquiler ejecutado.
- fecha_fin (2024-02-20) y dias_arrendamiento (384) ya estaban correctamente extraídos como PREVISTA (el Acta de Devolución real tiene el OCR ilegible), verificado sin cambios.
- Periodo de tenencia (384 días) por debajo de los 730 días de renting; se añade tag `elegibilidad_dudosa`.
- titular_empresa corregido de "NORTHGATE ESPAÑA RENTING FLEXIBLE SA" a "COMPANYIA GENERAL D'AIGUES DE CATALUNYA SA" (CIF A28659423 → A60401585). El valor anterior era el ARRENDADOR (empresa de alquiler / titular registral en DGT), no el arrendatario. Se sigue el criterio mayoritario del lote, donde `titular_empresa` recoge la sociedad del grupo Global Omnium que posee y usa el vehículo. El arrendador queda registrado en el cuerpo para no perder el dato.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con NORTHGATE. El contrato solo cubre 384d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 2338d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
