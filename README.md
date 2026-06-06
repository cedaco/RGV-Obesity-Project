# RGV-Obesity-Project

A data-driven public health analysis examining obesity prevalence in Hidalgo County, Texas and the Rio Grande Valley region relative to Texas and national benchmarks.

## Overview
This project uses CDC PLACES 2024 county-level data to investigate the structural and behavioral drivers of elevated obesity rates in Hidalgo County, TX — which ranks in the 94th percentile nationally for obesity prevalence (44.2% vs. 37.4% national average). The analysis is designed to inform clinical providers and public health officials on where to focus intervention efforts.

## Methods

- Descriptive statistics — Hidalgo vs. Texas vs. national comparison
- One-sample t-tests for statistical significance
- Linear regression with residual analysis
- Logistic regression, Decision Tree, and Random Forest classification
- ROC curve analysis (Random Forest AUC: 0.9097)
- Principal Component Analysis (PCA) + K-Means clustering
- Pearson correlation analysis
- Monte Carlo simulation (10,000 iterations) for intervention modeling

## Key Findings

- Hidalgo County ranks 153rd out of 3,143 U.S. counties for obesity (94th percentile)
- The linear regression model predicts 36.32% obesity for Hidalgo based on its risk profile — the actual rate of 44.20% represents a +7.88 percentage point residual, suggesting unmeasured structural drivers (poverty, food desert access)
- Four variables where Hidalgo most significantly exceeds national averages: physical inactivity, short sleep duration, diabetes prevalence, and uninsured rate
- Monte Carlo simulation estimates a −7.18% reduction in obesity (95% CI: 2.65%–11.48%) if all four variables are simultaneously reduced to national average levels

## Data Source
CDC PLACES 2024 County Release — accessed via public API:
https://data.cdc.gov/resource/i46a-9kgh.csv?$limit=50000

No API key required.

## Requirements
- pandas
- numpy
- matplotlib
- seaborn
- scipy
- scikit-learn

## Usage
Open rgv_obesity_analysis.ipynb in Google Colab and run all cells sequentially. No local file uploads required — data is fetched directly from the CDC API.

## Report
A full PDF report suitable for clinical and public health audiences is included in this repository, covering methodology, results, clinical recommendations, and limitations in great depth.
