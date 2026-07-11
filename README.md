# Cloud Big Data Infrastructure — Final Project: HR Analytics with PySpark

## Project Overview
An end-to-end big-data pipeline built entirely in PySpark on a 10,000-record × 14-feature HR dataset — EDA, rule-based cleaning, three-method missing-value imputation, K-Means segmentation, and a constraint-aware workforce-decision engine, demonstrating Spark's distributed processing model (`local[*]`).

## Key Features
- **Spark ETL & Data Quality:** Logical-consistency rules, 3σ outlier removal, and label encoding; 22.09% of rows (2,209 of 10,000) arrived with missing values.
- **Three-Method Imputation (Spark MLlib):** Correlation-driven hierarchical mode fill (Work_Mode: 247 → 0 nulls); Gradient-Boosted Trees for salary regression (R² = 0.986), selected over Decision Tree, Random Forest, and Linear Regression; Logistic Regression for department classification — with a documented fallback where no model was accurate enough.
- **Unsupervised Segmentation:** K-Means (Elbow → K = 3), mapping the workforce to three distinct personas.
- **Decision-Support Engine:** Weighted scoring flagging a 15% workforce-reduction cohort (threshold 5.85) under a hard department-distribution constraint — logic designed with LLM assistance, implemented as deterministic PySpark rules.

## Tech Stack
Python · PySpark (Spark SQL, Spark MLlib) · scikit-learn (metrics) · Pandas, NumPy · Matplotlib, Seaborn

## Repository Content
- **`Cloud_Infrastructure_Analysis.ipynb`**: The full pipeline, all outputs embedded.
- **`HR_Employee_Data.txt`**: 10,000 × 14 HR dataset (CSV, no personal identifiers).
- **`Project_Presentation.pdf`**: 32-slide presentation (Hebrew).
