# Project: Sensor Data Analysis + Activity Recognition

This repository contains three notebooks prepared as coursework for the **“Introduction to Machine Learning”** class. The work walks through an end-to-end ML workflow on phone sensor data: exploration, feature engineering, and modelling with interpretation. The goal was to evaluate whether common activities (e.g., walking / sitting / cycling) can be meaningfully distinguished from sensor signals and which transformations and features help most.

---

## 1) Exploratory Data Analysis (EDA)

Work done in this stage:
- basic cleaning (missing values, outliers, type consistency),
- distribution and relationship analysis (correlations, temporal behaviour),
- 2D/3D visual exploration to check separability in feature space,
- initial clustering attempts to see whether the data naturally forms coherent groups,
- comparison of scaling/normalization choices and how they affect structure and separability.

Outcome: understanding data quality and structure (noise, scale differences, gaps) and defining directions for feature engineering.

---

## 2) Feature Engineering

This stage focused on extracting a stronger representation for downstream models:
- movement-related features (rhythm/tempo proxies, step-related signals, displacement/direction cues),
- interaction features capturing relationships across channels (e.g., correlation-based features),
- handling problematic values (NaN/Inf) and standardizing feature scales,
- testing non-linear distribution transforms to stabilize skew/heavy tails,
- dimensionality reduction and feature selection.

Outcome: multiple feature-set variants prepared for modelling comparisons.

---

## 3) Modelling

Modelling notebook contains comparative experiments and evaluation:
- baseline vs feature-engineered variants, including the effect of different transformations,
- clustering with multiple families of methods.
- cluster quality assessment using standard internal metrics.
- an auxiliary step: training a supervised model to predict cluster IDs.
- feature impact interpretation using explainability (SHAP) to identify what drives cluster assignment.

Outcome: comparison of modelling approaches and a clearer view of which feature groups carry the most signal.

---

## Key takeaways

- Covers the full ML workflow expected in an introductory ML course: EDA → feature engineering → modelling → interpretation.
- Highlights how scaling/transforms and dimensionality reduction impact clustering quality.
- Uses explainability as a diagnostic tool to understand what differentiates activity-related patterns.