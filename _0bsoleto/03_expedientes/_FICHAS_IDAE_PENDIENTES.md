---
doc_type: fichas_idae_aproximadas
cliente: global_omium_tra050
ejercicio: "2023"
total: 3
actualizado: 2026-08-19
aproximadas: ["1666MGR", "1667MGR", "8873KDN"]
---

# Fichas del IDAE asignadas por aproximacion

Estos tres expedientes **si tienen ficha asignada** en [[tra050/data/global_omium_tra050/_0bsoleto/03_expedientes/_FICHAS_IDAE|_FICHAS_IDAE.md]], pero la version no esta acreditada por un documento del vehiculo: se ha elegido razonando sobre la descripcion de la factura y el Excel. Por eso su `ahorro_fuente` es `FICHA_IDAE_APROXIMADA` y no `FICHA_IDAE`.

La diferencia importa: un `FICHA_IDAE` se defiende ante el certificador enseñando el permiso de circulacion al lado de la ficha. Estos tres no, todavia. **Lo que los convierte en acreditados es el permiso de circulacion o la ficha tecnica del electrico**, que es documentacion que ya se le pide al cliente por otros motivos.

En los tres se ha aplicado la regla 3 de [`docs/fichas_idae.md`](fichas_idae.md): ante duda irreducible, la version de **mayor consumo**, que es la que certifica **menos** ahorro. Equivocarse por ese lado no infla nada.

## `1666MGR` y `1667MGR` — OPEL VIVARO (CGAC, N1)

Bastidores `VXEV1ZKXZPZ019578` y `VXEV1ZKXZPZ019580`, facturas de Automoviles Palma del 27 y el 26 de abril de 2023.

**La descripcion de la factura fija la configuracion sin margen de duda:**

```
VIVARO-e FURGON-L-Electrico 100 kW + 75 kWh Bateri          44.149,59
```

Furgon, talla **L**, motor de **100 kW**, bateria de **75 kWh**. Eso descarta de golpe las tallas M y S y las versiones de 50 kWh, que eran la mitad del problema. Queda una sola incognita: **la generacion**, porque el IDAE tiene tres con esa misma configuracion y MTMA practicamente identica.

| Ficha IDAE | Generacion | Consumo | Autonomia | MTMA |
| :--- | :--- | ---: | ---: | ---: |
| `IDAE-564981` | Vivaro Furgon-e **(MY22.0)** L SELECT BEV 330 | **29,40** | 316 km | 3.045 |
| `IDAE-541725` / `IDAE-541730` | Vivaro-e (MY 21.0) Furgon Express/Select L BEV 330 | 25,85 | 329 km | 3.045 |
| `IDAE-598582` | Nuevo Vivaro Furgon-L (facelift) | 24,00 | 348 km | 3.053 |

**Asignada `IDAE-564981` (MY22.0, 29,40 kWh/100km)** por dos motivos que apuntan igual:

1. **La fecha.** Facturados en abril de 2023, y el bastidor lleva `P` en la posicion 10, que en Stellantis codifica el año de modelo 2023. El MY21 ya estaba superado y el facelift («Nuevo Vivaro», sin el `-e` en el nombre) todavia no se vendia. El MY22.0 es la generacion que estaba en catalogo en esa fecha.
2. **Es la conservadora.** 29,40 es el consumo mas alto de las tres, luego el ahorro que certifica es el menor.

> ⚠️ **Reserva anotada:** la fila del MY22.0 no cierra por dentro. 29,40 kWh/100km sobre 316 km exigen 92,9 kWh y la bateria es de 75 — un 24% de descuadre, cuando en las otras dos filas ese margen se queda en 11-14%, que es lo normal por perdidas de carga. Segun `docs/fichas_idae.md` eso es motivo para desconfiar de la fila entera. Se mantiene igualmente porque el error va del lado seguro, pero **si llega el permiso y el consumo homologado se parece mas a 24-26, hay que rehacer la asignacion**.

## `8873KDN` — RENAULT ZOE 40 (GAMASER, M1)

**No tiene carpeta documental**: ni factura, ni permiso, ni ficha tecnica. El unico rastro es el Excel de flota, y ahi si dice el modelo:

```
ALTA_20242025.csv:  ... RENAULT, ZOE 40, ... ELECTRICO ... Turismo
```

Es **el mismo modelo que el `5566KSD`**, que si tiene factura. Se le asigna la misma ficha, `IDAE-575365` (ZOE ZE 80 kW R110 Bateria 40 kWh, 16,90 kWh/100km), que ademas es **la unica ZOE de 40 kWh que existe en el catalogo del IDAE**: las dos entradas de esa bateria son R110 y declaran el mismo consumo.

Lo que queda sin cubrir es el motor. La fecha de matriculacion del Excel es **2017-10-10**, y en 2017 la ZOE 40 se vendia con el R90 (68 kW); el R110 llego despues. **El R90 no esta en el IDAE**, asi que no hay una ficha mejor que esta: comparten carroceria y bateria, y el consumo homologado apenas se mueve entre ambos.

Esta es la asignacion mas floja de las tres y conviene decirlo: descansa entera en una celda de Excel. Se cierra cuando llegue la carpeta del expediente, que ya esta pedida.
