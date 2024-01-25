# Solubility Prediction 
The project used a dataset of 2000 compounds including 17 features and experimental solubility to create a predictive model for estimating molecular solubility. The dataset was divided into two sets, a training set and a testing set, with a 7:3 ratio. The training set was then cross-validated to find the best parameters for three different regression models: Multiple Linear Regression (MLR), K-Nearest Neighbors (KNN) Regression, and Random Forest (RF) Regression. The cross-validation was also used to measure the model's uncertainty. Finally, each optimized model was used to predict solubility on the testing set. The RF Regression model performed the best, with an R-squared score of 0.66, outperforming the MLR and KNN Regression models, which scored 0.32 and 0.58, respectively.

Then, two follow-up studies were conducted:
1) The conformal analysis was built on the optimal model, to draw the prediction interval. The quantile for non-conformity scores' quantile was set as 0.9, resulting in an accurate case rate up to 90.5%.

2) A filter was applied to eliminate inorganic compounds in the dataset, which might be the potential outliers, resulting in the physicochemical properties (PCP) data. Then, two derived datasets were conducted, including molecular fingerprint (MF) dataset and the combined MFPCP dataset. The RandomForestRegressor was again built based on those three approaches. The results revealed that the MFPCP approach outperformed the other two, with an RMSE of 0.56, an MAE of 0.39, and an R2 of 0.70.

