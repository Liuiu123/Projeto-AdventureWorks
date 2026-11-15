# Projeto AdventureWorks

Projeto de análise de dados e Business Intelligence desenvolvido com **Microsoft Power BI**, utilizando a base de dados AdventureWorks DW 2020.

O objetivo é explorar os dados comerciais da AdventureWorks por meio de indicadores de desempenho, análises temporais e visualizações interativas, permitindo acompanhar a evolução das vendas e compreender melhor sua distribuição por canais, regiões e categorias de produtos.

## Objetivos do projeto

- Desenvolver um dashboard interativo para análise do desempenho comercial.
- Construir indicadores de vendas, custos, lucratividade e ticket médio.
- Analisar a evolução das vendas ao longo do tempo.
- Comparar o desempenho mensal por meio de indicadores MoM (Month over Month).
- Explorar a distribuição geográfica das vendas.
- Aplicar conceitos de modelagem de dados, contexto de filtro e inteligência temporal com DAX.

## Ferramentas e tecnologias

- **Microsoft Power BI:** construção do dashboard e visualização dos dados.
- **DAX (Data Analysis Expressions):** desenvolvimento de medidas e indicadores.
- **AdventureWorks DW 2020:** base de dados utilizada no projeto.

## Estrutura do dashboard

O relatório foi organizado em três páginas:

### 1. Intro — Visão geral

Página inicial com uma visão panorâmica do desempenho comercial.

Principais elementos:
- Distribuição das vendas por canal.
- Total de vendas.
- Evolução mensal das vendas.
- Distribuição geográfica por país e região.
- Análise de estados, províncias e cidades.

### 2. Sales — Desempenho de vendas

Página dedicada à análise dos principais indicadores comerciais e financeiros.

Indicadores e análises:
- Total Sales.
- Total Quantity Sales.
- Total Orders.
- Average Ticket Size.
- Gross Profit.
- Sales YTD.
- Análise detalhada por pedido e categoria de produto.

### 3. MoM Variation — Variação mensal

Página dedicada à comparação do desempenho das vendas entre meses consecutivos.

Indicadores:
- Total Sales.
- Sales Previous Month.
- Sales MoM Variation.
- Sales MoM Growth %.

Essa página permite identificar períodos de crescimento e retração nas vendas, analisando tanto a variação monetária quanto a variação percentual.

## Principais medidas DAX

Algumas das medidas desenvolvidas durante o projeto:

**Total Sales**
```dax
Total Sales = SUM(Sales[Sales Amount])
```

**Total Cost**
```dax
Total Cost = SUM(Sales[Total Product Cost])
```

**Gross Profit**
```dax
Gross Profit = [Total Sales] - [Total Cost]
```

**Average Ticket Size**
```dax
Average Ticket Size =
DIVIDE([Total Sales], [Total Orders])
```

**Sales Previous Month**
```dax
Sales Previous Month =
CALCULATE(
    [Total Sales],
    DATEADD('Date'[Date], -1, MONTH)
)
```

**Sales MoM Variation**
```dax
Sales MoM Variation =
[Total Sales] - [Sales Previous Month]
```

**Sales MoM Growth %**
```dax
Sales MoM Growth % =
DIVIDE(
    [Sales MoM Variation],
    [Sales Previous Month]
)
```

## Conhecimentos aplicados

Ao longo do desenvolvimento, foram trabalhados conceitos importantes de análise de dados e Business Intelligence:

- Criação e utilização de medidas DAX.
- Agregações e indicadores financeiros.
- Inteligência temporal.
- Análise Month over Month (MoM).
- Cálculo de crescimento percentual.
- Utilização de dimensão calendário.
- Análise por diferentes dimensões comerciais e geográficas.
- Construção de relatórios interativos.

## Visualizações do projeto

As capturas de tela do dashboard serão disponibilizadas nesta seção.

| Página | Arquivo |
|---|---|
| Intro | `images/dashboard_intro.png` |
| Sales | `images/dashboard_sales.png` |
| MoM Variation | `images/dashboard_mom_variation.png` |

## Como visualizar o projeto

1. Baixe o arquivo `.pbix` disponível neste repositório.
2. Abra o arquivo utilizando o Microsoft Power BI Desktop.
3. Navegue pelas três páginas do relatório e explore os filtros e visualizações interativas.

## Considerações finais

Este projeto faz parte do desenvolvimento de um portfólio prático na área de Análise de Dados e Business Intelligence.

O trabalho busca demonstrar a aplicação de conhecimentos técnicos na construção de indicadores, análise de desempenho comercial e transformação de dados em informações úteis para apoiar a tomada de decisões.

---

**Desenvolvido como projeto de portfólio em Análise de Dados e Business Intelligence.**