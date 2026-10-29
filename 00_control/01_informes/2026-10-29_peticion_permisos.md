---
doc_type: informe
tema: "Petición de permisos de circulación y fichas técnicas"
fecha: 2026-10-29
---

# Petición de permisos de circulación y fichas técnicas

R4b Misma subcategoría solo queda acreditada con el permiso de circulación o la ficha técnica (campo J). La subcategoría que tienen hoy las fichas se conserva como hipótesis de trabajo; esta petición sirve para corroborarla.

## Alcance

- Coches que podrían formar pareja: 196 altas y 143 bajas. No fallan ninguna regla del coche por sí solo y están en una sociedad con altas y bajas candidatas.
- Hay que pedir el documento de 262 coches: 195 altas y 67 bajas. No se piden los coches cuya subcategoría ya sale de un documento, ni las motos.
- Lista para el cliente: `05_generado/peticiones/2026-10-29_permisos_y_fichas.xlsx`.

## Por prioridad

- Prioridad 1, en una pareja propuesta: 64 altas y 28 bajas.
- Prioridad 2, con alguna arista admisible o potencial: 104 altas y 8 bajas.
- Prioridad 3, candidato sin arista hoy (el que puede subir el número de parejas): 27 altas y 31 bajas.

## Por sociedad

- 1001 AVSA: 28 altas y 13 bajas.
- 1002 G.O.INVERSIONES S.L.: 2 altas y 0 bajas.
- 1004 G.O.MEDIOAMBIENTE S.L.: 11 altas y 6 bajas.
- 1006 ARAGONESA SER.PUBLICOS SL: 3 altas y 4 bajas.
- 1009 GAMASER: 4 altas y 2 bajas.
- 1021 MEDICION AVANZADA CONTAD.: 18 altas y 1 baja.
- 1053 ISG: 15 altas y 4 bajas.
- 1064 AYWA SER.AMBIENTALES SL: 8 altas y 5 bajas.
- 1066 CANALIZ. CIVILES S.A.: 19 altas y 5 bajas.
- 1200 EMIVASA: 57 altas y 1 baja.
- 1203 E.Mixta Metropolitana, SA: 2 altas y 1 baja.
- 1319 UTE CHIVA(AV/EG): 2 altas y 0 bajas.
- 1400 EGEVASA: 2 altas y 13 bajas.
- 1490 EMPRESA MIXTA CALPE: 1 alta y 0 bajas.
- 1505 CGAC: 19 altas y 12 bajas.
- 1507 EMP.AG.POTABL.MALGRAT SA: 4 altas y 0 bajas.

## Cuando lleguen

- Guardar cada documento en `01_entrada/ALTAS|BAJAS/<matrícula>/`, extraerlo y regenerar con `coches.py --todas`.
- Comparar la subcategoría antes y después: corroborada, corregida o sin documento.
- Repetir `emparejar_v4.py --seco` y anotar aquí el cambio de parejas.
