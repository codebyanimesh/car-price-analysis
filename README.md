## 📌 Project Overview
This repository contains a comprehensive machine learning analysis of the secondary car market. Using a dataset of over 426,000 used cars (sampled from a 3 million record Kaggle dataset), this project identifies and quantifies the primary features that dictate a vehicle's value. 

The final deliverable translates raw vehicle data into actionable business intelligence, providing data-backed recommendations to help used car dealerships optimize their inventory acquisition and pricing strategies.

## ⚙️ Methodology
The analysis is strictly guided by the **CRISP-DM** (Cross-Industry Standard Process for Data Mining) framework to ensure all technical tasks align with the underlying business objectives:

1. **Business Understanding:** Framing the pricing problem as a supervised regression task.
2. **Data Understanding:** EDA, missing value analysis, and distribution checks.
3. **Data Preparation:** Data cleaning, imputation, handling outliers, and engineering features (e.g., converting manufacturing year to vehicle age).
4. **Modeling:** Utilizing **Ridge Regression (L2 Regularization)** via a `StandardScaler` pipeline to handle multicollinearity among high-dimensional categorical variables.
5. **Evaluation:** Assessing via RMSE, MAE, and R-squared, with a core focus on coefficient interpretability.
6. **Deployment:** Extracting top pricing drivers into a strategic business report.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (Ridge Regression, GridSearchCV, Pipelines)
* **Data Visualization:** `matplotlib`, `seaborn`

## 📊 Key Business Findings
Based on the regression coefficients, the following strategic insights were generated for inventory pricing:

* **Depreciation is King:** `car_age` and `odometer` mileage are the strongest negative drivers of price, showing steep, linear drops in value.
* **Engine Power Commands a Premium:** Vehicles with 8-cylinder and 10-cylinder engines retain significantly higher value than their 4- or 6-cylinder counterparts.
* **Drive Type Matters:** Four-wheel drive (`4wd`) is a major positive driver for price compared to front-wheel or rear-wheel drive, indicating a strong consumer willingness to pay for off-road/all-weather capability.
* **Fuel Economy vs. Longevity:** Diesel vehicles carry a substantial price premium over standard gas vehicles, likely due to engine longevity and heavy-utility use cases.

## 📂 Repository Structure
```text
├── data/
│   └── vehicles.csv           # Raw dataset (Note: May require unzipping or external download due to size)
├── notebooks/
│   └── car_analysis.ipynb        # Main Jupyter Notebook containing the CRISP-DM analysis
└── README.md                  # Project documentation
