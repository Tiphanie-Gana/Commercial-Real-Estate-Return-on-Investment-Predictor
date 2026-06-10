# Commercial Real Estate Return on Investment Predictor
## Overview
This project predicts the return on Investment potential for commercial real estate  properties in Australia, using listing data (price, area, location, property decription), I built an end to end regression model to estimate price per square meter -A strong proxy for investment attractiveness and ROI.

The goal was to help investors quickly evaluate properties based on features like location property type and textual descriptions.

## Dataset
- *Source*: Scraped commercial property listings across Australia (VIC, QLD, etc.)
- *Size*: \~1,595 records
- *Key Features*: Price, Area (m²), Location (lat/long), Property Type, NBN, Text Description
- *Target*: price_per_sqm (engineered)

## Key Steps in the Project

1. *Data Loading & EDA*
   - Explored distributions of price, area, and location
   - Handled missing values and outliers

2. *Data Preprocessing & Feature Engineering*
   - Cleaned price and area columns
   - Engineered price_per_sqm
   - Extracted features from text using *TF-IDF*
   - Numerical & categorical preprocessing pipeline

3. *Modeling*
   - Trained regression models (e.g., XGBoost / Random Forest)
   - Used Scikit-learn pipelines for consistency
   - Hyperparameter tuning (optional but recommended to add)

4. *Model Evaluation & Interpretability*
   - Metrics: R², MAE, RMSE
   - Used *SHAP* values to explain feature importance (location, area, and specific keywords in descriptions matter most)

## Results
- Best Model Performance: [e.g., R² = 0.XX | MAE = $XXX per sqm]
- Top features (from SHAP): Area, location-related terms, lease/Office keywords, etc.

## Technologies Used
- *Python*
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Pipelines, preprocessing)
- XGBoost / Random Forest
- SHAP (for interpretability)
- TF-IDF (text features)
