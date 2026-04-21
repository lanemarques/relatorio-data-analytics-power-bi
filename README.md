# 📊 Sales Report - Projeto de Data Analytics com Power BI

## 📌 Descrição

Este projeto foi desenvolvido com o objetivo de explorar dados de vendas utilizando o Power BI, aplicando conceitos de modelagem de dados, DAX e design interativos.

O relatório foi estruturado para permitir uma análise progressiva, saindo de uma visão geral até análises mais detalhadas sobre desempenho de produtos, países e comportamento ao longo do tempo.

A base utilizada neste projeto foi disponibilizada pela professora no repositório:

🔗 https://github.com/julianazanelatto/power_bi_analyst


---

## 🎯 Objetivo

* Criar um dashboard interativo e intuitivo
* Desenvolver medidas em DAX
* Explorar diferentes visuais analíticos
* Gerar insights a partir dos dados

---

## 🗂️ Estrutura do Relatório

O projeto foi organizado em **4 páginas**, sendo:


### 📄 Página 1 — Home Page

Prepara o usuário para exploração do relatório

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

## 📊 Principais Visuais Utilizados

* 📈 Gráfico de área → Evolução temporal das vendas
* 📊 Gráfico de Barras → Comparação entre categorias
* 🔵 Gráfico de Dispersão → Relação entre métricas
* 🟩 Treemap → Distribuição geográfica
* 📦 Gráfico Empilhado → Participação dos TOP 3 produtos
* 📊 Histograma → Distribuição de unidades vendidas

---

## 🧮 Medidas DAX

Exemplos de medidas utilizadas:

```DAX id="7j29sd"
Total Sales = SUM(Financials[Sales])

Total Profit = SUM(Financials[Profit])

Top 3 Sales Total = CALCULATE([Total Sales], TOPN(3, ALL(Financials[Product]), [Total Sales], DESC))

Top 3 Product = IF([Rank Product] <= 3, [Total Sales])
```

---

## 🧩  Modelagem de Dados utilizados:

Foi implementado um modelo dimensional simplificado, com a separação da dimensão de tempo (Calendar), permitindo análises temporais mais eficientes.

* Tabela fato: `Financials`
* Tabela dimensão: `Calendar`

A tabela calendário foi enriquecida com:

* Ano
* Dia da semana
* Número da semana
* Número do Mês
* Nome do mês
* Nome do Semestre 

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

Mesmo sem a utilização de clusterização automática, foi possível identificar agrupamentos visuais nos dados, a partir da relação entre unidades vendidas e vendas por mês.

---

## 🏆 Principais Insights

* Existem diferenças relevantes de desempenho entre países
* Alguns períodos apresentam maior eficiência de vendas
* A relação entre volume e receita varia conforme o produto

---

📎 Arquivo do Projeto

O relatório foi exportado em formato .pbix e também disponibilizado como imagem (.pdf) para visualização.

---

## 🚀 Conclusão

O projeto demonstra como o Power BI pode ser utilizado para transformar dados em insights estratégicos, combinando visualizações eficientes, modelagem adequada e análise de dados.

---

## 🛠️ Ferramentas Utilizadas

* Power BI
* DAX (Data Analysis Expressions)
* Modelagem Dimensional simplificada