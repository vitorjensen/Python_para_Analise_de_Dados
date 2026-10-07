# Análise Exploratória de Danos Informados (CEMADEN)

Análise exploratória de dados (EDA) feita em Python sobre a base **Danos Informados** do CEMADEN, que reúne ocorrências de desastres e calamidades registradas nas regiões do Brasil ao longo de 2024, incluindo eventos com mortes ou feridos.

O objetivo do projeto é praticar Python para Data Science, cobrindo desde a limpeza dos dados até a análise univariada e a correlação entre variáveis.

## O que tem no notebook

1. **Tratamento dos dados**
   - Remoção de colunas não utilizadas (de 53 para 14 colunas)
   - Substituição de valores "0" por nulos
   - Contagem de valores nulos e duplicados

2. **Análise exploratória**
   - Identificação das categorias de desastres (coluna COBRADE)
   - Separação entre colunas categóricas e numéricas
   - Análise univariada das colunas categóricas (UF, Status, datas e municípios mais recorrentes)
   - Análise univariada das colunas numéricas (distribuição via KDE plot)
   - Matriz de correlação linear entre as variáveis numéricas

## Principais resultados

- Total de registros: 6.032 linhas
- 49 categorias distintas de desastres
- 8 colunas categóricas e 6 numéricas
- Nenhum registro duplicado
- As colunas de "Danos Humanos" (DH) se mostraram relevantes para entender a gravidade de um desastre e a vulnerabilidade de cada localidade

## Ferramentas utilizadas

- **pandas** e **numpy** — leitura, limpeza e manipulação dos dados
- **matplotlib** e **seaborn** — visualização (countplot, barplot, kdeplot)
- Google Colab como ambiente de desenvolvimento
