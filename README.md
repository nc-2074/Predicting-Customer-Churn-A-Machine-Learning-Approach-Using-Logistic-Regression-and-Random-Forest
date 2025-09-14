# Predicting Customer Churn: A Machine Learning Approach Using Logistic Regression and Random Forest

## Project Overview

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




