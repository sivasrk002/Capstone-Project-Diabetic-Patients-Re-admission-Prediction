# Capstone-Project
## Diabetic Patients’ Re-admission Prediction 

* ML project to predict the potential diabetes patients who are prone to get readmitted within 30 days of discharge.
* **Objective:** To help hospitals filter out patients and provide them with better post discharge care, monitoring and education.
* Use Statistics and Visualization techniques to understand the important factors which affect the target class and get business inferences.
* Final Model building - Use classification techniques to design a classifier model.

### Problem Statement: 
To identify the factors that lead to the high readmission rate of diabetic patients within 30 days post discharge and correspondingly to predict the high-risk diabetic-patients who are most likely to get readmitted within 30 days so that the quality of care can be improved along with improved patient’s experience, health of the population and reduce costs by lowering readmission rates. Also, to identify the medicines that are the most effective in treating diabetes. 

### Data Source: 
UCI Dataset Link 

### Dataset name: 
Diabetes 130-US hospitals for years 1999-2008 Data Set 

## Code and Resources Used
**Python Version:** 3.8  
**Packages:** pandas, numpy, statsmodel, scipy, matplotlib, seaborn, sklearn

## Dataset Features and Description
* The data set is chosen from UCI machine learning repository and is a 10-years (from 1999 to 2008) historical data set of clinical care at 130 US hospitals and integrated delivery networks. 
* It contains 101766 records and includes 50 features 
* Features represent patient demographic details, data collected during the admission and discharge, and medications given during the encounter.

## Data Cleaning steps
* Redundant Columns removal
* Data Type casting
*	Missing values handling
*	Data Encoding

## EDA steps
* **Five point Descriptive Statistics** - Univariate description of both the numerical and categorical variables
* **Correlation and Pair plot** - Distribution and the relation between the numerial variables
* **Univariate, Bivariate and Multivariate Analysis** - Plotting Countplots, Barplots and 100% stacked barplots to visualize and infer the importance of the feature

### Variable identification:
1. Independent variables (49): encounter_id, patient_nbr, race, gender, age, weight, admission_type_id, discharge_disposition_id, admission_source_id, time_in_hospital, payer_code, medical_specialty, num_lab_procedures, num_procedures, num_medications, number_outpatient, number_emergency, number_inpatient, diag_1, diag_2, diag_3, number_diagnoses, max_glu_serum, A1Cresult, metformin, repaglinide, nateglinide, chlorpropamide, glimepiride, 
acetohexamide, glipizide, glyburide, tolbutamide, pioglitazone, rosiglitazone, acarbose, miglitol, troglitazone, tolazamide, examide, citoglipton, insulin, glyburide-metformin,  glipizide-metformin, glimepiride-pioglitazone, metformin-rosiglitazone, metformin-pioglitazone, change, diabetesMed. 
 
2. Dependent variable (1): readmitted (Categorical) 

### Background:
Diabetes Mellitus (DM) is a chronic disease where the blood has high sugar level. It can occur when the pancreas does not produce enough insulin, or when the body cannot effectively use the insulin it produces (WHO). Diabetes is a progressive disease that can lead to a significant number of health complications and profoundly reduce the quality of life. While many diabetic patients manage the health complication with diet and exercise, some require medications to control blood glucose level. As published by a research article named “The relationship between diabetes mellitus and 30-day readmission rates”, it is estimated that 9.3% of the population in the United States have diabetes mellitus (DM), 28% of which are undiagnosed. In recent years, government agencies and healthcare systems have increasingly focused on 30-day readmission rates to determine the complexity of their patient populations and to improve quality. Thirty-day readmission rates for hospitalized patients with DM are reported to be between 14.4 and 22.7%, much higher than the rate for all hospitalized patients (8.5–13.5%).

## Feature Selection
* VIF Factor for multi collinearity
* Mann Whitney statistical Test for numerical features
* Chi-Square Yate's Correction statistical Test for categorical features
* Reverse Backward Elimation method

## Final Model building Approach
* Model building – 10 models for dataset
* Model performance metrics – Precision, Recall, Accuracy, ROC_AUC
* Model selection – Precison and Recall Ranks
* Hyper parameter tuning - GridSearchCV
* Final model – Best classifier model with good Recall and Precision Score and for this dataset XGB_Classifier satifies the following

### Impact on business: 
Hospital readmission is an important contributor to total medical expenditures and is an emerging indicator of quality of care. Diabetes, similar to other chronic medical conditions, is associated with increased risk of hospital readmission. As mentioned in the article “Correction to: Hospital Readmission of Patients with Diabetes”, hospital readmission is a high-priority health care quality measure and target for cost reduction, particularly within 30 days of discharge. The burden of diabetes among hospitalized patients is substantial, growing, and costly, and readmissions contribute a significant portion of this burden. Reducing readmission rates among patients with diabetes has the potential to greatly reduce health care costs while simultaneously improving care. Our aim is to provide some insights into the risk factors for readmission and also to identify the medicines that are the most effective in treating diabetes. 


