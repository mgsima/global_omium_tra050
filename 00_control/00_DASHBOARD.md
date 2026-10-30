---
doc_type: dashboard_control
campana: "global_omnium"
fecha: "2026-10-29"
fecha_limite_v1: "2026-11-20"
umbral_lote: 10
criterio_prioritario: "Viabilidad con baja carga documental (v1.1) > Ahorro marginal"
tags:
    - "dashboard"
    - "global_omnium"
    - "control"
---

# Cuadro de Mando Documental TRA050

## Reglas de Operacion y Decision

* **Regla de Formacion de Lotes:** Agrupaciones homogeneas de minimo 10 unidades de la misma Comunidad Autonoma y mismo ejercicio.
* **Fecha Limite Clave (20 de noviembre de 2026):**
  * Toda documentacion que llegue **antes del 20/11/2026**:
    * Se evalua de inmediato contra la **Vista 1 (Recoleccion v1)** con la documentacion base disponible.
    * Si la documentacion base esta completa, se emite en lote bajo Ficha v1.1 sin esperar a los documentos nuevos.
    * Excepcion de ahorro: solo se envia bajo v2.0 si el cliente aporta las ITVs con odometro y la **Vista 4 (Ahorro)** demuestra mayor ahorro real que el estandar de v1.1.
  * Toda documentacion que llegue **despues del 20/11/2026**:
    * Pasa obligatoriamente a Ficha Nueva (v2.0) y debe completar toda la **Vista 2 (Recoleccion v2)**.
* **Prioridad Operativa:** Viabilidad de salida rapida con poca documentacion prevalece sobre maximizar kWh.

## Estados Documentales Oficiales

* **ok:** Documento aportado y valido. No entra en peticiones.
* **falta:** Documento ausente. Se pide al cliente.
* **pendiente_lectura:** Archivo recibido en carpeta pero nadie lo ha abierto aun.
* **subsanar:** Archivo leido que no vale o tiene incidencias. Se pide correccion al cliente.
* **formato_invalido:** Documento correcto pero en formato no admitido (imagen, Word). Se pide en PDF.
* **faltan_datos:** Para documentos generados que no pueden redactarse por faltar datos base.
* **na:** No aplica a este expediente (ejemplo: leasing si fue compra directa, o 2 recibos IVTM si hay permiso).

## Estructura de las Cuatro Vistas

* **Vista 1 · Recoleccion v1 (Documentos Base):**
  * Rastreo de la documentacion minima del cliente para sacar el expediente por Ficha v1.1.
  * Factura VE, Permiso VE, Ficha tecnica VE, Propiedad VC (o renting), Ficha tecnica VC, Salida VC y Poderes/DNI.
* **Vista 2 · Recoleccion v2 (Todos los Documentos a Recoger):**
  * Rastreo de la recoleccion completa requerida por la Ficha TRA050.E v2.0.
  * Incluye los base mas: ITV 9/12 meses en vigor, clausula anti-holding, leasing VE > 2 años, 2 recibos IVTM y odometro en ITV.
* **Vista 3 · Documentos Generados (Comun):**
  * Rastreo de los documentos contractuales y tecnicos que redacta y aporta el equipo de auditoria.
  * Contrato de cesion interno, convenio CAE del lote, Anexo I de ayudas publicas, ficha IDAE y ficha oficial TRA050.
* **Vista 4 · Ahorro por Coche / Pareja:**
  * Metricas de calculo de cada pareja: categoria, CVA, CVN, km anuales y ahorro anual en kWh bajo v1.1 y bajo v2.0.
  * Columna de diferencia para decidir objetivamente si merece la pena tramitar bajo v2.0.

## Base de Datos de Control y Recoleccion

![[data/global_omium_tra050/00_control/00_DASHBOARD.base]]
