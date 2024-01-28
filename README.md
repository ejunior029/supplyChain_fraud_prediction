# Detecção de Operações Fraudulentas - DataCo Global

## 🚀 Descrição do Projeto
Este repositório é o coração do projeto de analytics da DataCo Global, onde mergulhamos profundamente nos dados para desvendar as operações da empresa e otimizar seu desempenho. Nosso foco principal foi na detecção de fraudes, visando salvar a empresa de perdas significativas e impulsionar sua eficiência operacional.

## Pré-Processamento Dos Dados
- Foram consideradas as vendas realizadas somente até setembro/2017 devido a um possível problema operacional na base, que fez com que após esta data apenas vendas a novos clientes fossem consideradas, desconsiderando os clientes antigos. Além disso, os clientes novos compravam apenas uma vez. Sendo assim, para não trabalhar com um conjunto de dados com uma possível interferência, foi realizado este filtro.
- Foram removidas todas as variáveis não entendidas como importantes para o modelo.
- Foi criado um Pipeline para fazer o pré-processamento automaticamente no conjunto de testes, de tal forma que considerasse:
  - O tratamento de variáveis categóricas com o CatBoostEncoder
  - O preenchimento de valores faltantes para variáveis categóricas com a moda
  - O preenchimento de valores faltantes para variáveis numéricas com a mediana
 
## 🤖 Modelagem

Os dados foram divididos em 70% para treino e 30% para teste, sendo que são extremamente desbalanceados, conforme a Figura abaixo:

<img src="https://i.ibb.co/7zjpbkF/fraude.png">

Possuindo apenas 2,3% de operações fraudulentas. Além disso, foi construída uma função de validação cruzada estratificada (pois a base é desbalanceada), dividindo os dados em 5 folds. Com isso, foram obtidas 5 valores para cada métrica, sendo realizada a média para chegar à um único valor representativo.

## Métricas Obtidas Pelo Modelo
Neste projeto foram utilizados os seguintes modelos:

- LightGBM
- XGBoost
- CatBoost
- Balanced Random Forest

O XGboost obteve o melhor desempenho geral, apresentando:

- Média da ROC_AUC: 0.8933
- Média da Revocação: 0.9587
- Média da Medida-F1: 0.2058

Com isso, o XGBoost foi escolhido para identificar o quanto a DataCo Global poderia deixar de perder se possuísse um modelo antifraude para fazer a segurança de operações financeiras de pagamento dos clientes.

## 💡Métricas De Negócio
<h4> Economia Significativa:</h4> Implementação do modelo de detecção de fraude resultaria em uma economia estimada de $1.09 milhão.
<h4> Desafios Identificados:</h4> A análise revelou uma perda potencial de $24 mil devido a operações fraudulentas não detectadas.
<h4> Impacto Líquido:</h4> Com as melhorias propostas, a economia total projetada é de aproximadamente $1.06 milhão.


