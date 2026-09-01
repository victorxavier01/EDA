# EDA — Exploratory Data Analysis

Repositório com projetos de Análise Exploratória de Dados (EDA) usando Python e Jupyter Notebooks.

A ideia é mostrar a evolução do trabalho, do aprendizado à escala:

1. **[01-ecommerce-basico](./01-ecommerce-basico/)** — base sintética pequena (1.000 pedidos): fundamentos de EDA e primeira modelagem;
2. **[02-ecommerce-uk](./02-ecommerce-uk/)** — dados reais (541.909 transações, UK Online Retail): análise completa de negócio;
3. **[03-ecommerce-1m](./03-ecommerce-1m/)** — base sintética em escala (1M de transações): manipulação e visualização com dados grandes;
4. **[04-credit-card-fraud](./04-credit-card-fraud/)** — 10.000 transações sintéticas: sinais de fraude por horário, valor, categoria e risco.

| Projeto | Dataset | Escopo |
|---------|---------|--------|
| [01-ecommerce-basico](./01-ecommerce-basico/) | 1.000 pedidos (sintético) | KPIs, RFM, K-Means, Regressão Linear |
| [02-ecommerce-uk](./02-ecommerce-uk/) | 541.909 transações reais (UK) | Saúde financeira, sazonalidade, devoluções, geografia |
| [03-ecommerce-1m](./03-ecommerce-1m/) | 1.000.123 transações (sintético, global) | KPIs, análises temporais, sazonalidade, perfil do cliente |
| [04-credit-card-fraud](./04-credit-card-fraud/) | 10.000 transações (sintético) | Taxa de fraude por horário, valor, categoria e sinais de risco |

---

## Projetos

### 01-ecommerce-basico

Análise exploratória de **1.000 pedidos** de um e-commerce simulado, inspirado no dataset [Online Retail](https://www.kaggle.com/datasets/ertugrulesol/online-retail-data).

**O que é analisado:**
- Carregamento e limpeza de dados
- KPIs e tendências de vendas
- Perfil demográfico dos clientes
- Satisfação e análise de reviews
- Segmentação de clientes via RFM + K-Means Clustering
- Modelo de regressão linear para previsão de satisfação (resultado negativo, reportado como tal)

[Ver mais detalhes em 01-ecommerce-basico/README.md](./01-ecommerce-basico/README.md)

---

### 02-ecommerce-uk

Análise exploratória de **541.909 transações** de uma loja online britânica de presentes (dezembro 2010 — dezembro 2011).

**KPIs Destacados:**

| KPI | Valor |
|-----|-------|
| Receita Líquida | ~£9,7M |
| Receita Bruta | ~£10,6M |
| Perda com Devoluções | ~£896K (8,4%) |
| Ticket Médio (por fatura) | ~£514 |
| Transações Positivas | 531.285 |
| Clientes Ativos | 4.339 |
| ARPU (líquida) | ~£2.247 |

[Ver mais detalhes em 02-ecommerce-uk/README.md](./02-ecommerce-uk/README.md)

---

### 03-ecommerce-1m

Análise exploratória de **1.000.123 transações** de uma loja de varejo global (fevereiro/2024 — fevereiro/2026, base sintética em escala).

**KPIs Destacados:**

| KPI | Valor |
|-----|-------|
| Receita Total | $403.3M |
| Lucro Total | $160.9M |
| Margem Média | 39.5% |
| Ticket Médio | $403.24 |
| Clientes Únicos | 991.945 |
| Devolvidos | ~10% |

[Ver mais detalhes em 03-ecommerce-1m/README.md](./03-ecommerce-1m/README.md)

---

### 04-credit-card-fraud

Análise exploratória de **10.000 transações** de cartões de crédito (base sintética), identificando quais variáveis mais discriminam fraudes de transações legítimas.

**KPIs Destacados:**

| KPI | Valor |
|-----|-------|
| Total de transações | 10.000 |
| Taxa de fraude | 1.51% (151) |
| Ticket médio | $175.95 |
| Ticket médio das fraudes | $216.18 (+23%) |
| Transações estrangeiras | 9.78% |
| Fraudes entre 0h–3h | 80% do total (taxa de 6–9%) |

[Ver mais detalhes em 04-credit-card-fraud/README.md](./04-credit-card-fraud/README.md)

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
|------------|-----|
| [pandas](https://pandas.pydata.org/) | Manipulação e transformação de dados |
| [numpy](https://numpy.org/) | Cálculos numéricos |
| [plotly](https://plotly.com/python/) | Gráficos interativos |
| [seaborn](https://seaborn.pydata.org/) | Visualizações estatísticas |
| [matplotlib](https://matplotlib.org/) | Gráficos complementares |
| [scikit-learn](https://scikit-learn.org/) | ML (clustering K-Means, regressão linear) |
| [scipy](https://scipy.org/) | Testes estatísticos |
| [jupyter](https://jupyter.org/) | Ambiente de desenvolvimento |

---

## Execução

Clone o repositório e instale as dependências:

```bash
pip install -r requirements.txt
```

Execute os notebooks no Jupyter:

```bash
jupyter notebook
```

Ou abra com VS Code usando a extensão Jupyter.

---

## Autor

| Plataforma | Link |
|------------|------|
| GitHub | [victorxavier01](https://github.com/victorxavier01) |
| LinkedIn | [Victor Xavier](https://www.linkedin.com/in/victor-xavier-89a339378/) |
| Medium | [medium.com/@lvsxmk23](https://medium.com/@lvsxmk23) |

---

## Licença

[MIT](LICENSE) — © 2026 Victor Xavier
