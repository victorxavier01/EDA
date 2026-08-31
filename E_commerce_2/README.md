# EDA: E-commerce UK

Análise exploratória de dados com **541.909 transações** de uma loja de varejo online britânica. O dataset abrange o período de dezembro de 2010 a dezembro de 2011.

**Dataset**: []()

## Sumário

- Visão Geral (#-visão-geral)
- Resultados Principais (#-resultados-principais)
- Dados
- Tecnologias Utilizadas (#-tecnologias-utilizadas)
- Execução (#-execução)
- Seções da Análise (#-seções-da-análise)
- Fontes (#-fontes)

---

## Visão Geral

Investigação de comportamento de compra de uma loja online de vendas de presentes britânica:

- **Saúde financeira** da empresa (receita bruta, líquida, ticket médio)
- **Sazonalidade** das vendas ao longo do tempo
- **Devoluções e cancelamentos**
- **Comportamento geográfica**
- **Geração de insights**

---

## Resultados Principais

| KPI | Valor |
| --- | --- |
| Receita Líquida | ~£40M |
| Receita Bruta | ~£45M |
| Perda com Devoluções | ~£896K (8,4% da receita bruta) |
| Ticket Médio | ~£70 |
| Transações Positivas | ~500K |
| Clientes Ativos | ~4.339 |
| ARPU | ~£2.660 |
| Produtos Únicos | ~4.070 |
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

---

## Técnologias Utilizados

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

jupyter notebook e_commerce.ipynb
Ou utilize VS Code com a extensao Jupyter para uma experiéncia integrada.

## Autor

**Github**: [Github](https://github.com/victorxavier01)

**LinkedIn**: [LinkedIn](https://www.linkedin.com/in/victor-xavier-89a339378/)

**Medium**: [Medium](https://medium.com/@lvsxmk23)




