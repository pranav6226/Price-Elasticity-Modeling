# Price Elasticity Modeling Using PySpark

This repository contains the code and report for our **Big Data Analytics** project on **Price Elasticity Modelling (PED)** using **PySpark**. The project aims to analyze the relationship between price changes and consumer demand to help businesses optimize their pricing strategies for maximizing revenue.

## Team Members
- **Keerthi Krishna Aiyappan**
- **Himanshu Hegde**
- **Pranav Mahesh Mekal**
- **Sheikh Mohammad Nawazish Khalandar**

## Project Overview

Price Elasticity Modelling (PED) helps businesses understand how demand for a product responds to changes in price. By analyzing price sensitivity, we can identify optimal pricing strategies that balance revenue growth and customer demand.

Key concepts covered:
- **Elastic Demand** (|E| > 1): Highly responsive to price changes.
- **Inelastic Demand** (|E| < 1): Demand remains stable despite price changes.
- **Unitary Elasticity** (|E| = 1): Proportional changes in price and demand.

## Objectives
- Develop a reproducible **price optimization** model to **maximize revenue**.
- Incorporate **non-linear models** to better capture demand-price relationships.
- Integrate **competitor and promotional data** for improved accuracy.
- Implement **PySpark-based modeling** for scalable big data processing.

## Methodology

1. **Data Pre-processing**
   - Handling missing values and outliers.
   - Encoding categorical variables.
   - Using a **time-based split** for maintaining data consistency.

2. **Exploratory Data Analysis (EDA)**
   - Analyzing **price trends** from 2002-2003.
   - Identifying **cross-metric correlations** (e.g., impact of discounts).
   - Comparing **market share** of different manufacturers.

3. **Feature Engineering**
   - Creating **price positioning features**.
   - Adding **historical moving averages** (30, 60, 90-day trends).
   - Incorporating **regional and promotional factors**.

4. **Modeling & Evaluation**
   - Implemented **Random Forest, Decision Tree, and Gradient Boosting Trees**.
   - Optimized hyperparameters for best performance.
   - Evaluated models using **RMSE, MAE, and MAPE**.

| Model            | MedAPE (%) | RMSE | MAE  |
|-----------------|-----------|------|------|
| Random Forest   | 68        | 25   | 20   |
| Gradient Boosting | 66      | 25   | 20   |
| Decision Tree   | 67        | 26   | 21   |

5. **Price Optimization**
   - Used **SciPy optimizers** (L-BFGS-B & SLSQP) due to PySpark limitations.
   - Implemented **constraints** to avoid unrealistic pricing shifts.
   - Modeled **product-specific price adjustments** to maximize revenue.

## Results
- Optimized pricing increased revenue while maintaining product demand.
- Example: For **Product 54163**, reducing price from **$11 → $8** increased quantity sold by **1.6%** and **revenue by 32.1%**.
- Achieved a **4.9% increase** in product quantity sales over a specific time period.

## Challenges
- **Data inconsistencies** limited price variation.
- **PySpark lacked optimizers**, requiring a mix of **Scipy + PySpark**.
- **Memory constraints** required working with a subset of data.

## Files in This Repository
- **`Project_Code.ipynb`** - Jupyter Notebook with all code implementations.
- **`Report.docx`** - Detailed project report with methodology, results, and analysis.
