# Distributed Wildfire Confidence Prediction with H2O.ai

A distributed ML project classifying satellite-observed wildfire events into **Low**, **Nominal**, and **High** confidence categories using NASA VIIRS SNPP 2023 active-fire data.

## Highlights
- Distributed training with a **2-node H2O cluster**
- H2O Distributed Random Forest for multiclass classification
- Data preparation and feature engineering over global satellite observations
- Evaluation with accuracy, AUC, and F1-score
- Scalable model training on large datasets

## Workflow
`VIIRS SNPP data → preprocessing & feature engineering → 2-node H2O cluster → Distributed Random Forest → evaluation`

## Dataset
NASA FIRMS / VIIRS SNPP global active-fire records for 2023. Consult the notebook for exact columns, filtering, and experimental configuration.

## Tech stack
Python · H2O.ai · Distributed Random Forest · pandas · SciPy · Satellite data · Distributed computing

## Reproducibility
Requires a compatible H2O environment and cluster setup. Start with the notebook and setup notes; multi-node configuration may need adaptation.

## Result
The portfolio/resume reports **0.070 per-class error**. See the notebook/report for the metric definition and evaluation setup before comparing against other models.

## Repository
[View source code](https://github.com/kananpandit02/wildfire_pred_h2o)

**Kanan Pandit** · [Portfolio](https://kananpanditportfolio.netlify.app/) · [LinkedIn](https://linkedin.com/in/kananpandit02)
