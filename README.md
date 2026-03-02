## Dataset
The dataset used in this project was sourced from Kaggle and is not included in the repository due to file size restrictions.

You can download it here:  
[London Housing Dataset – Kaggle](https://www.kaggle.com/datasets)

Please make sure to place it in the project root directory as:
`kaggle_london_house_price_data.csv`

----

# London Rent Price Analysis

## What factors drive rental prices across London?

This project analyzed over 390,000 London rental listings to identify the key drivers of rent prices and built a predictive model to estimate rental costs based on property characteristics.

----

## Key Findings

### Top 3 Price Drivers:

1. **Floor Area:** The single strongest predictor (48% importance). Larger properties command significantly higher rents.
2. **Location (Latitude/Longitude):** Combined 38% importance. Geographic position within London has massive impact on pricing.
3. **Bathrooms:** 7% importance. Number of bathrooms matters more than bedrooms for rental pricing.

## Model Performance:

* Achieved **R² = 0.9551** using Random Forest Regressor (tuned)
* Mean Absolute Error: £197.50/month
* Root Mean Squared Error: £738.97/month
* Model accurately predicts rental prices within 3-5% for most properties

### Unexpected Insight:
Number of bedrooms (5% importance) and living rooms (2% importance) have surprisingly low impact on rent compared to total floor area, suggesting renters and landlords price based on total space rather than room configuration.

----

## Methodology

### 1. Problem Statement & Objectives
* Defined research question: Which property features most strongly influence London rental prices?
* Established evaluation criteria for model comparison

### 2. Exploratory Data Analysis
* Analyzed 390,000+ rental listings across London
* Visualized price distributions across boroughs, property types, and features
* Identified missing data patterns and outliers

### 3. Feature Engineering & Preprocessing
* **Data Cleaning:** Removed duplicates, handled 25k+ missing floor area values using median imputation
* **Feature Engineering:** 
  - Created `price_per_sqm` metric
  - Calculated distance from city center using Haversine formula
  - One-hot encoded categorical variables (tenure, property type)
* **Scaling:** Standardized numeric features using StandardScaler

### 4. Modeling Approaches
* **Baseline:** Linear Regression (R² = 0.49, MAE = £1,244)
* **Random Forest:** Initial model (R² = 0.93, MAE = £319)
* **XGBoost:** Alternative tree-based model (R² = 0.79, MAE = £763)
* **Neural Network:** Deep learning approach (R² = 0.48, MAE = £1,270) — underperformed due to overfitting

### 5. Hyperparameter Tuning
* Tuned Random Forest using GridSearchCV
* Optimized: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`
* **Final Model:** Random Forest with tuned parameters achieved R² = 0.9551

### 6. Model Comparison & Feature Importance
* Random Forest (tuned) significantly outperformed all other models
* Feature importance analysis revealed floor area as dominant predictor
* Location (lat/lon) second most important, room counts had minimal impact

### 7. Visualization & Reporting
* Created performance comparison charts across all models
* Visualized feature importance rankings
* Generated insights for stakeholders

----

## Files

**[Part 1](./Final_Project_pt1.ipynb)** - Problem Statement and Objectives

**[Part 2](./Final_Project_pt2.ipynb)** - Exploratory Data Analysis

**[Part 3](./Final_Project_pt3.ipynb)** - Feature Engineering & Preprocessing

**[Part 4](./Final_Project_pt4.ipynb)** - Modeling Approaches (Linear Regression, Random Forest, XGBoost, Neural Network)

**[Part 5](./Final_Project_pt5.ipynb)** - Evaluation & Hyperparameter Tuning

**[Part 6](./Final_Project_pt6.ipynb)** - Model Comparison & Insights

**[Part 7](./Final_Project_pt7.ipynb)** - Visualization & Reporting

----

## Tools Used

- **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow/Keras)
- **Jupyter Notebook**
- **Machine Learning:** Linear Regression, Random Forest, XGBoost, Neural Networks
- **Techniques:** Cross-validation, GridSearchCV, Feature Engineering, StandardScaler
