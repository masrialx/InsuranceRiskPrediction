# Insurance Risk Prediction Project

Welcome to the **Insurance Risk Prediction** project! This repository contains the code and resources for tasks related to Exploratory Data Analysis (EDA), Data Version Control (DVC), CI/CD with GitHub Actions, A/B Hypothesis Testing, and Statistical Modeling.

## Table of Contents
- [Project Overview](#project-overview)
- [Task 1: Git and GitHub](#task-1-git-and-github)
  - [Git Version Control](#git-version-control)
  - [CI/CD with GitHub Actions](#cicd-with-github-actions)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Task 2: Data Version Control (DVC)](#task-2-data-version-control-dvc)
  - [Install DVC](#install-dvc)
  - [Set Up Local Remote Storage](#set-up-local-remote-storage)
  - [Add Data](#add-data)
- [Task 3: A/B Hypothesis Testing](#task-3-ab-hypothesis-testing)
  - [Select Metrics](#select-metrics)
  - [Data Segmentation](#data-segmentation)
  - [Statistical Testing](#statistical-testing)
  - [Analyze and Report](#analyze-and-report)
- [Task 4: Statistical Modeling](#task-4-statistical-modeling)
  - [Data Preparation](#data-preparation)
  - [Modeling Techniques](#modeling-techniques)
  - [Model Building](#model-building)
  - [Model Evaluation](#model-evaluation)
  - [Feature Importance Analysis](#feature-importance-analysis)
- [Getting Started](#getting-started)
- [Key Performance Indicators (KPIs)](#key-performance-indicators-kpis)

## Project Overview
This project aims to analyze insurance data and predict risk factors. The tasks have been divided into four main sections: Git and GitHub setup for version control, CI/CD pipelines, data analysis using Exploratory Data Analysis (EDA) and Data Version Control (DVC), A/B Hypothesis Testing, and Statistical Modeling.

## Task 1: Git and GitHub

### Git Version Control
The first step is to establish version control for the project using Git and GitHub. This includes:
- Creating a GitHub repository.
- Committing changes frequently to document the progress.
- Creating a new branch `task-1` for day 1 analysis.
- Writing descriptive commit messages to explain each change.

### CI/CD with GitHub Actions
We set up GitHub Actions to automate the process of testing and deploying the code. The actions will run tests whenever changes are made and ensure that the project is always in a deployable state.

### Exploratory Data Analysis (EDA)
Exploratory Data Analysis (EDA) is the key to understanding the data and discovering insights. In this task, we will perform several analyses:
- **Data Summarization:**
  - Descriptive statistics (mean, median, standard deviation, etc.) for numerical features such as TotalPremium, TotalClaim.
  - Data structure check to ensure variables are correctly formatted.
- **Data Quality Assessment:**
  - Checking for missing values and handling them appropriately.
- **Univariate Analysis:**
  - Plotting histograms for numerical columns.
  - Plotting bar charts for categorical columns.
- **Bivariate or Multivariate Analysis:**
  - Exploring relationships between variables like `TotalPremium` and `TotalClaims` using scatter plots and correlation matrices.
- **Outlier Detection:**
  - Using box plots to detect outliers in numerical data.
- **Trends Over Geography:**
  - Analyzing changes in insurance cover type, premium, auto make, etc., across different geographical regions.

### Data Visualization
- Create at least **3 beautiful plots** to highlight key insights from the analysis.

## Task 2: Data Version Control (DVC)

### Install DVC
To begin versioning our data, we install **DVC (Data Version Control)** with the following command:
```bash
pip install dvc
```

### Set Up Local Remote Storage
1. Create a storage directory to store the versioned data.
```bash
mkdir ./dvc_storage
```
2. Set up the local storage as a DVC remote:
```bash
dvc remote add -d localstorage ./dvc_storage
```

### Add Data
1. Add your dataset (e.g., `data.csv`) to the project directory and track it with DVC:
```bash
dvc add data.csv
```
2. Commit the changes to version control:
```bash
git add data.csv.dvc
git commit -m "Task-2: Added data and started tracking with DVC"
```

### Push Data to Local Remote
Push your versioned data to the local storage:
```bash
dvc push
```

## Task 3: A/B Hypothesis Testing

### Select Metrics
Choose the key performance indicator (KPI) that will measure the impact of the features being tested.

### Data Segmentation
- **Group A (Control Group):** Plans without the feature.
- **Group B (Test Group):** Plans with the feature.
- For features with more than two classes, you may need to select two categories to split the data as Group A and Group B. Ensure the two groups are statistically equivalent except for the feature being tested.

### Statistical Testing
- Conduct appropriate tests such as chi-squared for categorical data or t-tests/z-tests for numerical data.
- Analyze the p-value from the statistical test:
  - If p-value < 0.05, reject the null hypothesis.
  - If p-value >= 0.05, fail to reject the null hypothesis.

### Analyze and Report
Analyze the statistical outcomes to determine if there's evidence to reject the null hypotheses. Document all findings and interpret the results within the context of their impact on business strategy and customer experience.

## Task 4: Statistical Modeling

### Data Preparation
- **Handling Missing Data:** Impute or remove missing values.
- **Feature Engineering:** Create new features that might be relevant to TotalPremium and TotalClaims.
- **Encoding Categorical Data:** Use one-hot encoding or label encoding to make categorical data suitable for modeling.
- **Train-Test Split:** Divide the data into a training set and a test set, typically using a 70:30 or 80:20 ratio.

### Modeling Techniques
- **Linear Regression**
- **Decision Trees**
- **Random Forests**
- **Gradient Boosting Machines (GBMs):**
  - **XGBoost**

### Model Building
- Implement the selected models (Linear Regression, Random Forests, and XGBoost).

### Model Evaluation
- Evaluate each model using appropriate metrics like accuracy, precision, recall, and F1-score.

### Feature Importance Analysis
- Analyze which features are most influential in predicting retention.
- Use SHAP (SHapley Additive exPlanations) or LIME (Local Interpretable Model-agnostic Explanations) to interpret the model's predictions.

### Report Comparison Between Each Model's Performance

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/yourusername/InsuranceRiskPrediction.git
cd InsuranceRiskPrediction
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

3. Make sure you have DVC installed and set up for version control:
```bash
pip install dvc
```

4. To run the analyses, follow the instructions in the project’s individual notebooks or scripts in the repository.

## Key Performance Indicators (KPIs)

### Task 1 KPIs:
- **Dev Environment Setup:** Successfully set up the project environment and GitHub repository.
- **Relevant Skill Demonstrated:** Proficiency in Git, GitHub, and CI/CD with GitHub Actions.
- **Exploratory Data Analysis (EDA):**
  - Clear and accurate summary of the data.
  - Use of statistical methods for data understanding.
  - Visualizing key trends and insights from the data.

### Task 2 KPIs:
- **Data Versioning:** Successful setup and use of DVC for data tracking.
- **Commit Messages:** Well-defined commit messages and version control of data changes.
- **Data Push to Remote:** Successful push of versioned data to the DVC remote storage.

### Task 3 KPIs:
- **Hypothesis Testing:** Successful implementation of A/B testing for different hypotheses.
- **Statistical Analysis:** Proper statistical testing and correct interpretation of p-values.
- **Reporting:** Clear and concise documentation of findings and their impact on business strategy.

### Task 4 KPIs:
- **Data Preparation:** Handling missing data and proper feature engineering.
- **Model Building:** Successful implementation of various machine learning models.
- **Model Evaluation:** Evaluation of models with appropriate metrics.
- **Model Interpretability:** Use of SHAP or LIME for feature importance analysis and model interpretation.

### Key Points in this `README.md`:
- Clear sections for all four tasks.
- Instructions for getting started with the repository and setting up the environment.
- Defined KPIs that explain the key objectives for each task.
- Friendly and helpful language for easy understanding.
