# EDA: Fraudes com Cartões de Crédito

Análise exploratória de **10.000 transações** de cartões de crédito para identificar quais variáveis mais discriminam fraudes de transações legítimas e fundamentar os próximos passos da detecção.

É importante lembrar que é uma base de dados **sintética**, isto é, dados gerados artificialmente para estudo/prática de análise de dados.

**Dataset**: [Kaggle](https://www.kaggle.com/datasets/miadul/credit-card-fraud-detection-dataset)

## Sumário

- [Visão Geral](#vis%C3%A3o-geral)
- [Resultados Principais](#resultados-principais)
- [Dados](#dados)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Execução](#execu%C3%A7%C3%A3o)
- [Autor](#autor)

---

## Visão Geral

Investigação exploratória de detecção de fraude em cartões de crédito:

- **KPIs gerais** (taxa de fraude, volume financeiro, ticket médio, transações estrangeiras)
- **Análise de horário** (taxa de fraude e volume por hora do dia)
- **Análise de valor** (distribuição do valor das transações por classe)
- **Categoria do estabelecimento** (taxa de fraude por merchant category)
- **Sinais de risco** (transação estrangeira, location mismatch, device trust score, velocity, idade)
- **Análise cruzada** (combinações de sinais e correlações)
- **Geração de insights e recomendações**

---

## Resultados Principais

| KPI | Valor |
| --- | --- |
| Total de transações | 10.000 |
| Total de fraudes | 151 |
| Taxa de fraude | 1.51% |
| Volume total | $1.759.498,49 |
| Ticket médio | $175.95 |
| Ticket médio das fraudes | $216.18 (+23%) |
| Valor defraudado | $32.643,63 (1.86% do total) |
| Transações estrangeiras | 978 (9.78%) |

**Insights principais:**

- **Meia-noite é o epicentro**: 80% das fraudes (121/151) acontecem entre 0h–3h, com taxas de 6–9% contra a média geral de 1.51%
- **Transação estrangeira**: taxa de fraude de 8.38% (~11× a baseline)
- **Location mismatch**: taxa de fraude de 8.40% (~10× a baseline)
- **Velocity ≥ 5**: 10.4% de fraude; e **81%** de todas as fraudes ocorreu em dispositivos com trust score baixo (25–44)
- **Estrangeira + location mismatch**: taxa de **34.1%** — apenas 0.85% do volume captura 19% das fraudes
- **Regra simples**: "noturno + sinal geográfico" sinaliza 3% das transações e captura 63% das fraudes (precisão 31.5%)
- **Categoria e idade são discriminadores fracos**: Grocery lidera com 2.01%, mas a variação entre categorias é pequena (1.17–2.01%); idade varia entre 1.3% e 1.8%

---

## Dados

Base sintética com **10.000 linhas** e **10 colunas**:

| Coluna | Tipo | Descrição |
| --- | --- | --- |
| `transaction_id` | int | Identificador da transação (único, 1–10000) |
| `amount` | float | Valor da transação ($) |
| `transaction_hour` | int | Hora do dia da transação (0–23) |
| `merchant_category` | str | Categoria do estabelecimento (5: Clothing, Electronics, Food, Grocery, Travel) |
| `foreign_transaction` | int | 1 se a transação é estrangeira, 0 caso contrário |
| `location_mismatch` | int | 1 se há divergência de localização, 0 caso contrário |
| `device_trust_score` | int | Score de confiança do dispositivo (25–99) |
| `velocity_last_24h` | int | Número de transações nas últimas 24h (0–9) |
| `cardholder_age` | int | Idade do portador do cartão (18–69) |
| `is_fraud` | int | 1 = fraude, 0 = legítima |

### Pontos de Qualidade (verificados na limpeza)

- **Nenhum valor faltante** em nenhuma coluna e **nenhuma linha duplicada** (ou `transaction_id` duplicado)
- `device_trust_score` nunca é menor que 25 (piso do "dispositivo não confiável")
- Apenas **1 transação com `amount = 0.00`** (caso-limite isolado)

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
| --- | --- |
| **Pandas** | Manipulação e transformação de dados |
| **NumPy** | Cálculos numéricos |
| **Plotly** | Gráficos interativos |
| **Matplotlib** | Gráficos complementares (cards de KPIs) |
| **Seaborn** | Heatmap de correlação |
| **Jupyter** | Ambiente de desenvolvimento |

## Execução

1. Instale as dependências: `pip install pandas numpy plotly matplotlib seaborn`
2. Execute: `jupyter notebook eda_credit_fraud.ipynb` ou abra no VS Code com a extensão Jupyter.

## Autor

**Github**: [victorxavier01](https://github.com/victorxavier01)

**LinkedIn**: [Victor Xavier](https://www.linkedin.com/in/victor-xavier-89a339378/)

**Medium**: [medium.com/@lvsxmk23](https://medium.com/@lvsxmk23)
