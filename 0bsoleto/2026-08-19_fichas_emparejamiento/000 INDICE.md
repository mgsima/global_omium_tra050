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
| [[0767MJM]] | [[5875KPY]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[0971MXH]] | [[7001LLV]] | MEDICION AVANZADA CONTAD. | Furgoneta/Furgón | A_ACREDITADO |
| [[1066MWL]] | [[1947LMM]] | CGAC | Turismo | C_CONDICIONADO |
| [[1108KHK]] | [[2653LTG]] | G.O.MEDIOAMBIENTE S.L. | Turismo | C_CONDICIONADO |
| [[1666MGR]] | [[T5455BB]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[1667MGR]] | [[5949LLV]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[2076MJP]] | [[6586KPD]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[2120MFK]] | [[4535KFH]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[2704MXG]] | [[9377LMG]] | AVSA | Furgoneta/Furgón | B_INDICIO |
| [[2705MXG]] | [[4926LMS]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[2720MWP]] | [[9428LKC]] | AVSA | Turismo | C_CONDICIONADO |
| [[2722MXG]] | [[3598LKS]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[2737MXG]] | [[5937LLV]] | AVSA | Furgoneta/Furgón | C_CONDICIONADO |
| [[3103MXJ]] | [[6736LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | A_ACREDITADO |
| [[3105MWZ]] | [[7970LKX]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3111MWZ]] | [[0383LKK]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3116MXJ]] | [[8767LLW]] | G.O.MEDIOAMBIENTE S.L. | Furgoneta/Furgón | B_INDICIO |
| [[3121MWZ]] | [[3904LLT]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3122MWZ]] | [[8066LKY]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3133MWZ]] | [[4170LKY]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3143MWZ]] | [[9417LKC]] | EMIVASA | Turismo | A_ACREDITADO |
| [[3147MXJ]] | [[6741LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | A_ACREDITADO |
| [[3154MXJ]] | [[7015LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | C_CONDICIONADO |
| [[3157MXJ]] | [[6844LLV]] | EGEVASA | Furgoneta/Furgón | B_INDICIO |
| [[3178MXJ]] | [[6987LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | C_CONDICIONADO |
| [[3191MXJ]] | [[8313LLZ]] | EGEVASA | Furgoneta/Furgón | B_INDICIO |
| [[3246MXJ]] | [[7055LLV]] | AYWA SER.AMBIENTALES SL | Furgoneta/Furgón | B_INDICIO |
| [[4073MXK]] | [[5932LLV]] | CGAC | Furgoneta/Furgón | A_ACREDITADO |
| [[4597LGC]] | [[9305LMG]] | ISG | Furgoneta/Furgón | C_CONDICIONADO |
| [[5020MWL]] | [[3569LKS]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[5230MXL]] | [[6794LLV]] | UTE CHIVA(AV/EG) | Furgoneta/Furgón | C_CONDICIONADO |
| [[5566KSD]] | [[6994KGK]] | G.O.MEDIOAMBIENTE S.L. | Turismo | C_CONDICIONADO |
| [[6007MWV]] | [[7017KWW]] | AVSA | Turismo | A_ACREDITADO |
| [[6015MWV]] | [[7962LKX]] | AVSA | Turismo | A_ACREDITADO |
| [[6029MWV]] | [[5255LKX]] | AVSA | Turismo | A_ACREDITADO |
| [[6033MWV]] | [[5243LKX]] | CANALIZ. CIVILES S.A. | Turismo | A_ACREDITADO |
| [[6037MWV]] | [[5996LKM]] | CANALIZ. CIVILES S.A. | Turismo | A_ACREDITADO |
| [[6042MWV]] | [[0269LLK]] | AVSA | Turismo | A_ACREDITADO |
| [[6082MWV]] | [[5493LLD]] | E.Mixta Metropolitana, SA | Turismo | A_ACREDITADO |
| [[6083MWV]] | [[5829LLX]] | AVSA | Turismo | A_ACREDITADO |
| [[6084MWV]] | [[9418LKC]] | AVSA | Turismo | A_ACREDITADO |
| [[6089MWV]] | [[9504LDD]] | AVSA | Turismo | A_ACREDITADO |
| [[6094MWV]] | [[9494LKC]] | AVSA | Turismo | A_ACREDITADO |
| [[6097MWV]] | [[1451LDY]] | AVSA | Turismo | A_ACREDITADO |
| [[6124MWV]] | [[9276LMB]] | ISG | Turismo | A_ACREDITADO |
| [[6126MWV]] | [[3043KBJ]] | ISG | Turismo | A_ACREDITADO |
| [[6128MWV]] | [[0251LLK]] | ISG | Turismo | C_CONDICIONADO |
| [[6209MWV]] | [[4223LJV]] | EMP.AG.POTABL.MALGRAT SA | Turismo | B_INDICIO |
| [[6233MXY]] | [[1192LPK]] | CGAC | Turismo | C_CONDICIONADO |
| [[6245MWV]] | [[3931LLT]] | E.Mixta Metropolitana, SA | Turismo | A_ACREDITADO |
| [[6334MXF]] | [[6997LLV]] | AVSA | Furgoneta/Furgón | B_INDICIO |
| [[6398MWV]] | [[0019LLR]] | CGAC | Turismo | A_ACREDITADO |
| [[6439MWV]] | [[0246LLK]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[6442MWV]] | [[3942LLT]] | G.O.MEDIOAMBIENTE S.L. | Turismo | B_INDICIO |
| [[6444MWV]] | [[4988LLY]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[6445MWV]] | [[9413LKC]] | CGAC | Turismo | A_ACREDITADO |
| [[6492MWV]] | [[0818LKK]] | MEDICION AVANZADA CONTAD. | Turismo | A_ACREDITADO |
| [[6493MWV]] | [[8030LKY]] | MEDICION AVANZADA CONTAD. | Turismo | A_ACREDITADO |
| [[6558MWV]] | [[9977LLM]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[6559MWV]] | [[9019LBN]] | G.O.MEDIOAMBIENTE S.L. | Turismo | A_ACREDITADO |
| [[7775MXF]] | [[5969LLV]] | GAMASER | Furgoneta/Furgón | C_CONDICIONADO |
| [[8349MXG]] | [[5918LLV]] | ISG | Furgoneta/Furgón | C_CONDICIONADO |
| [[8597MWT]] | [[4938LMS]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[8628MWT]] | [[7399LLP]] | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | C_CONDICIONADO |
| [[8634MWT]] | [[9369LMG]] | CANALIZ. CIVILES S.A. | Furgoneta/Furgón | B_INDICIO |
| [[8662NDJ]] | [[1485LSB]] | EMIVASA | Turismo | B_INDICIO |
| [[8873KDN]] | [[1751LHM]] | GAMASER | Turismo | B_INDICIO |
| [[8994MSH]] | [[6756LLV]] | CGAC | Furgoneta/Furgón | C_CONDICIONADO |
| [[9050MWN]] | [[8298KZS]] | AVSA | Turismo | A_ACREDITADO |
