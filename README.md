# Predicting Customer Churn: A Machine Learning Approach Using Logistic Regression and Random Forest

## Project Overview

![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![RStudio](https://img.shields.io/badge/RStudio-75AADB?style=for-the-badge&logo=rstudio&logoColor=white)
![Tidyverse](https://img.shields.io/badge/Tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white)
![ggplot2](https://img.shields.io/badge/ggplot2-5C0C0C?style=for-the-badge)
![caret](https://img.shields.io/badge/caret-1F78D3?style=for-the-badge)
![randomForest](https://img.shields.io/badge/randomForest-0D7029?style=for-the-badge)
![pROC](https://img.shields.io/badge/pROC-3B99CD?style=for-the-badge)
![patchwork](https://img.shields.io/badge/patchwork-5C0C0C?style=for-the-badge)

<!-- Text-based badges for packages without common logos -->
![glmnet](https://img.shields.io/badge/glmnet-8C0D73?style=for-the-badge)
![ROSE](https://img.shields.io/badge/ROSE-C7245A?style=for-the-badge)
![scales](https://img.shields.io/badge/scales-2F6C9C?style=for-the-badge)
![car](https://img.shields.io/badge/car-9D442D?style=for-the-badge)

This project was made with the goal of predicting customer churn for a telecom company (Telco) using machine learning. Customer churn is a critical business problem, because getting new customers is more expensive than retaining existing ones. By analyzing customer data, this project identifies key factors influencing churn and builds predictive models to flag at-risk customers, which can be used to inform proactive retention strategies.

The analysis compares two machine learning models:
1.  **LASSO Logistic Regression** 
2.  **Random Forest** 

## Repository Structure

- Data/  
  - `Telco Customer Churn Dataset.csv` — Raw dataset (from Kaggle)  
- Code/  
  - `R-Code Output` — Rmd File Knitted into a pdf  
  - `Telco Churn Analysis.Rmd` — R Markdown report with visualizations  
- Report/  
  - `Predicting Customer Churn.pdf` — Final report with analysis, visualizations, and conclusions  
- README.md — This file  

## Key Objectives

1.  **Predict Churn:** Build a classification model to accurately predict if a customer will churn.
2.  **Compare Models:** Evaluate and compare the performance of Logistic Regression and Random Forest models.
3.  **Identify Drivers:** Uncover the most important factors leading to customer churn to inform business strategy.

## Installation & Setup

### Prerequisites

To run this code, you need to have **R** and **RStudio** installed on your machine.

1.  **Install R:** [https://cran.r-project.org/](https://cran.r-project.org/)
2.  **Install RStudio (Desktop):** [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)

### Required R Packages

Run the following command in your R console to install all necessary packages:

```r
install.packages(c(
  "dplyr",
  "ggplot2",       
  "scales",         
  "patchwork",      
  "glmnet", 
  "caret",         
  "pROC",
  "ROSE",
  "randomForest",
  "car"
))
```

## Dataset

- **Source:** IBM Telco Customer Churn Dataset on Kaggle  
- **Link:** [https://www.kaggle.com/datasets/blastchar/telco-customer-churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
- **Description:** The dataset contains 7,043 customer records with 21 attributes, including demographic information, account details, and services subscribed. The target variable is **Churn**, indicating whether the customer left the company.  

## Key Findings & Business Implications

The analysis revealed that the most significant drivers of churn are:  
- **Low Tenure:** New customers are at the highest risk.  
- **Contract Type:** Month-to-month contracts have significantly higher churn rates.  
- **Internet Service:** Fiber optic customers are more likely to churn, potentially due to cost or competition.  
- **Payment Method:** Paying by electronic check is associated with higher churn.  
- **Lack of Add-on Services:** Customers without online security, tech support, backup, or device protection are more likely to leave.  

### Recommended Business Actions
- Incentivize long-term contracts for month-to-month customers.  
- Proactively engage with high-risk segments (e.g., fiber optic users, electronic check payers).  
- Improve service value by bundling essential add-ons.  
- Use the Random Forest model to generate a target list for retention campaigns.  

## Model Performance Summary

| Model                    | Accuracy | Sensitivity (Recall) | Precision | AUC  |
|---------------------------|----------|----------------------|-----------|------|
| LASSO Logistic Regression | 0.74     | 0.79                 | 0.51      | 0.819|
| Random Forest             | 0.69     | 0.86                 | 0.45      | 0.82 |

- **Random Forest** is recommended for *proactive identification* of likely churners due to its higher recall.  
- **Logistic Regression** is best for *understanding the key drivers* behind churn.  

## Limitations & Future Work

- **Data Limitations:** The dataset is a single snapshot in time; lacks service history or support interactions.  
- **Causality:** Models identify correlations, not causation.  
- **Class Imbalance:** Churn is a rare event, limiting precision.  

### Future Work
- Incorporate temporal data and customer service interactions.  
- Test advanced models like **Gradient Boosting Machines (XGBoost)** for improved performance.  




