# Zomato Restaurant Analysis — EDA

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
End-to-end data cleaning and exploratory data analysis on a multi-source 
restaurant dataset — combining CSV and nested JSON API data to extract 
meaningful insights on ratings, pricing, cuisines, and service availability 
across multiple countries.

---

## Dataset
- Sources: CSV dataset + JSON API (nested, multi-source)
- Scope: Restaurants across multiple countries
- Target: Clean, enrich, and analyze restaurant data

---

## Work Done

### Data Collection & Integration
- Loaded and parsed nested JSON API response into structured DataFrame
- Combined CSV and JSON sources into unified dataset
- Extracted relevant fields, ignored noise (events, offers, API keys)

### Data Cleaning
- Flattened nested JSON structure using normalization
- Dropped columns with high missing value percentage
- Dropped rows with negligible missing values (Country)
- Removed irrelevant columns — URLs, switch to order menu, events
- Fixed data types — Votes → int, Ratings → float, Lat/Long → float
- Removed duplicate restaurant entries using Restaurant ID

### Data Enrichment
- Mapped Country Code → Country Name using external country dataset
- Currency standardization — resolved ambiguous symbols across formats:
  - `Rs., INR, Indian Rupees` → `INR`
  - `$, Dollar($), NZ$` → standardized ISO codes using Country column
- Cuisines column — split by comma, stripped spaces, exploded to one cuisine per row

### Feature Engineering
- Renamed columns to readable format
- Reordered columns logically
- Dropped redundant columns — City ID, Zipcode

### Exploratory Data Analysis
- Rating distribution and most common rating categories
- City-wise average ratings and votes vs rating relationship
- Country-wise average cost and price range vs rating correlation
- Most popular cuisines and highest voted cuisine categories
- Online delivery, table booking, and service availability vs rating impact
- Country-wise and city-wise restaurant distribution

---

## Key Findings
- More votes indicate more reliable ratings but not necessarily higher ones
- Expensive restaurants tend to have slightly better ratings — correlation is weak
- Service availability (delivery, booking) has some impact on ratings but is not dominant
- Currency inconsistencies across countries required country-aware standardization
- Multi-value cuisine column required explode — direct analysis without fixing gave incorrect results

---

## Critical Skills Demonstrated
- Multi-source data integration (CSV + JSON API)
- Nested JSON flattening and extraction
- Real-world currency standardization using contextual mapping
- Multi-value column normalization using explode
- End-to-end cleaning pipeline on genuinely messy data

---

## Tech Stack
Python | Pandas | NumPy | Matplotlib | Seaborn

---

## Status
Complete — dataset cleaned, enriched, and analyzed.
All four EDA projects complete → moving to ML algorithms.