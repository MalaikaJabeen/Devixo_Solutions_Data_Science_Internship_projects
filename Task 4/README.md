#  Financial Performance Analysis — Top 2,000 Companies (2024)

##  Project Overview

This project analyzes the **financial performance of 2,000 companies in 2024** using Python for data cleaning, exploratory data analysis, feature engineering, and statistical analysis, followed by an **interactive Power BI dashboard** for business-focused visualization.

The analysis focuses on company profitability, financial scale, asset efficiency, market valuation, and differences across countries.

The project was completed as part of a **Business Analytics project/internship task**.

---

##  Objectives

The main objectives of this project are to:

* Clean and prepare the raw financial dataset
* Identify missing values and duplicate records
* Correct inappropriate data types
* Detect potential outliers
* Perform exploratory data analysis (EDA)
* Compare companies based on sales, profit, assets, and market value
* Analyze country-level financial performance
* Create meaningful financial performance metrics
* Identify profitable and loss-making companies
* Examine relationships between financial variables
* Build an interactive Power BI dashboard
* Generate business insights and recommendations
* Develop a basic machine learning model for profit prediction

---

##  Dataset

**Dataset:** `Top 2000 Companies Financial Data 2024.csv`

The dataset contains approximately **2,000 companies** and includes the following main variables:

| Column         | Description                 |
| -------------- | --------------------------- |
| `Name`         | Company name                |
| `Country`      | Country of the company      |
| `Sales`        | Company sales               |
| `Profit`       | Company profit              |
| `Assets`       | Total company assets        |
| `Market Value` | Market value of the company |

The original dataset also contained an `Unnamed: 0` column, which was removed during data cleaning because it represented an unnecessary index.

###  Dataset Limitation

The dataset represents a **2024 financial snapshot**. Therefore, genuine year-over-year growth or historical trends cannot be calculated from this dataset alone.

---

#  Part 1 — Data Cleaning & Preparation

The raw dataset was prepared using **Python and Pandas**.

### Cleaning steps included:

* Removed the unnecessary `Unnamed: 0` column
* Checked for missing values
* Handled missing company and country information
* Checked and removed duplicate records
* Converted financial columns to appropriate numeric data types
* Investigated potential outliers using the **IQR method**
* Verified the final dataset before analysis

### Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

---

#  Feature Engineering

Several additional financial metrics were created to provide deeper analysis.

### 1. Profit Margin

Measures the percentage of sales retained as profit.

```text
Profit Margin = (Profit / Sales) × 100
```

### 2. Return on Assets (ROA)

Measures how effectively a company generates profit from its assets.

```text
ROA = (Profit / Assets) × 100
```

### 3. Asset Turnover

Measures how efficiently company assets generate sales.

```text
Asset Turnover = Sales / Assets
```

### 4. Market Value to Sales

Measures market valuation relative to sales.

```text
Market Value / Sales
```

### 5. Market Value to Assets

Measures market valuation relative to total assets.

```text
Market Value / Assets
```

### 6. Profitability Status

Companies were classified as:

* **Profitable**
* **Loss**
* **Break-even**

### 7. Company Size

Companies were categorized into four groups based on sales:

* Small
* Medium
* Large
* Very Large

### 8. Companies in Country

A country-level company count was created to support regional analysis.

---

#  Part 2 — Exploratory Data Analysis

The EDA investigates the distribution, relationships, and patterns within the financial data.

### Key visualizations include:

1. Sales distribution
2. Profit distribution
3. Market Value distribution
4. Top 10 companies by Sales
5. Top 10 companies by Profit
6. Top 10 companies by Market Value
7. Number of companies by Country
8. Average Profit by Country
9. Average Sales by Country
10. Profit Margin distribution
11. Sales vs Profit
12. Assets vs Market Value
13. Sales vs Market Value
14. Profitability Status distribution
15. Company Size distribution
16. ROA distribution
17. Asset Turnover distribution
18. Correlation Heatmap

Detailed findings from these analyses are documented in the project notebook.

---

#  Part 3 — Key Performance Indicators (KPIs)

The project uses financial KPIs relevant to the available dataset.

### Main KPIs

* **Total Sales**
* **Total Profit**
* **Total Assets**
* **Total Market Value**
* **Average Sales**
* **Average Profit**
* **Overall Profit Margin**
* **Average ROA**
* **Average Asset Turnover**
* **Number of Companies**
* **Number of Countries**
* **Profitable Companies**
* **Loss-Making Companies**

### Overall Profit Margin

```text
Overall Profit Margin =
Total Profit / Total Sales × 100
```

This is calculated using aggregated sales and profit rather than simply averaging individual company margins.

---

#  Part 4 — Power BI Dashboard

A two-page **Power BI dashboard** was built to present the main numbers and charts from the analysis in a simple, business-friendly layout.

##  Page 1 — Companies Financial Analysis

![Companies Financial Analysis](images/Dashboard_1.png)

A general overview of company finances.

### KPI Cards

* Average Sales — 26.22
* Average Profit — 4.02
* Average Market Value — 45.00
* Average Assets — 119.09

### Visuals

* **Profit Margin Per Country** — distribution of profit margin values
* **Financial Size Comparison** — sum of profit and sum of assets compared against market value
* **Market Value vs Assets** — scatter plot with each company shown as a point

---

##  Page 2 — Sales Analysis

![Sales Analysis](images/Dashboard_2.png)

Focuses on company sales and how sales relate to market value and country.

### KPI Cards

* Average Sales — 26.22
* Total Sales — 51,683.80
* Highest Sales — 657.30
* Number of Companies — 2,001

### Visuals

* **Sales vs Market Value** — scatter plot by company
* **Sales by Country** — distribution of sales across countries
* **Sales by Country Map** — geographic view of sales
* **Top 10 Companies by Sales** — led by Walmart, Amazon, Sinopec and PetroChina

---

#  Bonus — Machine Learning

A basic **Linear Regression** model was developed to investigate whether company financial scale can be used to predict profit.

### Features

* Sales
* Assets
* Market Value

### Target

* Profit

### Model

```text
Linear Regression
```

The dataset was cleaned for missing values before training the model.

### Evaluation Metrics

The model was evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

The model is intended primarily as an analytical experiment rather than a production-grade financial forecasting system.

---

#  Business Questions

This project aims to answer questions such as:

1. Which companies generate the highest sales?
2. Which companies generate the highest profit?
3. Which companies have the highest market value?
4. Which countries contain the largest number of companies?
5. How does financial performance vary across countries?
6. Are companies with higher sales necessarily more profitable?
7. How strongly are sales related to profit?
8. How does market value relate to sales and assets?
9. Which companies have the strongest profit margins?
10. Which companies use their assets most efficiently?
11. How does profitability differ across company sizes?
12. How are financial scale and market valuation related?

> **Note:** Detailed insights and actionable recommendations are provided separately in the project notebook.

---

#  Tools & Technologies

| Tool             | Purpose                                   |
| ---------------- | ----------------------------------------- |
| Python           | Data analysis and preprocessing           |
| Pandas           | Data manipulation                         |
| NumPy            | Numerical calculations                    |
| Matplotlib       | Data visualization                        |
| Seaborn          | Statistical visualization                 |
| Scikit-learn     | Machine learning                          |
| Power BI         | Interactive dashboard                     |
| Jupyter Notebook | Analysis environment                      |
| GitHub           | Project version control and documentation |

---

#  Project Structure

```text
Financial-Performance-Analysis/
│
├── Top 2000 Companies Financial Data 2024.csv
├── Financial_Performance_Analysis.ipynb
├── Financial_Performance_Dashboard.pbix
├── README.md
└── images/
    ├── Dashboard_1.png
    └── Dashboard_2.png
```

---

#  Conclusion

This project provides an end-to-end **financial analytics workflow**, starting from raw data preparation and exploratory analysis in Python and progressing to financial KPI development, machine learning experimentation, and interactive Power BI reporting.

The analysis combines **profitability, efficiency, company scale, country-level performance, and market valuation** to provide a comprehensive view of corporate financial performance.

The project demonstrates practical skills in:

* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Financial Analytics
* Data Visualization
* KPI Development
* Power BI Dashboard Development
* Machine Learning

Detailed analysis, insights, and recommendations are available in the accompanying **Jupyter Notebook**.

---

##  Author

**Malaika Jabeen**

BS Computer Science
Data Science & Data Analytics Enthusiast
