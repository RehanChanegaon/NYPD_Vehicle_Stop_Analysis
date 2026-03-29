# Project Documentation

## Project Title

NYPD Vehicle Stop Analysis

---

## 1. Introduction

This project analyzes vehicle stop data collected by the New York Police Department (NYPD) to understand patterns in policing behavior, demographic disparities, and factors influencing search and arrest decisions.

Vehicle stops are one of the most common forms of interaction between law enforcement and civilians. By analyzing this data, the project aims to uncover trends that can help evaluate fairness, accountability, and decision-making in policing practices.

---

## 2. Objectives

The main objectives of this project are:

* Identify demographic patterns in vehicle stops
* Analyze how age distribution varies across race and gender
* Examine how police actions relate to location and demographics
* Determine factors influencing vehicle searches
* Build a predictive model to estimate the likelihood of arrest

---

## 3. Dataset Description

The dataset used is the **NYPD Vehicle Stop Reports dataset**, which includes:

* Demographic information (race, gender, age)
* Vehicle stop details
* Police actions (search, arrest, seizure, force used)
* Consent and checkpoint indicators
* Geographic coordinates (X and Y)

This dataset allows both exploratory analysis and predictive modeling.

---

## 4. Data Preprocessing

The following preprocessing steps were applied:

### 4.1 Handling Missing Values

* Numerical columns such as age and coordinates were imputed using median values
* Rows with missing target variables were removed

### 4.2 Encoding

* Binary columns (Y/N) were converted into numeric format (1/0)

### 4.3 Data Cleaning

* Standardized categorical values such as race and gender
* Converted age to numeric format

### 4.4 Class Imbalance

* SMOTE (Synthetic Minority Oversampling Technique) was applied for arrest prediction to balance the dataset

---

## 5. Methodology

The project is divided into five key analytical questions:

---

### Q1: What are the key demographic patterns in NYPD vehicle stops?

Approach:

* Frequency distributions for gender, race, and age
* Visualization using bar plots and histograms
* Chi-square test to analyze association between race and arrest

---

### Q2: How does driver age distribution vary by race and gender?

Approach:

* Boxplots of age grouped by race and gender
* Comparative statistical summaries

---

### Q3: How do police actions correlate with demographics and location?

Approach:

* Spatial visualization using coordinates
* Scatter plots and density maps
* Identification of high-activity regions

---

### Q4: What factors influence whether a vehicle is searched?

Approach:

* Correlation heatmap
* Logistic regression model
* Evaluation using accuracy, confusion matrix, and AUC

---

### Q5: Can we predict whether an arrest will be made?

Approach:

* Feature selection from stop-related variables
* Handling imbalance using SMOTE
* Random Forest classification model
* Evaluation using:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * ROC Curve
  * AUC score

---

## 6. Models Used

### 6.1 Logistic Regression

Used to analyze factors influencing vehicle search decisions. This model helps interpret relationships between features and the probability of a search.

### 6.2 Random Forest Classifier

Used for arrest prediction. It captures nonlinear relationships and interactions between variables and provides feature importance insights.

---

## 7. Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC Curve
* Area Under Curve (AUC)

These metrics provide a comprehensive understanding of both overall performance and class-specific prediction quality.

---

## 8. Key Findings

* Vehicle stops are heavily skewed toward **male drivers**
* Most stops occur in the **20–40 age group**
* Certain racial groups appear more frequently in stop data
* Search likelihood is associated with factors such as:

  * Arrest occurrence
  * Vehicle seizure
  * Police actions
* Arrest prediction using Random Forest shows strong performance, indicating that arrest outcomes are influenced by measurable features

---

## 9. Limitations

* The dataset does not include full contextual details behind each stop
* Potential bias in data collection cannot be ruled out
* Some features may indirectly reflect outcomes rather than causes
* Geographic data is limited to coordinates without contextual mapping

---

## 10. Future Improvements

* Incorporate additional socio-economic data
* Perform hyperparameter tuning for improved model performance
* Use cross-validation for more robust evaluation
* Integrate interactive visualizations (e.g., dashboards)
* Apply fairness-aware machine learning techniques

---

## 11. Conclusion

This project demonstrates that NYPD vehicle stop data contains meaningful patterns related to demographics, location, and police actions. Both exploratory analysis and predictive modeling suggest that search and arrest decisions are not random but influenced by observable factors.

The findings highlight the importance of data-driven analysis in understanding law enforcement practices and can contribute to discussions on fairness and accountability.

---

## 12. Reproducibility

To reproduce this project:

1. Place the dataset in the `data/` folder
2. Install dependencies using `requirements.txt`
3. Run the Jupyter notebook step by step
4. Ensure `random_state=42` is used for consistency

---
