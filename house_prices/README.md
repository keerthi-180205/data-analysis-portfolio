# California Housing Analysis — EDA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
End-to-end Exploratory Data Analysis on the California Housing dataset to
understand key factors influencing median house values across geographical
districts in California.

---

## Dataset
- 20,640 districts, 10 features
- Target: `median_house_value`
- Each row represents a geographical block, not an individual house

---

## Work Done

### Data Cleaning
- Identified 207 missing values in `total_bedrooms` (~1% of dataset)
- Analyzed missing value distribution across `ocean_proximity` groups
- Dropped missing rows — no significant bias observed

### Feature Understanding
- Location features: `longitude`, `latitude`
- Housing features: `total_rooms`, `total_bedrooms`, `housing_median_age`
- Demographic features: `population`, `households`
- Economic feature: `median_income`
- Categorical feature: `ocean_proximity`

### Univariate Analysis
- `median_house_value` distribution — right-skewed, majority in lower-mid range
- Identified price cap at $500,000 — ceiling effect present

### Outlier Detection and Handling
- Used boxplot and IQR method
- Identified ~1,064 values beyond upper bound
- Critical insight: values are not true outliers — dataset has a hard price cap at $500,000
- Decision: retained all values as valid high-value observations

### Log Transformation
- Applied log transformation on `median_house_value`
- Reduced skewness significantly
- Improved linearity for modeling
- Observed: capping effect persists after transformation — rescaled but not removed

### Bivariate Analysis
- `median_income` vs `median_house_value` — strong positive relationship
- `median_income` vs `log_median_house_value` — more linear trend post-transformation
- Identified saturation effect at high income levels due to price capping

### Correlation Analysis
- Strongest predictor: `median_income`
- Redundant features: `total_rooms` and `total_bedrooms` highly correlated
- Weak individual predictors identified for feature selection

---

## Key Findings
- `median_income` is the strongest predictor of house value
- Dataset has a hard price cap at $500,000 — models may learn incorrect relationships at high income levels
- Log transformation improves data spread but does not eliminate capping effect
- `total_rooms` and `total_bedrooms` are redundant — ratio features would be more meaningful
- Missing data in `total_bedrooms` shows no geographic bias

---

## Critical Insight
The ~1,064 flagged outliers are not errors — they represent genuinely
high-value properties compressed by a data collection ceiling. Removing
them would introduce bias. This distinction between true outliers and
capped values is essential for correct modeling decisions.

---

## Tech Stack
Python | Pandas | NumPy | Matplotlib | Seaborn

---

## Status
Complete — dataset cleaned, transformed, and analyzed.
Ready for ML modeling with informed feature engineering decisions.