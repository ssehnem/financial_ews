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
