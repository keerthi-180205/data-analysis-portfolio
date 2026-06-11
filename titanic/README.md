# Titanic Survival Analysis — EDA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
Exploratory Data Analysis on the Titanic dataset to identify key factors 
influencing passenger survival. Focus is on deep analytical reasoning — 
feature relationships, confounding effects, and real-world interpretation.

---

## Dataset
- 891 passengers, 12 features
- Target: Survived (0 = No, 1 = Yes)

---

## Data Cleaning
- Age → Group-wise median imputation by Pclass and Sex
- Cabin → Extracted Deck information, remaining labeled Unknown
- Embarked → Filled with mode (2 missing values)

---

## Feature Engineering
- Deck — extracted from Cabin column
- Family Size — SibSp + Parch + 1

---

## Key Findings
- Gender is the strongest survival predictor — females survived at significantly higher rates
- Survival decreases from 1st → 2nd → 3rd class
- Embarked adds independent information even within the same Pclass
- Small families (2–3 members) survived at higher rates than solo travelers or large families
- Within Pclass 1, higher fare passengers had better survival — fare has partial predictive value
- Upper deck passengers showed higher survival rates

---

## Tech Stack
Python | Pandas | NumPy | Matplotlib | Seaborn

---

## Next
House Prices dataset → extended into full ML project