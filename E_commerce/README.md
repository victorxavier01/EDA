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

### 1. Carregamento e Limpeza

- Verificação e conversão de tipos de dados (`order_date` para datetime)
- Criação de features temporais e engenharia de features (`receita`, `mes`, `trimestre`, `dia-semana`, `faixa_etaria`)
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
- Nota média por categoria (sports & outdoors lidera com ~3.99)
- Relação entre preço e quantidade por categoria
- **Conclusão**: notas consistentes entre categorias

### 5. Segmentacao (RFM + Clustering)

- **RFM Analysis**: Calcula Recency, Frequency e Monetary para cada cliente
- **K-Means Clustering**: Elbow method para seleção de K=4 clusters ótimos
- **Regressao Linear**: Modelo para prever receita a partir de preço e quantidade (split 80/20)
- Visualizações: scatter plot, barras de spend, distribuição de clusters

### Principal Insights

1. **Eletronicos é a categoria mais rentável**, merecendo mais investimentos em estoque e marketing
2. **Satisfacao do cliente em nivel moderado** (~3.5/5), com oportunidades de melhoria
3. **Segmentacao RFM permite marketing direcionado** com 4 perfis de clientes identificados

### Performance do Modelo

O modelo de regressao linear para previsao de receita apresentou metricas completas de avaliacao (R² e RMSE) calculadas no split de teste (20% dos dados).

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
