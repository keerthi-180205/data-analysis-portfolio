# Netflix Content Analysis — EDA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
End-to-end Exploratory Data Analysis on the Netflix Movies and TV Shows dataset
to uncover content trends, regional patterns, and platform growth insights.

---

## Dataset
- 8,807 titles, 12 features
- Content types: Movies and TV Shows

---

## Work Done

### Data Cleaning
- Set `show_id` as index
- Type conversions: `type` and `rating` → category, `date_added` → datetime
- Fixed date format inconsistencies (leading spaces, parsing errors)
- Missing values: filled `director`, `cast`, `country` with Unknown; dropped rows with few nulls
- Removed duplicates and leading/trailing whitespace
- Fixed invalid rating entries (`"66 min"` etc.) and negative `content_age` values

### Feature Engineering
- `year_added` and `month` — extracted from `date_added` for temporal analysis
- `duration_value` and `duration_type` — separated numeric duration from unit
- `content_age` — gap between release year and Netflix addition year
- Split + explode: `listed_in` → genres, `cast` → actors, `country` → individual countries

### Analysis Performed
- Basic distribution — Movies vs TV Shows, rating distribution, country distribution
- Time-based — year-wise content growth, month-wise seasonality
- Categorical — genre distribution, genre vs type, genre vs rating (pivot analysis)
- Multi-dimensional — country vs type, country vs genre diversity, duration vs country
- Entity analysis — top directors, most frequent actors (post-explode)
- Content freshness — `content_age` distribution and anomaly detection

### Techniques Used
`groupby()` | `value_counts()` | `unstack()` | `idxmax()` | `explode()` |
`str.split()` | `str.strip()` | conditional filtering | multi-value column handling

---

## Key Findings
- Netflix added 3x more content between 2016–2019 compared to prior years
- Movies dominate the platform but TV Show proportion is growing
- US, India, and UK are top content-producing countries
- Drama and International content are the most listed genres
- Most content is added in Q4 — clear seasonal pattern
- Content freshness varies significantly by country and genre

---

## Tech Stack
Python | Pandas | NumPy | Matplotlib | Seaborn

---

## Status
Complete — dataset cleaned, features engineered, insights documented.