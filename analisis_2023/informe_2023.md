# Analisis del ejercicio 2023 — vehiculos nuevos de Global Omnium

Generado el 2026-08-07 a partir de `emparejar_tra050_v3.py`. Criterio: ficha TRA050 v1.1 y criterio 25-11.01.

## 1. Que hay

| Concepto | Vehiculos |
| :--- | ---: |
| Altas con fecha de adquisicion en 2023 | 35 |
| — fuera del ambito CAE o no validas | 5 |
| **Aptas para la ficha TRA050** | **30** |
| — con pareja asignada | 7 |
| — sin pareja | 23 |

### Altas de 2023 descartadas

| Matricula | Sociedad | Marca / modelo | Fecha | Motivo |
| :--- | :--- | :--- | :--- | :--- |
| 1428KDP | EMP.MUN.SERVEIS PUBLICS | RENAULT ZOE 40 | 2023-01-01 | Adquisicion 2023-01-01 anterior al 2023-01-25 (fuera del ambito CAE); fecha tomada del Excel, confirmar con factura/matriculacion |
| 8867KDN | CGAC | RENAULT ZOE 40 | 2023-01-05 | Adquisicion 2023-01-05 anterior al 2023-01-25 (fuera del ambito CAE) |
| 8868KDN | CGAC | RENAULT ZOE 40 | 2023-01-25 | Adquisicion 2023-01-25 anterior al 2023-01-25 (fuera del ambito CAE) |
| 8877KDN | CGAC | RENAULT ZOE 40 | 2023-01-05 | Adquisicion 2023-01-05 anterior al 2023-01-25 (fuera del ambito CAE) |
| P8325BDH | VALORIA INVESTMENTS 2011 | CORVUS UTV TERRAIN | 2023-07-31 | Matricula no valida ('P8325BDH'): no es un vehiculo |

> **Punto a decidir sobre las cuatro ZOE de enero de 2023.** El filtro aplicado excluye toda adquisicion anterior al 2023-01-25, fecha de entrada en vigor del RD 36/2023, por entender que la actuacion debe ejecutarse dentro del sistema CAE. El ambito de aplicacion de la ficha admite ademas vehiculos electricos "de primera matriculacion anterior al 25 de enero de 2023 que no hayan sido generadores de ahorros del sistema CAE", redaccion pensada para el electrico de segunda mano. Si el verificador acepta esa lectura para estos cuatro, habria que comprobar antes que ninguno ha generado ya CAE y volver a lanzar el emparejamiento con el filtro relajado. No se ha hecho aqui: es una decision de criterio, no de calculo.

### Reparto de las altas aptas

| Sociedad | Con pareja | Sin pareja |
| :--- | ---: | ---: |
| CGAC | 5 | 20 |
| G.O.MEDIOAMBIENTE S.L. | 1 | 1 |
| VALORIA INVESTMENTS 2011 | 0 | 1 |
| GAMASER | 1 | 0 |
| MEDICION AVANZADA CONTAD. | 0 | 1 |

| Categoria | Con pareja | Sin pareja |
| :--- | ---: | ---: |
| Furgoneta/Furgón | 5 | 21 |
| Turismo | 2 | 2 |

## 2. Altas con pareja: estado del expediente

### 0767MJM ← 5875KPY · `C_CONDICIONADO`

- **Nuevo:** PEUGEOT E-PARTNER PRO 100 KW (Furgoneta/Furgón), CGAC, adquirido 2023-07-19 (origen: DOCUMENTO)
- **Sustituido:** FIAT FIORINO 1.3 MULTIJET 80 CV (DIESEL, ALQUILER_CORTA_DURACION, NORTHGATE), baja 2023-06-30 (origen: DOCUMENTO), desfase -19d sobre la ventana 2023-04-19..2024-01-19
- **Posesion:** 1716d, DEFENDIBLE (minimo 365d)

**Documentos en el expediente** (1 del nuevo, 5 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 0767MJM | `1505A2827802674000000742023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo 5875KPY | `- 5875KPY FT.pdf` | FICHA_TECNICA | Ficha tecnica / tarjeta ITV del vehiculo | 5.4 |
| antiguo 5875KPY | `- 5875KPY PC.pdf` | PERMISO_CIRCULACION | Permiso de circulacion | 5.5 |
| antiguo 5875KPY | `5875KPY ACTA DEVOLUCION.pdf` | ACTA_DEVOLUCION | Acta de devolucion del vehiculo a la arrendadora, firmada en conformidad | 5.6-renting |
| antiguo 5875KPY | `5875KPY ACTA ENTREGA.pdf` | ACTA_ENTREGA | Acta de entrega firmada entre arrendador y usuario | 5.6-renting |
| antiguo 5875KPY | `5875KPY CONTRATO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas
- `R2` [POSESION] Contratos de alquiler **anteriores** de 5875KPY. El contrato en carpeta (`CE/0820-2023-00394`, entrega 17/02/2023) solo cubre desde febrero de 2023 hasta la devolucion del 30/06/2023: **149 dias documentados frente a los 365 exigidos**. Los 1.716 dias de posesion salen del historico del Excel, no de un documento. Sin los contratos previos, la R2 no esta acreditada.

> **REVISION MANUAL 2026-08-10 — no hay nada documental que pedir.** El informe pedia aqui una "prueba de salida del patrimonio de 5875KPY" en forma de compraventa, factura o cambio de titularidad DGT. **Esa peticion no procede.** El vehiculo estaba alquilado a NORTHGATE: Global Omnium nunca fue titular, asi que no existe compraventa ni cambio de titularidad que aportar. La salida del patrimonio la acredita el acta de devolucion a la arrendadora, `5875KPY ACTA DEVOLUCION.pdf`, **que ya esta en carpeta, en PDF y es legible**: devolucion el 30/06/2023 en Barcelona (El Prat). La tabla de arriba ya la contabilizaba como 5.6-renting; el listado se contradecia con ella. Del expediente solo faltan los dos tramites (5.1 y 5.2) y los contratos previos que sostienen la posesion.

### 1666MGR ← T5455BB · `A_ACREDITADO`

- **Nuevo:** OPEL VIVARO E-FURGON (Furgoneta/Furgón), CGAC, adquirido 2023-04-27 (origen: DOCUMENTO)
- **Sustituido:** FORD TRANSIT 1.8 TDCI 80 CV (DIESEL, PROPIEDAD, PROPIEDAD), baja 2023-03-09 (origen: DOCUMENTO), desfase -49d sobre la ventana 2023-01-27..2023-10-27
- **Posesion:** 8833d, ACREDITADA (minimo 365d)

**Documentos en el expediente** (1 del nuevo, 4 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 1666MGR | `1505A4670002774000000362023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo T5455BB | `T5455BB FACTURA VENTA.pdf` | TRANSMISION | Factura o contrato que acredita la venta del vehiculo sustituido | 5.6 |
| antiguo T5455BB | `T5455BB FICHA TECNICA 1.pdf` | FICHA_TECNICA | Ficha tecnica / tarjeta ITV del vehiculo | 5.4 |
| antiguo T5455BB | `T5455BB FICHA TECNICA.pdf` | FICHA_TECNICA | Ficha tecnica / tarjeta ITV del vehiculo | 5.4 |
| antiguo T5455BB | `T5455BB PERMISO CIRCULACION.pdf` | PERMISO_CIRCULACION | Permiso de circulacion | 5.5 |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas

### 1667MGR ← 5949LLV · `A_ACREDITADO`

- **Nuevo:** OPEL VIVARO E-FURGON (Furgoneta/Furgón), CGAC, adquirido 2023-04-26 (origen: DOCUMENTO)
- **Sustituido:** PEUGEOT PARTNER 1.5 HDI 98 CV (DIESEL, RENTING, AYVENS), baja 2023-04-08 (origen: DOCUMENTO), desfase -18d sobre la ventana 2023-01-26..2023-10-26
- **Posesion:** 761d, ACREDITADA (minimo 730d)

**Documentos en el expediente** (1 del nuevo, 3 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 1667MGR | `1505A4670002774000000342023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo 5949LLV | `5949LLV ACTA DEVOLUCION.pdf` | ACTA_DEVOLUCION | Acta de devolucion del vehiculo a la arrendadora, firmada en conformidad | 5.6-renting |
| antiguo 5949LLV | `5949LLV CONTRATO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |
| antiguo 5949LLV | `MA5949LLV.pdf` | FICHA_TECNICA | Ficha tecnica (tarjeta ITV) de 5949LLV: PEUGEOT Partner Premium Standard 600kg BlueHDi 100, categoria J=N1, homologacion e2\*2007/46\*0625\*10. Revision manual 2026-08-10 | 5.4 |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas

> **REVISION MANUAL 2026-08-10.** Se pedia la ficha tecnica de 5949LLV: **ya la tenemos**. El fichero `MA5949LLV.pdf`, que el clasificador dejaba como SIN_CLASIFICAR por el nombre, lleva **dos documentos dentro del mismo PDF**: la tarjeta ITV / ficha tecnica (5.4, con el historico de inspecciones) y el permiso de circulacion de la DGT. Ambos en PDF y legibles. Confirma ademas la categoria N1 usada en R4. No hay que pedir ninguno de los dos.

### 2076MJP ← 6586KPD · `B_INDICIO`

- **Nuevo:** RENAULT KANGOO VAN E-TECH (Furgoneta/Furgón), CGAC, adquirido 2023-07-25 (origen: DOCUMENTO)
- **Sustituido:** OPEL COMBO 1.3 CDTI 95 CV (DIESEL, RENTING, AYVENS), baja 2023-10-26 (origen: DOCUMENTO), desfase +93d sobre la ventana 2023-04-25..2024-01-25
- **Posesion:** 1870d, ACREDITADA (minimo 730d)

**Documentos en el expediente** (1 del nuevo, 4 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 2076MJP | `1505A4604951674000000882023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo 6586KPD | `6586KPD ACTA DEVOLUCION.jpeg` | ACTA_DEVOLUCION | Acta de devolucion firmada en conformidad. **FORMATO NO VALIDO: es una imagen JPEG, no un PDF** | 5.6-renting |
| antiguo 6586KPD | `6586KPD ACTA ENTREGA.pdf` | ACTA_ENTREGA | Acta de entrega firmada entre arrendador y usuario | 5.6-renting |
| antiguo 6586KPD | `6586KPD CONTRATO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |
| antiguo 6586KPD | `MA6586KPD (1).pdf` | FICHA_TECNICA | Ficha tecnica (tarjeta ITV) de 6586KPD: OPEL Combo Van, categoria J=N1, homologacion e3\*2007/46\*0076\*14. Revision manual 2026-08-10 | 5.4 |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas
- `5.6` [FORMATO] Acta de devolucion de 6586KPD **en PDF**. El acta esta y es legible (26/10/2023 15:54, 177.987 km, conductor JACINTO PLAZA, recepciona COBE PLAN MOLINS), pero se aporto como imagen JPEG y la normativa exige documento oficial en PDF. **No hay que volver a pedir el acta, solo el mismo documento en PDF.** Revision manual 2026-08-10

> **REVISION MANUAL 2026-08-10.** Se pedia tambien la ficha tecnica de 6586KPD: **ya la tenemos**. El fichero `MA6586KPD (1).pdf`, que el clasificador dejaba como SIN_CLASIFICAR por el nombre, es la tarjeta ITV del vehiculo, en PDF y legible. Confirma ademas la categoria N1 usada en R4. No hay que pedirla. De este expediente lo unico documental que falta es el acta de devolucion **en PDF**.

### 2120MFK ← 4535KFH · `C_CONDICIONADO`

- **Nuevo:** RENAULT KANGOO VAN E-TECH (Furgoneta/Furgón), CGAC, adquirido 2023-07-25 (origen: DOCUMENTO)
- **Sustituido:** PEUGEOT PARTNER 1.6 HDI 75 CV (DIESEL, ALQUILER_CORTA_DURACION, NORTHGATE), baja 2023-09-19 (origen: DOCUMENTO), desfase +56d sobre la ventana 2023-04-25..2024-01-25
- **Posesion:** 2135d, DEFENDIBLE (minimo 365d)

**Documentos en el expediente** (1 del nuevo, 6 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 2120MFK | `1505A4604951674000000842023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo 4535KFH | `- 4535KFH FT.pdf` | FICHA_TECNICA | Ficha tecnica / tarjeta ITV del vehiculo | 5.4 |
| antiguo 4535KFH | `- 4535KFH PC.pdf` | PERMISO_CIRCULACION | Permiso de circulacion | 5.5 |
| antiguo 4535KFH | `4535KFH ACTA DEVOLUCION.pdf` | ACTA_DEVOLUCION | Acta de devolucion del vehiculo a la arrendadora, firmada en conformidad | 5.6-renting |
| antiguo 4535KFH | `4535KFH ACTA ENTREGA.pdf` | ACTA_ENTREGA | Acta de entrega firmada entre arrendador y usuario | 5.6-renting |
| antiguo 4535KFH | `4535KFH CONTRATO ANEXO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |
| antiguo 4535KFH | `4535KFH CONTRATO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas
- `R2` [POSESION] Contratos de alquiler **anteriores** de 4535KFH. El contrato en carpeta (`CE/0820-2023-00393`) solo cubre desde febrero de 2023 hasta la devolucion del 19/09/2023: **230 dias documentados frente a los 365 exigidos**. Los 2.135 dias de posesion salen del historico del Excel, no de un documento. Sin los contratos previos, la R2 no esta acreditada.

> **REVISION MANUAL 2026-08-10 — no hay nada documental que pedir.** Mismo caso que 0767MJM: se pedia una "prueba de salida del patrimonio de 4535KFH" en forma de compraventa o cambio de titularidad, y **no procede**, porque el vehiculo estaba alquilado a NORTHGATE y Global Omnium nunca fue titular. El acta de devolucion `4535KFH ACTA DEVOLUCION.pdf` **ya esta en carpeta, en PDF y es legible**: devolucion el 19/09/2023 en Barcelona (El Prat), 11.800 km, bastidor VF37ABHW6HJ860569, firmada el 26/09/2023. Del expediente solo faltan los dos tramites (5.1 y 5.2) y los contratos previos que sostienen la posesion.

### 5566KSD ← 6994KGK · `C_CONDICIONADO`

- **Nuevo:** RENAULT ZOE 40 (Turismo), G.O.MEDIOAMBIENTE S.L., adquirido 2023-12-22 (origen: DOCUMENTO)
- **Sustituido:** PEUGEOT 208 1.2 82 CV (GASOLINA, ALQUILER_CORTA_DURACION, AYVENS), baja 2023-12-01 (origen: DOCUMENTO), desfase -21d sobre la ventana 2023-09-22..2024-06-22
- **Posesion:** 815d, ACREDITADA (minimo 365d)

**Documentos en el expediente** (1 del nuevo, 2 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| nuevo 5566KSD | `1004A4604951674000001122023.PDF` | FACTURA_ADQUISICION | Factura de adquisicion del vehiculo nuevo | 5.3 |
| antiguo 6994KGK | `6994KGK ACTA DEVOLUCION.pdf` | ACTA_DEVOLUCION | Acta de devolucion del vehiculo a la arrendadora, firmada en conformidad | 5.6-renting |
| antiguo 6994KGK | `6994KGKCondicionesparticulares_20251021092603.699_X.doc` | CONTRATO_RENTING | Condiciones particulares del contrato de alquiler nº 406863, LEASEPLAN SERVICIOS S.A. (A-78007473) como arrendador y GLOBAL OMNIUM MEDIOAMBIENTE SL (B46017018) como arrendatario, inicio 13/09/2021. **FORMATO NO VALIDO: es un .doc, no un PDF.** Revision manual 2026-08-10 | 5.5-renting |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas
- `5.4` [AUSENTE] Ficha tecnica de 6994KGK (vehiculo sustituido)
- `5.5` [FORMATO] Condiciones particulares del contrato de alquiler de 6994KGK **en PDF**. El documento esta y acredita la posesion (arrendatario GLOBAL OMNIUM MEDIOAMBIENTE SL, la misma sociedad del alta), pero se aporto en Word. **No hay que volver a pedir el contrato, solo el mismo documento en PDF.** Revision manual 2026-08-10
- `R2` [POSESION] Facturas mensuales o certificado del arrendador que acrediten el alquiler **ininterrumpido** de 6994KGK entre 13/09/2021 y 01/12/2023

> **REVISION MANUAL 2026-08-10 — la prueba de salida del patrimonio tampoco procede pedirla.** Se pedia compraventa o cambio de titularidad de 6994KGK: el vehiculo estaba alquilado a LEASEPLAN/AYVENS y Global Omnium nunca fue titular, asi que no existe tal documento. Lo acredita el acta de devolucion `6994KGK ACTA DEVOLUCION.pdf`, **ya en carpeta, en PDF y legible**: salida el 01/12/2023 con 96.951 km.

> **REVISION MANUAL 2026-08-10 — este es el punto debil del expediente.** El contrato aportado dice literalmente *"Duracion Contrato: Un mes prorrogable"*, con inicio 13/09/2021 y cuota de 315 €/mes. Los 815 dias de posesion salen de restar fechas (inicio y devolucion), no de la duracion pactada. Un alquiler mensual renovado puede tener interrupciones, asi que el contrato **por si solo no prueba la posesion continuada** que exige la R2. Hay que pedir las facturas del periodo o un certificado de LEASEPLAN/AYVENS. Lo que estaba anotado como duda —la etiqueta 'ALQUILER_CORTA_DURACION'— es lo de menos: lo que decide es el periodo, y es el periodo lo que hay que documentar.

### 8873KDN ← 1751LHM · `B_INDICIO`

- **Nuevo:** RENAULT ZOE 40 (Turismo), GAMASER, adquirido 2023-11-01 (origen: EXCEL)
- **Sustituido:** VOLKSWAGEN T-ROC 1.6 TDI 115 CV (DIESEL, RENTING, VWRENTING), baja 2023-08-31 (origen: EXCEL), desfase -62d sobre la ventana 2023-08-01..2024-05-01
- **Posesion:** 1155d, ACREDITADA (minimo 730d)

**Documentos en el expediente** (0 del nuevo, 2 del sustituido)

| Vehiculo | Fichero | Tipo | Descripcion | Cubre |
| :--- | :--- | :--- | :--- | :--- |
| antiguo 1751LHM | `1751LHM CONTRATO ANEXO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |
| antiguo 1751LHM | `1751LHM CONTRATO.pdf` | CONTRATO_RENTING | Contrato de renting con el solicitante como arrendatario | 5.5-renting |

**Falta para cerrar el expediente**

- `5.1` [TRAMITE] Ficha TRA050 firmada por el representante legal
- `5.2` [TRAMITE] Anexo I: declaracion responsable de ayudas publicas
- `5.3` [SIN_CARPETA] Factura de adquisicion de 8873KDN (vehiculo nuevo)
- `5.4` [AUSENTE] Ficha tecnica de 1751LHM (vehiculo sustituido)
- `5.6` [AUSENTE] Acta de entrega/devolucion de 1751LHM firmada en conformidad

## 3. Altas sin pareja: que vehiculo antiguo haria falta

Para cada una, el perfil exacto que tendria que cumplir un vehiculo sustituido para que la pareja fuera admisible. Las cuatro condiciones son simultaneas y ninguna admite excepcion.

### 0404MGW — OPEL VIVARO E-FURGON

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-05-17 (EXCEL)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-02-17 y 2023-11-17 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 0408MGW — OPEL VIVARO E-FURGON

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-05-17 (EXCEL)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-02-17 y 2023-11-17 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 0477MGW — OPEL VIVARO E-FURGON

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-05-09 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A4670002774000000432023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-02-09 y 2023-11-09 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 0777MJM — PEUGEOT E-PARTNER PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-19 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000722023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-19 y 2024-01-19 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 0778MJM — PEUGEOT E-PARTNER PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-19 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000732023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-19 y 2024-01-19 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 0800MJM — PEUGEOT E-PARTNER PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-19 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000712023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-19 y 2024-01-19 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 1255MJM — PEUGEOT E-EXPERT PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-21 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000772023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-21 y 2024-01-21 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 1256MJM — PEUGEOT E-EXPERT PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-21 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000792023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-21 y 2024-01-21 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 1258MJM — PEUGEOT E-EXPERT PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-21 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000782023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-21 y 2024-01-21 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 1261MJM — PEUGEOT E-EXPERT PRO 100 KW

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-21 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A2827802674000000762023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-21 y 2024-01-21 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 1406KDP — RENAULT ZOE 40

- **Sociedad:** MEDICION AVANZADA CONTAD. (`1021`) · **Categoria:** Turismo (`4`) · **Adquirido:** 2023-02-16 (EXCEL)
- **Bloqueo actual:** R5 — 2 bajas de su sociedad y categoria, ninguna en la ventana. Mas cercanas: 0818LKK (2025-01-10, +694d), 8030LKY (2025-01-16, +700d)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente MEDICION AVANZADA CONTAD. (`1021`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Turismo (`4`) exacta |
| R5 fecha de venta o entrega | entre 2022-11-16 y 2023-08-16 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 2043MJP — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-25 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A4604951674000000852023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-25 y 2024-01-25 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 2062MJP — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-07-25 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A4604951674000000872023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-04-25 y 2024-01-25 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 2087MJP — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-03-03 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 3 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 5949LLV → 1667MGR)
- **Documentos del vehiculo nuevo:** `1505A4604951674000000162023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2022-12-03 y 2023-09-03 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 2340MGR — OPEL VIVARO E-FURGON

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-04-26 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A4670002774000000332023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-01-26 y 2023-10-26 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 2343MGR — OPEL VIVARO E-FURGON

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-04-27 (DOCUMENTO)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** `1505A4670002774000000352023.PDF` (FACTURA_ADQUISICION)

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-01-27 y 2023-10-27 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 3140MHW — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-06-28 (EXCEL)
- **Bloqueo actual:** Competencia — habia 4 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK, 5949LLV → 1667MGR)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-03-28 y 2023-12-28 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 3192MHW — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-06-28 (EXCEL)
- **Bloqueo actual:** Competencia — habia 4 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK, 5949LLV → 1667MGR)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-03-28 y 2023-12-28 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 3201MHW — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-06-28 (EXCEL)
- **Bloqueo actual:** Competencia — habia 4 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK, 5949LLV → 1667MGR)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-03-28 y 2023-12-28 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 3219MHW — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-06-28 (EXCEL)
- **Bloqueo actual:** Competencia — habia 4 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK, 5949LLV → 1667MGR)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-03-28 y 2023-12-28 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 4564MHF — RENAULT KANGOO VAN E-TECH

- **Sociedad:** CGAC (`1505`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-05-31 (EXCEL)
- **Bloqueo actual:** Competencia — habia 5 baja(s) admisible(s) pero otras altas de la misma sociedad las aprovechan mejor (T5455BB → 1666MGR, 5875KPY → 0767MJM, 6586KPD → 2076MJP, 4535KFH → 2120MFK)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente CGAC (`1505`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-02-28 y 2023-11-30 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 5357MDX — E-TUK FACTORY LIMO GT

- **Sociedad:** VALORIA INVESTMENTS 2011 (`8010`) · **Categoria:** Turismo (`4`) · **Adquirido:** 2023-02-15 (EXCEL)
- **Bloqueo actual:** R1 — la sociedad VALORIA INVESTMENTS 2011 no aporta ninguna baja elegible
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente VALORIA INVESTMENTS 2011 (`8010`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Turismo (`4`) exacta |
| R5 fecha de venta o entrega | entre 2022-11-15 y 2023-08-15 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

### 9605MMH — RENAULT KANGOO VAN E-TECH

- **Sociedad:** G.O.MEDIOAMBIENTE S.L. (`1004`) · **Categoria:** Furgoneta/Furgón (`5`) · **Adquirido:** 2023-12-22 (EXCEL)
- **Bloqueo actual:** R5 — 1 bajas de su sociedad y categoria, ninguna en la ventana. Mas cercanas: 8767LLW (2025-02-11, +417d)
- **Documentos del vehiculo nuevo:** _ninguno_

**Perfil del vehiculo antiguo que se necesita**

| Condicion | Exigencia |
| :--- | :--- |
| R1 sociedad | exactamente G.O.MEDIOAMBIENTE S.L. (`1004`), no otra del grupo ni la arrendadora |
| R3 combustible | de combustion: diesel, gasolina, GLP, gas natural **o hibrido**. Solo queda fuera el electrico puro |
| R4 categoria | Furgoneta/Furgón (`5`) exacta |
| R5 fecha de venta o entrega | entre 2023-09-22 y 2024-06-22 |
| R2 posesion | >= 730d si renting, >= 365d si propiedad, contada hasta la fecha de baja |
| Regimen | RENTING o PROPIEDAD; el alquiler de corta duracion no acredita posesion |

## 4. Por que no se pueden usar todas: techo estructural

El limite no es el metodo de emparejamiento, es el inventario de bajas. Para cada combinacion sociedad + categoria en la que hay altas de 2023, esta es la lista completa de bajas elegibles del grupo, con su fecha de salida y su destino actual.

### CGAC · Furgoneta/Furgón — 25 altas de 2023, 5 cerradas, 20 sin pareja

Altas de 2023-03-03 a 2023-07-25. Una baja solo sirve si salio entre **2022-12-03** y **2024-01-25**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

| Baja | Salida | Regimen | Dentro del rango util | Destino |
| :--- | :--- | :--- | :-: | :--- |
| T5455BB | 2023-03-09 | PROPIEDAD | si | usada por 1666MGR (2023-04-27) |
| 5949LLV | 2023-04-08 | RENTING | si | usada por 1667MGR (2023-04-26) |
| 5875KPY | 2023-06-30 | ALQUILER_CORTA_DURACION | si | usada por 0767MJM (2023-07-19) |
| 4535KFH | 2023-09-19 | ALQUILER_CORTA_DURACION | si | usada por 2120MFK (2023-07-25) |
| 6586KPD | 2023-10-26 | RENTING | si | usada por 2076MJP (2023-07-25) |
| 2258JPC | 2024-02-08 | RENTING | no | **LIBRE** |
| 3595KDF | 2024-02-20 | ALQUILER_CORTA_DURACION | no | **LIBRE** |
| 9094KRJ | 2024-03-03 | RENTING | no | **LIBRE** |
| 6756LLV | 2024-06-28 | RENTING | no | usada por 8994MSH (2024-06-10) |
| 3569LKS | 2024-11-07 | RENTING | no | usada por 5020MWL (2024-11-18) |
| 5932LLV | 2025-03-27 | RENTING | no | usada por 4073MXK (2024-12-20) |
| 4938LMS | 2025-04-08 | RENTING | no | usada por 8597MWT (2024-11-28) |

**Techo:** 5 baja(s) elegibles en el rango util frente a 25 altas. Deficit de **20** vehiculos antiguos.

**Descartadas dentro del rango util.** Son las unicas que se podrian recuperar sin ampliar el inventario, y solo si la documentacion desmiente al Excel:

| Baja | Salida | Regimen segun Excel | Proveedor | Posesion por contrato | Desde matriculacion | Motivo del descarte | Que la recuperaria |
| :--- | :--- | :--- | :--- | ---: | ---: | :--- | :--- |
| 1947KMM | 2023-02-01 | ALQUILER_CORTA_DURACION | AYVENS | 0 d | ? d | Posesion 0d < 730d exigidos para un vehiculo tenido en arrendamiento | **la ficha tecnica o el permiso de circulacion**: no consta fecha de matriculacion, asi que ni siquiera se puede evaluar la antiguedad del vehiculo |
| 3447KFH | 2023-09-19 | ALQUILER_CORTA_DURACION | NORTHGATE | 230 d | ? d | Posesion 230d < 730d exigidos para un vehiculo tenido en arrendamiento | **la ficha tecnica o el permiso de circulacion**: no consta fecha de matriculacion, asi que ni siquiera se puede evaluar la antiguedad del vehiculo |

**Casi encajan.** Bajas libres que se quedan fuera de la ventana de la alta mas proxima por menos de 120 dias. Merece la pena revisar la fecha real de entrega en el acta o la de adquisicion en la factura antes de descartarlas:

| Baja | Salida | Alta mas proxima | Ventana de esa alta | Se pasa por |
| :--- | :--- | :--- | :--- | ---: |
| 2258JPC | 2024-02-08 | 2062MJP (2023-07-25) | 2023-04-25 .. 2024-01-25 | 14 d |
| 3595KDF | 2024-02-20 | 2062MJP (2023-07-25) | 2023-04-25 .. 2024-01-25 | 26 d |
| 9094KRJ | 2024-03-03 | 2062MJP (2023-07-25) | 2023-04-25 .. 2024-01-25 | 38 d |

### VALORIA INVESTMENTS 2011 · Turismo — 1 altas de 2023, 0 cerradas, 1 sin pareja

Altas de 2023-02-15 a 2023-02-15. Una baja solo sirve si salio entre **2022-11-15** y **2023-08-15**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

_No hay ninguna baja elegible de esta sociedad y categoria en todo el Excel._

**Techo:** 0 baja(s) elegibles en el rango util frente a 1 altas. Deficit de **1** vehiculos antiguos.

### G.O.MEDIOAMBIENTE S.L. · Turismo — 1 altas de 2023, 1 cerradas, 0 sin pareja

Altas de 2023-12-22 a 2023-12-22. Una baja solo sirve si salio entre **2023-09-22** y **2024-06-22**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

| Baja    | Salida     | Regimen                 | Dentro del rango util | Destino                        |
| :------ | :--------- | :---------------------- | :-------------------: | :----------------------------- |
| 9105KTC | 2023-03-13 | RENTING                 |          no           | **LIBRE**                      |
| 2179KNN | 2023-04-11 | RENTING                 |          no           | **LIBRE**                      |
| 2675KGJ | 2023-10-31 | ALQUILER_CORTA_DURACION |          si           | **LIBRE**                      |
| 2678KGJ | 2023-11-03 | ALQUILER_CORTA_DURACION |          si           | **LIBRE**                      |
| 6994KGK | 2023-12-01 | ALQUILER_CORTA_DURACION |          si           | usada por 5566KSD (2023-12-22) |
| 2653LTG | 2024-06-07 | ALQUILER_CORTA_DURACION |          si           | usada por 1108KHK (2024-06-14) |
| 9019LBN | 2024-10-02 | RENTING                 |          no           | usada por 6559MWV (2024-11-25) |
| 4988LLY | 2025-01-19 | RENTING                 |          no           | usada por 6444MWV (2024-11-29) |
| 3942LLT | 2025-03-14 | RENTING                 |          no           | usada por 6442MWV (2024-11-26) |
| 0246LLK | 2025-04-11 | RENTING                 |          no           | usada por 6439MWV (2024-11-26) |
| 9977LLM | 2025-04-24 | RENTING                 |          no           | usada por 6558MWV (2024-11-28) |

**Techo:** 4 baja(s) elegibles en el rango util frente a 1 altas. Deficit de **0** vehiculos antiguos.

**Descartadas dentro del rango util.** Son las unicas que se podrian recuperar sin ampliar el inventario, y solo si la documentacion desmiente al Excel:

| Baja | Salida | Regimen segun Excel | Proveedor | Posesion por contrato | Desde matriculacion | Motivo del descarte | Que la recuperaria |
| :--- | :--- | :--- | :--- | ---: | ---: | :--- | :--- |
| 6529LTJ | 2024-04-24 | ALQUILER_CORTA_DURACION | AYVENS | 57 d | ? d | Posesion 57d < 730d exigidos para un vehiculo tenido en arrendamiento | **la ficha tecnica o el permiso de circulacion**: no consta fecha de matriculacion, asi que ni siquiera se puede evaluar la antiguedad del vehiculo |

### G.O.MEDIOAMBIENTE S.L. · Furgoneta/Furgón — 1 altas de 2023, 0 cerradas, 1 sin pareja

Altas de 2023-12-22 a 2023-12-22. Una baja solo sirve si salio entre **2023-09-22** y **2024-06-22**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

| Baja | Salida | Regimen | Dentro del rango util | Destino |
| :--- | :--- | :--- | :-: | :--- |
| 8767LLW | 2025-02-11 | RENTING | no | usada por 3116MXJ (2024-12-23) |

**Techo:** 0 baja(s) elegibles en el rango util frente a 1 altas. Deficit de **1** vehiculos antiguos.

### GAMASER · Turismo — 1 altas de 2023, 1 cerradas, 0 sin pareja

Altas de 2023-11-01 a 2023-11-01. Una baja solo sirve si salio entre **2023-08-01** y **2024-05-01**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

| Baja | Salida | Regimen | Dentro del rango util | Destino |
| :--- | :--- | :--- | :-: | :--- |
| 1751LHM | 2023-08-31 | RENTING | si | usada por 8873KDN (2023-11-01) |

**Techo:** 1 baja(s) elegibles en el rango util frente a 1 altas. Deficit de **0** vehiculos antiguos.

### MEDICION AVANZADA CONTAD. · Turismo — 1 altas de 2023, 0 cerradas, 1 sin pareja

Altas de 2023-02-16 a 2023-02-16. Una baja solo sirve si salio entre **2022-11-16** y **2023-08-16**, y ademas dentro de la ventana de la alta concreta a la que se asigne.

| Baja | Salida | Regimen | Dentro del rango util | Destino |
| :--- | :--- | :--- | :-: | :--- |
| 0818LKK | 2025-01-10 | RENTING | no | usada por 6492MWV (2024-11-29) |
| 8030LKY | 2025-01-16 | RENTING | no | usada por 6493MWV (2024-11-26) |

**Techo:** 0 baja(s) elegibles en el rango util frente a 1 altas. Deficit de **1** vehiculos antiguos.

### Parejas de 2023 que dependen del criterio de posesion, no de la etiqueta

Desde el 2026-08-07 una baja no se descarta porque su contrato se llame 'alquiler', 'cedido' o 'pre-entrega': lo que decide es que el periodo de posesion supere los 730 dias (365 en propiedad). Estas parejas de 2023 existen gracias a ese criterio y **hay que comprobarlas contra el contrato antes de presentarlas**.

| Alta | Baja | Etiqueta en el Excel | Dias por contrato | Dias desde matriculacion | Estado | Riesgo |
| :--- | :--- | :--- | ---: | ---: | :--- | :--- |
| [[0767MJM]] | [[5875KPY]] | ALQUILER_CORTA_DURACION | 149 | 1716 | DEFENDIBLE | **alto** — el contrato no llega al umbral por si solo |
| [[2120MFK]] | [[4535KFH]] | ALQUILER_CORTA_DURACION | 230 | 2135 | DEFENDIBLE | **alto** — el contrato no llega al umbral por si solo |
| [[5566KSD]] | [[6994KGK]] | ALQUILER_CORTA_DURACION | 815 | ? | ACREDITADA | medio — el contrato ya cubre el umbral, falta confirmar continuidad |

Las 3 estan marcadas `regimen_a_verificar: true` en su ficha, con el detalle de que documento pedir.

## 5. Resumen: que falta en conjunto

| Requisito TRA050 v1.1 | Descripcion | Expedientes a los que le falta |
| :--- | :--- | ---: |
| 5.1 | Ficha TRA050 cumplimentada y firmada por el representante legal | 7 de 7 |
| 5.2 | Declaracion responsable de ayudas publicas (Anexo I) | 7 de 7 |
| 5.3 | Factura justificativa de la adquisicion del vehiculo nuevo | 1 de 7 |
| 5.4 | Ficha tecnica del vehiculo antiguo | 2 de 7 |
| 5.5 | Acreditacion de posesion del antiguo (permiso de circulacion o IVTM; en renting, contrato con el solicitante como arrendatario) | 0 de 7 ausentes · 1 solo pendiente de reenviar en PDF |
| 5.6 | Acreditacion de que el antiguo ya no esta en su patrimonio (achatarramiento o cambio de titularidad DGT; en renting, acta de devolucion) | 1 de 7 ausente · 1 mas solo pendiente de reenviar en PDF |
| R2 | Prueba documental de la posesion minima: el contrato en carpeta no llega al minimo exigido y el resto del periodo solo consta en el Excel | 3 de 7 |

> **REVISION MANUAL 2026-08-10.** Estas cifras bajaron tras comprobar a mano los documentos que el clasificador dejaba como SIN_CLASIFICAR. Tres de ellos eran documentos validos y utiles que estabamos a punto de volver a pedir: `MA5949LLV.pdf` y `MA6586KPD (1).pdf` son las fichas tecnicas de esas dos bajas (5.4), y `6994KGKCondicionesparticulares...doc` es el contrato de alquiler que acredita la posesion de 6994KGK (5.5). Los dos primeros son PDF y no requieren nada mas; el tercero solo hay que pedirlo de nuevo en PDF.
>
> El 5.6 bajo de 4 a 1 por un motivo distinto: en **0767MJM (5875KPY)**, **2120MFK (4535KFH)** y **5566KSD (6994KGK)** se pedia una prueba de salida del patrimonio en forma de compraventa o cambio de titularidad DGT. **Esa peticion no procede en ninguno de los tres**: los tres vehiculos estaban alquilados y Global Omnium nunca fue titular, asi que ese documento no existe ni puede existir. La salida del patrimonio la acredita el acta de devolucion a la arrendadora, y **las tres actas estan en carpeta, en PDF y son legibles**. La tabla de documentos de cada expediente ya las contaba como 5.6-renting: el listado de faltantes se contradecia con su propia tabla. El unico 5.6 realmente ausente es el de **8873KDN (1751LHM)**.
