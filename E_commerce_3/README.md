# EDA: E-Commerce com 1 milhão de dados

Análise exploratória de dados com mais de **1 milhão de transações** de uma loja de varejo global. Os dados vão de **fevereiro/2024 a fevereiro/2026**.
É importante lembrar que é uma base de dados **sintética**, isto é, dados gerados artificialmente para estudo/prática de análise de dados.

**Importante**: Como o arquivo .csv excede os 100mbs, então não foi possível envia-lo ao GitHub. Por esse motivo, os dados deverão ser baixados manualmente!

**Dataset**: [Kaggle](https://www.kaggle.com/datasets/akrambelha/global-e-commerce-dataset-1m-records-20242026)

## Sumário

- [Visão Geral](#vis%C3%A3o-geral)
- [Resultados Principais](#resultados-principais)
- [Dados](#dados)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Execução](#execu%C3%A7%C3%A3o)
- [Autor](#autor)
- [Fontes](#fontes)

---

## Visão Geral

Investigação exploratória de uma base global de e-commerce:

- **KPIs gerais** (receita, lucro, ticket médio, margem, devoluções)
- **Análises temporais** (receita e lucro por ano, sazonalidade mensal, dias úteis vs fim de semana)
- **Perfil do cliente** (gênero, faixa etária, segmento, cidades)
- **Geração de insights e recomendações**

---

## Resultados Principais

| KPI | Valor |
| --- | --- |
| Transações | 1.000.123 |
| Clientes Únicos | 991.945 |
| Produtos Únicos | 753.516 |
| Países | 10 |
| Receita Total | $403.3M |
| Lucro Total | $160.9M |
| Margem Média | 39.5% |
| Ticket Médio | $403.24 |
| Avaliação Média | 3.0/5 |
| Dias de Entrega (média) | 7.5 |
| Devolvidos | ~10% |

---

## Dados

Base sintética com **1.000.123 linhas** e **62 colunas**, agrupadas em:

| Grupo | Colunas |
| --- | --- |
| Pedido | `order_id`, `order_date`, `order_year`, `order_month`, `order_day`, `order_hour`, `order_minute`, `order_second`, `is_weekend`, `order_status`, `return_reason` |
| Cliente | `customer_id`, `customer_name`, `gender`, `age`, `customer_segment`, `country`, `city`, `customer_loyalty_score`, `total_orders_by_customer`, `account_creation_date` |
| Produto | `product_id`, `product_name`, `category`, `sub_category`, `brand`, `product_rating_avg`, `product_reviews_count`, `stock_quantity` |
| Financeiro | `unit_price_usd`, `quantity`, `discount_percent`, `discount_amount_usd`, `total_price_usd`, `cost_usd`, `profit_usd`, `tax_usd`, `currency`, `profit_margin_percent` |
| Pagamento/Entrega | `payment_method`, `payment_status`, `installment_plan`, `shipping_method`, `shipping_cost_usd`, `delivery_days`, `shipping_country`, `warehouse_location`, `delivery_status` |
| Comportamento | `rating`, `review_sentiment`, `customer_feedback`, `coupon_used`, `coupon_code`, `campaign_source`, `device_type`, `traffic_source`, `session_duration_minutes`, `pages_visited`, `abandoned_cart_before`, `fraud_risk_score`, `order_priority`, `support_ticket_created` |

---

## Tecnologias Utilizadas

| Tecnologia | Uso |
| --- | --- |
| **Pandas** | Manipulação e transformação de dados |
| **NumPy** | Cálculos numéricos |
| **Plotly** | Gráficos interativos |
| **Matplotlib** | Gráficos complementares (cards de KPIs) |
| **Jupyter** | Ambiente de desenvolvimento |

## Execução

1. Baixe o `data.csv` no [Kaggle](https://www.kaggle.com/datasets/akrambelha/global-e-commerce-dataset-1m-records-20242026) e coloque na pasta do projeto.
2. Instale as dependências: `pip install pandas numpy plotly matplotlib`
3. Execute: `jupyter notebook eda_ecommerce_3.ipynb` ou abra no VS Code com a extensão Jupyter.

## Autor

**Github**: [victorxavier01](https://github.com/victorxavier01)

**LinkedIn**: [Victor Xavier](https://www.linkedin.com/in/victor-xavier-89a339378/)

**Medium**: [medium.com/@lvsxmk23](https://medium.com/@lvsxmk23)

## Fontes

- [Global E-Commerce Dataset — 1M records (2024-2026)](https://www.kaggle.com/datasets/akrambelha/global-e-commerce-dataset-1m-records-20242026) — Kaggle (dataset sintético)
