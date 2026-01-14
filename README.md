# Employee-Attrition-Risk-Analysis
Analyzing employee behavior and workload patterns to understand and reduce attrition risk using HR analytics.

# Employee Attrition Risk Analysis

HR analytics case study to explore which factors are associated with employees leaving the company, using behavioral, workload, and compensation data from 14,999 employees.

## Overview

In many organizations, high employee turnover leads to increased hiring costs, knowledge loss, and reduced team productivity. This project analyzes an HR dataset to understand which factors are most strongly associated with attrition, such as satisfaction level, performance evaluation, number of projects, work hours, tenure, and salary bands. [file:12]

The main objective is to use exploratory data analysis (and optionally simple modeling) to help HR teams identify at-risk employee segments and design better retention strategies. [file:12]

## Dataset

- **Source:** HR employee dataset (`employe.csv`), originally shared via Google Drive. [file:12]  
- **Rows:** 14,999 employees. [file:12]  
- **Columns:** 10 features. [file:12]

Key features: [file:12]

- `satisfactoryLevel`: Employee satisfaction level (0–1 scale)  
- `lastEvaluation`: Most recent performance evaluation score (0–1)  
- `numberOfProjects`: Number of projects handled  
- `avgMonthlyHours`: Average monthly work hours  
- `timeSpent.company`: Years spent at the company  
- `workAccident`: Whether the employee had a work accident (0/1)  
- `left`: Whether the employee left the company (1 = left, 0 = stayed)  
- `promotionInLast5years`: Whether the employee was promoted in the last 5 years (0/1)  
- `dept`: Department (e.g., sales, support, technical)  
- `salary`: Salary level (e.g., low, medium, high)  

> Note: The file name in the notebook is `employe.csv`; update the path if you keep it in a `data/` folder. [file:12]

## Objectives

- Inspect and understand the distribution of key HR attributes. [file:12]  
- Compare feature distributions between employees who stayed vs. those who left (`left` variable). [file:12]  
- Identify patterns in satisfaction, workload, and tenure that relate to higher attrition. [file:12]  
- Analyze attrition across departments and salary levels to find vulnerable groups. [file:12]

## Methods and Analysis

The notebook typically includes:

- **Data loading and inspection**  
  - Load the CSV with Pandas and display the first few rows. [file:12]  
  - Check shape, data types, and basic descriptive statistics. [file:12]  
  - Verify missing values across columns.

- **Exploratory data analysis (EDA)**  
  - Distribution plots for `satisfactoryLevel`, `lastEvaluation`, `avgMonthlyHours`, and `timeSpent.company`. [file:12]  
  - Count plots and bar charts for `dept`, `salary`, and the `left` column. [file:12]  
  - Group-by analysis to compare averages for employees who left vs. stayed. [file:12]  
  - Cross-tabulations of `left` by department and salary level. [file:12]

- **Visualization**  
  - Histograms and KDE plots to see how satisfaction and hours differ for those who left. [file:12]  
  - Bar plots for attrition rate by department and salary band. [file:12]  
  - Correlation heatmap for numeric features to see relationships between workload, evaluation, and attrition. [file:12]

- **(Optional) Modeling**  
  - Basic train/test split and simple classification model (e.g., Logistic Regression, Random Forest) to predict `left` and interpret feature importance.

## Tech Stack

- **Language:** Python 3  
- **Libraries:**  
  - `pandas`, `numpy` for data handling  
  - `matplotlib`, `seaborn` for visualization [file:12]  
  - Optionally: `scikit-learn` for basic classification models  
- **Environment:** Jupyter / Google Colab [file:12]

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/<your-username>/employee-attrition-analytics.git
   cd employee-attrition-analytics

2. Create and activate a virtual environment (optional but recommended):
   python -m venv .venv
   source .venv/bin/activate   # On Windows: .venv\Scripts\activate

3. Install dependencies:
   pip install -r requirements.txt

4. Place employe.csv in a data/ folder (or the root) and update the path in the notebook if    necessary.

5. Open the notebook:
   jupyter notebook 9_casestudy_attrition_reduction.ipynb
   or upload it to Google Colab and ensure the CSV path (e.g., /content/employe.csv) is correct.
