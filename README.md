# IFRS9 Probability of Default (PD) Modelling

This repository contains the implementation of a **Probability of Default (PD) model** developed under the **IFRS9** framework. The model is designed to predict both 12-month and lifetime PD for loan portfolios. The project includes thorough data preprocessing, feature engineering, model development, and evaluation to ensure accurate and compliant default risk predictions.

## Key Components

### 1. Data Quality Assessment
- **Missing Data Handling**: Managed missing values for critical variables like `Credit Score`, `Account Management Score`, and `County Court Judgement`, applying stage-specific techniques (e.g., imputation or removal based on the account stage).
- **Outlier Detection**: Identified and corrected data anomalies, including unrealistic values in `Loan to Value` and negative values in `Remaining Months on Book`.
- **Data Cleansing**: Adjusted data inconsistencies across both company and individual account datasets to ensure accurate modeling.

### 2. 12-Month PD Model
- **Logistic Regression**: Developed logistic regression models to predict the 12-month PD for both company and individual accounts.
- **Feature Engineering**: Utilized key variables like `Days in Arrears`, `Loan to Value`, `Credit Score`, `Account Management Score`, and more.
- **Staging Rules**: Aligned the model predictions with **IFRS9 stages** (Stage 1 and 2 for non-defaults, Stage 3 for defaults).
- **Multicollinearity Check (VIF)**: Used Variance Inflation Factor (VIF) analysis to address multicollinearity and ensure the selected features contributed meaningfully to the model.

### 3. Lifetime PD Model
- **Survival Analysis**: Extended the PD prediction for Stage 2 and Stage 3 accounts by calculating lifetime PD through cumulative survival analysis, based on the 12-month PD and the remaining loan term.

### 4. Data Visualization
- **PD Distribution Plots**: Visualized the distribution of 12-month and lifetime PD to explore risk patterns across different stages and account types.
- **Box Plots & Heatmaps**: Provided deeper insights into the relationships between key features like `Days in Arrears`, `Loan to Value`, and other variables impacting default probability.

### 5. Model Interpretation & Evaluation
- **Coefficient Analysis**: Examined model coefficients to validate their impact on default predictions (e.g., `Days in Arrears` had a positive effect, while `Credit Score` had a negative one).
- **Model Performance**: Assessed the performance of the PD model using various metrics and visualizations to evaluate how well the model captures default risk.

### 6. Future Enhancements
- Suggested adding additional features such as `Debt-to-Income Ratio`, `Annual Income`, and macroeconomic factors (`GDP Growth`, `Unemployment Rate`, `Interest Rates`) to improve the model's predictive power.

## Files Included
- **Jupyter Notebooks**: Contain the complete code for data cleaning, model development, and analysis.
- **PDF Reports**: Summarize the methodology, data quality checks, and key model findings.

