# 🏬 Rossmann - Previsão de Vendas com Data Science

## 1. Problema de negócio

A Rossmann é uma das maiores redes de drogarias da Europa, com mais de 3.000 lojas espalhadas por diversos países. Atuando em um mercado altamente competitivo, a empresa busca constantemente otimizar suas operações para maximizar o faturamento e melhorar a experiência do cliente.

Recentemente, o CEO da Rossmann solicitou uma solução para prever as vendas das lojas nas próximas 6 semanas. Essas previsões permitirão uma melhor priorização das reformas das lojas, garantindo que investimentos sejam feitos de forma mais estratégica.

Atualmente, as decisões são tomadas com base em dados históricos e experiência dos gerentes de loja, o que pode levar a previsões imprecisas e oportunidades perdidas. O objetivo deste projeto é desenvolver um modelo de Machine Learning para tornar esse processo mais eficiente e baseado em dados.


## 🎯 2. Objetivo do Projeto

Criar um modelo de Machine Learning capaz de prever as vendas das lojas da Rossmann com base em dados históricos e fatores externos.

Com essas previsões, a empresa poderá tomar decisões mais estratégicas, como priorizar quais lojas devem ser reformadas primeiro, otimizando os investimentos e melhorando os resultados financeiros.

## 3. Planejamento da Solução

### 📌 Produto Final

A solução foi desenvolvida no formato de API, permitindo que sistemas e dispositivos móveis possam acessar as previsões de vendas de forma prática.

    Observação: Inicialmente, a API seria implantada no Heroku, mas devido a algumas dificuldades técnicas, a implementação pode ser feita em outras plataformas, como Render, Railway ou AWS Lambda.

### 🚀 Metodologia

Para desenvolver esse projeto, utilizei a metodologia CRISP-DM, que permite uma entrega estruturada e eficiente.

As etapas seguidas foram:

    1. Definição do Problema
        Os gerentes das lojas solicitaram uma previsão de vendas para as próximas 6 semanas.

    2. Entendimento do Negócio
        Em conversa com os gerentes, identificamos que essa demanda veio do CEO da empresa.
        O objetivo era utilizar as previsões para priorizar quais lojas deveriam ser reformadas primeiro.

    3. Coleta de Dados
        Os dados foram extraídos do banco de dados da Rossmann, incluindo informações de vendas, calendário, promoções, concorrência e sazonalidade.

    4. Limpeza e Preparação dos Dados
        Renomeação das colunas para um formato mais intuitivo.
        Tratamento de valores ausentes (NAs).
        Ajuste dos tipos de variáveis.
        Análise estatística para melhor compreensão dos dados.
        Criação de um mapa mental de hipóteses para direcionar a análise exploratória.

    5 .Exploração dos Dados
        Análise univariada para entender a distribuição das variáveis.
        Análise bivariada para validar hipóteses e identificar variáveis importantes para o modelo.
        Análise multivariada para entender a correlação entre variáveis.

    6. Preparação para Modelagem
        Normalização e padronização de variáveis numéricas.
        Codificação de variáveis categóricas (encoding).
        Transformação da variável resposta para melhor performance do modelo.
        Seleção de variáveis utilizando o método Boruta, garantindo que apenas os atributos mais relevantes fossem utilizados no modelo.

    7. Modelagem com Algoritmos de Machine Learning
        Foram testados os seguintes modelos:
            Average Model
            Regressão Linear
            Regressão Linear Lasso
            Random Forest Regressor
            XGBoost Regressor
        Todos os modelos passaram por um processo de validação cruzada (cross-validation).
        Os melhores resultados foram obtidos com Random Forest Regressor e XGBoost Regressor.
        O modelo escolhido foi o XGBoost Regressor, que passou por ajuste fino de hiperparâmetros (fine-tuning) utilizando Random Search.

    8. Avaliação do Modelo
        As métricas finais do modelo foram:
            MAE (Erro Absoluto Médio): 749.83684
            MAPE (Erro Percentual Médio Absoluto): 11.23%
            RMSE (Raiz do Erro Quadrático Médio): 1069.467

## 🔜 Próximos Passos

Com a primeira versão do modelo implementada, a próxima iteração do processo CRISP-DM pode trazer novas melhorias e insights:

    Identificação de Novas Hipóteses: Explorar fatores externos que possam impactar as vendas, como clima, eventos sazonais e campanhas de marketing.
    Engenharia de Variáveis: Criar novas features baseadas em dados históricos e interações entre variáveis.
    Melhoria do Modelo: Testar novos algoritmos e técnicas de otimização de hiperparâmetros para melhorar a precisão das previsões.
    Deploy em Produção: Avaliar plataformas alternativas para hospedar a API, garantindo escalabilidade e facilidade de manutenção.
    Monitoramento do Modelo: Implementar métricas para acompanhar a performance do modelo ao longo do tempo e detectar necessidade de re-treinamento.