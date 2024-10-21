# IFRS9-Probability-of-Default-PD-Modelling

This repository contains the code and notebooks for developing a Probability of Default (PD) model under the IFRS9 framework. The focus is on predicting both 12-month and lifetime PD for loan portfolios, with a detailed approach to data preprocessing, feature selection, and model evaluation to ensure accurate default risk predictions.

Key Components
1. Data Quality Assessment
Missing Data Handling: Analyzed and managed missing values in key variables such as Credit Score, Account Management Score, and County Court Judgement using stage-specific techniques like imputation or removal based on the risk profile (Stage 1, 2, or 3).
Outlier Detection: Identified and corrected anomalies in variables such as Loan to Value (e.g., unrealistic values above 1) and Remaining Months on Book (e.g., negative durations).
Data Cleansing: Adjusted incorrect entries and ensured data consistency across company and individual account datasets.
2. 12-Month PD Model
Logistic Regression: Built logistic regression models to predict the 12-month PD for both company and individual loan accounts.
Feature Engineering: Selected key features such as Days in Arrears, Loan to Value, Credit Score, Account Management Score, and others critical to PD predictions.
Staging Rules: Classified loans into IFRS9 stages (Stage 1 and 2 for non-defaults, Stage 3 for defaults), aligning predictions with the IFRS9 guidelines.
Multicollinearity Check (VIF): Used Variance Inflation Factor (VIF) to address multicollinearity and select the most relevant features for the model.
3. Lifetime PD Model
Survival Analysis: Extended the PD prediction for Stage 2 and Stage 3 accounts, using cumulative survival analysis to calculate lifetime PD based on the 12-month PD and the remaining loan term.
4. Data Visualization
PD Distribution Plots: Visualized the predicted 12-month and lifetime PD distributions to understand risk across different stages and account types.
Box Plots & Heatmaps: Explored relationships between variables, highlighting key insights into how factors like Days in Arrears and Loan to Value affect default probability.
5. Model Interpretation & Evaluation
Coefficient Analysis: Interpreted the logistic regression model coefficients to ensure they aligned with expectations. For example, factors such as Days in Arrears were expected to have a positive relationship with PD, while Credit Score was expected to have a negative impact.
Model Performance: Evaluated the model using performance metrics and visualizations to assess how well the PD model captures risk across different loan stages.
6. Future Enhancements
Suggested additional features to improve model performance, such as Debt-to-Income Ratio, Annual Income, and macroeconomic factors like GDP Growth, Unemployment Rate, and Interest Rates, for more robust risk prediction in a forward-looking context.
Files Included
Jupyter Notebooks: Code for data preprocessing, model development, and evaluation.
PDF Reports: Summary of data quality tests, PD model analysis, and key findings.
