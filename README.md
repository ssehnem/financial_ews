# Predicting Financial Crises: A Machine Learning Analysis of the 1929 Crash
*(Previsão de Crises Financeiras: Uma Análise de Machine Learning do Crash de 1929)*

[🇺🇸 English Version](#-english) | [🇧🇷 Versão em Português](#-português)

---

## 🇺🇸 English

### Overview
This repository contains the code and data for my undergraduate thesis (TCC). The project investigates the application of Machine Learning models to identify patterns and early warning signals (EWS) preceding the 1929 stock market crash. By leveraging historical data from the Dow Jones Industrial Average (DJIA) and macroeconomic indicators, the project aims to evaluate how modern algorithms capture non-linear market anomalies leading up to extreme downturns.

### Repository Structure
- `tcc_ver3.ipynb`: Main Jupyter/Colab Notebook containing the Exploratory Data Analysis (EDA), feature engineering, model training, and evaluation.
- `data/`: Directory containing the historical dataset (`dow_jones_data.csv`). 

### Models and Methodology
- **Data Preparation:** Feature engineering including moving averages (3-month, 12-month), rolling volatility (6-month), and drawdowns to capture market conditions.
- **Algorithms:** Logistic Regression (baseline), Random Forest, and Gradient Boosting Classifier.
- **Validation:** Implementation of `TimeSeriesSplit` (purged cross-validation) to prevent look-ahead bias and respect the chronological nature of financial data.
- **Explainability:** Application of SHAP (SHapley Additive exPlanations) values to interpret feature importance and model decisions.

### Requirements
To run this project locally, ensure you have Python 3 installed along with the following libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap scipy
```

### Usage
1. Clone this repository.
2. Ensure the `dow_jones_data.csv` file is correctly placed in the `data/` folder.
3. Open `tcc_ver3.ipynb` in Jupyter Notebook or Google Colab and run the cells sequentially to reproduce the data preparation, visualizations, and model training.

---

## 🇧🇷 Português

### Sobre o Projeto
Este repositório contém o código e os dados do meu Trabalho de Conclusão de Curso (TCC). O projeto investiga a aplicação de modelos de Machine Learning para identificar padrões e sinais de alerta precoce (EWS - *Early Warning Signals*) que antecederam o crash da bolsa de 1929. Utilizando dados históricos do índice Dow Jones (DJIA) e dados macroeconômicos, o objetivo é avaliar como algoritmos modernos capturam anomalias de mercado não-lineares antes de quedas extremas.

### Estrutura do Repositório
- `TCC_Dow_Jones_Final.ipynb`: Notebook principal (Jupyter/Colab) contendo a Análise Exploratória de Dados (EDA), engenharia de variáveis (*feature engineering*), treinamento e avaliação dos preditores.
- `data/`: Diretório contendo a base de dados histórica (`dow_jones_data.csv`).

### Metodologia
- **Engenharia de Variáveis:** Criação de médias móveis (3 e 12 meses), volatilidade contínua (desvio padrão de 6 meses) e *drawdowns*. O alvo (target) é focado na previsão de quedas bruscas em uma janela de 3 meses (`crash_3m`).
- **Algoritmos:** Regressão Logística (modelo base), Random Forest e Gradient Boosting Classifier.
- **Validação:** Implementação de `TimeSeriesSplit` com *gap* de exclusão (*purged cross-validation*) para evitar vazamento de dados (*look-ahead bias*) e respeitar a ordem cronológica estrita.
- **Explicabilidade:** Aplicação dos valores SHAP (*SHapley Additive exPlanations*) para interpretar o peso e a importância das variáveis na tomada de decisão dos modelos.

### Pré-requisitos
Para executar este projeto localmente, você precisa ter o Python 3 instalado juntamente com as seguintes bibliotecas:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn shap scipy
```

### Como Executar
1. Faça o clone deste repositório.
2. Certifique-se de que o arquivo `dow_jones_data.csv` está localizado dentro da pasta `data/`.
3. Abra o arquivo `tcc_ver3.ipynb` no Jupyter Notebook ou suba-o para o Google Colab e execute as células sequencialmente para reproduzir as análises, os gráficos e o treinamento dos modelos.
