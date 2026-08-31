# EDA: E-Commerce Simulado

Análise exploratória de **1000 pedidos de um e-commerce simulado**.

**Dataset**: [Kaggle](https://www.kaggle.com/datasets/ertugrulesol/online-retail-data)

---

## Sumário

- [Projeto](#projeto)
- [Dados](#dados)
- [Tecnologias](#tecnologias)
- [Resultados e Insights](#resultados-e-insights)
- [Execução](#execução)
- [Autor](#autor)

---

## Projeto

Este projeto realiza uma análise dos dados de vendas de e-commerce, desde limpeza e preparação até a modelagem preditiva e segmentação de clientes.

### Objetivos

- Entender o faturamento da empresa e evolução ao longo do tempo
- Analisar o perfil demográfico, gênero, faixa etária e localização
- Avaliar a satisfação do cliente e suas correlações
- Segmentar os clientes para campanhas de marketing direcionadas

## Dados

O dataset contem **1000 pedidos** com 13 colunas originais.

### Colunas

| Coluna | Descrição |
|--------|-----------|
| `customer_id` | ID único do cliente |
| `order_date` | Data do pedido |
| `product_id` | ID do produto |
| `category_id` | ID da categoria |
| `category_name` | Nome da categoria |
| `product_name` | Nome do produto |
| `quantity` | Quantidade vendida |
| `price` | Preço unitário |
| `payment_method` | Forma de pagamento |
| `city` | Cidade do cliente |
| `review_score` | Nota de avaliação (1-5) |
| `gender` | Gênero do cliente |
| `age` | Idade do cliente |


### Categorias de produtos

1. Electronics
2. Sports & Outdoors
3. Books & Stationery
4. Home & Living
5. Fashion

### Formas de pagamento

1. Credit Card
2. Cash on Delivery
3. Bank Transfer

---

## Tecnologias

| Tecnologia | Uso |
|------------|-----|
| **pandas** | Manipulação e análise de dados |
| **numpy** | Operações numéricas |
| **plotly** | Visualizações interativas |
| **seaborn** | Visualizações estatísticas |
| **matplotlib** | Visualizações estáticas |
| **scikit-learn** | Clustering K-Means e Regressão Linear |
| **scipy** | Métodos estatísticos |
| **jupyter** | Ambiente de desenvolvimento |

---

## Metodologia

### 1. Carregamento e Limpeza

- Verificação e conversão de tipos de dados (`order_date` para datetime)
- Criação de features temporais e engenharia de features (`receita`, `mes`, `trimestre`, `faixa_etaria`)
- Tratamento de valores (mediana para `review_score`, "Desconhecido" para `gender`)

### 2. KPIs e Tendencias

- KPIs calculados: receita total, ticket médio, total de pedidos, média de reviews, clientes únicos
- Evolução da receita mensal (gráfico de linha)
- Receita por categoria de produto (gráfico de barras)
- Distribuição por forma de pagamento (gráfico de pizza)

### 3. Perfil Demográfico

- Distribuição por gênero (gráfico de pizza)
- Distribuição por faixa etária (gráfico de barras)
- **Conclusão**: distribuição homogênea entre gêneros e faixas etárias

### 4. Satisfacao e Review

- Histograma da distribuição de notas
- Nota média por categoria (Sports & Outdoors lidera com ~4.07)
- Relação entre preço e quantidade por categoria
- **Conclusão**: notas consistentes entre categorias, com média geral próxima de ~4.0/5

### 5. Segmentacao (RFM + Clustering)

- **RFM Analysis**: Calcula Recency, Frequency e Monetary para cada cliente (cada cliente tem exatamente 1 pedido nesta base, então Frequency = 1 para todos e a segmentação fica efetivamente em Recência + Monetário)
- **K-Means Clustering**: Elbow method para seleção de K=4 clusters
- **Regressão Linear**: Modelo para prever satisfação (`review_score`) a partir de preço e quantidade (split 80/20) — R² ≈ 0,44%
- Visualizações: scatter plot, barras de spend, distribuição de clusters

### Principal Insights

1. **Electronics é a categoria mais rentável**, merecendo mais investimentos em estoque e marketing
2. **Satisfação do cliente em bom nível** (~4.0/5), com notas consistentes entre categorias
3. **Preço e quantidade não explicam a satisfação** (R² ≈ 0): em dados reais, investigaríamos outras variáveis (entrega, atendimento, produto)
4. **Segmentação por Recência + Monetário permite marketing direcionado** com 4 perfis de clientes identificados

### Performance do Modelo

O modelo de regressão linear para previsão de satisfação apresentou **R² de 0.44%** e **RMSE de 1.10 pontos** (escala 1-5), calculados no split de teste (20% dos dados). O R² próximo de zero indica que preço e quantidade não explicam a variação da satisfação nesta base — resultado negativo, reportado como tal (ver seção 5 do notebook).

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

Nota: Este projeto utiliza um dataset sintético gerado artificialmente. As features apresentam valores semelhantes e os insights são limitados pela natureza dos dados. Para análise com dados reais, recomenda-se expandir o dataset e explorar features mais diversificadas.
