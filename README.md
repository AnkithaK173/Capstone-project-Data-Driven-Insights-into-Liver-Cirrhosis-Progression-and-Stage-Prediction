# Capstone-project-Data-Driven-Insights-into-Liver-Cirrhosis-Progression-and-Stage-Prediction


## Overview

This project aims to uncover insights into liver cirrhosis progression and predict its stages using Python for exploratory data analysis (EDA) and machine learning models. Additionally, it integrates SQL for structured queries and Power BI for intuitive visualizations, providing a comprehensive analysis of liver cirrhosis data.

## Objectives

- Perform detailed data cleaning and preprocessing.
- Conduct exploratory data analysis (EDA) to analyze trends and feature relationships.
- Develop machine learning models to accurately predict cirrhosis stages.
- Extract insights from the dataset using SQL queries.
- Build interactive dashboards using Power BI for decision-making.

## Dataset

- **Name:** Liver Cirrhosis Progression Dataset
- **Description:** Contains demographic, clinical, and lab data of liver cirrhosis patients.
- **Attributes:** Includes features like Age, Gender, Stage, Bilirubin, Albumin, and Prothrombin Time.
- **File Format:** CSV

## Project Workflow

### Step 1: Data Cleaning

- **Handle Missing Values:** Imputation with mean or mode as appropriate for missing numerical and categorical values.
- **Remove Duplicates:** Ensured that duplicate records were removed for accurate analysis.
- **Outliers:** Managed outliers to prevent data skew.
- **Normalization and Scaling:** Applied to numerical data for uniformity across features.

### Step 2: Exploratory Data Analysis (EDA)

- **Visualizations:**
  - Distribution plots for features such as Age, Bilirubin, Albumin.
  - Heatmaps to understand correlations between features.
  - Bar charts for stage-wise patient distribution.
  
- **Insights:** 
  - Gender-based distribution and its relation to liver cirrhosis stages.
  - Key correlations between lab results (Bilirubin, Albumin, Prothrombin Time) and cirrhosis stages.

### Step 3: Machine Learning

- **Algorithms Used:**
  - Logistic Regression
  - Decision Trees
  - Random Forest
  - Gradient Boosting
  
- **Metrics for Model Evaluation:**
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  
- **Outcome:** 
  - Achieved a [insert accuracy here]% prediction accuracy with the best model.
  - The model demonstrated reliable stage prediction.

### Step 4: SQL Querying

- **Data Import:** The cleaned dataset was imported into MySQL for structured querying.
- **SQL Queries Performed:**
  - Gender and stage-wise distribution.
  - Average lab results by cirrhosis stage.
  - Patient segmentation by age group.

  _[Detailed SQL queries are provided below.]_

### Step 5: Power BI Visualization

- Designed interactive dashboards to visualize:
  - Gender and stage distributions.
  - Trends in lab test values.
  - KPIs for extreme cases.
  
- Enabled filtering by patient demographics and cirrhosis stages, making the dashboards dynamic and user-friendly.

## Key Results

- **Key Predictors:** Identified Bilirubin, Albumin, and Prothrombin Time as significant predictors of cirrhosis stages.
- **Model Accuracy:** Achieved [insert accuracy here]% prediction accuracy with the best-performing model.
- **Operational Insights:** Created actionable SQL queries for operational insights, helping clinicians understand key metrics and trends.
- **Power BI Dashboard:** Developed a comprehensive dashboard that allows healthcare professionals to make data-driven decisions about patient management.

## Tools and Technologies

- **Python:** pandas, matplotlib, seaborn, scikit-learn
- **SQL:** MySQL for database management and queries
- **Power BI:** Data visualization and dashboard creation

## Conclusion

This project demonstrates the power of data-driven insights in healthcare. Through EDA and machine learning, it uncovers trends and builds reliable prediction models for cirrhosis staging. The integration of SQL and Power BI provides a holistic view of patient data, enabling actionable insights for clinicians to improve patient outcomes.

---

### Detailed SQL Queries

1. **Gender and Stage-wise Distribution:**
   ```sql
   SELECT Gender, Stage, COUNT(*) as Patient_Count
   FROM cirrhosis_data
   GROUP BY Gender, Stage;
