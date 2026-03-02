## Dataset
The dataset used in this project was sourced from Kaggle and is not included in the repository due to file size restrictions.

You can download it here:  
[London Housing Dataset – Kaggle](https://www.kaggle.com/datasets)

Please make sure to place it in the project root directory as:
`kaggle_london_house_price_data.csv`

----

# London Rent Price Analysis

## What factors drive rental prices across London?

This project analyzed over 3,700 London rental listings to identify the key drivers of rent prices and built a predictive model to estimate rental costs based on property characteristics.

----

## Key Findings
### Top 3 Price Drivers:

#### 1. Property Type — Houses rent for significantly more than flats/studios
#### 2. Number of Bedrooms — Each additional bedroom increases rent by approximately £400-500/month
#### 3. Location (Borough) — Central/West London boroughs command 40-60% premiums over outer areas

## Model Performance:

* Achieved **R² = 0.78** using Random Forest Regressor
* Mean Absolute Error: £350/month
* Model accurately predicts rental prices within 15-20% for most properties

## Actionable Insight:
Landlords can optimize pricing by benchmarking against similar properties in the same borough with matching bedroom counts. Renters should prioritize location and property type as the primary cost factors.

----

## Methodology
### 1. Data Collection & Cleaning

* **Source:** Kaggle London Housing Dataset (3,700+ listings)
* **Cleaning:** Removed duplicates, handled missing values, standardized borough names
* **Feature Engineering:** Created price-per-bedroom, distance-to-center, and categorical encodings

### 2. Exploratory Analysis

* Visualized price distributions across boroughs, property types, and bedroom counts
* Identified outliers and seasonal trends
* Correlation analysis to isolate key predictors

### 3. Modeling

* Baseline: Linear Regression (R² = 0.64)
* Final Model: Random Forest Regressor (R² = 0.78)
* Validation: 80/20 train-test split with cross-validation

### 4. Results & Interpretation

* Feature importance analysis confirmed location and property type as dominant factors
* Residual analysis showed model performs well across price ranges except luxury segment (£5k+/month)

----

Part 1 - Data loading & initial exploration

Part 2 - Data cleaning & preprocessing

Part 3 - Feature engineering

Part 4 - Exploratory data analysis

Part 5 - Baseline modeling (Linear Regression)

Part 6 - Advanced modeling (Random Forest)

Part 7 - Results & interpretation
