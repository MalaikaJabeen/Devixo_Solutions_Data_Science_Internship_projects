# Vehicle Pricing Analysis & Interactive Dashboard

##  Project Overview

This project was developed as part of **Week 3 of the Data Science Internship at Devixo Solutions**.

The project focuses on transforming raw vehicle data into meaningful business insights through **data exploration, data validation, feature engineering, KPI calculation, exploratory analysis, and an interactive dashboard**.

The dataset contains **5,000 vehicle records and 7 original attributes**, including manufacturer, model, engine size, fuel type, year of manufacture, mileage, and price.

The project also includes a **bonus machine learning component** that uses vehicle characteristics to predict vehicle prices.

---

##  Objectives

* Explore and understand the raw vehicle dataset
* Validate data quality and consistency
* Perform feature engineering
* Calculate relevant business KPIs
* Analyze vehicle manufacturers, models, fuel types, mileage, age, engine size, and prices
* Identify meaningful business insights
* Develop an interactive dashboard
* Provide business recommendations based on the analysis
* Build a predictive vehicle-price model as a bonus

---

##  Dataset

The dataset contains **5,000 rows and 7 columns**.

### Original Features

| Feature               | Description                                                       |
| --------------------- | ----------------------------------------------------------------- |
| `Manufacturer`        | Vehicle manufacturer, such as Ford, Porsche, Toyota, VW, and BMW  |
| `Model`               | Vehicle model, such as Fiesta, 718 Cayman, Mondeo, RAV4, and Polo |
| `Engine size`         | Engine displacement in liters                                     |
| `Fuel type`           | Fuel type such as Petrol, Diesel, or Hybrid                       |
| `Year of manufacture` | Year in which the vehicle was manufactured                        |
| `Mileage`             | Vehicle mileage                                                   |
| `Price`               | Listed vehicle price in US dollars                                |

---

##  Data Validation

The dataset was validated for:

* Data types
* Missing values
* Duplicate records
* Duplicate column names
* Invalid numerical values
* Categorical consistency
* Potential outliers

No missing values or duplicate records were identified during validation.

Potential outliers in variables such as price and mileage were investigated rather than automatically removed, as extreme observations may represent genuine vehicles in the market.

---

##  Feature Engineering

Several additional features were created to support deeper analysis:

* `Vehicle_Age`
* `Mileage_per_Year`
* `Price_per_Mile`
* `Engine_Category`
* `Mileage_Category`
* `Age_Category`
* `Price_Category`

These engineered features help segment vehicles and identify relationships between vehicle characteristics and pricing.

---

##  KPI Analysis

Key Performance Indicators calculated for the dataset include:

* Total Vehicles
* Average Vehicle Price
* Median Vehicle Price
* Average Mileage
* Average Vehicle Age
* Average Engine Size

These KPIs provide a quick overview of the vehicle dataset and are used as key metrics in the dashboard.

---

##  Exploratory Analysis

The analysis investigates:

### Manufacturer Analysis

* Which manufacturers have the most vehicles?
* Which manufacturers have the highest average prices?
* Which manufacturers dominate the premium price segment?

### Model Analysis

* Which models have the highest average prices?
* Which models have the highest number of listings?

### Vehicle Characteristics

* Relationship between mileage and price
* Relationship between vehicle age and price
* Relationship between engine size and price
* Differences in price across fuel types

### Price Segmentation

Vehicles were categorized into different price segments to examine the characteristics of budget, mid-range, and premium vehicles.

---

##  Interactive Dashboard

An interactive dashboard was developed to present the major findings in a clear and business-oriented format.

### Dashboard Components

**KPI Cards**

* Total Vehicles
* Average Price
* Median Price
* Average Mileage
* Average Vehicle Age

**Visual Analysis**

* Vehicles by Manufacturer
* Average Price by Manufacturer
* Top Models by Average Price
* Mileage vs Price
* Vehicle Age vs Price
* Engine Size vs Price
* Average Price by Fuel Type
* Premium Vehicles by Manufacturer

The dashboard allows users to explore the vehicle market from different perspectives and identify pricing patterns.

---

##  Business Insights

The analysis produces **15 business insights** covering:

* Manufacturer distribution
* Vehicle pricing
* Model-level pricing
* Mileage
* Vehicle age
* Engine size
* Fuel type
* Premium vehicle distribution

The insights are derived directly from the dataset and visual analysis.

---

##  Business Recommendations

Based on the findings, **10 data-driven business recommendations** are provided.

These recommendations focus on areas such as:

* Vehicle pricing
* Premium-market positioning
* Manufacturer strategy
* Mileage considerations
* Vehicle age
* Fuel-type trends
* Inventory segmentation

---

##  Bonus: Predictive Vehicle Price Modeling

The original internship task mentions creating a predictive sales trend. However, this dataset does not contain sales dates, sales quantities, or transaction-level revenue data.

Therefore, the bonus component is implemented as a **Predictive Vehicle Price Model**.

### Target Variable

```text
Price
```

### Input Features

* Manufacturer
* Model
* Engine Size
* Fuel Type
* Year of Manufacture
* Mileage

Categorical variables are encoded for machine-learning purposes.

### Model

A **Random Forest Regressor** is used to predict vehicle prices.

### Evaluation Metrics

The model is evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

The model's performance is evaluated on a separate test dataset to measure how well it generalizes to unseen vehicle records.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Jupyter Notebook**
* **Interactive Dashboarding Tool**

---

##  Project Structure

```text
Vehicle-Pricing-Analysis/
│
├── data/
│   └── vehicle_dataset.csv
│
├── notebooks/
│   └── vehicle_analysis.ipynb
│
├── dashboard/
│   └── dashboard_file
│
├── report/
│   └── business_report.pdf
│
└── README.md
```

*The exact file names and folders may vary depending on the final project structure.*

---

##  Project Workflow

```text
Raw Dataset
     ↓
Data Exploration
     ↓
Data Validation
     ↓
Feature Engineering
     ↓
KPI Calculation
     ↓
Exploratory Analysis
     ↓
Interactive Dashboard
     ↓
Business Insights
     ↓
Business Recommendations
     ↓
Executive Summary
     ↓
Bonus: Price Prediction Model
```

---

##  Internship Project

**Developed as part of the Data Science Internship — Week 3**

**Organization:** Devixo Solutions

**Focus:** Advanced Concepts & Real-World Project Development
