# Predição de Preços de Ações usando Regressão Linear

Este projeto visa a predição de preços de fechamento da ação PETR4 utilizando um modelo de Regressão Linear implementado do zero, sem o uso de bibliotecas de machine learning como scikit-learn ou tensorflow. Também comparamos os resultados com o artigo "Cryptocurrency Price Prediction Using Linear Regression and Long Short-Term Memory (LSTM)", para discutir a viabilidade da regressão linear nesse cenário.

## Objetivo

O principal objetivo deste projeto é avaliar a eficácia da Regressão Linear na predição de preços de ações ao longo do tempo. Utilizamos o histórico da PETR4 e analisamos três escalas de tempo: dias, semanas e meses.

## Estrutura do Projeto

1. **Coleta de Dados**: Utilizamos a biblioteca `yfinance` para coletar os dados históricos da ação PETR4 entre 2020 e 2023.
   
2. **Análise e Pré-processamento**: Focamos no preço de fechamento da ação, criamos variáveis independentes (Dias, Semanas e Meses) e aplicamos pré-processamento para lidar com dados ausentes e padronizar os valores.
   
3. **Criação de Janelas Deslizantes**: Para treinar nosso modelo, utilizamos janelas deslizantes, onde cada janela contém `k` dias (ou semanas/meses) de histórico e o modelo prevê o valor de fechamento do próximo período.
   
4. **Implementação do Modelo de Regressão Linear**: Implementamos o modelo linear do zero, utilizando a biblioteca `autograd` para calcular os gradientes de maneira automática e otimizar os parâmetros via descida de gradiente.
   
5. **Avaliação do Modelo**: Após o treinamento, realizamos previsões no conjunto de teste e avaliamos o desempenho do modelo através de métricas como o Erro Médio Absoluto (MAE) e o Erro Quadrático Médio (MSE).
   
6. **Visualização dos Resultados**: Geramos gráficos que comparam as previsões do modelo com os dados reais, para verificar o desempenho da Regressão Linear.

## Requisitos

Para rodar o projeto, é necessário ter instalados os seguintes pacotes Python:

- `yfinance`
- `pandas`
- `matplotlib`
- `autograd`
- `numpy`

Você pode instalar todos os pacotes executando o comando:

```bash
pip install -r requirements
```
