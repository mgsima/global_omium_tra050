---
doc_type: indice_carpeta
carpeta: analisis_2023
cliente: Global Omnium
campana: TRA050
actualizado: 2026-08-10
---

# `analisis_2023/` — qué es cada fichero

Entregables y análisis del **ejercicio 2023** de la campaña TRA050 de Global
Omnium. Es el primer lote que se envía al cliente.

## Lo que se envía al cliente

| Fichero | Qué es |
| :--- | :--- |
| `peticion_cliente_2023.md` | **Carta en texto plano lista para enviar por correo.** Lo que falta para cerrar los siete expedientes, agrupado en documentación ausente, documentos en formato no válido y acreditación del periodo de posesión. |
| `altas_2023_sin_pareja.csv` | Los 28 vehículos nuevos de 2023 sin vehículo sustituido asignado. Para cada uno, los criterios que debería cumplir una baja candidata: sociedad, categoría, ventana de fechas y posesión mínima. Sirve para que el cliente los busque en su flota. Lo genera `scripts/global_omnium/altas_2023_sin_pareja.py`. |

## Análisis de trabajo

| Fichero | Qué es |
| :--- | :--- |
| `informe_2023.md` | Informe principal del ejercicio. Estado expediente a expediente de las 7 parejas, los criterios de búsqueda de las altas sin pareja, el techo estructural por sociedad y el resumen de requisitos que faltan. **Contiene las anotaciones de la revisión manual del 2026-08-10.** |
| `emparejamiento_tra050_v3.csv` | Las 69 parejas de toda la campaña (7 de 2023, 60 de 2024, 2 de 2025), con la verificación regla a regla R1–R6, el nivel de confianza y la acción pendiente. 27 columnas. |
| `descartes_tra050_v3.csv` | Los 352 vehículos descartados, con el motivo de cada descarte. |
| `informe_tra050_v3.md` | Informe de la ejecución del emparejador v3 del 2026-08-07: reglas aplicadas y resultado global. |
| `informe_situacion_2023.md` | Informe de situación del ejercicio 2023 previo, del 2026-08-07. |
| `expediente_2023.csv` | Vista reducida del expediente de 2023, con los requisitos por pareja. |
| `datos_ahorro_2023.csv` | Inventario documental por ID CAE y datos del vehículo antiguo para el cálculo de ahorro. |

## Advertencias antes de tocar nada

* **`informe_2023.md` y `emparejamiento_tra050_v3.csv` tienen correcciones hechas
  a mano.** Reejecutar `scripts/global_omnium/emparejar_tra050_v3.py` las
  perdería. Ese script conserva además rutas muertas (`DB_PATH` línea 40 y
  `OUT_DIR` línea 44, apuntando a `Resultados_Auditoria/`).

* **La revisión manual del 2026-08-10 retiró 6 peticiones al cliente** que el
  informe generaba y que no procedían: tres documentos que ya estaban en carpeta
  pero sin clasificar por el nombre del fichero, y tres pruebas de salida del
  patrimonio que no pueden existir porque los vehículos estaban alquilados y el
  solicitante nunca fue titular. El detalle está anotado en el propio
  `informe_2023.md` y en las notas de `5949LLV`, `6586KPD` y `6994KGK`.

* **Hallazgo nuevo de esa revisión (requisito R2):** en `5875KPY`, `4535KFH` y
  `6994KGK` el contrato que hay en carpeta no cubre el periodo mínimo de
  posesión. Los días que maneja el análisis salen del histórico del Excel, que
  no es prueba documental. Es el punto de riesgo real del lote.

* Nada se borra: lo que quede superado se mueve a `0bsoleto/` con la fecha por
  delante en el nombre y una entrada aquí explicando por qué dejó de valer.
