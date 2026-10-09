# Análise Exploratória de Carros
## Contexto

Este documento resume o estudo conceitual realizado a partir do notebook `Análise_Exploratória_de_Carros.ipynb`, um projeto prático de treinamento em Python para Data Science, com foco em Análise Exploratória de Dados (EDA) aplicada a uma base de anúncios de veículos usados.

A base trabalhada possui **15.411 linhas e 13 colunas**, sendo 6 categóricas e 7 numéricas, sem dados nulos, mas com 167 linhas duplicadas identificadas.

## Ferramentas e bibliotecas utilizadas

- **pandas** — leitura, limpeza e manipulação da base de dados (`read_csv`, `drop`, `rename`, `groupby`, `duplicated`, `nunique`, `info`).
- **numpy** — suporte a operações numéricas.
- **seaborn** — visualizações estatísticas (`kdeplot`, `countplot`, `heatmap`, `barplot`).
- **matplotlib** — customização e composição dos gráficos (`figure`, `subplot`, títulos, rótulos).
- **warnings** — supressão de avisos durante a geração dos gráficos.

## Etapas do processo

1. **Importação e inspeção inicial**
   Carregamento do CSV, visualização das primeiras e últimas linhas (`head`, `tail`) e exibição das colunas disponíveis.

2. **Tratamento de dados**
   - Remoção de coluna irrelevante (`Unnamed: 0`).
   - Verificação de dados nulos, duplicados e valores únicos por coluna.
   - Identificação e correção de inconsistências (ex.: veículos com `seats = 0`, corrigidos para 5).
   - Remoção de coluna redundante (`mileage`) e renomeação de coluna (`km_driven` → `MileAge`).

3. **Classificação de atributos**
   Separação automática das colunas em **numéricas** e **categóricas**, com base no tipo de dado (`dtype`).

4. **Análise Univariada**
   - Distribuição das variáveis numéricas com gráficos de densidade (`kdeplot`).
   - Frequência das variáveis categóricas com gráficos de contagem (`countplot`).

5. **Análise Multivariada**
   - **Correlação linear** entre variáveis numéricas, visualizada com `heatmap`.
   - **Análise bivariada**: preço médio de venda agrupado por tipo de combustível, com visualização em `barplot`.

## Principais conceitos aplicados

- **Data Cleaning**: tratamento de duplicados, valores inconsistentes e colunas redundantes.
- **Classificação de variáveis**: separação numérica vs. categórica como base para escolha do tipo de gráfico.
- **Análise Univariada**: entendimento da distribuição de cada variável isoladamente.
- **Análise Multivariada**: relação entre variáveis (correlação) e comparação de médias entre grupos (bivariada).
- **Visualização de dados** como ferramenta central de exploração, priorizando gráficos simples e diretos (densidade, contagem, mapa de calor e barras).
