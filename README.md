# 📈 Insurance Charges Prediction with Linear Regression

![python](https://img.shields.io/badge/python-3.11.9-red) ![pandas](https://img.shields.io/badge/pandas-2.2.3-orange) ![numpy](https://img.shields.io/badge/numpy-2.2.3-yellow) ![matplotlib](https://img.shields.io/badge/matplotlib-3.10.0-green) ![seaborn](https://img.shields.io/badge/seaborn-0.13.2-blue) ![statsmodels](https://img.shields.io/badge/statsmodels-0.14.4-indigo) ![scikit_learn](https://img.shields.io/badge/scikit_learn-1.6.1-violet) 

This project demonstrates the use of **linear regression** to predict individual medical insurance charges based on demographic and lifestyle features. The analysis follows a structured data science workflow, including exploratory data analysis (EDA), feature engineering, model training, and evaluation.

The repository contains the following:

|Description|File|
|:-|:-|
|Analysis notebook with all code used to generate the results, including comments and notes. |  `Insurance_Charges_Prediction_Linear_Regression.ipynb`|
|Dataset file containing all data used in the analysis. [Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)  | `insurance.csv`|
|Analysis report discussing findings in more detail. | `Insurance_Charges_Prediction_Analysis_Report.pdf`|

## Project Overview

This project demonstrates the use of a linear regression model to predict individual medical insurance charges based on customers' demographic and lifestyle factors.

- **Dataset:** [Medical Cost Personal Dataset (Kaggle)](https://www.kaggle.com/datasets/mirichoi0218/insurance)  
  Contains 1,338 records with features: age, sex, BMI, number of children, smoking status, region, and insurance charges.

- **Objectives:**
  - **EDA:** Understand feature distributions, relationships, and data quality.
  - **Feature Selection:** Identify the most predictive variables for insurance charges.
  - **Model Training:** Build and evaluate linear regression models, including regularized variants.
  - **Interpretation:** Assess model performance and provide actionable insights for insurance pricing.

## Key Features

- **Data Cleaning & Preprocessing:**  
  - Removal of duplicates and confirmation of no missing values  
  - One-hot encoding of categorical variables (sex, smoker, region)

- **Exploratory Data Analysis (EDA):**  
  - Statistical summaries and visualizations (histograms, boxplots, pairplots)
  - Correlation analysis and identification of outliers

- **Feature Selection:**  
  - Backward elimination using OLS regression p-values  
  - Lasso regularization for automated feature selection

- **Model Training & Evaluation:**  
  - Linear regression using both statsmodels and scikit-learn  
  - Train-test split (80/20) for robust evaluation  
  - Metrics: R², RMSE, MAE  
  - Residual and actual vs. predicted plots for diagnostic analysis

- **Result Interpretation:**  
  - Analysis of feature importance and group effects (e.g., smoker vs. non-smoker)
  - Recommendations for model improvement and business application

## Results

- **Key Predictors:**  
  - Smoking status is the strongest predictor of higher charges.
  - Age and BMI show moderate positive correlations with charges.
  - Gender and region have minimal impact after encoding.

- **Model Performance:**  
  - Linear regression explains ~80% of the variance in charges (R² ≈ 0.80).
  - RMSE and MAE indicate some large errors, mainly due to outliers and distinct subgroups (smokers vs. non-smokers).
  - Lasso regularization did not significantly improve performance or address group banding.

- **Insights:**  
  - The model tends to average between smoker and non-smoker groups, suggesting separate models may yield better predictions.
  - Outliers and unmeasured factors (e.g., pre-existing conditions) limit prediction accuracy for extreme cases.

## Technologies Used

- Python (Pandas, NumPy, scikit-learn, statsmodels, Matplotlib, Seaborn)
- Jupyter Notebook

## Insights & Impact

- **Actionable Insights:**  
  - Smoking status should be a key factor in insurance pricing.
  - Outlier handling and subgroup modeling (e.g., separate models for smokers) can improve accuracy.
  - The workflow provides a template for adapting international datasets to local insurance contexts.

- **Methodological Value:**  
  - Demonstrates the importance of EDA, feature engineering, and model diagnostics in regression tasks.
  - Highlights the limitations of linear models in the presence of strong group effects and outliers.

**Author:** Jishen Harilal  
**LinkedIn:** www.linkedin.com/in/jishen-harilal  
**Contact:** jishen2108@gmail.com  

---

*For more details, see the full analysis in Insurance_Charges_Prediction_Linear_Regression.ipynb.*
