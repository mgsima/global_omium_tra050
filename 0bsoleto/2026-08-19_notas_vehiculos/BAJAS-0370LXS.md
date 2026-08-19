---
matricula: "0370LXS"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT BOXER L2 H2"
bastidor: "VF3YCBPFB12087563"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "CANALIZACIONES CIVILES, S.A."
titular_cif: "A12013561"
numero_contrato: "2025 / 074"
conductor_habitual: "NO_CONSTA"
conductor_dni: "NO_CONSTA"
base_ubicacion: "Poligono Industrial Carrascal - Oeste, Camino de Albal, 65, 46469 Beniparrell (Valencia)"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-03-13"
fecha_fin: "2025-01-01"
dias_arrendamiento: 660
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 660d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 0370LXS (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT BOXER L2 H2 | Origen: PDF: [[0370LXS BAJA ALQUILER.pdf]] | Markdown: [[0370LXS BAJA ALQUILER.md]]
- Bastidor: VF3YCBPFB12087563 | Origen: PDF: [[0370LXS CONTRATO DE ALQUILER.pdf]] | Markdown: [[0370LXS CONTRATO DE ALQUILER.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: CANALIZACIONES CIVILES, S.A. (CIF: A12013561) | Origen: PDF: [[0370LXS CONTRATO DE ALQUILER.pdf]] | Markdown: [[0370LXS CONTRATO DE ALQUILER.md]]
- Conductor: NO_CONSTA (DNI: NO_CONSTA)
- Número Contrato: 2025 / 074 | Origen: PDF: [[0370LXS BAJA ALQUILER.pdf]] | Markdown: [[0370LXS BAJA ALQUILER.md]]
- Base / Ubicación: Poligono Industrial Carrascal - Oeste, Camino de Albal, 65, 46469 Beniparrell (Valencia) | Origen: PDF: [[0370LXS BAJA ALQUILER.pdf]] | Markdown: [[0370LXS BAJA ALQUILER.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("Poligono Industrial Carrascal - Oeste, Camino de Albal, 65, 46469 Beniparrell (Valencia)"), provincia de Valencia.
- Fecha Inicio: 2023-03-13 | Origen: PDF: [[0370LXS CONTRATO DE ALQUILER.pdf]] | Markdown: [[0370LXS CONTRATO DE ALQUILER.md]]
- Fecha Fin: 2025-01-01 (fecha del propio evento de baja; "Fecha hasta real" no legible en el documento) | Origen: PDF: [[0370LXS BAJA ALQUILER.pdf]] | Markdown: [[0370LXS BAJA ALQUILER.md]]
- Días Arrendamiento / Tenencia: 660 días (Calculado entre 2023-03-13 y 2025-01-01)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[0370LXS BAJA ALQUILER.pdf]] | Markdown: [[0370LXS BAJA ALQUILER.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[0370LXS CONTRATO DE ALQUILER.pdf]] | Markdown: [[0370LXS CONTRATO DE ALQUILER.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[0370LXS FICHA TECNICA.pdf]] | Markdown: [[0370LXS FICHA TECNICA.md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO)
- PDF: [[0370LXS PERMISO DE CIRCULACION.pdf]] | Markdown: [[0370LXS PERMISO DE CIRCULACION.md]] (Tipo: PERMISO_CIRCULACION, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)
- fecha_inicio: de "2025-01-01" a "2023-03-13". El valor anterior procedía del documento de BAJA ([[0370LXS BAJA ALQUILER.md]], contrato 2025/074), que corresponde al cierre/baja del arrendamiento, no al inicio. El inicio real consta en [[0370LXS CONTRATO DE ALQUILER.md]] ("2. Alta Alquiler", Beniparrell, lunes 13 de marzo de 2023, entrega "desde lunes, 13 de marzo de 2023").
- fecha_fin: de "2025-03-31" a "2025-01-01". El valor anterior era la "Fecha hasta prevista" (una previsión, no el hecho real) del documento de BAJA. El campo "Fecha hasta real" de ese mismo documento no es legible/está en blanco, por lo que, siguiendo la prioridad establecida, se usa la fecha del propio evento de baja (cabecera del documento y campo "Fecha desde" del formulario de BAJA: miércoles, 1 de enero de 2025).
- dias_arrendamiento: 660
- titular_empresa: de "Transportes y Líneas del Mediterráneo, S.L." a "CANALIZACIONES CIVILES, S.A.". El valor anterior era la empresa de alquiler (arrendador, letrero/CIF B46244554 que figura en la cabecera de ambos documentos), no el titular/arrendatario. El arrendatario real, identificado como "CLIENTE" en [[0370LXS CONTRATO DE ALQUILER.md]], es CANALIZACIONES CIVILES, S.A. (CIF A12013561); el documento de BAJA lo cita como CANALIZACIONES CIVILES, S.A.U.
- titular_cif: de "B46244554" (CIF de la empresa de alquiler) a "A12013561" (CIF real del cliente/arrendatario).

> [!danger] EL UMBRAL DE 730 DÍAS DEPENDE DE UN CAMPO ILEGIBLE — VERIFICAR EL PDF ORIGINAL
> El formulario de BAJA de TLM declara un par de fechas (`Fecha desde: 01/01/2025` / `Fecha hasta prevista: 31/03/2025`) y el campo decisivo, `Fecha hasta real`, sale del OCR como `120`, ilegible.
> - Si la devolución efectiva fue el **01/01/2025** → 660 días → **NO** alcanza el umbral de renting.
> - Si fue el **31/03/2025** → **749 días** → **SÍ** lo alcanza.
>
> Este expediente cruza el umbral de elegibilidad en función de ese dato. Se ha optado por 660 días por ser la lectura conservadora, pero **no es una conclusión firme**: hay que abrir [[0370LXS BAJA ALQUILER.pdf]] y leer "Fecha hasta real" a ojo antes de decidir. Es el único vehículo del lote donde la ambigüedad del formulario TLM cambia el resultado.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con TLM. El contrato solo cubre 660d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
