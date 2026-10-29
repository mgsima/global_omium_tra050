---
doc_type: informe
tema: "Revisión de las bajas descartadas por R2 Posesión"
fecha: 2026-10-29
---

# Revisión de las bajas descartadas por R2 Posesión

Pregunta del usuario: de las bajas descartadas por no llegar a dos años de posesión, ¿qué porcentaje se descartó por error?

## Resultado

- 54 bajas estaban descartadas por R2 Posesión. En las 54 era el único motivo de descarte.
- 2 estaban mal descartadas: 9244JFB y 0370LXS. Son el 3,7 % de las 54, o el 4,3 % de las 47 que se pueden comprobar.
- 45 están bien descartadas.
- 7 no se pueden comprobar con lo que hay. En el peor caso, si las 7 también fueran errores, serían 9 de 54 (16,7 %).
- Ya he corregido las dos fichas. Con ellas, `emparejar_v4.py --seco` pasa de 63 a 64 parejas (de 385.971 a 391.579 kWh/año) y el techo, de 64 a 65. La pareja nueva es de la sociedad 1066, con 0370LXS.

## Método

- Para cada baja he comparado dos fuentes independientes:
    - las fechas de inicio y salida de la ficha, sacadas de los documentos;
    - la hoja `BAJA2022202320242025` del Excel de flota, columnas «Tipo Contrato», «F.Vig.Inicio», «F.Devolución/Baja», «Nº cuotas Ini.Rent.» y «Cambio Vehículo por».
- Si las dos coinciden con pocos días de diferencia, el descarte se da por bueno.
- Cuando no coinciden, o la baja está cerca del umbral, he leído los documentos y, si hacía falta, el PDF original.
- Para cada baja que no coincidía he calculado los días con las fechas más favorables de las dos fuentes. Si ni así llega al umbral, el error de dato no cambia el resultado.

## Los 2 errores

- **9244JFB**: moto L3e de la sociedad 1021, en propiedad.
    - La ficha contaba 0 días: la extracción tomó como inicio la fecha de la factura de venta (2024-09-23), que es la salida.
    - El permiso la pone a nombre de MEDICION AVANZADA DE CONTADORES SA (campo C.1.1). Los campos I e I.1 coinciden en el 28-04-2015, así que la sociedad la matriculó nueva a su nombre, y según R2 Posesión esa fecha vale. El Excel da la misma.
    - Resultado: 3.436 días; cumple el mínimo de 365.
    - No gana pareja: la sociedad 1021 no tiene ningún alta L3e dentro de la ventana de R5 Ventana.
- **0370LXS**: furgoneta N1 de la sociedad 1066, con tres contratos de TLM encadenados.
    - La ficha contaba 660 días: la revisión de julio tomó como salida el 01/01/2025. En el PDF, esa fecha es el inicio del contrato 2025/074, no la devolución.
    - El campo «Fecha hasta real» está en blanco: es una plantilla sin rellenar, no un dato ilegible.
    - El Excel da como «F.Devolución/Baja» el 2025-03-31, el PDF se imprimió el 01/04/2025 y la fecha prevista del contrato es el 31/03/2025.
    - Resultado: del 2023-03-13 al 2025-03-31, 749 días; cumple el mínimo de 730.
    - Pendiente: el acta de devolución firmada o la factura de cierre de TLM, y el documento del contrato de 2024 (2024/252), del que solo hay datos del Excel.

## Las 7 que no se pueden comprobar

No tienen ningún documento: todo lo que sabemos sale del Excel, que solo muestra el último contrato de cada coche.

- 0962LBT: 413 días, alquiler con WASTERENT. Puede haber un contrato anterior.
- 1541LDT: 596 días, alquiler con WASTERENT. Puede haber un contrato anterior.
- 4921LGX: 637 días, «otros autorizados». Puede haber un contrato anterior.
- 6112LXB: 595 días, renting a 48 cuotas devuelto antes de tiempo. Puede haber un contrato anterior.
- 2138CTS: el Excel lo da como «CEDIDO» por un ayuntamiento y 0 días. Lo más probable es que no fuera de la sociedad.
- 1947KMM: alquiler, 0 días según el Excel.
- 0168KYM: alquiler, dado de baja por siniestro a los 166 días.

Para las cuatro primeras hay que pedir al cliente la cadena de contratos del coche. Las tres últimas casi seguro se quedan fuera.

## Las 45 bien descartadas

- Casi todas son alquileres cortos: el Excel las tiene como ALQUILER, con motivo «ALTANECESIDAD» y de 0 a 3 cuotas. Muchas son coches matriculados años antes, con decenas de miles de kilómetros. Un ejemplo es 0289LJZ: contrato «Un mes prorrogable», entregado con 99.611 km.
- En cuatro de ellas, los documentos y el Excel no coinciden, pero ninguna llega al umbral ni con las fechas más favorables:
    - 1947LMM: como mucho 525 días.
    - 4161FVT: como mucho 597 días, con dos contratos seguidos.
    - 3595KDF: como mucho 384 días.
    - 7431JTL: como mucho 553 días.
- Lista completa: 0041LWY, 0289LJZ, 0360KLY, 0824MCY, 1722MGL, 1865LDL, 1918LMY, 1947LMM, 2042MSX, 2056MSX, 2502LZC, 2653LTG, 2842LYK, 3264MDB, 3310MDB, 3447KFH, 3452LZP, 3483KWB, 3595KDF, 4161FVT, 4295MRH, 4535KFH, 4655MGJ, 4836MGD, 5056LWD, 5188MGJ, 5244MGJ, 5249MGJ, 5262MGK, 5351MGK, 5713LWX, 5875KPY, 6529LTJ, 6742MGH, 6901MPH, 6909MPH, 6937MPH, 7017MPH, 7431JTL, 7621KGX, 7706KJH, 8170LCK, 8497MPH, 8677MGK, 9853KXP.

## Otros hallazgos

- 44 fichas tienen el régimen RENTING (sacado de la extracción) donde el Excel pone ALQUILER. No cambia nada: el mínimo es 730 días en los dos casos.
- **Fallo de `coches.py`, corregido el 2026-10-29**: al regenerar una ficha, los datos marcados MANUAL en la propia ficha se conservaban, pero los campos que dependen de ellos se calculaban antes de aplicarlos: `dias_posesion`, `estado_posesion`, `elegible`, `motivos_no_elegible`, `estado`, el resumen y la trazabilidad.
    - Ahora `construir()` recibe la ficha actual y aplica sus datos MANUAL (función `aplicar_manuales`) antes de evaluar las reglas.
    - He regenerado en memoria las 473 fichas y las he comparado con las del disco: solo cambian 0370LXS y 9244JFB, que después he regenerado con el script.
    - `emparejar_v4.py` no se veía afectado, porque vuelve a evaluar las reglas a partir de las fechas.
