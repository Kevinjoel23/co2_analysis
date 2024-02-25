## co2_analysis

Model Description:
------------------
- **Model Type:** The model used is a pipeline consisting of preprocessing steps followed by a CatBoostRegressor.

Preprocessing:
--------------
- **Numeric Features:** For numeric features (`SA`, `TPV`, `C`, `H`, `N`, `O`, `T`, `P`), the pipeline applies KNN imputation with 10 neighbors for missing values followed by standard scaling.
- **Categorical Features:** Categorical features (`type_Hierarchical`, `type_Macroporous`, `type_Mesoporous`, `type_Microporous`) are passed through without any transformation.

Regressor:
-----------
- **Model:** CatBoostRegressor is utilized with the following hyperparameters:
  - **Loss Function:** Root Mean Squared Error (`RMSE`)
  - **Regularization Parameter:** L2 Regularization with a value of 1
  - **Learning Rate:** 0.1
  - **Number of Estimators:** 300

Model Performance:
-------------------
- **Training R-squared Score:** The model achieves a very high R-squared score of approximately 0.999 on the training data.
- **Testing R-squared Score:** On the testing data (20% split), the model performs slightly lower but still achieves a respectable R-squared score of around 0.881.

Data Split:
------------
- **Train-Test Split Ratio:** The data is split into a training set and a testing set with a ratio of approximately 80% for training and 20% for testing.


# Force Plot for first point
![force_plot1](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/c06c44cd-b4a1-489e-b3b7-c1f8610e32a2)

# Force Plot for fourth point
![force_plot2](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/8698cf5c-7b73-4498-9028-c45e6807e8e8)

# Waterfall Plot for the analysis
![waterfall](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/37e6596c-ca6e-49af-9857-a2f5248f547f)

# Beeswarm Plot for the analysis
![beeswarm](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/061008a1-f82b-48e3-8b47-eb14ac500f8d)


# 3 Partial Dependence Plots for attribute pairs
![C_vs_H](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/f5b44dd8-2f1d-49f0-984e-87f5ca9e109f)

![SA_vs_TPV](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/0709f3dd-ae3c-496d-8079-d047a6de1818)

![SA_vs_T](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/a6dd1531-6ef8-414b-9d7b-640cf9d30c42)

![SA_vs_O](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/2cdaab11-6bda-416e-bb16-eadb05ff32d6)

![SA_vs_N](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/3a1252c1-f91c-4dbb-978f-59e9d743eb91)

![N_vs_H](https://github.com/Kevinjoel23/co2_analysis/assets/99750001/45bd938b-8d80-435b-861f-fd13f3c1e174)
