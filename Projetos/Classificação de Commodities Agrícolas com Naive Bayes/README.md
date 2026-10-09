# Classificação de Commodities Agrícolas com Naive Bayes

## Objetivo

Analisar a variação mensal dos preços do **café** e da **soja** (dados do Cepea) e treinar um modelo de **Naive Bayes** para classificar, mês a mês, qual ativo seria a melhor opção de investimento: **Café**, **Soja** ou **Nenhum**.

## Principais pontos explorados

**1. Preparação e tratamento de dados**
- Junção de três bases (café, soja e dólar) com `merge` pela coluna de data.
- Conversão de datas e limpeza de valores numéricos em formato brasileiro (ponto de milhar e vírgula decimal).

**2. Análise de variáveis**
- Cálculo da variação percentual mensal de cada commodity com `pct_change`.
- Criação da variável alvo `Investe` a partir de uma regra de negócio comparando as variações.

**3. Análise exploratória**
- Gráficos de evolução de preços e de variação mensal.
- Comparativo anual das recomendações com `groupby`, `pivot` e `melt`, visualizado com seaborn.

**4. Machine learning**
- Classificação utilizando o modelo **Gaussian Naive Bayes** (scikit-learn) para variáveis contínuas.
- Divisão entre treino e teste com amostragem estratificada, preservando a proporção das classes.

**5. Pontos de Avaliação sobre o modelo**
- Acurácia, relatório de classificação (precisão, recall e F1) e **matriz de confusão**.
- Tabela de valores reais versus previstos, com análise dos erros do modelo.

## Ponto de atenção

A variável alvo foi criada a partir das mesmas variações usadas como entrada do modelo. Por isso, o modelo reproduz uma regra já definida e não prevê o comportamento futuro do mercado. O foco do projeto é didático: praticar o ciclo completo de tratamento, análise e classificação.

## Tecnologias

Python · pandas · numpy · matplotlib · seaborn · scikit-learn · Google Colab

