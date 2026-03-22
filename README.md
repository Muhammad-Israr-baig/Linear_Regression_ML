# Diabetes Progression Analysis using Multiple Linear Regression

This project contains a professional implementation of a **Multiple Linear Regression** model designed to predict the progression of diabetes. Utilizing the Scikit-Learn diagnostic dataset, the project establishes a predictive mapping between ten physiological variables and a quantitative measure of disease progression.

---
## Technical Overview

The model follows a standard supervised learning pipeline to calculate the relationship between baseline features and the target progression metric:

$$y = \beta_0 + \beta_1x_1 + \beta_2x_2 + \dots + \beta_{10}x_{10} + \epsilon$$

### Dataset Specifications
The analysis utilizes the **Diabetes Dataset**:
* **Sample Size:** 442 instances.
* **Feature Set ($X$):** 10 baseline variables, including Age, Sex, Body Mass Index (BMI), and blood serum measurements.
* **Target Variable ($y$):** A quantitative measure of disease progression recorded one year after the baseline.

---

## Project Workflow

## 1. Data Initialization & Inspection
The dataset is loaded and partitioned into features ($X$) and labels ($y$). Initial shape verification ensures data integrity:
* **Feature Shape:** `(442, 10)`.
* **Label Shape:** `(442,)`.

## 2. Feature Visualization (EDA)
A scatter plot is employed to assess the distribution and potential linearity between a specific feature (index 5 of the transposed data) and the target variable. This step is critical for validating the assumptions of a linear model.



## 3. Model Implementation
The model is constructed using a **train-test split** to evaluate out-of-sample performance:
* **Algorithm:** Ordinary Least Squares (OLS) Linear Regression.
* **Training Ratio:** 80% Training, 20% Testing.
* **Framework:** `sklearn.linear_model.LinearRegression`.

## 4. Performance Metrics
Based on the execution results, the model achieved the following:
* **$R^2$ Score:** Approximately **0.515**, indicating the model explains ~51.5% of the variance in the target data.
* **Intercept ($\beta_0$):** ~152.08.
* **Coefficients ($\beta_n$):** A vector of 10 weights representing the relative impact of each physiological feature.

---
## Installation & Usage

## Prerequisites
Ensure you have a Python environment with the following dependencies installed:

```bash
pip install scikit-learn matplotlib
