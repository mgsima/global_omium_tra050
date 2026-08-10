---
matricula: "8767LLW"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT INDUST. Partner Premium Standard 600kg Bluehdi73kw (1.499Cc 73Kw (98Cv) 05 Vel. 4p 2 Plazas Diesel)"
bastidor: "VR3EFYHYCLN564500"
combustible: "Diesel"
categoria: "N1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "GLOBAL OMNIUM MEDIOAMBIENTE SL"
titular_cif: "B46017018"
numero_contrato: "486.727/5"
conductor_habitual: "NO_CONSTA"
conductor_dni: "NO_CONSTA"
base_ubicacion: "CL GRAN VIA MARQUES DEL TURIA,00019, 46005 VALENCIA"
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2021-02-19"
fecha_fin: "NO_CONSTA"
dias_arrendamiento: "NO_CONSTA"
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: false
coche_emparejado: "[[3116MXJ]]"
emparejamiento_nivel: "B_INDICIO"
emparejamiento_pendiente: "confirmar fecha de baja con el documento de entrega; aportar acta de devolucion firmada"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: false
---

# FICHA VEHÍCULO: 8767LLW (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: [[3116MXJ]]
- Marca / Modelo: PEUGEOT INDUST. Partner Premium Standard 600kg Bluehdi73kw (1.499Cc 73Kw (98Cv) 05 Vel. 4p 2 Plazas Diesel) | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Bastidor: VR3EFYHYCLN564500 | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Diesel
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: GLOBAL OMNIUM MEDIOAMBIENTE SL (CIF: B46017018) | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Conductor: NO_CONSTA (DNI: NO_CONSTA)
- Número Contrato: 486.727/5 | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Base / Ubicación: CL GRAN VIA MARQUES DEL TURIA,00019, 46005 VALENCIA | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("CL GRAN VIA MARQUES DEL TURIA,00019, 46005 VALENCIA"), provincia de Valencia.
- Fecha Inicio: 2021-02-19 | Origen: PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]]
- Fecha Fin: NO_CONSTA | Acta de devolución presente pero SIN CUMPLIMENTAR: PDF: [[8767LLW ACTA ENTREGA.pdf]] | Markdown: [[8767LLW ACTA ENTREGA.md]]
- Días Arrendamiento / Tenencia: NO_CONSTA (Fechas de inicio o fin ausentes)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[8767LLW ACTA ENTREGA.pdf]] | Markdown: [[8767LLW ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[8767LLW CONDICIONES.pdf]] | Markdown: [[8767LLW CONDICIONES.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)
- Fecha Fin cambiada de NO_EXISTE_DOCUMENTO a NO_CONSTA: el archivo "ACTA ENTREGA" SÍ contiene un ACTA DE DEVOLUCIÓN de LeasePlan, pero es la plantilla en blanco (todos los campos figuran como `[___]/[___]/[___]`, sin fecha, hora ni persona que recepciona). El documento existe; el dato no.
- `tiene_acta_devolucion` se mantiene en false de forma deliberada: un acta sin cumplimentar no acredita la devolución ante el Verificador.
- ACCIÓN REQUERIDA: solicitar a LeasePlan el acta de devolución firmada y fechada. Sin ella no puede cerrarse el periodo de tenencia de este renting.

## APÉNDICE A LA REVISIÓN MANUAL (2026-08-10)
La conclusión de arriba se mantiene sin cambios: el acta no acredita la devolución y hay que pedirla. Se añaden tres datos que no constaban y que conviene llevar a la petición:
- **La matrícula del acta de devolución no es la de este vehículo.** En la línea 74 del markdown se lee `Matrícula 8667 LLW`, no 8767LLW. Puede ser un error de OCR (un 7 leído como 6) o puede que el acta sea de otro vehículo. Hay que aclararlo antes de reclamar, porque cambia lo que se pide.
- El acta **no está del todo en blanco**: tiene 63.312 km, conductor `FERNAN DOMIGIS`, y dos firmas de cuatro (Conforme Cliente/Conductor y Conforme Transporte, líneas 313 y 315), con la observación `1109-25` en la casilla de Transporte. Lo que falta es el bloque **Fecha de Devolución**, que sí está vacío.
- El acta de devolución va **dentro del PDF llamado `8767LLW ACTA ENTREGA.pdf`**, a partir de su línea 59: son dos documentos en un solo fichero. El nombre del fichero solo nombra el primero, y por eso el detector automático no la ve.
