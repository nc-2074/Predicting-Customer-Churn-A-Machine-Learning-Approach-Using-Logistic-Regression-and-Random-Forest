# Predicting Customer Churn A Machine Learning Approach Using Logistic Regression and Random Forest

## 📖 Project Overview

This project aims to predict customer churn for a telecom company (Telco) using machine learning. Customer churn is a critical business problem, as acquiring new customers is far more expensive than retaining existing ones. By analyzing customer data, this project identifies key factors influencing churn and builds predictive models to flag at-risk customers, enabling proactive retention strategies.

The analysis compares two machine learning models:
1.  **LASSO Logistic Regression** (for interpretability and identifying key drivers).
2.  **Random Forest** (for high predictive performance and capturing complex patterns).

## 📁 Repository Structure

Telco-Customer-Churn-Prediction/
│
├── Data/
│ └── telco_churn_data.csv # Raw dataset (from Kaggle)
│
├── Code/
│ ├── Telco_Churn_Analysis.R # Main R script for data cleaning, EDA, and modeling
│ └── Telco_Churn_Analysis.Rmd # R Markdown file for generating the report with visualizations
│
├── Output/
│ ├── Predicting_Customer_Churn.pdf # Final report with full analysis, visualizations, and conclusions
│
└── README.md # This file


## 🎯 Key Objectives

1.  **Predict Churn:** Build a classification model to accurately predict if a customer will churn.
2.  **Compare Models:** Evaluate and compare the performance of Logistic Regression and Random Forest models.
3.  **Identify Drivers:** Uncover the most important factors leading to customer churn to inform business strategy.

## 🔧 Installation & Setup

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


