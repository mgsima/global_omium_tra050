---
matricula: 2042MSX
rol: BAJA
tags:
  - vehiculo
  - baja
  - global_omnium
  - revision_manual
  - elegibilidad_dudosa
tipo_vehiculo: COMBUSTION_DIESEL
marca_modelo: PEUGEOT Partner 2024 Standard 600kg BlueHDi 100 S&S
bastidor: VR3EDYHT7RN547479
combustible: DIESEL
categoria: N1
regimen: ALQUILER_CORTA_DURACION
servicio_dgt: NO_ESPECIFICADO
titular_empresa: MALCODIGITAL GROUP SAL
titular_cif: NO_CONSTA
numero_contrato: 11206873-1
conductor_habitual: CONDUCTOR AUTORIZADO POR LA EMPRESA
conductor_dni: NO_CONSTA
base_ubicacion: VILA-REAL
comunidad_autonoma: "Comunidad Valenciana"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: 2024-09-06
fecha_fin: 2024-12-05
dias_arrendamiento: 90
fecha_matriculacion: 2024-07-10
tiene_acta_devolucion: false
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 90d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 2042MSX (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT Partner 2024 Standard 600kg BlueHDi 100 S&S | Origen: PDF: [[2042MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2042MSX - DOCUMENTACIÓN.md]]
- Bastidor: VR3EDYHT7RN547479 | Origen: PDF: [[2042MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2042MSX - DOCUMENTACIÓN.md]]
- Categoría: N1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: DIESEL
- Régimen: ALQUILER_CORTA_DURACION (3 meses) | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Servicio DGT: NO_ESPECIFICADO
- Titular: MALCODIGITAL GROUP SAL (CIF: NO_CONSTA) | Origen: PDF: [[2042MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2042MSX - DOCUMENTACIÓN.md]]
- Conductor: CONDUCTOR AUTORIZADO POR LA EMPRESA (DNI: NO_CONSTA) | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Número Contrato: 11206873-1 (autorización) | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Base / Ubicación: VILA-REAL | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Comunidad Autónoma: Comunidad Valenciana | Derivada de `base_ubicacion` ("VILA-REAL"), provincia de Castellón.
- Fecha Inicio: 2024-09-06 (inicio del alquiler) | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Fecha Fin: NO_CONSTA (devolución PREVISTA 2024-12-05, no acreditada como consumada) | Origen: PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]]
- Días Arrendamiento / Tenencia: 90 días (Calculado entre 2024-09-06 y 2024-12-05)
- Fecha Matriculación: 2024-07-10 | Origen: PDF: [[2042MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2042MSX - DOCUMENTACIÓN.md]]

## INVENTARIO DOCUMENTAL
- PDF: [[2042MSX - DOCUMENTACIÓN.pdf]] | Markdown: [[2042MSX - DOCUMENTACIÓN.md]] (Tipo: REVISION_MANUAL, Formato: PDF, Estado: VALIDO)
- PDF: [[2042MSX CONTRATO.pdf]] | Markdown: [[2042MSX CONTRATO.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)

## REVISIÓN MANUAL (2026-07-23)

> [!warning] ELEGIBILIDAD TRA050 EN DUDA — NO PROCESAR SIN VALIDACIÓN
> Este expediente presenta tres incompatibilidades con la ficha TRA050:
> 1. **No es un vehículo antiguo.** Es un PEUGEOT Partner **matriculado el 10/07/2024**, dos meses antes del contrato.
> 2. **No hay propiedad ni renting.** El contrato es un **alquiler de corta duración de MALCODIGITAL GROUP SAL** (06/09/2024 a 05/12/2024, 90 días). El régimen constaba como PROPIEDAD, lo que lo hacía pasar por un caso ordinario.
> 3. **No alcanza ningún umbral de posesión.** 90 días frente a los 365 exigidos en propiedad o los 730 en renting.
>
> Todo apunta a un **vehículo de sustitución temporal**, no a un vehículo de flota dado de baja. Debe confirmarse con Global Omnium si corresponde excluirlo de la campaña.

- Régimen corregido de PROPIEDAD a ALQUILER_CORTA_DURACION. Este valor NO pertenece al enum del esquema (PROPIEDAD | RENTING): se ha usado de forma deliberada para que el expediente no pase silenciosamente los controles de `rules.py`.
- Fecha Fin cambiada de NO_APLICA a NO_CONSTA: el contrato fija una devolución PREVISTA el 05/12/2024, pero no hay acta que acredite que se consumó.
- Número de contrato añadido desde el campo AUTORIZACIÓN del contrato (11206873-1).
- REVISAR TAMBIÉN 2056MSX: matrícula correlativa, mismo proveedor y misma estructura documental (DOCUMENTACIÓN + CONTRATO). Probablemente el mismo caso.

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con MALCO. El contrato solo cubre 90d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando 148d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
