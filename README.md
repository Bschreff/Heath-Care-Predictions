# Heath Care Predictions

## An investigation of factors that may contribute to a person suffering a Stroke.

## Brian Schreffler

### Business Problem: 
Do any of the features have a strong or high correlation to whether or not a person has suffered a stroke?  
Can we predict if a person could have a stroke or is likely to have a stroke from this data?

### The Data:
The data consisted of 5110 rows, and 11 columns as listed below. The Data came from Kaggle: https://www.kaggle.com/code/sujithmandala/stroke-prediction-xgboost-99-3-auc
Attribute Information
| Variable Name.        |Description                                                                                                               
|------------------------|----------------------------------------------------------------------------------------|
|1) id:                 |unique identifier                                                                       |
|2) gender:             |"Male", "Female" or "Other"                                                             |
|3) age:                |age of the patient                                                                      |
|4) hypertension:       |0 if the patient doesn't have hypertension, 1 if the patient has hypertension.          |
|5) heart_disease:      |0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease. |
|6) ever_married:       |"No" or "Yes"                                                                           |
|7) work_type:          |"children", "Govt_jov", "Never_worked", "Private" or "Self-employed"                    |
|8) Residence_type:     |"Rural" or "Urban"                                                                      |
|9) avg_glucose_level:  |average glucose level in blood                                                          |
|10) bmi:               |body mass index                                                                         |
|11) smoking_status:    |"formerly smoked", "never smoked", "smokes" or "Unknown"*                               |
|12) stroke:            |1 if the patient had a stroke or 0 if not                                               |
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient                    

#### Data Cleaning:
I removed Gender other and used SimpleImputer from scikitlearn to impute the missing values for 'bmi' on the training data to avoid data leakage.

### Insights from Visualizing the Data:
![Unknown](https://user-images.githubusercontent.com/116525770/222199330-e106179f-f5da-42cd-9579-2abeeb7d9aab.png)


