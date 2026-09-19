# Devixo Solutions – Task 02

## Data Cleaning & Feature Engineering

This project was completed as part of my **Data Science Internship at Devixo Solutions**.

The objective of this task was to clean a real-world electric vehicle dataset, perform feature engineering, prepare categorical and numerical variables, and transform the dataset into an analysis-ready format.

## Dataset

**Dataset:** Electric Vehicle Market and Pricing Dataset

The dataset contains information about electric vehicles from different brands, including pricing, battery capacity, driving range, performance, sales, safety, and other specifications.

The dataset contains **2,000+ records** and includes both numerical and categorical variables.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

## Data Cleaning

The following data-cleaning steps were performed:

* Checked for missing values
* Checked for duplicate records
* Examined data types
* Checked numerical values against their expected ranges
* Identified potential outliers using the **Interquartile Range (IQR)** method
* Reviewed potential outliers before deciding whether they required treatment

No missing values or duplicate records were found in the dataset, so no imputation or duplicate removal was required.

## Outlier Analysis

Potential outliers were identified using the IQR method for variables such as:

* `range_miles`
* `horsepower`
* `annual_sales_units`
* `price_usd`

The identified observations were reviewed against the expected ranges and vehicle characteristics. Valid extreme values were retained rather than being removed simply because they were statistically unusual.

## Feature Engineering

Several new features were created from the existing variables:

* **Range Efficiency** – driving range relative to battery capacity
* **Price per Range Mile** – vehicle price relative to its driving range
* **Power-to-Weight Ratio** – horsepower relative to vehicle weight
* **Torque-to-Weight Ratio** – torque relative to vehicle weight
* **Battery-to-Weight Ratio** – battery capacity relative to vehicle weight
* **Vehicle Age** – calculated from the manufacturing year
* **Range Category** – vehicles grouped into Short, Medium, and Long range categories

These features provide additional information for analysing vehicle efficiency, performance, pricing, and characteristics.

## Categorical Encoding

Categorical variables were converted into numerical form using **one-hot encoding** with `drop_first=True`.

The encoded variables included:

* Brand
* Variant
* Drive Type
* Body Type
* Country of Origin
* Market Segment

The `model` column was retained as a categorical identifier.

## Feature Scaling

Selected numerical features were standardized using **StandardScaler** from Scikit-learn.

This brings numerical features to a comparable scale and prepares them for further analysis or machine learning applications.

## Project Files

```text
Task_02_Data_Cleaning_Feature_Engineering/
│
├── Task_02_Data_Cleaning_Feature_Engineering.ipynb
├── EV_Market_Cleaned.csv
├── Task_02_Report.pdf
├── README.md
└── screenshots/
```

### Files Included

* **Jupyter Notebook** – contains the complete data cleaning, feature engineering, encoding, and scaling workflow.
* **Cleaned Dataset** – contains the processed dataset after the required transformations.
* **Task 02 Report** – provides a written summary of the methodology, processing steps, findings, and results as required for the internship submission.
* **README** – provides an overview of the project and the steps performed.

## Final Outcome

The dataset was cleaned, feature-engineered, encoded, and standardized to make it suitable for further analysis and machine learning applications.

The complete **Jupyter Notebook, cleaned dataset, and required project report** are included in this GitHub repository for reference and evaluation.

## Internship

**Devixo Solutions – Data Science Internship**
**Task 02: Data Cleaning & Feature Engineering**
