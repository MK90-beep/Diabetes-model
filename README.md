#  Predicting Diabetes Status Using Biomedical and Demographic Data

##  Structure

1. [Overview](#-overview)  
2. [Problem Statement](#-problem-statement)  
3. [Objectives](#-objectives)  
   - Business Objectives  
   - Analysis Objectives  
4. [Stakeholders](#-stakeholders)  
5. [Dataset Description](#-dataset-description)  
6. [Data Preprocessing Steps](#-data-preprocessing-steps)  
7. [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)  
8. [Modeling](#-modeling)  
   - Models Used  
   - Train-Test Strategy  
9. [Evaluation Metrics](#-evaluation-metrics)  
10. [Key Results](#-key-results)  
11. [Tools & Libraries](#-tools--libraries)  
12. [Future Work](#-future-work)  

---

##  Overview
Diabetes is a growing global health concern. Early detection can prevent serious complications such as heart disease, kidney failure, and blindness. However, timely diagnosis is often hampered by limited access to specialized testing—especially in resource-constrained environments.

In this project, I applied machine learning to predict diabetes status using basic biomedical and demographic data. This predictive model serves as a decision support tool to assist healthcare providers in identifying at-risk individuals earlier and more efficiently.

---

##  Problem Statement
*How can we leverage existing routine lab test results and demographic attributes to automatically and accurately classify a patient as diabetic or non-diabetic, especially in settings where full diagnostic testing is unavailable or delayed?*

---

##  Objectives

### Business Objectives
- Support early identification of diabetic patients using existing data.
- Reduce the burden on healthcare providers through automated risk prediction.
- Improve patient outcomes by enabling timely intervention.

### Analysis Objectives
- Build a binary classification model to predict diabetes status.
- Evaluate model performance using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC-AUC

---

##  Stakeholders

| Stakeholder          | Benefit                                      |
|----------------------|----------------------------------------------|
| Doctors/Nurses       | Quick decision-making support                |
| Hospital Managers    | Improved triage and resource allocation      |
| Patients             | Earlier diagnosis and care                   |
| Public Health Agencies | Population-level diabetes tracking and prevention |
| Data Scientists      | Opportunity to build interpretable and deployable models |

---

##  Dataset Description

The dataset consists of patient demographic data and routine lab test results.

| Feature      | Description                                                  |
|--------------|--------------------------------------------------------------|
| ID         | Unique identifier                                            |
| No_Pation  | Patient number or record ID                                  |
| Gender     | F (Female) or M (Male)                                       |
| AGE        | Age in years                                                 |
| Urea       | Urea level (kidney function marker)                          |
| Cr         | Creatinine level                                             |
| HbA1c      | Glycated hemoglobin (%) — avg. blood sugar                   |
| Chol       | Total cholesterol                                            |
| TG         | Triglycerides                                                |
| HDL        | Good cholesterol                                             |
| LDL        | Bad cholesterol                                              |
| VLDL       | Very bad cholesterol                                         |
| BMI        | Body mass index (kg/m²)                                      |
| CLASS      | Diabetes status: Y (Diabetic) or N (Non-diabetic)           |

---

##  Data Preprocessing Steps
- Cleaned ambiguous values and standardized labels.
- Removed entries with missing or placeholder values.
- Filtered the dataset to binary classification only (Y vs. N).
- Encoded categorical variables (Gender, CLASS).
- Scaled numerical features using StandardScaler.
- Applied *SMOTE* to handle class imbalance.

---

##  Exploratory Data Analysis (EDA)
- Visualized class distribution.
- Examined outliers using boxplots.
- Computed correlation heatmaps between numeric features.
- Identified key predictors like *HbA1c, **BMI, and **Chol*.

---

##  Modeling

###  Models Used
- *Logistic Regression*: Interpretable baseline model.
- (Optional: Add other models like Decision Trees, Random Forests, etc. if used)

###  Train-Test Strategy
- 70/30 split using train_test_split.
- Feature transformation and SMOTE applied on *training data only*.

---

##  Evaluation Metrics

| Metric     | Description                              |
|------------|------------------------------------------|
| Accuracy   | Overall correctness of predictions       |
| Precision  | Correct positives / total predicted      |
| Recall     | Correct positives / actual positives     |
| F1-Score   | Harmonic mean of precision and recall    |
| ROC-AUC    | Model's ability to separate classes      |

---

## Key Results
- Logistic Regression achieved a *satisfactory balance between precision and recall*, indicating reliable prediction for both classes.
- *ROC curve* and *confusion matrix* visualizations confirmed the model’s discriminative ability.

---

## Tools & Libraries

*Languages:*  
- Python

*Libraries:*  
- pandas, numpy – Data manipulation  
- matplotlib, seaborn – Visualization  
- scikit-learn – Preprocessing, modeling, evaluation  
- imblearn – SMOTE for class imbalance handling  

---

##  Future Work
- Experiment with other classifiers like *Random Forest, **XGBoost*.
- Deploy model in a web interface using *Flask* or *Streamlit*.
- Perform *feature importance analysis* to explain predictions.
- Apply *cross-validation* for improved robustness.

