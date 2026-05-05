# Relatório Técnico — Predição de Risco de Câncer de Colo do Útero

---

## 1. Introdução

Este projeto tem como objetivo analisar fatores de risco relacionados ao câncer de colo do útero utilizando técnicas de análise de dados e Machine Learning.

A partir de um dataset contendo informações clínicas e comportamentais de pacientes, foram realizadas etapas de análise exploratória, tratamento de dados, construção de modelos preditivos e interpretação dos resultados.

O foco principal foi identificar padrões nos dados e avaliar a capacidade dos modelos em prever diagnósticos positivos.

---

## 2. Análise Exploratória de Dados (EDA)

A análise exploratória foi conduzida com o objetivo de entender melhor o comportamento das variáveis e identificar possíveis padrões.

Inicialmente, foi analisada a distribuição da variável target (Biopsy), onde foi possível observar um desbalanceamento entre as classes, com maior número de casos negativos. Esse ponto é importante, pois pode influenciar o desempenho dos modelos.

A variável idade também foi analisada, sendo possível observar a concentração das pacientes em determinadas faixas etárias. Comparações entre pacientes com diagnóstico positivo e negativo foram feitas utilizando boxplots, permitindo identificar possíveis diferenças entre os grupos.

Outras variáveis analisadas incluíram:
- Tabagismo
- Número de parceiros sexuais
- Histórico de doenças sexualmente transmissáveis (DSTs)

Essas análises foram feitas utilizando diferentes tipos de gráficos, como histogramas, boxplots, violinplots e gráficos de contagem.

Também foi gerado um mapa de correlação entre as variáveis numéricas, permitindo identificar possíveis relações entre elas.

De forma geral, a EDA ajudou a levantar hipóteses sobre fatores que podem estar associados ao risco de câncer de colo do útero.

---

## 3. Estratégias de Pré-processamento

Durante a etapa de preparação dos dados, foi realizada uma análise detalhada dos valores ausentes.

Foi identificado que algumas colunas apresentavam mais de 90% de valores nulos, como aquelas relacionadas ao tempo desde diagnóstico de DSTs. Essas colunas foram removidas, pois a imputação poderia introduzir viés significativo.

Para as demais variáveis com valores ausentes, foi utilizada imputação pela mediana, por ser uma abordagem robusta e menos sensível a outliers.

Em seguida, os dados foram separados entre variáveis independentes (features) e variável target.

Também foi realizada a divisão dos dados em conjunto de treino e teste, permitindo avaliar a capacidade de generalização dos modelos.

Para o modelo de Regressão Logística, foi aplicada a padronização dos dados utilizando StandardScaler, garantindo que todas as variáveis estivessem na mesma escala.

---

## 4. Modelos Utilizados

### 4.1 Regressão Logística

A Regressão Logística foi utilizada como primeiro modelo, pois é amplamente aplicada em problemas de classificação binária.

Esse modelo estima a probabilidade de uma instância pertencer à classe positiva, sendo bastante interpretável e adequado para aplicações na área da saúde.

---

### 4.2 Árvore de Decisão

A Árvore de Decisão também foi utilizada por sua facilidade de interpretação.

Esse modelo cria regras de decisão baseadas nas variáveis do dataset, permitindo entender de forma mais intuitiva como as previsões são feitas.

Além disso, a árvore permite identificar quais variáveis são mais relevantes para o modelo.

---

## 5. Resultados e Avaliação

Os modelos foram avaliados utilizando métricas como acurácia, recall e F1-score.

O recall foi considerado a métrica mais importante neste projeto, pois mede a capacidade do modelo de identificar corretamente os casos positivos.

Em aplicações médicas, reduzir falsos negativos é essencial, já que esse tipo de erro representa pacientes doentes que não foram identificados pelo modelo.

A matriz de confusão foi utilizada para analisar o desempenho de forma mais detalhada, permitindo visualizar os acertos e erros dos modelos.

A análise mostrou que ambos os modelos apresentaram desempenho satisfatório, com diferenças relacionadas à interpretabilidade e comportamento das previsões.

---

## 6. Interpretação dos Resultados (SHAP)

Para aumentar a transparência dos modelos, foi utilizada a biblioteca SHAP.

Essa técnica permite identificar o impacto de cada variável nas previsões, mostrando quais fatores mais influenciam o modelo.

A análise de explicabilidade contribuiu para entender melhor o comportamento dos modelos e reforçar a confiança nos resultados obtidos.

---

## 7. Conclusão

O projeto demonstrou como técnicas de análise de dados e Machine Learning podem ser aplicadas para identificar padrões e analisar riscos na área da saúde.

Os modelos desenvolvidos apresentaram desempenho satisfatório, com destaque para a importância do recall na identificação de casos positivos.

Além disso, o uso de técnicas de explicabilidade permitiu compreender melhor as decisões dos modelos.

Por fim, é importante destacar que os modelos não substituem avaliação médica, mas podem ser utilizados como ferramentas de apoio à tomada de decisão.
