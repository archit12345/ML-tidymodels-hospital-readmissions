# ML-tidymodels-hospital-readmissions

# Predicting Risk of Hospital Readmission Within 30 Days of Discharge Using Machine Learning Models With Tidymodels in R

This project builds and evaluates machine learning models to predict whether a patient will be readmitted to the hospital within 30 days. Using structured patient data and modern ML tools in R, the project aims to inform hospital strategies for identifying patients at low-risk and high-risk of readmission. 

Link to project on RPubs: https://rpubs.com/architn01/1323685

## Dataset

- **Source:** `hospital_readmissions.csv` (uploaded manually)
- **Target Variable:** `readmitted` (binary: 1 = Yes, 0 = No)

## Methods

- **Preprocessing:**
  - Normalized numeric features
  - One-hot encoded categorical variables
  - 80/20 train-test split

- **Modeling Approach:**  
  Built and compared eight classifiers using the `tidymodels` framework:
  - Decision Tree
  - Logistic Classification
  - Naive Bayes
  - k-Nearest Neighbor
  - Random Forest
  - Linear Support Vector Machine (SVM)
  - Radial Basis Function with SVM
  - XGBoost

- **Tuning:**
  - k-fold cross-validation
  - Grid search for hyperparameter tuning 

- **Evaluation Metrics:**
  - ROC AUC
  - F1 Score
  - Sensitivity & Specificity
  - Confusion Matrix
  - Feature Importance Plot (`vip()` package)

## Results

- **Best Model:** Logistic Classification
- **ROC AUC:** 0.65
- **F1 Score:** 0.72
- **Accuracy** 0.61
- **Specificity** 0.28
- **Sensitivity** 0.88
- **Top Predictors:**
  -  Number of prior patient visits
  -  Length of hospital stay
  -  Taking diabetes medication
  -  Admit source emergency room
  -  Age
