---
doc_type: indice_fichas_emparejamiento
fecha: 2026-08-07
parejas: 69
---

# Indice de fichas de emparejamiento TRA050

Una ficha por vehiculo: **245 altas** y **245 bajas** del Excel, tengan carpeta documental o no.

## Como revisar

Cada ficha de alta emparejada trae la **verificacion regla a regla** con el valor real que satisface cada una, y una tabla de **candidatas alternativas** con las demas bajas que tambien cumplian todo. Si alguna alternativa encaja mejor por conocimiento del expediente, ahi se ve.

## Reglas aplicadas

| # | Regla | Umbral |
| :- | :--- | :--- |
| R1 | Misma sociedad del grupo | `Cod.Sociedad` alta = baja |
| R2 | Posesion minima | 365d en propiedad / 730d si se tuvo por contrato. **La etiqueta del contrato en el Excel no descarta**: decide el periodo de posesion. Las bajas cuyo contrato no se llama RENTING ni PROPIEDAD se admiten marcadas `regimen_a_verificar: true` |
| R3 | Alta electrica pura; baja de combustion, **hibrido incluido** (solo se excluye el electrico puro como sustituido) | |
| R4 | Misma categoria | no se admite sustitucion entre categorias |
| R5 | Ventana | −3 / +6 meses |
| R6 | Ambito CAE | adquisicion posterior al 2023-01-25 |

## Resultado

- **69 parejas**: 37 acreditadas, 11 por indicio, 21 condicionadas
- Altas no elegibles: 13 | Bajas no elegibles: 61

## Parejas

| Alta | Baja | Sociedad | Categoria | Nivel |
| :--- | :--- | :--- | :--- | :--- |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0767MJM]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5875KPY]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0971MXH]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7001LLV]] | MEDICION AVANZADA CONTAD. | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1066MWL]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1947LMM]] | CGAC | Turismo | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1108KHK]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2653LTG]] | G.O.MEDIOAMBIENTE S.L. | Turismo | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1666MGR]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/T5455BB]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1667MGR]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5949LLV]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2076MJP]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6586KPD]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2120MFK]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4535KFH]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2704MXG]] | [[9377LMG]] | AVSA | Furgoneta/Furgón | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2705MXG]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4926LMS]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2720MWP]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9428LKC]] | AVSA | Turismo | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2722MXG]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3598LKS]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/2737MXG]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5937LLV]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3103MXJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6736LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3105MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7970LKX]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3111MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0383LKK]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3116MXJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8767LLW]] | G.O.MEDIOAMBIENTE S.L. | Furgoneta/Furgón | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3121MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3904LLT]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3122MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8066LKY]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3133MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4170LKY]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3143MWZ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9417LKC]] | EMIVASA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3147MXJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6741LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3154MXJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7015LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3157MXJ]] | [[6844LLV]] | EGEVASA | Furgoneta/Furgón | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3178MXJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6987LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3191MXJ]] | [[8313LLZ]] | EGEVASA | Furgoneta/Furgón | B_INDICIO |
| [[3246MXJ]] | [[7055LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4073MXK]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5932LLV]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[4597LGC]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9305LMG]] | ISG | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5020MWL]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3569LKS]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5230MXL]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6794LLV]] | UTE CHIVA(AV/EG) | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5566KSD]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6994KGK]] | G.O.MEDIOAMBIENTE S.L. | Turismo | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6007MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7017KWW]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6015MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7962LKX]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6029MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5255LKX]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6033MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5243LKX]] | CANALIZ. CIVILES S.A. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6037MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5996LKM]] | CANALIZ. CIVILES S.A. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6042MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0269LLK]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6082MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5493LLD]] | E.Mixta Metropolitana, SA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6083MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5829LLX]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6084MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9418LKC]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6089MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9504LDD]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6094MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9494LKC]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6097MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1451LDY]] | AVSA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6124MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9276LMB]] | ISG | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6126MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3043KBJ]] | ISG | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6128MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0251LLK]] | ISG | Turismo | C_CONDICIONADO |
| [[6209MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4223LJV]] | EMP.AG.POTABL.MALGRAT SA | Turismo | B_INDICIO |
| [[6233MXY]] | [[1192LPK]] | CGAC | Turismo | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6245MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3931LLT]] | E.Mixta Metropolitana, SA | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6334MXF]] | [[6997LLV]] | AVSA | Furgoneta/Furgón | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6398MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0019LLR]] | CGAC | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6439MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0246LLK]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6442MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/3942LLT]] | G.O.MEDIOAMBIENTE S.L. | Turismo | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6444MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/4988LLY]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6445MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9413LKC]] | CGAC | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6492MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/0818LKK]] | MEDICION AVANZADA CONTAD. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6493MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8030LKY]] | MEDICION AVANZADA CONTAD. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6558MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9977LLM]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6559MWV]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9019LBN]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/7775MXF]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5969LLV]] | GAMASER | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8349MXG]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/5918LLV]] | ISG | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8597MWT]] | [[4938LMS]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[8628MWT]] | [[7399LLP]] | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8634MWT]] | [[9369LMG]] | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | B_INDICIO |
| [[8662NDJ]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1485LSB]] | EMIVASA | Turismo | B_INDICIO |
| [[8873KDN]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/1751LHM]] | GAMASER | Turismo | B_INDICIO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8994MSH]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/6756LLV]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/9050MWN]] | [[tra050/data/global_omium_tra050/_0bsoleto/2026-08-19_fichas_emparejamiento/8298KZS]] | AVSA | Turismo | A_ACREDITADO |
