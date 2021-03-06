# Avaliador de Imóveis

Solução completa de Data Science: Avaliador de imóveis da cidade de Ponta Grossa - PR.   
Desenvolvido desde a definição do problema, coleta, limpeza e análise dos dados, até a modelagem e disponibilização dos resultados em uma aplicação web.
Projeto final do curso [Como criar uma solução completa de Data Science](https://curso.mariofilho.com/).

## Etapas do Projeto

### 1 - Definição do Problema

O problema principal abordado nesse projeto é a precificação de imóveis. Será possível criar uma solução automatizada que faça a avaliação de imóveis? Suponhamos que você seja um corretor de imóveis, porém está 
sem tempo para avaliar os diversos imóveis que recebe dos seus clientes. Com a solução apresentada aqui 
é possível precificar imóveis somente com as principais características do imóvel.

### 2 - Coleta dos Dados [scraping.ipynb](./scraping.ipynb)

A coleta dos dados foi feita através de WebScraping do site [Procure Imóvel](https://procureimovel.com.br/).
Foram coletadas todas as casas disponíveis do site no dia 19 de Junho de 2020. Para essa etapa foi utilizado
a biblioteca BeatifulSoup. A páginas html foram baixadas do Procure Imóveis e os dados foram coletados de cada imóvel. Todo o código do scraping está no arquivo [scraping.ipynb](./scraping.ipynb).  

O dataset criado nesse projeto foi publicado no Kaggle [Casas à Venda - Ponta Grossa PR](https://www.kaggle.com/victorstein/casas-venda-ponta-grossa-pr)

### 3 - Preparação dos Dados [dataCleaning.ipynb](./dataCleaning.ipynb)

Como ss dados coletados das páginas html são "sujos" é importante que a Limpeza e Preparação dos dados seja bem feita. Foram feitas limpezas de características com muitos dados faltantes e limpeza de alguns dados absurdos. Nessa etapa utilizou-se principalmente da biblioteca Pandas e Numpy. O código pode ser visualizados no arquivo [dataCleaning.ipynb](./dataCleaning.ipynb)

### 4 - Análise de Dados [EDA.ipynb](./EDA.ipynb)

Etapa do projeto onde são extraídas algumas informações dos dados. Foram analisadas as distribuições dos valores, as tendências dos imóveis em relação ao preço e a correlação entre as variáveis. Nessa etapa foi utilizado principalmente matplotlib e seaborn. [EDA.ipynb](./EDA.ipynb)

### 5 - Modelagem [modelo.ipynb](./modelo.ipynb)

Nessa etapa foi criado o modelo de regressão que fará a precificação dos imóveis. Nessa etapa o dataset foi dividido entre treino e validação e foram criados modelos (RandomForest e LightGBM) para a tarefa. Após a criação do modelo foi executado o tuning dos hiperparâmetros com Random Search e Bayesian Optimization, melhorando o modelo em 10% na sua métrica primária.


## Tecnologias utilizadas

- Linguagem de Programação: Python
- IDE: Jupyter Lab
- Bibliotecas:
    + beautifulsoup4==4.8.2
    + joblib==0.14.1
    + numpy==1.19.0
    + Flask==1.1.1
    + lightgbm==2.3.1
    + numpy==1.19.0
    + pandas==1.0.4
    + requests==2.22.0
    + scikit-learn==0.23.1
    + scikit-optimize==0.7.4
    + scipy==1.5.1
    + seaborn==0.10.0
    + statsmodels==0.11.0
    + tqdm==4.42.1
    + matplotlib==2.1.2

## Kaggle

Com os dados coletados na parte do scraping foi criado um dataset com as casas à venda da cidade de Ponta Grossa - PR. O dataset está disponível no Kaggle [Casas à Venda - Ponta Grossa PR](https://www.kaggle.com/victorstein/casas-venda-ponta-grossa-pr). 

## Contato

Victor Stein - [LinkedIn](www.linkedin.com/in/victor-stein) 
