# Data Analysis Portfolio

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

A collection of end-to-end exploratory data analysis and data cleaning projects
on real-world datasets — built as part of my ML/AI engineering journey targeting
LLM and Agents engineering roles.

Each project follows a structured pipeline:
raw data → cleaning → EDA → insights → documented findings.

---

## Projects

| # | Dataset | Difficulty | Key Skills | Notebook |
|---|---------|------------|------------|----------|
| 1 | Titanic Survival Analysis | Easy | Missing values, encoding, EDA | [View](./titanic/titanic_eda.ipynb) |
| 2 | Netflix Content Analysis | Medium | Text cleaning, date parsing, multi-value columns | [View](./netflix/netflix_eda.ipynb) |
| 3 | House Prices Analysis | Medium | Outlier detection, correlation, skewness | [View](./house-prices/house_prices_eda.ipynb) |
| 4 | Zomato Restaurant Analysis | Hard | Inconsistent formats, multi-language text, business EDA | [View](./zomato/zomato_eda.ipynb) |

---

## Project Highlights

### 1. Titanic — Survival Analysis
> Difficulty: Easy

**Objective:** Analyze survival patterns across passenger demographics.

**Key techniques:**
- Missing value imputation (Age, Cabin)
- Categorical encoding (Sex, Embarked)
- Survival analysis by gender, class, and age group

**Key finding:** Female passengers in 1st class had the highest survival rate at ~97%.

---

### 2. Netflix Movies & TV Shows — Content Analysis
> Difficulty: Medium

**Objective:** Uncover content trends across genres, countries, and release years.

**Key techniques:**
- Multi-value column splitting (genres, cast, directors)
- Date parsing and formatting standardization
- Country-wise and year-wise content distribution analysis

**Key finding:** Netflix added 3x more content between 2016–2019 compared to prior years.

---

### 3. House Prices — Real Estate Analysis
> Difficulty: Medium

**Objective:** Identify key drivers of house prices across 79 features.

**Key techniques:**
- Outlier detection and treatment (IQR method)
- Log transformation for skewed distributions
- Correlation heatmap and feature importance analysis

**Key finding:** Overall quality, living area, and basement size are the top 3 price predictors.

> Note: This dataset is extended into a full ML project → [House Price Prediction](https://github.com/yourusername/house-price-prediction)

---

### 4. Zomato — Restaurant Analysis
> Difficulty: Hard

**Objective:** Analyze restaurant trends, ratings, and cuisine popularity across cities.

**Key techniques:**
- Multi-language and inconsistent text normalization
- Duplicate detection and removal at scale
- Rating distribution and cuisine-level business insights

**Key finding:** North Indian cuisine dominates listings but Continental restaurants have higher average ratings.

---

## Tech Stack

- **Language:** Python 3.10
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Environment:** Jupyter Notebook
- **Version Control:** Git + GitHub

---

## Repository Structure

```
data-analysis-portfolio/
├── titanic/
│   ├── titanic_eda.ipynb
│   └── README.md
├── netflix/
│   ├── netflix_eda.ipynb
│   └── README.md
├── house-prices/
│   ├── house_prices_eda.ipynb
│   └── README.md
├── zomato/
│   ├── zomato_eda.ipynb
│   └── README.md
└── README.md
```

---

## Connect

- LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/keerthi-n)
- GitHub: [github.com/yourusername](https://github.com/keerthi-180205)
- Email: keerthin180205@email.com