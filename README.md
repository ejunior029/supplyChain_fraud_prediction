# Detecção de Operações Fraudulentas - DataCo Global

## Descrição do Projeto
Este repositório contém todas as análises e modelos desenvolvidos para o projeto de análise de dados da DataCo Global, uma renomada empresa global do setor de supply chain. O objetivo foi explorar a base de dados de operações da empresa para extrair insights valiosos, identificar pontos de melhoria e prever tendências futuras.

## Pré-Processamento Dos Dados
- Foram consideradas as vendas realizadas somente até setembro/2017 devido a um possível problema operacional na base, que fez com que após esta data apenas vendas a novos clientes fossem consideradas, desconsiderando os clientes antigos. Além disso, os clientes novos compravam apenas uma vez. Sendo assim, para não trabalhar com um conjunto de dados com uma possível interferência, foi realizado este filtro.
- Foram removidas todas as variáveis não entendidas como importantes para o modelo.
- Foi criado um Pipeline para fazer o pré-processamento automaticamente no conjunto de testes, de tal forma que considerasse:
  - O tratamento de variáveis categóricas com o CatBoostEncoder
  - O preenchimento de valores faltantes para variáveis categóricas com a moda
  - O preenchimento de valores faltantes para variáveis numéricas com a mediana
    
## Métricas Obtidas Pelo Modelo

## 💡Métricas De Negócio
<h3> Economia Significativa:</h3> Implementação do modelo de detecção de fraude resultaria em uma economia estimada de $1.09 milhão.
<h3> Desafios Identificados:</h3> A análise revelou uma perda potencial de $24 mil devido a operações fraudulentas não detectadas.
<h3> Impacto Líquido:</h3> Com as melhorias propostas, a economia total projetada é de aproximadamente $1.06 milhão.


