# 📊 Sales Report - Projeto de Data Analytics com Power BI

## 📌 Descrição

Este projeto foi desenvolvido com o objetivo de explorar dados de vendas utilizando o Power BI, aplicando conceitos de modelagem de dados, DAX e design interativo.

O relatório foi estruturado para permitir uma análise progressiva, saindo de uma visão geral até análises mais detalhadas sobre desempenho de produtos, países e comportamento ao longo do tempo, evoluindo para uma abordagem dinâmica com o uso de parâmetros.

A base utilizada neste projeto foi disponibilizada pela professora no repositório:

🔗 https://github.com/julianazanelatto/power_bi_analyst

---

## 🎯 Objetivo

* Criar um dashboard interativo e intuitivo
* Desenvolver medidas em DAX
* Explorar diferentes visuais analíticos
* Gerar insights a partir dos dados
* Implementar análise dinâmica com parâmetros

---

## 🗂️ Estrutura do Relatório

O projeto foi organizado em **5 páginas**, sendo:

---

### 📄 Página 1 — Home Page

Prepara o usuário para exploração do relatório.

---

### 📄 Página 2 — Visão Geral

Apresenta os principais indicadores do negócio:

* Total de Vendas
* Total de Unidades Vendidas
* Total de Descontos
* Total de Lucro
* Total Bruto

Além disso:

* Evolução de vendas ao longo do tempo
* Análise por segmento
* Vendas por produto
* Distribuição geográfica (Treemap por país)

---

### 📄 Página 3 — Detalhes de Vendas: Análise Temporal e Distribuição

Focada em explorar o comportamento dos dados:

* Vendas por semestre
* Lucro por trimestre
* Histograma de unidades vendidas (distribuição)
* Ranking de produtos por volume

Recursos adicionais:

* Alternância entre visualização por **semestre e mês**
* Tabela analítica com detalhamento trimestral

---

### 📄 Página 4 — Detalhes de Vendas: Análise de Desempenho de Vendas

Análise aprofundada de performance:

* 🔝 Top 3 produtos mais vendidos
* 🌍 Máximo vendido por país
* 📊 Top 3 produtos por país
* 🔵 Gráfico de dispersão (Unidades vendidas vs Vendas por mês)
* 📉 Relação entre volume e receita

---

### 📄 Página 5 — Análise Dinâmica de Performance Financeira

Página interativa criada com o uso de parâmetros, permitindo maior flexibilidade na exploração dos dados.

Funcionalidades:

* Seleção dinâmica de dimensões:

  * Country
  * Product
  * Segment

* Alternância entre métricas:

  * Total Sales
  * Total Profit
  * Total Units Sold

* Análise temporal por mês e ano, evitando agregações indevidas entre períodos

Visualizações:

* Gráfico de barras (categoria dinâmica)
* Gráfico de linha (métricas ao longo do tempo)

Essa página foi construída com foco em storytelling, permitindo ao usuário explorar diferentes perspectivas do negócio de forma interativa.

---

## 📊 Principais Visuais Utilizados

* 📈 Gráfico de área → Evolução temporal das vendas
* 📊 Gráfico de barras → Comparação entre categorias
* 🔵 Gráfico de dispersão → Relação entre métricas
* 🟩 Treemap → Distribuição geográfica
* 📦 Gráfico empilhado → Participação dos TOP 3 produtos
* 📊 Histograma → Distribuição de unidades vendidas
* 📉 Gráfico de linha → Evolução dinâmica de métricas

---

## 🧮 Medidas DAX

Exemplos de medidas utilizadas:

```DAX
Total Sales = SUM(Financials[Sales])

Total Profit = SUM(Financials[Profit])

Total Units Sold = SUM(Financials[Units Sold])

Top 3 Sales Total = CALCULATE([Total Sales], TOPN(3, ALL(Financials[Product]), [Total Sales], DESC))

Top 3 Product = IF([Rank Product] <= 3, [Total Sales])
```

---

## 🧩 Modelagem de Dados

Foi implementado um modelo dimensional simplificado, com a separação da dimensão de tempo (Calendar), permitindo análises temporais mais eficientes.

* Tabela fato: `Financials`
* Tabela dimensão: `Calendar`

A tabela calendário foi enriquecida com:

* Ano
* Dia da semana
* Número da semana
* Número do mês
* Nome do mês
* Nome do semestre

---

## 🎛️ Análise Dinâmica com Parâmetros

Foi implementada uma nova abordagem de análise utilizando parâmetros de campos no Power BI, permitindo:

* Alternância dinâmica entre dimensões de análise
* Troca interativa de métricas financeiras
* Exploração personalizada dos dados

Essa abordagem proporciona uma experiência mais analítica e próxima de cenários reais de negócio.

---

## 🔍 Análises Desenvolvidas

### 📈 Análise Temporal

Permite acompanhar a evolução das vendas e identificar sazonalidades.

### 🔵 Análise de Dispersão

O gráfico de dispersão relaciona:

* Unidades vendidas (volume)
* Vendas (receita)

Cada ponto representa um período, permitindo identificar padrões de desempenho.

### 🧠 Análise de Cluster (visual)

Mesmo sem a utilização de clusterização automática, foi possível identificar agrupamentos visuais nos dados a partir da relação entre unidades vendidas e vendas por mês.

---

## 🏆 Principais Insights

* Existem diferenças relevantes de desempenho entre países
* Alguns períodos apresentam maior eficiência de vendas
* A relação entre volume e receita varia conforme o produto

---

## 🔄 Evolução do Projeto

Este projeto foi expandido com a criação de uma nova página de análise dinâmica, incorporando parâmetros de campos para permitir maior interatividade e flexibilidade na exploração dos dados.

---

## 📎 Arquivo do Projeto

O relatório foi exportado em formato `.pbix` e também disponibilizado como imagem para visualização.

---

## 🚀 Conclusão

O projeto demonstra como o Power BI pode ser utilizado para transformar dados em insights estratégicos, evoluindo de análises descritivas para uma abordagem dinâmica e interativa.

A adição de parâmetros amplia a capacidade analítica do relatório, permitindo maior flexibilidade na exploração dos dados e melhor suporte à tomada de decisão.

---

## 🛠️ Ferramentas Utilizadas

* Power BI
* DAX (Data Analysis Expressions)
* Modelagem Dimensional Simplificada

---

## 👩‍💻 Autora

Projeto desenvolvido por **Elaine Marques** como parte do desafio de Power BI.
