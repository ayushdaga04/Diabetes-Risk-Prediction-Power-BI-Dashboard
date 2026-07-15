# Diabetes-Risk-Prediction-Power-BI-Dashboard
CDC BRFSS 2015 Health Indicators — 253,680 records  Predicting diabetes risk from self-reported health indicators, and an interactive Power BI dashboard built on the same data.
Project Overview

Diabetes affects 38M+ Americans, and clinical testing is costly and inaccessible for many. This project asks: can self-reported survey data predict diabetes risk? Using the CDC's Behavioral Risk Factor Surveillance System (BRFSS 2015) dataset — 253,680 responses, 21 health and demographic features — we built and compared four machine learning models, then turned the dataset into an interactive Power BI dashboard.

Key Results


Best model: Gradient Boosting — 85% accuracy, 0.8156 AUC
Compared against Logistic Regression (AUC 0.808), Random Forest (0.810), Decision Tree (0.798)
Strongest predictors: BMI, high blood pressure, high cholesterol, difficulty walking, age category — consistent with established clinical research
Feature selection via Chi-Square + Mutual Information (top 15 features); class weighting to handle the 194K/35K class imbalance
Evaluated with AUC rather than accuracy alone, because the imbalanced classes make accuracy misleading


Power BI Dashboard

Interactive dashboard built as a dimensional model on the same dataset:


Star schema: fact table (253,680 survey records) + Age, Income, and Education dimension tables
DAX measures using CALCULATE / DIVIDE / ALL — diabetes rate, respondent counts, rate-vs-overall comparison
Finding surfaced by the model: overall diabetes rate ~14%, dropping to ~8% in the highest income bracket — the income–health relationship is visible in two clicks
File: dashboard/CDC_Diabetes_Dashboard.pbix — open with Power BI Desktop (free)
<img width="868" height="485" alt="Screenshot 2026-07-14 at 10 08 19 PM" src="https://github.com/user-attachments/assets/d65763ea-5500-4e63-93f2-c8625452cbc9" />

