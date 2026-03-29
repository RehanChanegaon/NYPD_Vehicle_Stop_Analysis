# NYPD Vehicle Stop Analysis

This project analyzes NYPD vehicle stop data to uncover demographic patterns, search and arrest trends, and predictive factors behind vehicle searches and arrests. The analysis combines exploratory data analysis, statistical testing, and machine learning models to answer five key research questions.

## Project Overview

The project focuses on understanding:

1. What are the key demographic patterns in NYPD vehicle stops?
2. How does driver age distribution vary by race and gender?
3. How do police actions such as searches and arrests correlate with demographics and location?
4. What factors influence whether a vehicle is searched during a stop?
5. Can we predict whether an arrest will be made based on vehicle stop characteristics?

This analysis was completed as part of **DATA 605**.

---

## Dataset

The dataset used in this project is:

**NYPD Vehicle Stop Reports**

It contains information such as:
- Demographics of stopped individuals
- Age, race, and gender
- Search and arrest outcomes
- Vehicle seizure and consent-related indicators
- Geographic coordinates of stops
- Stop-related police actions

---

## Methods Used

### Data Preprocessing
- Handled missing values using imputation and selective row removal
- Converted binary categorical flags into numeric format
- Standardized demographic columns for analysis
- Used SMOTE to address class imbalance in arrest prediction

### Statistical and Exploratory Analysis
- Gender, age, and race distribution analysis
- Boxplots of age distribution across race and gender
- Chi-square test for race vs arrest association
- Correlation heatmap for search-related factors
- Geographic location-based police action visualization

### Machine Learning Models
- **Logistic Regression** for understanding factors influencing vehicle searches
- **Random Forest Classifier** for arrest prediction
- **SMOTE** for class balancing
- Evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix
  - ROC Curve
  - AUC Score

---

## Key Findings

- Vehicle stops predominantly involve **males**, especially those aged **20 to 40**
- **Black and Hispanic individuals** appear most frequently in vehicle stop records
- Age distributions vary across race and gender groups
- Search outcomes are associated with factors such as arrest, vehicle seizure, force used, and summons issued
- Arrest prediction achieved strong performance using **Random Forest with SMOTE**, showing that arrest outcomes can be predicted from stop-level characteristics

---

## Repository Structure

```text
NYPD-Vehicle-Stop-Analysis/
│── data/
│   └── NYPD_Vehicle_Stop_Reports.xlsx
│── notebooks/
│   └── 605_Project.ipynb
│── images/
│── README.md
│── requirements.txt
│── .gitignore
│── LICENSE
│── PROJECT_DOCUMENTATION.md
