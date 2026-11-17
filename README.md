# Estudo de Machine Learning Para Identificar Fatores Mais Relevantes Para Ocorrência de Doenças Cardíacas

Projeto de estudo de classificação binária (com ou sem doença cardíaca) usando **XGBoost**, com análise exploratória dos dados e identificação das variáveis mais relevantes para a previsão.

## Dataset

- Dados clínicos de pacientes (idade, sexo, tipo de dor no peito, pressão arterial, colesterol, frequência cardíaca máxima, entre outros).
- Variável alvo: `target` (0 = sem doença, 1 = com doença).
- Fonte: Heart Disease (UCI Machine Learning Repository). https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset
- Foi removida 723 linhas duplicadas antes da modelagem.

## Metodologia

1. Análise exploratória: valores ausentes, correlações, proporção de classes e gráficos.
2. Divisão em treino (80%) e teste (20%).
3. Treino de um modelo XGBoost com todas as variáveis.
4. Extração da importância das variáveis e seleção das 10 mais relevantes.
5. Retreino do modelo apenas com essas 10 variáveis.
6. Avaliação com validação cruzada (5 folds), matriz de confusão e `classification_report`.

## Resultados

- Validação cruzada (5 folds), MÉTRICA: **84,1% (± 2,3%)**
- Acurácia no teste: XX%
- Recall da classe "com doença": XX%
- Precision da classe "com doença": XX%

Variáveis mais importantes: LISTA DAS 3 A 5 PRIMEIRAS DE `top_variables`.

## Tecnologias

Python, pandas, NumPy, scikit-learn, XGBoost, Matplotlib, Seaborn.

## Limitações

- O dataset é pequeno (~300 pacientes), então os resultados podem variar com outra divisão dos dados.
- O modelo tem fins educacionais e não substitui avaliação médica.
