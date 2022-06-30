# SBALoans-using-H2O

The dataset used was a subset of the original dataset from the U.S SBA loan database. The data set included information on whether the loan was paid off in full (PIF) or if the SMA had to charge off any amount (CHGOFF) and how much that amount was. The analysis of SBA loans prediction was performed using H2O package. The dataset was given with a most important feature – “term” missing to make the training process complicated. The below two classification models were trained:

Generalized Linear Model (GLM)
Gradient Boosting Machine Model (GBM)
Implemented feature engineering, target and categorical encoding to improve the performance of my models.

The GLM model after performing model tuning ran with a performance of AUC value of 0.73 on the test dataset.

Interpreted finally trained GLM model by plotting permutation feature importance

The GBM model after model tuning performed with an AUC value of 0.82, and Accuracy of 0.85 on the test dataset

Interpreted final GBM model by plotting global feature importance using shapley values, permutation feature importance, summary plot and individual observation analysis using shapley values.

The most important feature is UrbanRural. It looks like it has a positive correlation with SHAP values. The higher the value of UrbanRural feature, the higher is the SHAP value(impact on model output). The second important feature is BankState. The third important feature is SBA_Appv. It has a negative correlation with SHAP values. The higher the value of SBA_Appv, the lower is the SHAP value(impact on model output)
