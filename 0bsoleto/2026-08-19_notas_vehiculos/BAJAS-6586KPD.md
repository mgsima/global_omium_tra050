---
matricula: "6586KPD"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "OPEL COMBO"
bastidor: "WQL6ZZU1AJ9641363"
combustible: "DIESEL"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "COMPANYIA GENERAL D AIGUES CATALUNY"
titular_cif: "A60401585"
numero_contrato: "70.262.446/15.492"
conductor_habitual: "JACINTO PLAZA"
conductor_dni: "07948198-L"
base_ubicacion: "NO_CONSTA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "INFERIDA"
fecha_inicio: "2018-09-12"
fecha_fin: "2023-10-26"
dias_arrendamiento: 1870
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "[[2076MJP]]"
emparejamiento_nivel: "B_INDICIO"
emparejamiento_pendiente: "aportar el acta de devolucion en PDF: el fichero en carpeta es una imagen JPEG y la normativa TRA050 exige documento oficial en PDF. El contenido es correcto y legible (devolucion 26/10/2023 15:54, 177987 km, conductor JACINTO PLAZA), asi que NO hay que volver a pedir el acta al cliente, solo el mismo documento en PDF"
formato_documental_no_valido: true
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: false
---

# FICHA VEHÍCULO: 6586KPD (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: [[2076MJP]]
- Marca / Modelo: OPEL COMBO | Origen: PDF: [[6586KPD CONTRATO.pdf]] | Markdown: [[6586KPD CONTRATO.md]]
- Bastidor: WQL6ZZU1AJ9641363 | Origen: PDF: [[6586KPD CONTRATO.pdf]] | Markdown: [[6586KPD CONTRATO.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: COMPANYIA GENERAL D AIGUES CATALUNY (CIF: A60401585) | Origen: PDF: [[6586KPD CONTRATO.pdf]] | Markdown: [[6586KPD CONTRATO.md]]
- Conductor: JACINTO PLAZA (DNI: 07948198-L) | Origen: JPEG: [[6586KPD ACTA DEVOLUCION.jpeg]] | Markdown: [[6586KPD ACTA DEVOLUCION.md]]
- Número Contrato: 70.262.446/15.492 | Origen: PDF: [[6586KPD CONTRATO.pdf]] | Markdown: [[6586KPD CONTRATO.md]]
- Base / Ubicación: NO_CONSTA
- Comunidad Autónoma: Cataluña | INFERIDA: no consta la ubicación en el expediente. Los 22 vehículos del mismo titular (CIF A60401585) con ubicación documentada están todos en Cataluña.
- Fecha Inicio: 2018-09-12 | Origen: [[ACTA_ENTREGA.pdf]]
- Fecha Fin: 2023-10-26 | Origen: JPEG: [[6586KPD ACTA DEVOLUCION.jpeg]] | Markdown: [[6586KPD ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 1870 días (Calculado entre 2018-09-12 y 2023-10-26)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- JPEG: [[6586KPD ACTA DEVOLUCION.jpeg]] | Markdown: [[6586KPD ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: JPEG, Estado: INVALIDO)
- PDF: [[6586KPD ACTA ENTREGA.pdf]] | Markdown: [[6586KPD ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[6586KPD CONTRATO.pdf]] | Markdown: [[6586KPD CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[MA6586KPD (1).pdf]] | Markdown: [[MA6586KPD (1).md]] (Tipo: FICHA_TECNICA, Formato: PDF, Estado: VALIDO) — revision manual 2026-08-10

> **REVISION MANUAL 2026-08-10 — DOCUMENTO YA APORTADO.** El informe de 2023 pedia
> al cliente la ficha tecnica de este vehiculo. **Ya la tenemos.** El fichero
> `MA6586KPD (1).pdf` es la **tarjeta ITV / ficha tecnica** (requisito 5.4):
> D.1 OPEL, D.2 "Combo-D-VAN / ZXU1A / SN2BN", D.3 "Combo Van", J = **N1**,
> K = e3\*2007/46\*0076\*14, bastidor W0L6ZZU1AJ9641363, I 04-09-2018,
> titular C.1.1 LEASE PLAN SERVICIOS SA. La categoria N1 confirma la R4 del
> emparejamiento con [[2076MJP]].
>
> El clasificador lo daba como `PERMISO_CIRCULACION` por el nombre opaco del
> fichero (`MA<matricula>.pdf`). Que el titular sea la arrendadora es lo normal en
> renting: la posesion de Global Omnium la acredita [[6586KPD CONTRATO.pdf]], que
> tambien esta en carpeta. **No pedir la ficha tecnica.** De este expediente lo
> unico que falta es el acta de devolucion en PDF.

> **PENDIENTE DE COMPROBAR — FORMATO.** Revision manual 2026-08-10. El acta de
> devolucion de este vehiculo es el unico fichero `.jpeg` de todo el expediente
> (703 PDF, 40 Word, 1 xlsx, 1 jpeg). El validador de formato de
> `convert_all_to_markdown.py:26` solo marca `.doc` y `.docx`, asi que la imagen
> paso como valida; y `generate_vehicle_notes.py:34` comprueba `mf.stem`, que
> nunca lleva extension, por lo que le anadio `.pdf` al nombre. De ahi que el
> inventario dijera `[[6586KPD ACTA DEVOLUCION.pdf]] (Formato: PDF, Estado:
> VALIDO)`: ese fichero no existe. Corregido a mano.
>
> El contenido del acta es correcto y legible: devolucion 26/10/2023 a las 15:54,
> 177.987 km, conductor JACINTO PLAZA (DNI 07948198-L), recepciona COBE PLAN
> MOLINS. **No hay que pedirle al cliente el acta: la tiene.** Hay que pedirle el
> mismo documento en PDF. Por eso el nivel baja de A_ACREDITADO a B_INDICIO: es
> un tramite de formato, no una duda sobre el fondo.
