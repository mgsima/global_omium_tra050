---
tipo: "informe"
fecha: "2026-10-29"
tags:
    - "global_omnium"
    - "emparejamiento"
---

# Sankey de altas y bajas · 2026-10-29

- Foto del 2026-10-29: las 473 fichas de `03_coches/` (244 altas y 229 bajas) cruzadas con `emparejar_v4.py`. No se regenera sola.
- Cada coche cuenta 1. Una pareja son 2 unidades: 66 parejas son 66 altas + 66 bajas = 132.
- Qué significa cada desenlace:
    - En pareja: entra en una de las 51 parejas propuestas sin siniestro.
    - Pareja dudosa: entra en una de las 15 parejas cuya baja salió por siniestro. Solo según el Excel («CANCELADO POR SINIESTRO»); en general no se pueden presentar. El emparejador las usa solo cuando no hay una pareja sin siniestro para ese hueco.
    - Faltan bajas (en altas) / Faltan altas (en bajas): tiene compañeros admisibles, pero todos están ya emparejados con otro coche; en un emparejamiento máximo no queda ninguno libre. 103 altas y 3 bajas. En el 1c van juntos como «Compite y pierde».
    - Sin pareja posible: pasa las reglas del coche, pero no tiene ningún compañero que cumpla R1 Sociedad, R4b Misma subcategoría y R5 Ventana, ni ocupado ni libre. 33 altas y 96 bajas.
    - Falta un dato: solo tiene aristas SIN_DATOS. 1 baja (0894LKM, sin fecha de salida).
    - No elegible: alguna regla del coche en FALLA. 42 altas y 63 bajas.
- Sociedades por su código. Las de menos de 15 coches, juntas en «Otras». Códigos:
    - 1001: AVSA
    - 1004: G.O.MEDIOAMBIENTE S.L.
    - 1021: MEDICION AVANZADA CONTAD.
    - 1053: ISG
    - 1064: AYWA SER.AMBIENTALES SL
    - 1066: CANALIZ. CIVILES S.A.
    - 1069: JEMAR E HIJOS S.L.
    - 1200: EMIVASA
    - 1400: EGEVASA
    - 1505: CGAC
- Las etiquetas van sin tildes ni eñes: el sankey de Mermaid no las admite y el diagrama no compila.

## 1a · Altas: total → sociedad → estado

```mermaid
---
config:
    sankey:
        showValues: true
---
sankey-beta

"Total altas","1200",57
"Total altas","1505",55
"1505","No elegible",35
"1200","Faltan bajas",34
"Total altas","1001",28
"Total altas","Otras",26
"Total altas","1021",19
"Total altas","1066",19
"1200","Sin pareja posible",16
"1021","Faltan bajas",15
"Total altas","1004",15
"Total altas","1053",15
"1001","En pareja",14
"1066","Faltan bajas",13
"Otras","Sin pareja posible",12
"1505","Faltan bajas",11
"1001","Faltan bajas",10
"1053","Faltan bajas",10
"Total altas","1064",8
"1200","En pareja",7
"1004","En pareja",6
"1505","En pareja",6
"Otras","Faltan bajas",6
"1004","Sin pareja posible",5
"1066","En pareja",5
"1001","Pareja dudosa",4
"1004","No elegible",3
"1021","En pareja",3
"1053","Pareja dudosa",3
"1064","En pareja",3
"1064","Faltan bajas",3
"1505","Pareja dudosa",3
"Otras","En pareja",3
"Otras","No elegible",3
"1053","En pareja",2
"1064","Pareja dudosa",2
"1400","En pareja",2
"Otras","Pareja dudosa",2
"Total altas","1400",2
"1004","Faltan bajas",1
"1021","No elegible",1
"1066","Pareja dudosa",1
```

## 1b · Bajas: total → sociedad → estado

```mermaid
---
config:
    sankey:
        showValues: true
---
sankey-beta

"Total bajas","1505",48
"1505","No elegible",33
"Total bajas","1001",33
"Total bajas","Otras",32
"Otras","Sin pareja posible",23
"Total bajas","1066",19
"Total bajas","1069",19
"Total bajas","1400",17
"Total bajas","1004",16
"Total bajas","1021",15
"1001","En pareja",14
"1001","Sin pareja posible",12
"1069","Sin pareja posible",11
"1400","Sin pareja posible",11
"Total bajas","1053",11
"Total bajas","1200",11
"1066","Sin pareja posible",9
"1021","Sin pareja posible",8
"1069","No elegible",8
"Total bajas","1064",8
"1200","En pareja",7
"1004","En pareja",6
"1053","Sin pareja posible",6
"1505","En pareja",6
"1505","Sin pareja posible",6
"1004","No elegible",5
"1004","Sin pareja posible",5
"1066","En pareja",5
"1001","Pareja dudosa",4
"1021","No elegible",4
"1066","No elegible",4
"1021","En pareja",3
"1053","Pareja dudosa",3
"1064","En pareja",3
"1200","Sin pareja posible",3
"1505","Pareja dudosa",3
"Otras","En pareja",3
"Otras","No elegible",3
"1001","No elegible",2
"1053","En pareja",2
"1064","Pareja dudosa",2
"1064","Sin pareja posible",2
"1400","En pareja",2
"1400","Faltan altas",2
"1400","No elegible",2
"Otras","Pareja dudosa",2
"1001","Falta un dato",1
"1064","No elegible",1
"1066","Pareja dudosa",1
"1200","No elegible",1
"Otras","Faltan altas",1
```

## 1c · Bajas y altas juntas

- Bajas a la izquierda («1505 B»), altas a la derecha («1505 A»); se juntan en el estado, en el centro.
- «En pareja» y «Pareja dudosa» quedan equilibrados: 51 y 15 bajas entran, 51 y 15 altas salen.
- En el resto de estados la entrada y la salida no cuadran: el nodo toma el ancho del lado mayor.

```mermaid
---
config:
    sankey:
        showValues: true
---
sankey-beta

"1200 A","Total altas",57
"1505 A","Total altas",55
"Total bajas","1505 B",48
"No elegible","1505 A",35
"Compite y pierde","1200 A",34
"1505 B","No elegible",33
"Total bajas","1001 B",33
"Total bajas","Otras B",32
"1001 A","Total altas",28
"Otras A","Total altas",26
"Otras B","Sin pareja posible",23
"1021 A","Total altas",19
"1066 A","Total altas",19
"Total bajas","1066 B",19
"Total bajas","1069 B",19
"Total bajas","1400 B",17
"Sin pareja posible","1200 A",16
"Total bajas","1004 B",16
"1004 A","Total altas",15
"1053 A","Total altas",15
"Compite y pierde","1021 A",15
"Total bajas","1021 B",15
"1001 B","En pareja",14
"En pareja","1001 A",14
"Compite y pierde","1066 A",13
"1001 B","Sin pareja posible",12
"Sin pareja posible","Otras A",12
"1069 B","Sin pareja posible",11
"1400 B","Sin pareja posible",11
"Compite y pierde","1505 A",11
"Total bajas","1053 B",11
"Total bajas","1200 B",11
"Compite y pierde","1001 A",10
"Compite y pierde","1053 A",10
"1066 B","Sin pareja posible",9
"1021 B","Sin pareja posible",8
"1064 A","Total altas",8
"1069 B","No elegible",8
"Total bajas","1064 B",8
"1200 B","En pareja",7
"En pareja","1200 A",7
"1004 B","En pareja",6
"1053 B","Sin pareja posible",6
"1505 B","En pareja",6
"1505 B","Sin pareja posible",6
"Compite y pierde","Otras A",6
"En pareja","1004 A",6
"En pareja","1505 A",6
"1004 B","No elegible",5
"1004 B","Sin pareja posible",5
"1066 B","En pareja",5
"En pareja","1066 A",5
"Sin pareja posible","1004 A",5
"1001 B","Pareja dudosa",4
"1021 B","No elegible",4
"1066 B","No elegible",4
"Pareja dudosa","1001 A",4
"1021 B","En pareja",3
"1053 B","Pareja dudosa",3
"1064 B","En pareja",3
"1200 B","Sin pareja posible",3
"1505 B","Pareja dudosa",3
"Compite y pierde","1064 A",3
"En pareja","1021 A",3
"En pareja","1064 A",3
"En pareja","Otras A",3
"No elegible","1004 A",3
"No elegible","Otras A",3
"Otras B","En pareja",3
"Otras B","No elegible",3
"Pareja dudosa","1053 A",3
"Pareja dudosa","1505 A",3
"1001 B","No elegible",2
"1053 B","En pareja",2
"1064 B","Pareja dudosa",2
"1064 B","Sin pareja posible",2
"1400 A","Total altas",2
"1400 B","Compite y pierde",2
"1400 B","En pareja",2
"1400 B","No elegible",2
"En pareja","1053 A",2
"En pareja","1400 A",2
"Otras B","Pareja dudosa",2
"Pareja dudosa","1064 A",2
"Pareja dudosa","Otras A",2
"1001 B","Falta un dato",1
"1064 B","No elegible",1
"1066 B","Pareja dudosa",1
"1200 B","No elegible",1
"Compite y pierde","1004 A",1
"No elegible","1021 A",1
"Otras B","Compite y pierde",1
"Pareja dudosa","1066 A",1
```

## 1d · Bajas y altas juntas, sin sociedades

- Lo mismo que el 1c, sin el paso por sociedad: 229 bajas a la izquierda, 244 altas a la derecha.
- «Falta un dato» solo tiene una baja (0894LKM) y ninguna alta; va abajo y en el centro (alineación a la izquierda y orden de las filas).

```mermaid
---
config:
    sankey:
        showValues: true
        nodeAlignment: left
---
sankey-beta

"Total bajas","En pareja",51
"Total bajas","Pareja dudosa",15
"Total bajas","Compite y pierde",3
"Total bajas","Sin pareja posible",96
"Total bajas","No elegible",63
"Total bajas","Falta un dato",1
"En pareja","Total altas",51
"Pareja dudosa","Total altas",15
"Compite y pierde","Total altas",103
"Sin pareja posible","Total altas",33
"No elegible","Total altas",42
```

## 2 · Total → rol → desenlace

- Altas y bajas comparten los nodos «En pareja», «Pareja dudosa», «Sin pareja posible» y «No elegible»: el ancho suma los dos roles.

```mermaid
---
config:
    sankey:
        showValues: true
---
sankey-beta

"Total coches","Altas",244
"Total coches","Bajas",229
"Altas","Faltan bajas",103
"Bajas","Sin pareja posible",96
"Bajas","No elegible",63
"Altas","En pareja",51
"Bajas","En pareja",51
"Altas","No elegible",42
"Altas","Sin pareja posible",33
"Altas","Pareja dudosa",15
"Bajas","Pareja dudosa",15
"Bajas","Faltan altas",3
"Bajas","Falta un dato",1
```

## 3 · Las 66 parejas: sociedad → categoría → segura o dudosa

- Sociedad y categoría del alta (en pareja, la de la baja es la misma por R1 Sociedad y R4b Misma subcategoría).
- Segura: 51 parejas sin siniestro. Dudosa: 15 parejas cuya baja salió por siniestro según el Excel.

```mermaid
---
config:
    sankey:
        showValues: true
---
sankey-beta

"Cat. M1","Segura",36
"Parejas propuestas","1001",18
"Cat. N1","Segura",15
"1001","Cat. M1",14
"Cat. N1","Dudosa",13
"Parejas propuestas","1505",9
"1200","Cat. M1",7
"Parejas propuestas","1200",7
"1505","Cat. N1",6
"Parejas propuestas","1004",6
"Parejas propuestas","1066",6
"1004","Cat. M1",5
"1064","Cat. N1",5
"Parejas propuestas","1053",5
"Parejas propuestas","1064",5
"Parejas propuestas","Otras",5
"1001","Cat. N1",4
"1053","Cat. N1",3
"1066","Cat. M1",3
"1066","Cat. N1",3
"1505","Cat. M1",3
"Otras","Cat. N1",3
"Parejas propuestas","1021",3
"1021","Cat. M1",2
"1053","Cat. M1",2
"1400","Cat. N1",2
"Cat. M1","Dudosa",2
"Otras","Cat. M1",2
"Parejas propuestas","1400",2
"1004","Cat. N1",1
"1021","Cat. N1",1
```
