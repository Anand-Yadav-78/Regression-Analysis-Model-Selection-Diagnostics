# Regression-Analysis-Model-Selection-And-Diagnostics


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## Ames Housing Price Prediction: A Regression Analysis with Rigorous Model Selection & Diagnostics
This repository contains an end-to-end data science project focused on predicting house sale prices using the Ames, Iowa housing dataset. The primary goal is not simply to achieve high predictive accuracy, but to construct a statistically sound, interpretable, and defensible linear regression model.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# 📋 Problem Statement
The real estate market relies on accurate property valuation. This project moves beyond simple heuristics to build a data-driven model that explains the factors influencing a home's value. The key challenge is to navigate a dataset with a large number of features, identify the most significant price drivers, and validate the final model against common statistical pitfalls to ensure its real-world reliability.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# 📊 Data Summary
The analysis is based on the popular Ames Housing dataset, which contains 1460 observations and 79 diverse explanatory variables. These features describe nearly every aspect of residential homes, including:

Property Attributes: Lot area, overall quality, year built, basement size.

Location & Neighborhood: Physical location within Ames.

Structural Features: Number of rooms, garage size, fireplace presence.

The target variable for this regression analysis is SalePrice.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# 🛠️ Methodology & Techniques
To ensure the model is both accurate and trustworthy, a sophisticated and systematic methodology was employed, focusing on statistical rigor at each step.

Data Preprocessing: Handled missing values using median and mode imputation and performed one-hot encoding for categorical variables. The target variable (SalePrice) was log-transformed to normalize its distribution.

Systematic Model Selection: A Forward Stepwise Selection algorithm was used to build the model iteratively, evaluating which variables to add based on three distinct criteria:

Adjusted R²

Mallows' Cₚ

Akaike Information Criterion (AIC)

Multicollinearity Check: The Variance Inflation Factor (VIF) was calculated to detect and handle redundancy among predictor variables, ensuring stable coefficient estimates.

Predictive Validation: The Predicted Residual Sum of Squares (PRESS) statistic was used as a robust cross-validation method to assess the model's ability to predict new, unseen data.

Influence Diagnostics: A full suite of diagnostics was run to identify influential outliers that could disproportionately affect the model's performance. Key metrics included:

Cook's Distance

DFFITS

Leverage

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# 🚀 Tools and Libraries
This project was built using Python 3 and the following core data science libraries:

Pandas: For data manipulation and analysis.

NumPy: For numerical operations.

Scikit-learn: For data preprocessing and train-test split.

Statsmodels: For advanced statistical modeling, regression diagnostics, and VIF calculation.

Matplotlib & Seaborn: For data visualization and diagnostic plotting.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

# 💡 Inference and Conclusion
The analysis yielded a robust 15-variable linear regression model that successfully explains a significant portion of the variance in house prices, achieving an R² of 0.895 on the hold-out test set.

The most critical insight emerged from the influence diagnostics and remediation steps. After identifying and removing 96 influential outliers, the model's fit on the training data improved dramatically (Adjusted R² increased from 0.85 to 0.92). However, when evaluated on the unseen test data, this "cleaner" model performed slightly worse.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## Final Conclusion: 

This demonstrates a crucial trade-off between a model's statistical purity and its real-world predictive power. The original model, while containing statistical "noise" from outliers, was more robust and generalized better to new, unseen data. This highlights that the most statistically "perfect" model is not always the most practical one for prediction. For this use case, the model trained on the complete dataset is recommended for its superior predictive performance.
