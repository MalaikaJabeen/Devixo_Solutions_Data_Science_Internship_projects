# Pakistan Air Quality Analysis (2015–2025)

**Data Science Internship — Devixo Solutions — Task 1: Exploratory Data Analysis & Statistical Analysis**

## Project Description

This project performs a complete Exploratory Data Analysis (EDA) and statistical analysis on 11 years of monthly air quality data across 10 major Pakistani cities. The goal is to clean and validate the data, examine feature relationships and correlations, visualize temporal and geographic pollution patterns, and translate the statistical findings into actionable business insights and recommendations for policy-makers, health-service providers, and businesses operating in high-pollution regions.

## Dataset Information

- **File:** `pakistan_air_quality_monthly_2015_2025.csv`
- **Size:** 1,320 rows × 23 columns (21 after cleaning)
- **Coverage:** 10 cities (Faisalabad, Gujranwala, Hyderabad, Islamabad, Karachi, Lahore, Multan, Peshawar, Quetta, Rawalpindi) × 12 months × 11 years (2015–2025)
- **Key columns:** `pm25_ugm3` (PM2.5 concentration), `aqi_us` (US AQI), `aqi_category`, `who_guideline_ratio`, `population_millions`, `season`, `is_smog_season`, `is_crop_burning_season`, `is_monsoon_season`, `covid_lockdown_period`
- **Source:** IQAir World Air Quality Report (2018–2025), IQAir city monitoring pages, a PMC research compilation, and the WHO Air Quality Life Index (AQLI) 2025 report. Pre-2018 records are flagged `Estimated (pre-monitoring era)`; later years are flagged `Verified`.

## Technologies Used

- Python 3
- Pandas & NumPy — data loading, cleaning, and aggregation
- Matplotlib & Seaborn — statistical visualization
- Jupyter Notebook — interactive analysis environment

## Analysis Performed

1. **Data discovery & structural inspection** — shape, dtypes, column names, duplicate checks
2. **Data cleaning** — dropped two mostly-empty columns (`pakistan_national_avg_pm25`, `pakistan_global_rank`, 360 missing values each), verified 0 duplicates and 0 missing values across the remaining 21 columns
3. **Data validation** — confirmed a balanced panel (132 records per city), verified year range (2015–2025) and category labels
4. **Feature analysis** — numerical summaries and group-by comparisons across city, province, season, month, and year
5. **Correlation analysis** — full correlation matrix and ranked correlation pairs across PM2.5, AQI, annual average, WHO guideline ratio, and population
6. **Data visualization** — 13 charts covering distribution/outliers, city and provincial comparisons, yearly and monthly trends, seasonal effects (smog, crop-burning, monsoon), AQI category frequency, and PM2.5–AQI relationship
7. **Business insights & recommendations** — 16 evidence-based insights and 6 actionable recommendations derived directly from the above

## Key Findings

- Average AQI across all records is **143.2** ("Unhealthy"); **52%** of all monthly observations are Unhealthy/Very Unhealthy/Hazardous, vs. only **26%** Good/Moderate.
- **Faisalabad, Gujranwala, Multan, and Lahore** — all in Punjab's industrial belt — are the four most polluted cities (avg. AQI 170–190), while **Islamabad and Karachi** are the least polluted (avg. AQI ~105–109).
- **Population size has no correlation with pollution** (r = -0.019) — Karachi (16.1M people) is far cleaner than smaller industrial cities like Faisalabad (3.8M).
- **Winter (Smog Season) AQI (196.9) is almost exactly double Summer/Monsoon AQI (98.2)**; January is the worst month (203.0), June the best (88.0).
- **Crop-burning season** adds a 41% AQI penalty (195.8 vs. 138.4); **COVID-19 lockdowns** cut AQI by 32% (98.5 vs. 144.6), proving activity reduction works.
- **PM2.5 correlates almost perfectly with AQI** (r = 0.952), confirming PM2.5 as the dominant pollutant.
- National PM2.5 fell to a low of 59.0 µg/m³ in 2020 (COVID year) but has since climbed to an **all-time high of 80.1 µg/m³ in 2025** — the pandemic-era improvement has fully reversed.
- Faisalabad's PM2.5 averages **24x the WHO guideline** (peaking at 53.3x); even the cleanest city, Islamabad, still averages 7.9x the WHO limit.

*(Full list of 16 insights available in the notebook and PDF report.)*

## Business Recommendations

1. **Concentrate intervention resources on the "Big Four" industrial Punjab cities** (Faisalabad, Gujranwala, Multan, Lahore) — pollution, not population, should drive budget allocation.
2. **Run time-boxed seasonal interventions for October–February** — winter and crop-burning season together account for the largest AQI swings.
3. **Pilot controlled activity-reduction measures** (e.g., odd-even vehicle schemes) during peak smog weeks, using the COVID lockdown period as a proven benchmark.
4. **Treat 2020–2025's rising trend as an urgent renewal signal** — pollution has fully rebounded past pre-pandemic levels.
5. **Target health/consumer-protection services** (respiratory care, air purifiers, insurance add-ons) at the Big Four cities during November–February.
6. **Benchmark Islamabad and Karachi's policies** — both remain low-AQI despite Karachi's large population, suggesting transferable best practices.

*(Full rationale for each recommendation available in the notebook and PDF report.)*

## Instructions to Run the Notebook

1. **Clone or download this repository**, ensuring `air_quality_analysis_FINAL.ipynb` and `pakistan_air_quality_monthly_2015_2025.csv` are in the same folder.
2. **Install the required libraries** (Python 3.8+ recommended):
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook air_quality_analysis_FINAL.ipynb
   ```
4. **Run all cells** in order (`Cell → Run All` or `Kernel → Restart & Run All`). The notebook reads the dataset using a relative path (`pd.read_csv("pakistan_air_quality_monthly_2015_2025.csv")`), so no path changes are needed as long as both files stay in the same directory.
5. The notebook will reproduce all 13 visualizations, the correlation analysis, and the full list of business insights and recommendations (Parts 6 and 7, at the end of the notebook).

## Deliverables

- `air_quality_analysis_FINAL.ipynb` — full annotated analysis notebook
- `pakistan_air_quality_monthly_2015_2025.csv` — source dataset
- `Devixo_Task1_Air_Quality_Report.pdf` — formatted project report with all required sections and screenshots

## Author

**Malaika Jabeen**
Data Science Intern, Devixo Solutions
GitHub: [mjcodes-77](https://github.com/mjcodes-77)
