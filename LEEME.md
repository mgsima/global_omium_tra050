# Global Omnium TRA050 — mapa de la carpeta

Repositorio de la campaña TRA050 del grupo **Global Omnium** (`git@github.com:mgsima/global_omium_tra050.git`). Contiene toda la documentación de la campaña: lo que entrega el cliente, lo que genera el programa y los análisis. El repositorio de código (`tra050`) no guarda material de esta campaña de ningún tipo.

**La raíz es el flujo.** El número dice en qué orden te encuentras cada cosa, de lo que entra a lo que sale. Desde el 2026-10-22 el emparejamiento se rehace desde cero sobre esta estructura: primero se audita cada coche por separado y después se combinan en parejas.

## Qué hay en cada sitio

- `00_control/`: lo que gobierna la campaña. Se escribe a mano, salvo `emparejamiento/`.
    - `REGLAS_EMPAREJAMIENTO.md`: las reglas activas, R1 Sociedad a R9 Salida, y cómo se elige entre parejas válidas.
    - `ESQUEMA_COCHE.md` y `ESQUEMA_PAREJA.md`: qué lleva el YAML y el cuerpo de cada nota.
    - `00_global_omnium.base`: la base de Obsidian.
    - `emparejamiento/`: la salida del emparejador (resumen con el certificado de máximo, aristas admisibles y potenciales). Se regenera entera en cada pasada.
- `01_entrada/`: lo que entrega el cliente. **Nunca lo escribe un script.**
    - `_flota/`: los dos Excel. El de cálculo CAE es la fuente de datos de la campaña, pero **no es prueba documental**.
    - `ALTAS/<MATRICULA>/` y `BAJAS/<MATRICULA>/`: una carpeta por vehículo con sus documentos tal como llegaron. 156 altas y 161 bajas.
- `02_extraido/`: lo derivado de la entrada. **No se renombra nunca**: el 1:1 con el original es la trazabilidad, y regenerarlo cuesta tokens de APIs externas.
    - `ALTAS/` y `BAJAS/`: conversión a Markdown de cada documento.
    - `_datos/<MATRICULA>.json`: datos extraídos por LLM, uno por vehículo.
    - `_flota/`: el Excel volcado (CSV, JSON y `global_omium.db`).
- `03_coches/<MATRICULA>.md`: **una ficha por vehículo del universo**, 473. Es la fuente de verdad del coche.
    - Incluye los que solo están en el Excel, con `tiene_documentos: false`.
    - Cada dato que decide una regla lleva su fuente: `DOCUMENTO`, `MANUAL`, `EXTRACCION` o `EXCEL`.
    - La escribe `scripts/global_omnium/coches.py`, que conserva lo escrito a mano.
- `04_parejas/<SOCIEDAD>/<ALTA>_<BAJA>.md`: una nota por pareja, la unidad que se presenta a verificación. Vacía todavía.
    - La sociedad es la carpeta, así la R1 Sociedad no se puede saltar.
    - `PROPUESTA` la puede deshacer el emparejador; `FIJADA` ya no la toca.
    - La escribe `scripts/global_omnium/emparejar_v4.py`.
- `05_generado/`: datos de relleno de los documentos que redactamos nosotros (cesión, Anexo I, ficha TRA050).
- `06_verificacion/`: lo que sale al verificador, montado por pareja.
- `_0bsoleto/`: material retirado, con la fecha en el nombre y el motivo en su `LEEME.md`. Ahí está el emparejamiento de agosto (`03_expedientes/`), del que se trajo lo escrito a mano.
- `Consideraciones.md`: contexto del cliente y requisitos de la campaña.

## Cómo se trabaja

- **1 · Fichas de coche:** `python scripts/global_omnium/coches.py --todas`. Con `--matricula X --seco` enseña una ficha sin escribirla.
- **2 · Auditoría del coche:** a mano, en su ficha. Se editan los `doc_*`, `estado`, los datos que haya que corregir (con `<dato>_fuente: "MANUAL"`) y las secciones «Notas de auditoría», «Incidencias» e «Historial».
- **3 · Emparejamiento:** `python scripts/global_omnium/emparejar_v4.py --seco` cuenta cuántas parejas salen y lo demuestra; sin `--seco`, escribe `04_parejas/` y `00_control/emparejamiento/`.
- **4 · Fijar:** cuando una pareja tenga trabajo encima o se le pidan papeles al cliente, `estado_pareja: "FIJADA"`.

## Reglas de esta carpeta

1. **No se borra nada.** Lo superado se mueve a `_0bsoleto/` con la fecha por delante en el nombre y una entrada en su `LEEME.md`.
2. **Los documentos fuente son de solo lectura.** No se reescriben ni se renombran los de `01_entrada/`, ni sus conversiones en `02_extraido/`.
3. **La ficha del coche y la nota de la pareja son la fuente de verdad.** El script recalcula lo derivado; el juicio se escribe a mano y el script lo conserva.
4. **Ningún script escribe fuera de esta carpeta.**
5. **Nunca commit ni push sin que el usuario lo pida** en esa conversación: este remoto lo ve el equipo.
6. **Las reglas se citan con código y nombre**: «R5 Ventana», nunca «R5» a secas.

## Historial

- **2026-10-27** — **`_0bsoleto/03_expedientes/0bsoleto/` pasa a `_0bsoleto/03_expedientes/_0bsoleto/`**, el último `0bsoleto/` que quedaba en la campaña, para que todo el proyecto use el mismo nombre. Sin tocar el contenido.

- **2026-10-22** — **El emparejamiento se rehace desde cero.**
    - Estructura nueva: `00_control/`, `03_coches/` y `04_parejas/`. `04_extraido/` pasa a `02_extraido/`, `08_generado/` a `05_generado/` y `02_verificacion/` a `06_verificacion/`. `05_planes/`, `06_reportes/` y `07_experimentos/` se retiraron (siguen en el historial de git).
    - `03_expedientes/` va entero a `_0bsoleto/03_expedientes/`.
    - Reglas v4 en `00_control/REGLAS_EMPAREJAMIENTO.md`. Respecto a agosto: R6 Año desde 2024, R4 Categoría por homologación y no por el Excel, sin posesión contada desde la matriculación, y R7 Alta nueva, R8 Titularidad y R9 Salida explícitas.
    - Se escriben las 473 fichas de `03_coches/`. Se migran las 68 revisiones manuales de agosto y los datos corregidos a mano (fuente `MANUAL`).
    - El emparejador v4, en seco, propone 63 parejas con el máximo demostrado. Las parejas todavía no se han escrito.
- **2026-10-22** — **El ejercicio 2023 queda rechazado entero.** Las compras de 2023 ya no son susceptibles de CAE. Lo montado para el verificador está en `_0bsoleto/2026-10-22_lote_2023_no_apto/`.
- **2026-08-19** — **Reorganización de la campaña** por fases, con un expediente por pareja en `03_expedientes/` y fichas de vehículo con los datos del Excel prefijados `excel_`. Hoy en `_0bsoleto/`.
