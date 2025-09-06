# Heart Disease Risk Prediction

This project leverages the **Framingham Heart Study dataset** to develop a comprehensive system for predicting **10-year risk of coronary heart disease (CHD)**. It is designed as an advanced, real-world project combining both supervised and unsupervised learning techniques, along with extensive feature engineering, visualization, and model interpretability.

## Project Overview
- **Dataset**: A subset of the Framingham Heart Study cohort (≈4,240 patients, 16 features). The key target is `TenYearCHD`, indicating whether a patient developed CHD within 10 years.
- **Focus**: Predictive modeling, clustering risk phenotypes, anomaly detection, and visualization of patient risk profiles.

## Key Components

### 1. Data Preprocessing
- Missing value handling using advanced imputation.
- Feature scaling and categorical encoding.
- Feature engineering: BMI categories, age decades, pulse pressure, smoking pack proxy, and more.

### 2. Supervised Learning
- Logistic Regression (calibrated for probability estimates).
- Random Forest, XGBoost, and LightGBM.
- Models evaluated with ROC AUC, precision-recall, F1, calibration, and Brier score.
- Risk calibration curves for clinical interpretability.

### 3. Unsupervised & Semi-Supervised Learning
- **Clustering** (KMeans, Agglomerative) to identify hidden patient phenotypes and subgroup risks.
- **Dimensionality Reduction** (PCA, UMAP) for visualization of patient clusters.
- **Anomaly Detection** using Isolation Forest and deep autoencoder reconstruction errors.
- **Feature Learning** with Autoencoders to extract compressed patient representations for improved supervised models.

### 4. Explainability & Visualization
- SHAP-ready feature importance analysis.
- PCA variance explained plots.
- UMAP cluster visualizations colored by risk.
- Cluster-level risk profiling.
- Anomaly score distributions.
- ROC, PR, and calibration plots.

### 5. Artifacts
- Preprocessing pipeline (`preprocessor.joblib`).
- Trained supervised models (`log_reg.joblib`, `rf.joblib`, `xgb.joblib`, `lgbm.joblib`).
- Autoencoder feature extractor and anomaly detection models.
- Visualizations for analysis and reporting.

## How to Implement
- Place the dataset (`framingham.csv`) in the `data/` folder.
- Run the notebook `Heart-Disease-Risk-Prediction.ipynb` to process data, train models, generate plots, and save artifacts.
- Outputs (models, encoders, plots) will be saved under `models/save/` for deployment.

## Deployment Potential
The project is structured for future deployment as a real-world application, such as:
- **Streamlit Web App** for interactive patient risk prediction.
- **API Service** (FastAPI/Flask) for integration with clinical systems.
- **Automated Risk Reports** with per-patient predictions and SHAP-based explanations.

---
This project demonstrates a research-level, end-to-end approach to **heart disease risk prediction**, combining predictive accuracy, interpretability, unsupervised patient profiling, and anomaly detection for robust real-world applicability.
