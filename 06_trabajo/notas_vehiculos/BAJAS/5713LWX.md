---
matricula: "5713LWX"
rol: "BAJA"
tags:
  - vehiculo
  - baja
  - global_omnium
  - elegibilidad_dudosa
  - revision_manual
tipo_vehiculo: "COMBUSTION_DIESEL"
marca_modelo: "PEUGEOT 208 Bluehdi 73kw (1 00cv) Active"
bastidor: "VR3UBYHTKN5814947"
combustible: "Gas-oil"
categoria: "M1"
regimen: "RENTING"
servicio_dgt: "NO_ESPECIFICADO"
titular_empresa: "EMPRESA GENERAL VALENCIANA DEL AGUA"
titular_cif: "A46615159"
numero_contrato: "448563"
conductor_habitual: "MANUEL RARO"
conductor_dni: "NO_CONSTA"
base_ubicacion: "GIRONA"
comunidad_autonoma: "Cataluña"
comunidad_fuente: "BASE_UBICACION"
fecha_inicio: "2023-10-02"
fecha_fin: "2024-04-01"
dias_arrendamiento: 182
fecha_matriculacion: "NO_CONSTA"
tiene_acta_devolucion: true
coche_emparejado: "SIN_EMPAREJAMIENTO"
emparejamiento_nivel: "SIN_EMPAREJAMIENTO"
emparejamiento_pendiente: "Posesion 182d < 730d exigidos para un vehiculo tenido en arrendamiento"
emparejamiento_revision: "v3 2026-08-07"
regimen_a_verificar: true
---

# FICHA VEHÍCULO: 5713LWX (BAJA)

## TRAZABILIDAD Y ORIGEN DE DATOS
- Coche Emparejado: SIN_EMPAREJAMIENTO
- Marca / Modelo: PEUGEOT 208 Bluehdi 73kw (1 00cv) Active | Origen: PDF: [[5713LWX ACTA DEVOLUCION.pdf]] | Markdown: [[5713LWX ACTA DEVOLUCION.md]]
- Bastidor: VR3UBYHTKN5814947 | Origen: PDF: [[5713LWX FICHA Y PERMISOS.pdf]] | Markdown: [[5713LWX FICHA Y PERMISOS.md]]
- Categoría: M1
- Tipo Vehículo / Motorización: COMBUSTION_DIESEL
- Combustible: Gas-oil
- Régimen: RENTING
- Servicio DGT: NO_ESPECIFICADO
- Titular: EMPRESA GENERAL VALENCIANA DEL AGUA (CIF: A46615159) | Origen: PDF: [[5713LWXCondicionesparticulares_20251021093531.814_X.doc]] | Markdown: [[5713LWXCondicionesparticulares_20251021093531.814_X.md]]
- Conductor: MANUEL RARO (DNI: NO_CONSTA) | Origen: PDF: [[5713LWX ACTA ENTREGA.pdf]] | Markdown: [[5713LWX ACTA ENTREGA.md]]
- Número Contrato: 448563 | Origen: PDF: [[5713LWXCondicionesparticulares_20251021093531.814_X.doc]] | Markdown: [[5713LWXCondicionesparticulares_20251021093531.814_X.md]]
- Base / Ubicación: GIRONA | Origen: PDF: [[5713LWX ACTA DEVOLUCION.pdf]] | Markdown: [[5713LWX ACTA DEVOLUCION.md]]
- Comunidad Autónoma: Cataluña | Derivada de `base_ubicacion` ("GIRONA"), provincia de Girona.
- Fecha Inicio: 2023-10-02 | Origen: PDF: [[5713LWXCondicionesparticulares_20251021093531.814_X.doc]] | Markdown: [[5713LWXCondicionesparticulares_20251021093531.814_X.md]]
- Fecha Fin: 2024-04-01 | Origen: PDF: [[5713LWX ACTA DEVOLUCION.pdf]] | Markdown: [[5713LWX ACTA DEVOLUCION.md]]
- Días Arrendamiento / Tenencia: 182 días (Calculado entre 2023-10-02 y 2024-04-01)
- Fecha Matriculación: NO_CONSTA

## INVENTARIO DOCUMENTAL
- PDF: [[5713LWX ACTA DEVOLUCION.pdf]] | Markdown: [[5713LWX ACTA DEVOLUCION.md]] (Tipo: BAJA_VEHICULO, Formato: PDF, Estado: VALIDO)
- PDF: [[5713LWX ACTA ENTREGA.pdf]] | Markdown: [[5713LWX ACTA ENTREGA.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[5713LWX FICHA Y PERMISOS.pdf]] | Markdown: [[5713LWX FICHA Y PERMISOS.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: PDF, Estado: VALIDO)
- PDF: [[5713LWXCondicionesparticulares_20251021093531.814_X.doc]] | Markdown: [[5713LWXCondicionesparticulares_20251021093531.814_X.md]] (Tipo: PROPIEDAD_ANTIGUO, Formato: WORD, Estado: INVALIDO)

- Alerta Formato: WORD_DETECTADO en [[5713LWXCondicionesparticulares_20251021093531.814_X.doc]]

## REVISIÓN MANUAL (2026-07-23)
- titular_empresa/titular_cif: de "LEASEPLAN SERVICIOS S.A." (CIF A-78007473) a "EMPRESA GENERAL VALENCIANA DEL AGUA" (CIF A46615159). El valor anterior era el ARRENDADOR (la propia LeasePlan), no el arrendatario/titular. [[5713LWXCondicionesparticulares_20251021093531.814_X.md]] identifica expresamente "arrendatario EMPRESA GENERAL VALENCIANA DEL AGUA CIF: A46615159". Discrepancia sin resolver: las actas de entrega/devolución identifican como "Cliente: 407699 - COMPANYIA GENERAL D AIGUES CATALUNY", distinto del arrendatario que figura en las condiciones particulares; se mantiene el dato de las condiciones particulares (fuente explícita de "arrendatario") y se deja constancia de la discrepancia.
- Fechas verificadas sin cambios: fecha_inicio (2023-10-02, coincide "Fecha salida" y "Fecha Entrega" en el mismo día según Condiciones Particulares) y fecha_fin (2024-04-01, Acta de Devolución cumplimentada), dias_arrendamiento (182, por debajo de 730 días de renting, ya reflejado antes de esta revisión).

> **PENDIENTE DE COMPROBAR — REGIMEN.** REGIMEN_A_VERIFICAR: el Excel etiqueta el contrato como 'ALQUILER_CORTA_DURACION' con AYVENS. El contrato solo cubre 182d, por debajo de los 730d exigidos; la pareja se sostiene unicamente contando ?d desde la matriculacion. COMPROBAR con doble motivo: hay que reconstruir con contratos la cadena completa de posesion, porque a dia de hoy lo unico documentado es la antiguedad del vehiculo, no que lo tuviera el solicitante
