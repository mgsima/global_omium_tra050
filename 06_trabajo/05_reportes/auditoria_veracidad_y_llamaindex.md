# 📋 Informe de Auditoría de Veracidad y Selección para LlamaIndex / LlamaCloud API
**Campaña:** Global Omnium TRA050  
**Fecha de Auditoría:** 2026-07-22  
**Autor:** Agente IA Auditor TRA050  

## 1. Resumen Ejecutivo
Se ha llevado a cabo una verificación exhaustiva de veracidad cruzando el 100% de las Notas de Coche en `resultados_creacion/global_omnium/notas_vehiculos/` (carpetas ALTAS y BAJAS) contra los textos extraídos en caché Markdown en `resultados_creacion/global_omnium/03_cache_markdown/`.

### Métricas Clave
* **Total Notas Comprobadas:** 317 (156 ALTAS, 161 BAJAS)
* **Notas con Veracidad Total Estricta (Datos completos sin fallbacks):** 38 notas (11.98%)
* **Notas con Fallbacks o Bastidor Pendiente:** 279 notas (88.02%)
* **Vehículos con Bastidor Faltante (`PENDIENTE_INCORPORAR`):** 148 vehículos (77 Altas, 71 Bajas)
* **Documentos Afectados que Requieren Reprocesamiento en LlamaIndex API:** 182 archivos

## 2. Desglose de Deficiencias de Veracidad Encontradas

### A. Bastidores VIN (17 Caracteres)
* En 148 vehículos (46.69%), la extracción previa con `liteparse` no logró obtener el bastidor VIN.
* Motivos principales:
  * PDFs escaneados donde el texto vectorial estaba completamente ausente o corrupto.
  * Tarjetas eITV y Permisos de Circulación donde las tablas fueron destruidas por el parser ligero.
  * Facturas de compra de vehículo nuevo donde la línea de chasis contenía artefactos de OCR.

### B. Inconsistencias de Combustible en Vehículos de ALTA
* Las 156 notas de ALTAS corresponden a vehículos `ELECTRICO_BEV`.
* No obstante, la plantilla YAML generó `combustible: "DIESEL"` por defecto cuando el texto del markdown no incluyó explícitamente el término "eléctrico" o "BEV" en las reglas de detección.

### C. NIFs y Nombres de Titular Asignados por Fallback
* Se detectaron 214 notas donde el NIF fue fijado automáticamente a `A60401585` (`COMPANYIA GENERAL D AIGUES CATALUNY`).
* En expedientes donde el comprador real figuraba como `Empresa Mixta Valenciana de Aguas, S.A.` (`A97197511`) o `Medición Avanzada de Contadores S.A.` (`A96674460`), el parser ignoró el NIF secundario.

## 3. Listado Exacto de Archivos que Requieren Reprocesamiento con LlamaIndex / LlamaCloud API

A continuación se detalla la lista de carpetas y archivos Markdown cuyo documento PDF de origen debe ser enviado obligatoriamente a la API de LlamaIndex / LlamaCloud para extracción visual estructurada:

### A. Documentos con Garabatos de OCR / Salida Incompleta (< 200 caracteres útiles)
1. `ALTAS/0602KHK/1053A4604951674000000132024.md` (Texto ininteligible, caracteres ``, ``)
2. `ALTAS/2043MJP/1505A4604951674000000852023.md` (OCR corrupto en tabla de chasis)
3. `ALTAS/2062MJP/1505A4604951674000000872023.md` (Basura de caracteres OCR)
4. `ALTAS/2076MJP/1505A4604951674000000882023.md` (OCR roto en factura)
5. `ALTAS/2087MJP/1505A4604951674000000162023.md` (OCR incompleto)
6. `ALTAS/2120MFK/1505A4604951674000000842023.md` (Fallo de OCR en datos clave)
7. `ALTAS/5566KSD/1004A4604951674000001122023.md` (Tabla de precios e IVA rota)
8. `ALTAS/8867KDN/8867KDN 1505A4604951674000000002023.md` (Fallo masivo de OCR)
9. `ALTAS/8868KDN/1505A4604951674000000092023.md` (OCR ininteligible)
10. `ALTAS/8877KDN/8877KDN 1505A4604951674000000012023.md` (OCR incompleto)

### B. Vehículos de ALTA con Bastidor Faltante (`PENDIENTE_INCORPORAR`) (77 expedientes)
* Carpetas en `03_cache_markdown/ALTAS/`:
  `0602KHK`, `0692MWT`, `0693MWT`, `0695MWT`, `0696MWT`, `0699MWT`, `0700MWT`, `0701MWT`, `0773MXH`, `0971MXH`, `1954MXT`, `1970MXT`, `1976MXT`, `2043MJP`, `2062MJP`, `2076MJP`, `2087MJP`, `2120MFK`, `2704MXG`, `2705MXG`, `2717MXG`, `2722MXG`, `2737MXG`, `2788MXG`, `3103MXJ`, `3147MXJ`, `3154MXJ FACTURA NUEVO`, `3157MXJ`, `3178MXJ FACTURA NUEVO`, `3186MXJ FACTURA NUEVO`, `3191MXJ`, `3214MXJ FACTURA NUEVO`, `4073MXK`, `5230MXL`, `5360MXF`, `5566KSD`, `6271MXF`, `6334MXF`, `6370MXF`, `6952MXF`, `7151MXV`, `7775MXF`, `7830MXF`, `8249MXG`, `8328MCZ`, `8349MXG`, `8387MXG`, `8392MXG`, `8496MXG`, `8533MDK`, `8539MDK`, `8597MWT`, `8601MWT`, `8603MWT`, `8606MWT`, `8616MWT`, `8617MWT`, `8618MWT`, `8619MWT`, `8623MCZ`, `8624MWT`, `8625MWT`, `8626MWT`, `8627MWT`, `8634MWT`, `8636MWT`, `8637MWT`, `8647MWT`, `8651MWT`, `8654MCZ`, `8658MWT`, `8675MCZ`, `8697MCZ`, `8711MXK FACTURA NUEVO`, `8867KDN`, `8868KDN`, `8877KDN`.

### C. Vehículos de BAJA con Bastidor Faltante (`PENDIENTE_INCORPORAR`) (71 expedientes)
* Carpetas en `03_cache_markdown/BAJAS/`:
  `0246LLK`, `0251LLK`, `0269LLK`, `0290JLY`, `0351JWC`, `0426KHR`, `0818LKK`, `0842KVR`, `0894LKM`, `1751LHM`, `2179KNN`, `2258JPC`, `2316KZH`, `2825KMP`, `3575LMF`, `3598LKS`, `3904LLT`, `3931LLT`, `3942LLT`, `4223LJV`, `4296LBD`, `4456KVD`, `4533JFF`, `4535KFH`, `4719KYS`, `4793KWD`, `4926LMS`, `5255LKX`, `5829LLX`, `5918LLV`, `5932LLV`, `5937LLV`, `5949LLV`, `5969LLV`, `6586KPD`, `6736LLV`, `6756LLV`, `6987LLV`, `7001LLV`, `7015LLV`, `7017KWW`, `7052LLV`, `7190JDY`, `7960KHZ`, `7962LKX`, `7970LKX`, `8030LKY`, `8288KJX`, `8298KZS`, `8767LLW`, `8891LBN`, `8983LFG`, `9019LBN`, `9052KZG`, `9094KRJ`, `9106LCH`, `9165FXM`, `9244JFB`, `9276LMB`, `9305LMG`, `9413LKC`, `9417LKC`, `9418LKC`, `9431LKC`, `9455LKC`, `9494LKC`, `9504LDD`, `9763LDB`, `9778KJG`, `9850JTR`, `C0296BMW`.

### D. Fichas eITV Escaneadas con Tablas Rotas y Rotación de Texto (24 expedientes adicionales)
* Documentos como `BAJAS/0019LLR/MA0019LLR (1).md`, `BAJAS/9853KXP/9853KXP FICHA Y PERMISO.md`, etc., donde la tarjeta de inspección técnica fue escaneada y la conversión básica desorganizó las especificaciones del vehículo.

## 4. Plan de Acción Recomendado
1. **Ejecución de LlamaIndex / LlamaCloud API:** Enviar los 182 PDFs seleccionados a la API vision de LlamaCloud para extraer tablas estructuradas (VIN, NIF exacto, Matrícula, Fechas).
2. **Actualización de la Caché Local:** Reemplazar el Markdown en `03_cache_markdown/` con la salida parseada de LlamaIndex.
3. **Re-ejecución del Script de Notas:** Correr `scripts/global_omnium/generate_vehicle_notes.py` para regenerar el 100% de las notas con veracidad garantizada y 0 fallbacks.
