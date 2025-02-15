# Análise e Previsão de Preços do Dólar e Bitcoin com Prophet

Este repositório contém uma análise dos preços históricos do Dólar (BRL/USD) e do Bitcoin (BTC/BRL) com a utilização de técnicas de previsão para o ano de 2025. O código é executado em um Jupyter Notebook e utiliza várias bibliotecas para manipulação de dados, visualização e modelagem preditiva, como `yfinance`, `ccxt`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, `statsmodels`, `prophet` e `scikit-learn`.

## Descrição do Código

O objetivo deste notebook é coletar os dados históricos dos preços do Dólar e Bitcoin, realizar uma análise exploratória, calcular a correlação entre esses ativos e, em seguida, utilizar modelos preditivos para prever os preços futuros de ambos para 2025.

### Etapas do Código

1. **Coleta de Dados**:
    - Utiliza a biblioteca `yfinance` para coletar os dados históricos do preço de fechamento do Dólar em relação ao Real (BRL/USD).
    - Usa a biblioteca `ccxt` para obter dados históricos de preço do Bitcoin em relação ao Real (BTC/BRL) a partir da exchange KuCoin.

2. **Análise Exploratória**:
    - Aplica transformações logarítmicas aos preços para facilitar a modelagem.
    - Exibe gráficos das evoluções de preço do Dólar e do Bitcoin.

3. **Cálculo de Correlação**:
    - Calcula a correlação de Pearson e Spearman entre os preços do Dólar e do Bitcoin para entender a relação entre os dois ativos.

4. **Previsão com Prophet**:
    - A biblioteca `Prophet` é usada para fazer previsões de séries temporais. O modelo é treinado com os dados históricos dos preços do Dólar e do Bitcoin.
    - O `Prophet` é uma biblioteca desenvolvida pelo Facebook que permite a criação de modelos preditivos para séries temporais. Ele se destaca pela facilidade de uso e capacidade de lidar com dados de séries temporais com padrões sazonais e tendências. A principal vantagem do Prophet é que ele não exige conhecimento profundo sobre a modelagem de séries temporais, tornando-o acessível para análise e previsão rápida.

5. **Previsão de Preços para 2025**:
    - Faz previsões para os próximos 365 dias para ambos os ativos.
    - Identifica os meses com os menores preços médios (indicados como melhores meses para compra) e os meses com os maiores preços médios (indicados como melhores meses para venda).

6. **Erro Quadrático Médio (MSE)**:
    - Calcula o erro quadrático médio (MSE) das previsões para o Dólar e Bitcoin, para avaliar a precisão do modelo.

7. **Resultados**:
    - Exibe as previsões de preços futuros, os melhores meses para comprar e vender simultaneamente Dólar e Bitcoin em 2025.

## Bibliotecas Utilizadas

- **`yfinance`**: Usada para baixar dados financeiros históricos, como os preços de fechamento do Dólar (BRL/USD).
- **`ccxt`**: Biblioteca para acessar dados de criptomoedas em várias exchanges, como a KuCoin, utilizada para coletar dados de preços do Bitcoin (BTC/BRL).
- **`pandas`**: Usada para manipulação e análise de dados, transformando os dados coletados em DataFrames e realizando operações como limpeza de dados e transformação.
- **`numpy`**: Biblioteca para operações matemáticas e de álgebra linear, usada para manipular arrays e fazer transformações logarítmicas.
- **`matplotlib` e `seaborn`**: Bibliotecas de visualização de dados para criar gráficos e analisar visualmente as séries temporais e resultados das previsões.
- **`scipy`**: Usada para cálculos estatísticos, como a correlação de Pearson e Spearman.
- **`statsmodels`**: Biblioteca para modelagem estatística, mas no código é o `Prophet` que realiza as previsões.
- **`prophet`**: Esta é a biblioteca central para previsão dos preços de séries temporais. O `Prophet` se destaca pela simplicidade e eficácia na modelagem de séries temporais com tendências sazonais, permitindo realizar previsões de longo prazo com boa acurácia. O modelo se ajusta automaticamente a tendências e sazonalidades, sem a necessidade de tunar muitos parâmetros manualmente.
- **`scikit-learn`**: Usada para métricas de avaliação, como o erro quadrático médio (MSE).

## Como Executar

1. Certifique-se de que todas as bibliotecas necessárias estão instaladas. Se ainda não estiverem, instale-as com o comando:

    ```bash
    pip install yfinance ccxt pandas numpy matplotlib seaborn scipy statsmodels prophet scikit-learn
    ```

2. Execute o código no Jupyter Notebook para carregar os dados, realizar a análise e visualizar as previsões.

## Resultados Esperados

- **Previsões para o Dólar e o Bitcoin em 2025**: Gráficos de previsão mostrando a tendência dos preços para os próximos meses.
- **Melhores meses para compra e venda**: Meses com os menores e maiores preços médios, para orientar decisões de investimento.
- **Erro Quadrático Médio (MSE)**: Indicadores da precisão do modelo para Dólar e Bitcoin.

## Conclusões

Este código fornece uma análise detalhada sobre os preços futuros do Dólar e do Bitcoin, utilizando o `Prophet`, uma poderosa ferramenta para previsão de séries temporais. A combinação de análise de correlação e previsão ajuda a tomar decisões informadas sobre o melhor momento para comprar ou vender esses ativos.

