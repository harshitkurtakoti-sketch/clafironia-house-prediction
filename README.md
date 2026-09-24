# 🏡 California Housing Value Predictor

An end-to-end Machine Learning web application and regression pipeline designed to predict median district housing values across California based on demographic, structural, and geographical indicators.
<img width="1901" height="942" alt="Screenshot 2026-09-24 170936" src="https://github.com/user-attachments/assets/d68412d6-e400-4d67-bc21-14d21ee70a39" />

---
<img width="1919" height="949" alt="image" src="https://github.com/user-attachments/assets/d5f4ff83-71f2-4655-b3c9-fd96dabbc354" />

## 📌 Project Introduction

Accurate real estate valuation is a critical challenge due to the complex, non-linear interplay between geographical positioning, socioeconomic factors, and neighborhood density. 

This project delivers a production-ready machine learning solution to estimate district-level median home values across California using census data. Starting from raw data ingestion and rigorous exploratory analysis, the pipeline implements automated statistical imputation, domain-specific ratio feature engineering, categorical encoding, and feature scaling. 

A baseline **Multiple Linear Regression** model was evaluated against an ensemble **Random Forest Regressor**[cite: 4]. The final optimized Random Forest model achieves an $R^2$ score of **~0.806** (outperforming the linear baseline's ~0.597) and reduces Root Mean Squared Error (RMSE) to **$50,368.16**[cite: 4]. The serialized pipeline is packaged into an interactive **Streamlit** dashboard for scenario modeling, real-time inference, and feature importance diagnostics.

---

## 🚀 Key Highlights & Features

- **Automated Data Cleaning:** Imputes missing values in `total_bedrooms` using training-set median statistics to prevent data leakage.
- **Domain Feature Engineering:** Computes structural indicators:
  - Rooms per Household ($\frac{\text{total\_rooms}}{\text{households}}$)
  - Bedrooms per Room ($\frac{\text{total\_bedrooms}}{\text{total\_rooms}}$)
  - Population per Household ($\frac{\text{population}}{\text{households}}$)
- **Robust Model Benchmarking:** Systematic empirical comparison between parametric (OLS Linear Regression) and ensemble non-parametric methods (Random Forest)[cite: 4].
- **Interactive UI (Streamlit):** Pre-configured geographical presets ("Urban / high income", "Inland family district", "Coastal community"), live input validation, feature scaling on inference, and dynamic top-8 feature importance charts.

---

## 🏗 Architecture & Machine Learning Pipelines
<img width="1901" height="942" alt="Screenshot 2026-09-24 170936" src="https://github.com/user-attachments/assets/11228198-bbc4-4ae2-aae5-c5e584a7ba2f" />
<img width="1901" height="942" alt="Screenshot 2026-09-24 170936" src="https://github.com/user-attachments/assets/a34cf531-2c10-4dfa-8967-bd718ba3ceaf" />
