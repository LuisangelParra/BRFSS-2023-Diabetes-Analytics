# BRFSS-2023-Diabetes-Analytics

This repository contains a single Jupyter notebook that walks through an end-to-end predictive analytics workflow on the 2023 BRFSS survey data, focused on diabetes risk.

## Overview

1. **Data loading & variable selection**  
   - Imported the 2023 BRFSS CSV  
   - Selected key health indicators and demographic features  

2. **Data cleaning & transformation**  
   - Handled missing values and recoded categorical codes  
   - Created an ordinal diabetes outcome (0 / 1 / 2 → binary)  
   - Scaled numeric variables  

3. **Exploratory analysis**  
   - Univariate summaries and boxplots for outlier detection  
   - Correlation heatmaps and bar charts to assess feature-target relationships  
   - Baseline “no-skill” classifier accuracy and AUC  

4. **Imbalance handling**  
   - Compared undersampling, oversampling, SMOTE variants (SMOTE, SMOTE+Tomek, SMOTEENN, ADASYN), NearMiss, etc.  
   - Benchmarked each approach using PyCaret’s `compare_models`  

5. **Model training & selection**  
   - Ran PyCaret experiments for each resampling method  
   - Evaluated top-3 models per experiment on a hold-out set  
   - Checked overfitting via CV vs. hold-out AUC gap analysis  

6. **Final model**  
   - Chose XGBoost trained on SMOTEENN-resampled data  
   - Demonstrated balanced high recall, precision and minimal overfitting  
   - Extracted and visualized feature importances  

## Contents

- `BRFSS2023_EDA_y_Modelo_PF.ipynb` – Complete analysis and modeling pipeline
  
## License

This project is released under the MIT License.  
