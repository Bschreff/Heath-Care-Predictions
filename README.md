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
#### Glucose Level Affect on Stroke

![Unknown](https://user-images.githubusercontent.com/116525770/222199330-e106179f-f5da-42cd-9579-2abeeb7d9aab.png)

>From the Bar Plot we can see that a higher glucose level affects the probability of a stroke.
#### Heart Disease Affect on Stroke

![Unknown-1](https://user-images.githubusercontent.com/116525770/222200269-13c180fe-d6f1-45fd-b70f-a933c0c9bf9f.png)

> This Bar Plot shows that Heart Disease has a larger affect on the probability of a stroke, more so in men than women.

### Modeling:
I chose to try XGBoost, Random Forest, and KNeighbors. The model I chose to use was Random Forest with a SMOTE pipeline, to even out my training data, which was highly skewed to negative for stroke.  I then used GridSearchCV to hypertune the parameters. The model has an accurcy score of 91% it also had the least amount of false negatives.

### Limatations and Next Steps:
The model could be tuned more and explore data that might add to the predictabilty of the model to improve accuray. My next step would be to continue to work with the current models and to expirement with others to get more accurate results.
A person could use the visuals to see there risk of stroke and try to lower that risk by lifestyle changes.

### Recomendations:
While analyzing the data the biggest factors to stroke seem to be Heart Disease, Former/Current smoker, and Glucose Level. These should be the things to take into consideration. There are more than just those factors but they have a very strong correlation to stroke dianosis. Adding information to the data set such as, exercise, diet habits, blood pressure, and alcohol use may help with machine learning model. I would recomend the following:
Keep a healthy diet cut some sugar to lower glucose levels.
Keep a healthy weight. 
Get regular physical activity. 
Don't smoke. 
If you have Heart Disease consult your doctor on ways to prevent strokes.

### For further information:

email: brianschreffler1105@gmail.com



