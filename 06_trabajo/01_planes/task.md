# Seguimiento de Tareas - Global Omnium 📋

Este documento realiza el seguimiento del proceso de preparación de los expedientes de la campaña de flota corporativa del grupo **Global Omnium**.

---

## 🚀 Estado de la Campaña

* **Fase Actual:** Fase 1: Planificación (En curso) ⏳.
* **Progreso de Ingesta:** 0 / 349 actuaciones procesadas.
* **Ahorro Estimado Total:** ~1,776,157 kWh.

---

## 🗓️ Checklist de Fares y Tareas

### `[/]` Fase 1: Planificación y Requisitos
* `[x]` Proponer la organización de carpetas para el cliente Global Omnium.
* `[x]` Crear la estructura de directorios bajo `resultados_creacion/global_omnium/`.
* `[x]` Redactar la planificación global en `ROADMAP.md`.
* `[/]` Redactar la documentación de requisitos corporativos en `requisitos_campana.md`.
* `[ ]` Desarrollar script de inventariado para comprobar la existencia física de PDFs de Altas y Bajas basándose en el listado del Excel.

### `[ ]` Fase 2: Extracción e Ingesta de Datos (Caché Local)
* `[ ]` Ejecutar el parser híbrido sobre las facturas de Altas en `00001 ALTAS/`.
* `[ ]` Ejecutar el parser híbrido sobre las actas y contratos de Bajas en `00002 BAJAS/`.
* `[ ]` Guardar la caché de texto en `03_cache_markdown/` para coste cero.
* `[ ]` Validar la integridad del texto extraído y solucionar posibles fallos de OCR.

### `[ ]` Fase 3: Consolidación y Cruce de Datos
* `[ ]` Agrupar los registros de la campaña por Sociedad filial, Comunidad Autónoma y Año de compra.
* `[ ]` Mapear los datos de NIF y representantes legales para cada una de las sociedades filiales.
* `[ ]` Recalcular los ahorros teóricos y detectar posibles discrepancias matemáticas empleando `rules.py`.

### `[ ]` Fase 4: Generación de Documentación Oficial
* `[ ]` Autogenerar el Convenio de Cesión en PDF para cada grupo consolidado.
* `[ ]` Rellenar el formulario oficial del Anexo I para cada coche (inyectando referencias catastrales y ayudas).
* `[ ]` Rellenar la Ficha CAE técnica.
* `[ ]` Copiar y renombrar todos los justificantes originales (Facturas, Permisos, Fichas de ITV) bajo `04_preparados_verificar/[ID_CAE]/` siguiendo el formato oficial de verificación.

### `[ ]` Fase 5: Auditoría y Reporte Final
* `[ ]` Auditar el lote de expedientes en `04_preparados_verificar/` usando el motor de consistencia cruzada.
* `[ ]` Resolver alertas por discrepancias menores de nombres o bastidores.
* `[ ]` Consolidar el ahorro total y generar los reportes de API en `05_reportes/`.
