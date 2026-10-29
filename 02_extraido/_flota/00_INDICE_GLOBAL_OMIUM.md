---
doc_type: auditoria_indice
fuente_excel: CALCULO CAE BV VEHICULOS 2025_09_29_Glob_Om_TRA050.xlsx
estado: extraido
---

# 🚗⚡ Índice y Resumen de Datos Extraídos - Global Omium (TRA050)

Se han extraído y normalizado con éxito **todas las hojas del archivo Excel principal de Global Omium**.
Este documento sirve como inventario y referencia cruzada para consultar los coches dados de baja y de alta.

## 📊 Resumen Ejecutivo por Hojas

| Hoja Original | Nombre Tabla / Archivo | Filas | Columnas | Matrículas Únicas Detectadas |
| :--- | :--- | :---: | :---: | :---: |
| `AE GF  (2)` | `AE_GF_2` | 157 | 66 | 310 |
| `AE GF ` | `AE_GF` | 157 | 66 | 310 |
| `RESUMEN ACT` | `RESUMEN_ACT` | 348 | 49 | 513 |
| `datos anexos` | `datos_anexos` | 348 | 57 | 513 |
| `DATOS Acuerdo GF` | `DATOS_Acuerdo_GF` | 348 | 57 | 513 |
| `TABLA SOC CAE` | `TABLA_SOC_CAE` | 22 | 14 | - |
| `Hoja2` | `Hoja2` | 223 | 2 | 223 |
| `SUSTITUCIONES ` | `SUSTITUCIONES` | 8 | 16 | - |
| `ALTA 20242025` | `ALTA_20242025` | 240 | 113 | 240 |
| `BAJA2022202320242025` | `BAJA2022202320242025` | 243 | 117 | 243 |

---

## 📂 Formatos de Acceso Disponibles

Los datos extraídos están estructurados en los siguientes formatos en la carpeta `Resultados_Auditoria/global_omium_extraido/` (y copia en `data/global_omium_tra050/datos_extraidos/`):

1. **Archivos CSV por Hoja:** `Resultados_Auditoria/global_omium_extraido/csv/*.csv`
2. **Archivos JSON por Hoja:** `Resultados_Auditoria/global_omium_extraido/json/*.json`
3. **JSON Global Unificado:** `Resultados_Auditoria/global_omium_extraido/global_omium.json`
4. **Base de Datos SQLite con Índices:** `Resultados_Auditoria/global_omium_extraido/global_omium.db`

---

## 🔍 Estructura Detallada de Columnas por Hoja

### 📋 Tabla: `AE_GF_2` (Hoja: `AE GF  (2)`)
- **Registros:** 157 filas | **Campos:** 66 columnas
- **Campos de Matrícula:** `Matricula, Matricula nueva`
- **Columnas extraídas:**
  ```text
  - columna_0
  - ID CAE
  - Matricula
  - TIPO VEHÍCULO
  - COMBUSTIBLE
  - Columna4
  - Columna5
  - Contrato
  - Acta de Entrega
  - Acta Devolución
  - BAJA
  - Ficha Técnica
  - Permiso de Circulación
  - IVTM
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - f Vig Inicio
  - F.Vig.Final
  - Tiempo Prop
  - Año
  - Cod.Sit.Contrato
  - Combustible2
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - Ceco.Imput
  - Columna1
  - Matricula nueva
  - Marca2
  - Modelo/Versión3
  - Combustible4
  - Ceco
  - Renov. Flota
  - Fecha Alta
  - Columna3
  - Cod.Sociedad5
  - Pedido
  - Sociedad6
  - Ceco imputado
  - Factura
  - Comunidad Autonoma
  - CHASIS/Bastidor
  - CVA
  - F
  - CVN
  - L
  - AE
  - Columna2
  - Vacias
  - Tipo vehículo2
  - Tipo combustible
  - ID CAE2
  - CVA2
  - f2
  - CVN2
  - L2
  - AE [kWh]
  - Comprobación
  - Comprobación 2
  - f23
  - CVN22
  - L23
  - columna_65
  ```

### 📋 Tabla: `AE_GF` (Hoja: `AE GF `)
- **Registros:** 157 filas | **Campos:** 66 columnas
- **Campos de Matrícula:** `Matricula, Matricula nueva`
- **Columnas extraídas:**
  ```text
  - columna_0
  - ID CAE
  - Matricula
  - TIPO VEHÍCULO
  - COMBUSTIBLE
  - Columna4
  - Columna5
  - Contrato
  - Acta de Entrega
  - Acta Devolución
  - BAJA
  - Ficha Técnica
  - Permiso de Circulación
  - IVTM
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - f Vig Inicio
  - F.Vig.Final
  - Fecha Devolución
  - Tiempo Prop
  - Año
  - Cod.Sit.Contrato
  - Combustible2
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - Ceco.Imput
  - Columna1
  - Matricula nueva
  - Marca2
  - Modelo/Versión3
  - Combustible4
  - Ceco
  - Renov. Flota
  - Fecha Alta
  - Columna3
  - Cod.Sociedad5
  - Pedido
  - Sociedad6
  - Ceco imputado
  - Factura
  - Comunidad Autonoma
  - CHASIS/Bastidor
  - CVA
  - F3
  - CVN
  - L
  - AE
  - Columna2
  - Vacias
  - Tipo vehículo2
  - Tipo combustible
  - CVA2
  - f2
  - CVN2
  - L2
  - AE [kWh]
  - Comprobación
  - Comprobación 2
  - f23
  - CVN22
  - L23
  - columna_65
  ```

### 📋 Tabla: `RESUMEN_ACT` (Hoja: `RESUMEN ACT`)
- **Registros:** 348 filas | **Campos:** 49 columnas
- **Campos de Matrícula:** `Matricula, Matricula nueva`
- **Columnas extraídas:**
  ```text
  - ID CAE
  - OK DE GF
  - Matricula
  - Contrato
  - Acta de Entrega
  - Acta Devolución
  - BAJA
  - Ficha Técnica
  - Permiso de Circulación
  - IVTM
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - f Vig Inicio
  - F.Vig.Final
  - Tiempo Prop
  - Año
  - Cod.Sit.Contrato
  - Combustible
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - Ceco.Imput
  - Columna1
  - Matricula nueva
  - Marca2
  - Modelo/Versión3
  - Combustible4
  - Ceco
  - Renov. Flota
  - Fecha Alta
  - Columna3
  - Cod.Sociedad5
  - Pedido
  - Sociedad6
  - Ceco imputado
  - Factura
  - Comunidad Autonoma
  - CHASIS/Bastidor
  - CVA
  - F
  - CVN
  - L
  - AE
  - Columna2
  - CALCULO GF
  - Vacias
  ```

### 📋 Tabla: `datos_anexos` (Hoja: `datos anexos`)
- **Registros:** 348 filas | **Campos:** 57 columnas
- **Campos de Matrícula:** `Matricula Antigua, Matricula nueva`
- **Columnas extraídas:**
  ```text
  - ID CAE
  - OK DE GF
  - Matricula Antigua
  - Contrato
  - Acta de Entrega
  - Acta Devolución
  - BAJA
  - Ficha Técnica
  - Permiso de Circulación
  - IVTM
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - f Vig Inicio
  - F.Vig.Final
  - Tiempo Prop
  - Año
  - Cod.Sit.Contrato
  - Combustible
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - Ceco.Imput
  - Columna1
  - Localidad
  - Provincia
  - Com. Aut.
  - Dirección
  - Huso
  - Coord.
  - Referencia Catastral
  - Descripción de la actuación
  - Matricula nueva
  - Marca2
  - Modelo/Versión3
  - Combustible4
  - Ceco
  - Renov. Flota
  - Fecha Alta
  - Columna3
  - Cod.Sociedad5
  - Pedido
  - Sociedad6
  - Ceco imputado
  - Factura
  - Comunidad Autonoma2
  - CHASIS/Bastidor
  - CVA
  - F
  - CVN
  - L
  - Ahorro estimado
  - Columna2
  - CALCULO GF
  - Vacias
  ```

### 📋 Tabla: `DATOS_Acuerdo_GF` (Hoja: `DATOS Acuerdo GF`)
- **Registros:** 348 filas | **Campos:** 57 columnas
- **Campos de Matrícula:** `Matricula Antigua, Matricula nueva`
- **Columnas extraídas:**
  ```text
  - ID CAE
  - OK DE GF
  - Matricula Antigua
  - Contrato
  - Acta de Entrega
  - Acta Devolución
  - BAJA
  - Ficha Técnica
  - Permiso de Circulación
  - IVTM
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - f Vig Inicio
  - F.Vig.Final
  - Tiempo Prop
  - Año
  - Cod.Sit.Contrato
  - Combustible
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - Ceco.Imput
  - Columna1
  - Localidad
  - Provincia
  - Com. Aut.
  - Dirección
  - Huso
  - Coord.
  - Referencia Catastral
  - Descripción de la actuación
  - Matricula nueva
  - Marca2
  - Modelo/Versión3
  - Combustible4
  - Ceco
  - Renov. Flota
  - Fecha Alta
  - Columna3
  - Cod.Sociedad5
  - Pedido
  - Sociedad6
  - Ceco imputado
  - Factura
  - Comunidad Autonoma2
  - CHASIS/Bastidor
  - CVA
  - F
  - CVN
  - L
  - Ahorro estimado
  - Columna2
  - CALCULO GF
  - Vacias
  ```

### 📋 Tabla: `TABLA_SOC_CAE` (Hoja: `TABLA SOC CAE`)
- **Registros:** 22 filas | **Campos:** 14 columnas
- **Columnas extraídas:**
  ```text
  - columna_0
  - Sociedad
  - Localidad
  - Provincia
  - Comunidad Autonoma
  - Dirección
  - Coordenadas
  - Referencia Catastral
  - Descripción de Actuación
  - Suma de AE (kWh)
  - columna_10
  - columna_11
  - columna_12
  - columna_13
  ```

### 📋 Tabla: `Hoja2` (Hoja: `Hoja2`)
- **Registros:** 223 filas | **Campos:** 2 columnas
- **Campos de Matrícula:** `NUEVAS MATRÍCULAS`
- **Columnas extraídas:**
  ```text
  - NUEVAS MATRÍCULAS
  - CHASIS
  ```

### 📋 Tabla: `SUSTITUCIONES` (Hoja: `SUSTITUCIONES `)
- **Registros:** 8 filas | **Campos:** 16 columnas
- **Columnas extraídas:**
  ```text
  - 7190JDY
  - columna_1
  - columna_2
  - columna_3
  - columna_4
  - X
  - columna_6
  - columna_7
  - OTROS
  - 8
  - OTROS AUTORIZADOS
  - CANCELADO
  - 2024-03-31 00:00:00
  - columna_13
  - 4
  - HÍBRIDO
  ```

### 📋 Tabla: `ALTA_20242025` (Hoja: `ALTA 20242025`)
- **Registros:** 240 filas | **Campos:** 113 columnas
- **Campos de Matrícula:** `Matrícula`
- **Columnas extraídas:**
  ```text
  - Situac.
  - Matrícula
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - Cod.Sit.Contrato
  - Cod.Sociedad
  - Sociedad
  - columna_9
  - Cod.Soc.Subro DE
  - Soc.subrogación DE
  - Cod.Soc.Pte.Sub A
  - Soc.Pte.Subrogación A
  - Nuesta Sol.Compras
  - Ref/Pedido Prov.
  - Cont.Marco Prov.
  - CPER/Pedido
  - Solicitada Devol.
  - Cod.Periodicidad
  - Periodicidad
  - Ind.IVA
  - KM Contratados
  - Cod.Tipo KM Contratados
  - Tipo KM Contratados
  - Cod.Tipo Prorroga
  - Tipo Prorroga
  - Marca
  - Modelo/Versión
  - Cód.Rotulación
  - Rotulación
  - Baca
  - Enganche
  - Separador
  - Cod. Combustible
  - Combustible
  - Cód.Vehículo Taller
  - Tipo Vehículo Taller
  - Accesorios particulares
  - Lugar de Pernota
  - Renov.Flota Año
  - Renov.Flota Mes
  - Cambio Vehículo por
  - DNI Conductor
  - Nombre Conductor
  - Compartido con
  - DNI Resp.Notif
  - Nombre Resp.Notificación
  - Origen Toma KM
  - Veh.Sustitución
  - Soc.Imput
  - Ceco.Imput
  - Cebe
  - Orden.Imput
  - ¿Refactura Grupo?
  - Cod.Zona
  - Zona
  - Cod.Delegación.
  - Delegación
  - Responsable
  - Línea negocio
  - Nº Tarjetas en vigor
  - Anexos
  - Cód.Servicio
  - Prorrateo
  - Anticipado
  - Observaciones
  - Cód.Centro trabajo
  - Nom.Centro trabajo
  - Categoría Veh.
  - Nom.Categoría Veh.
  - Via-T Solred
  - Inst.con Depósito
  - H24
  - Límite H24
  - Tarjeta SOLRED
  - Recurso compar.
  - Uso Mixto
  - Tfno.contacto
  - Persona contacto entrega
  - Nom.Persona contacto entrega
  - GPS
  - Código.GPS
  - Nombre.GPS
  - Cod.Tipología
  - Tipología
  - Notifica envío KM
  - Fecha efectiva Sub.
  - F.Alta Veh
  - F.Vig.Inicio
  - F.Vig.Final
  - F.Devolución/Baja
  - Nº cuotas Ini.Rent.
  - Nº cuotas Re-renting
  - Imp.Cuota SIN IVA
  - Imp.Cuota Suplidos
  - Imp.Cuota Veh.
  - Imp.Cuota CON IVA
  - Nº cuotas Prorroga
  - F.Fin Prórroga
  - KM Recorridos
  - Fecha Toma KM
  - F.Revisión ITV
  - Kms.Próxima Revisión
  - F.Alta Sustitución
  - F.Baja Sustitución
  - %.Imput
  - F.Vigencia
  - F.Hasta Imput.
  - F.Prevista Entrega
  - F.Prevista Devolución
  - Coef.Exceso Km
  - Coef.Defecto Km
  ```

### 📋 Tabla: `BAJA2022202320242025` (Hoja: `BAJA2022202320242025`)
- **Registros:** 243 filas | **Campos:** 117 columnas
- **Campos de Matrícula:** `Matrícula`
- **Columnas extraídas:**
  ```text
  - Situac.
  - Matrícula
  - Compañía/Proveedor
  - Cod.Tipo Contrato
  - Tipo Contrato
  - Situación Contrato
  - F.Vig.Final
  - Cod.Sit.Contrato
  - Combustible
  - Marca
  - Modelo/Versión
  - Cod.Sociedad
  - Sociedad
  - columna_13
  - columna_14
  - columna_15
  - columna_16
  - Cod.Soc.Subro DE
  - Soc.subrogación DE
  - Cod.Soc.Pte.Sub A
  - Soc.Pte.Subrogación A
  - Nuesta Sol.Compras
  - Ref/Pedido Prov.
  - Cont.Marco Prov.
  - CPER/Pedido
  - Solicitada Devol.
  - Cod.Periodicidad
  - Periodicidad
  - Ind.IVA
  - KM Contratados
  - Cod.Tipo KM Contratados
  - Tipo KM Contratados
  - Cod.Tipo Prorroga
  - Tipo Prorroga
  - Cód.Rotulación
  - Rotulación
  - Baca
  - Enganche
  - Separador
  - Cod. Combustible
  - Cód.Vehículo Taller
  - Tipo Vehículo Taller
  - Accesorios particulares
  - Lugar de Pernota
  - Renov.Flota Año
  - Renov.Flota Mes
  - Cambio Vehículo por
  - DNI Conductor
  - Nombre Conductor
  - Compartido con
  - DNI Resp.Notif
  - Nombre Resp.Notificación
  - Origen Toma KM
  - Veh.Sustitución
  - Soc.Imput
  - Ceco.Imput
  - Cebe
  - Orden.Imput
  - ¿Refactura Grupo?
  - Cod.Zona
  - Zona
  - Cod.Delegación.
  - Delegación
  - Responsable
  - Línea negocio
  - Nº Tarjetas en vigor
  - Anexos
  - Cód.Servicio
  - Prorrateo
  - Anticipado
  - Observaciones
  - Cód.Centro trabajo
  - Nom.Centro trabajo
  - Categoría Veh.
  - Nom.Categoría Veh.
  - Via-T Solred
  - Inst.con Depósito
  - H24
  - Límite H24
  - Tarjeta SOLRED
  - Recurso compar.
  - Uso Mixto
  - Tfno.contacto
  - Persona contacto entrega
  - Nom.Persona contacto entrega
  - GPS
  - Código.GPS
  - Nombre.GPS
  - Cod.Tipología
  - Tipología
  - Notifica envío KM
  - Fecha efectiva Sub.
  - F.Alta Veh
  - F.Vig.Inicio
  - columna_94
  - F.Devolución/Baja
  - Nº cuotas Ini.Rent.
  - Nº cuotas Re-renting
  - Imp.Cuota SIN IVA
  - Imp.Cuota Suplidos
  - Imp.Cuota Veh.
  - Imp.Cuota CON IVA
  - Nº cuotas Prorroga
  - F.Fin Prórroga
  - KM Recorridos
  - Fecha Toma KM
  - F.Revisión ITV
  - Kms.Próxima Revisión
  - F.Alta Sustitución
  - F.Baja Sustitución
  - %.Imput
  - F.Vigencia
  - F.Hasta Imput.
  - F.Prevista Entrega
  - F.Prevista Devolución
  - Coef.Exceso Km
  - Coef.Defecto Km
  ```

---

## 💡 Ejemplos de Consultas Rápidas

### Python / Pandas
```python
import pandas as pd
import sqlite3

# Opción A: Cargar desde CSV
df_bajas = pd.read_csv('Resultados_Auditoria/global_omium_extraido/csv/BAJA2022202320242025.csv')
df_altas = pd.read_csv('Resultados_Auditoria/global_omium_extraido/csv/ALTA_20242025.csv')

# Opción B: Consultar SQLite
conn = sqlite3.connect('Resultados_Auditoria/global_omium_extraido/global_omium.db')
df_resumen = pd.read_sql_query('SELECT * FROM RESUMEN_ACT WHERE Matricula = "3299KTP"', conn)
```
