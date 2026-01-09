# Optimal Oil Well Location Selection

## Overview

This project focuses on selecting the optimal region for drilling new oil wells by balancing **expected profitability** and **financial risk**. Using historical geological and production data, linear regression models and statistical simulation techniques were applied to estimate oil reserves, evaluate potential profits, and quantify uncertainty.

The project represents a complete, end-to-end **data-driven decision-making workflow** for a high-risk, high-investment business scenario.

---

## Problem Statement

Drilling new oil wells requires a large upfront investment and involves significant uncertainty. Selecting an unsuitable region can result in substantial financial losses.

The objective of this project is to **select the best region to drill 200 new oil wells**, maximizing expected net profit while keeping the probability of loss within acceptable limits. The decision is supported by predictive modeling and risk analysis rather than intuition.

---

## Dataset

The data consists of three independent regional datasets, each representing a candidate drilling region.  
Each dataset includes:

- Geological features (`f0`, `f1`, `f2`)
- Oil production volume (`product`)

The datasets were provided within a private academic environment and are therefore not publicly available.

---

## Methodology

### 1. Data Preparation
- Data loading and inspection
- Validation of data types and missing values
- Duplicate detection

### 2. Model Training
- Linear Regression models trained independently for each region
- Train/validation split (75/25)
- Model evaluation using RMSE to assess prediction accuracy

### 3. Well Selection Strategy
- Random sampling of 500 candidate wells per region
- Selection of the top 200 wells based on predicted oil reserves
- Comparison against the minimum production threshold required to avoid losses

### 4. Economic Evaluation
- Calculation of total revenue using actual production values
- Net profit estimation after subtracting total investment
- Comparison of expected profitability across regions

### 5. Risk Analysis
- Bootstrapping with 1,000 simulations per region
- Estimation of:
  - Expected net profit
  - 95% confidence intervals
  - Probability of financial loss

### 6. ROI Calculation
- Return on Investment (ROI) computed for the selected region
- Interpretation of profitability per dollar invested

---

## Evaluation Metrics

- **RMSE (Root Mean Squared Error):** Measures predictive accuracy of regression models  
- **Expected Net Profit:** Average profit across simulated scenarios  
- **Risk of Loss:** Percentage of simulations resulting in negative profit  
- **Confidence Intervals:** 95% interval to quantify uncertainty  
- **ROI:** Financial efficiency of the investment  

---

## Results

- All regions exceeded the minimum production threshold required to avoid losses.
- **Region 1** demonstrated:
  - The highest expected net profit
  - A 95% confidence interval entirely above zero
  - Practically zero probability of loss
- The estimated ROI for the selected region was approximately **5.25%**, meaning that for each dollar invested, about 5 cents of net profit are expected.

---

## Conclusions

The analysis indicates that **Region 1** is the optimal choice for drilling new oil wells, as it combines high expected profitability with minimal financial risk.

This project demonstrates the importance of integrating machine learning predictions with **statistical risk analysis** when making high-stakes business decisions. By incorporating uncertainty and downside risk, the final decision becomes more robust, realistic, and defensible.

---

## Technologies Used

- Python  
- pandas  
- NumPy  
- scikit-learn  
- Jupyter Notebook  
