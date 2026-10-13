# Mangrove-AGB-Radar-Optical-Fusion
Spatiotemporal dynamics of mangrove aboveground biomass (AGB) and canopy degradation mapping via harmonized multi-sensor radar-optical data fusion, 5-fold spatial LOTO cross-validation, and post-hoc Explainable AI (SHAP/MDI) architectures
# Spatiotemporal Dynamics of Mangrove AGB and Canopy Degradation

This repository contains the full cloud-computing scripts, multi-sensor feature space architectures, and machine learning pipelines needed to fully replicate and computationally verify the landscape aboveground biomass (AGB) metrics.

## 🚀 Key Framework Architecture
* **Google Earth Engine (GEE):** Executes annualized median compositing, relative Pseudo-Invariant Feature (PIF) normalization, and 34-variable master covariate stack extractions.
* **RStudio Core Engine:** Calmly executes a 5-fold spatially blocked Leave-One-Transect-Out (LOTO) cross-validation scheme to entirely eliminate neighborhood data-leakage bias.
* **Explainable AI (XAI):** Contrasts Random Forest MDI vectors against native Gradient Boosted XGBoost SHAP matrices.

## 🛠️ Execution Instuctions
1. Open and run the scripts in `1_GEE_JavaScript_Scripts/` inside your Google Earth Engine Code Editor to build the 10 m multi-sensor covariate grid.
2. Ingest the extracted matrices into RStudio and execute `2_RStudio_ML_Scripts/rf_vs_xgboost_regression.R` to evaluate cross-validation errors.
3. Track algorithmic transparency and variable contributions via `2_RStudio_ML_Scripts/shap_xai_feature_attribution.R`.
