# Estudo de Malha Logística — Altenburg

Projeto de análise de dados e diagnóstico logístico desenvolvido para suportar o estudo de malha da Altenburg, com foco em demanda geográfica, custos de frete, faturamento, cubagem, volume expedido e identificação de oportunidades de redesenho da operação logística.

## Objetivo

Este projeto tem como objetivo analisar a operação logística atual da Altenburg a partir de dados transacionais e geográficos, gerando insumos para responder perguntas como:

- Onde está concentrada a demanda da operação
- Quais regiões e UFs concentram maior faturamento, volume e custo logístico
- Qual é a relação entre frete, faturamento, cubagem e quantidade expedida
- Onde existem sinais de ineficiência logística na malha atual
- Quais regiões podem justificar aprofundamento em estudos de redistribuição de estoque, novos hubs ou revisão do modelo operacional

## Escopo analítico

A análise considera principalmente:

- Volume vendido por cidade, estado e região
- Faturamento por geografia
- Frete total e frete percentual sobre faturamento
- Cubagem expedida
- Quantidade por pedido/NF
- Consolidação correta da granularidade para evitar duplicidade de frete
- Comparativos por região, UF, cliente e família de produto
- Base para construção de cenários futuros de malha logística

## Estrutura do projeto

```bash
.
├── data/
│   ├── raw/                  # Bases originais extraídas
│   ├── processed/            # Bases tratadas e consolidadas
│   └── external/             # Dados auxiliares, mapas, referências
│
├── notebooks/
│   ├── 01_entendimento_dados.ipynb
│   ├── 02_limpeza_tratamento.ipynb
│   ├── 03_analise_exploratoria.ipynb
│   ├── 04_analise_geografica.ipynb
│   ├── 05_frete_faturamento_regiao.ipynb
│   └── 06_insights_malha_logistica.ipynb
│
├── src/
│   ├── preprocessing.py      # Funções de limpeza e transformação
│   ├── agregacoes.py         # Consolidações por NF, pedido, UF e região
│   ├── metricas.py           # KPIs logísticos e financeiros
│   └── visualizacoes.py      # Funções de gráficos e tabelas
│
├── outputs/
│   ├── graficos/
│   ├── tabelas/
│   └── relatorios/
│
├── dashboard/
│   └── looker_studio/        # Referências da modelagem das fontes
│
├── requirements.txt
└── README.md# data_science
