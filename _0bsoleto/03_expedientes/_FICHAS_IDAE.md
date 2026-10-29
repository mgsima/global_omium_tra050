---
doc_type: indice_fichas_por_expediente
cliente: global_omium_tra050
total: 5
actualizado: 2026-08-19
asignaciones: ["564981|1666MGR|CGAC", "564981|1667MGR|CGAC", "575365|5566KSD|G.O.MEDIOAMBIENTE S.L", "575365|8873KDN|GAMASER", "580989|2076MJP|CGAC"]
---

# Que ficha del IDAE usa cada expediente

El catalogo de fichas vive fuera de esta campana, en
[[referencia/idae/_INDICE.md|referencia/idae/]], porque es material publico
del IDAE por modelo de coche y lo comparten todas las campanas. Lo que si es
de aqui es la **asignacion**: que expediente declara que ficha, y con que
vehiculo. Por eso no esta en la ficha sino en esta nota.

La clave `asignaciones` del frontmatter es la que leen los scripts, en la
forma `<idae_id>|<matricula o bastidor>|<expediente>`. La tabla de abajo es
la misma informacion para leerla comodo.

El `CVN` sale de la ficha, como exige el Anexo II.A. Si el consumo que
declara el permiso del coche no cuadra con el de la ficha, la ficha no es la
suya.

El PDF de la ficha ya esta descargado en el catalogo comun, asi que el
slot 6 del expediente **no es `FALTA`**. Lo que si hay que hacer al montar el
expediente de verificacion es **copiar** ese PDF a
`data/global_omium_tra050/02_verificacion/<LOTE>/<EXPEDIENTE>/`: el paquete que se
entrega lo lleva dentro. Se copia, nunca se mueve, porque el catalogo lo
comparten las demas campanas.

| Expediente | Vehiculo | Ficha IDAE | PDF a copiar al expediente | CVN (kWh/100km) |
| :--- | :--- | :--- | :--- | ---: |
| CGAC | `1666MGR` | [[referencia/idae/IDAE-564981.md\|Opel Vivaro Furgón-e (MY22.0) L SELECT BEV 330 100kw/136CV]] | `referencia/idae/pdf/IDAE-564981.pdf` | 29.4 |
| CGAC | `1667MGR` | [[referencia/idae/IDAE-564981.md\|Opel Vivaro Furgón-e (MY22.0) L SELECT BEV 330 100kw/136CV]] | `referencia/idae/pdf/IDAE-564981.pdf` | 29.4 |
| CGAC | `2076MJP` | [[referencia/idae/IDAE-580989.md\|Renault KANGOO FURGON E-TECH 100% eléctrico KV1 L1 2 plazas start ev45 22kW (Semi: F1E1JA 10B)]] | `referencia/idae/pdf/IDAE-580989.pdf` | 17.45 |
| G.O.MEDIOAMBIENTE S.L | `5566KSD` | [[referencia/idae/IDAE-575365.md\|Renault ZOE E-TECH 100% eléctrico ZOE ZE - 80 kW R110 Batería 40kWh (semi: E1M MD 1NP,LIF B MD 1N,LIF B MD 1NP,4E1M MD 1NP,E1W MD 1NP)]] | `referencia/idae/pdf/IDAE-575365.pdf` | 16.9 |
| GAMASER | `8873KDN` | [[referencia/idae/IDAE-575365.md\|Renault ZOE E-TECH 100% eléctrico ZOE ZE - 80 kW R110 Batería 40kWh (semi: E1M MD 1NP,LIF B MD 1N,LIF B MD 1NP,4E1M MD 1NP,E1W MD 1NP)]] | `referencia/idae/pdf/IDAE-575365.pdf` | 16.9 |
