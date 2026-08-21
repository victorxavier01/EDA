# EDA — Exploratory Data Analysis

Repositório com projetos de Análise Exploratória de Dados (EDA) usando Python e Jupyter Notebooks.

| Projeto | Dataset | Escopo |
|---------|---------|--------|
| [E_commerce](./E_commerce/) | 1.000 pedidos simulados | KPIs, RFM, K-Means, Regressão Linear |
| [E_commerce_2](./E_commerce_2/) | 541.909 transações reais (UK) | Saúde financeira, sazonalidade, devoluções, geografia |

---

## Projetos

### E_commerce

Análise exploratória de **1.000 pedidos** de um e-commerce simulado, inspirado no dataset [Online Retail](https://www.kaggle.com/datasets/ertugrulesol/online-retail-data).

**O que é analisado:**
- Carregamento e limpeza de dados
- KPIs e tendências de vendas
- Perfil demográfico dos clientes
- Satisfação e análise de reviews
- Segmentação de clientes via RFM + K-Means Clustering
- Modelo de regressão linear para previsão de receita

[Ver mais detalhes em E_commerce/README.md](./E_commerce/README.md)

---

### E_commerce_2

Análise exploratória de **541.909 transações** de uma loja online britânica de presentes (dezembro 2009 — dezembro 2011).

**KPIs Destacados:**

| KPI | Valor |
|-----|-------|
| Receita Líquida | ~£40M |
| Receita Bruta | ~£45M |
| Perda com Devoluções | ~£896K (8,4%) |
| Ticket Médio | ~£70 |
| Transações Positivas | ~500K |
| Clientes Ativos | ~4.339 |
| ARPU | ~£2.660 |

[Ver mais detalhes em E_commerce_2/README.md](./E_commerce_2/README.md)

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
