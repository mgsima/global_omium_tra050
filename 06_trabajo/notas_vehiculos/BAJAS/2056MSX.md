---
matricula: 2056MSX
rol: BAJA
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: COMBUSTION_DIESEL
marca_modelo: PEUGEOT PARTNER
bastidor: VR3EDYHT0RN547484
combustible: DIESEL
categoria: N1
regimen: ALQUILER_CORTA_DURACION
servicio_dgt: NO_ESPECIFICADO
titular_empresa: MALCODIGITAL GROUP SAL
titular_cif: NO_CONSTA
numero_contrato: 11206873-1
conductor_habitual: JERSOVS, DMITRIJS
conductor_dni: BA543957
base_ubicacion: ALICANTE AIRPORT (ALC)
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: 2024-09-06
fecha_fin: 2024-12-05
dias_arrendamiento: 90
fecha_matriculacion: NO_CONSTA
tiene_acta_devolucion: false
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 90d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 2056MSX (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT PARTNER | Origen: PDF: [[2056MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2056MSX - DOCUMENTACIÓN.md]]
- Bastidor: VR3EDYHT0RN547484 | Origen: PDF: [[2056MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2056MSX - DOCUMENTACIÓN.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: ALQUILER_CORTA_DURACION (3 meses) | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Servicio DGT: NO_ESPECIFICADO
- Titular: MALCODIGITAL GROUP SAL (CIF: NO_CONSTA) | Origen: PDF: [[2056MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2056MSX - DOCUMENTACIÓN.md]]
- Conductor: JERSOVS, DMITRIJS (DNI: BA543957) | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Número Contrato: 11206873-1 | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Base / Ubicación: ALICANTE AIRPORT (ALC) | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("ALICANTE AIRPORT (ALC)"), provincia de Alicante.
- Fecha Inicio: 2024-09-06 (inicio del alquiler, 12:00) | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Fecha Fin: NO_CONSTA (devolución PREVISTA 2024-12-05, no acreditada como consumada) | Origen: PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]]
- Días Arrendamiento / Tenencia: 90 días (Calculado entre 2024-09-06 y 2024-12-05)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[2056MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2056MSX - DOCUMENTACIÓN.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[2056MSX CONTRATO.pdf]] | Markdown: [[2056MSX CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)

> [!warning] ELEGIBILIDAD TRA050 EN DUDA — NO PROCESAR SIN VALIDACIÓN
> Caso idéntico a [[2042MSX]]: alquiler de corta duración en **MALCO Rent a Car**, mismo número de autorización (11206873-1), mismo modelo PEUGEOT Partner **2024**, mismas fechas (06/09/2024 a 05/12/2024, 90 días), recogida y devolución en Alicante Airport.
> Un vehículo matriculado en 2024 y alquilado 90 días no puede ser el vehículo de combustión sustituido en una ficha TRA050. Confirmar con Global Omnium antes de incluirlo.

- Régimen corregido de RENTING a ALQUILER_CORTA_DURACION. Constaba como RENTING, lo que era engañoso: un alquiler de 90 días no cumple el umbral de 730 días del renting.
- Fecha Fin cambiada de NO_EXISTE_DOCUMENTO a NO_CONSTA: el contrato fija devolución PREVISTA el 05/12/2024, sin acta que acredite que se consumó.
- Titular corregido de "MALGO DIGITAL GROUP SAL" a "MALCODIGITAL GROUP SAL" (error de OCR, C leída como G).
- El conductor (JERSOVS, DMITRIJS, doc. BA543957) procede del contrato de alquiler y es el arrendatario firmante, no necesariamente personal de Global Omnium.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con MALCO. El contrato solo cubre 90d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
