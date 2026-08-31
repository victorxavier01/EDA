# EDA: E-commerce UK

Análise exploratória de dados com **541.909 transações** de uma loja de varejo online britânica. O dataset abrange o período de dezembro de 2010 a dezembro de 2011.

**Dataset**: [Online Retail — UCI ML Repository](https://archive.ics.uci.edu/dataset/502/online+retail)

## Sumário

- [Visão Geral](#vis%C3%A3o-geral)
- [Resultados Principais](#resultados-principais)
- [Dados](#dados)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Execução](#execu%C3%A7%C3%A3o)
- [Autor](#autor)

---

## Visão Geral

Investigação de comportamento de compra de uma loja online de vendas de presentes britânica:

- **Saúde financeira** da empresa (receita bruta, líquida, ticket médio)
- **Sazonalidade** das vendas ao longo do tempo
- **Devoluções e cancelamentos**
- **Comportamento geográfico**
- **Geração de insights**

---

## Resultados Principais

| KPI | Valor |
| --- | --- |
| Receita Líquida | ~£9,7M |
| Receita Bruta | ~£10,6M |
| Perda com Devoluções | ~£896K (8,4% da receita bruta) |
| Ticket Médio (por fatura) | ~£514 |
| Transações Positivas | 531.285 |
| Clientes Ativos | 4.339 |
| ARPU (líquida) | ~£2.247 |
| Produtos Únicos | ~3.941 |
| Países Atendidos | 38 |

---

## Dados

| Coluna | Tipo | Descrição |
| --- | --- | --- |
| `InvoiceNo` | String | Número da nota fiscal |
| `StockCode` | String | Código do produto |
| `Description` | String | Descrição do produto |
| `Quantity` | Integer | Quantidade vendida/devolvida |
| `InvoiceDate` | Datetime | Data da fatura |
| `UnitPrice` | Float | Preço unitário (£) |
| `CustomerID` | Float | ID do cliente (opcional) |
| `Country` | String | País de destino |

**Observações sobre os dados:**

- O arquivo é codificado em **ISO-8859-1** (levar em conta ao carregar: `encoding='ISO-8859-1'`).
- As datas de `InvoiceDate` vêm em formato **m/d/y** (ex.: `12/1/2010 8:26` = 1º de dezembro de 2010).
- **10.624 linhas** têm `Quantity` negativa — são devoluções/cancelamentos, tratadas separadamente na análise.

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
| --- | --- |
| **Pandas** | Manipulação e transformação de dados |
| **NumPy** | Cálculos numéricos |
| **Plotly** | Gráficos interativos |
| **Seaborn** | Visualizações estatísticas |
| **Matplotlib** | Gráficos complementares |
| **Scikit-learn** | Regressão linear |
| **SciPy** | Testes estatísticos |
| **Jupyter** | Ambiente de desenvolvimento |

## Execução

Instale as dependencias em `requirements.txt`:

```bash
pip install -r requirements.txt
```

### Como rodar

```bash
jupyter notebook eda_ecommerce_uk.ipynb
```

Ou utilize VS Code com a extensao Jupyter para uma experiéncia integrada.

## Autor

**Github**: [Github](https://github.com/victorxavier01)

**LinkedIn**: [LinkedIn](https://www.linkedin.com/in/victor-xavier-89a339378/)

**Medium**: [Medium](https://medium.com/@lvsxmk23)




