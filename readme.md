
# Stroke Prediction 

According to the World Health Organization (WHO) stroke is the 2nd leading cause of death globally, responsible for approximately 11% of total deaths.
This dataset is used to predict whether a patient is likely to get stroke based on the input parameters like gender, age, various diseases, and smoking status. Each row in the data provides relavant information about the patient.Therefore, our dependent variable here is stroke and we will try to predict this variable by using independent variables.



## Attribute Information


- id: unique identifier
- gender: "Male", "Female" or "Other"
- age: age of the patient
- hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
- heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
- ever_married: "No" or "Yes"
- work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
- Residence_type: "Rural" or "Urban"
- avg_glucose_level: average glucose level in blood
- bmi: body mass index
- smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
- stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient

Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target. Since it will be a kaggle submission, the output should be;



## Sample Output

```javascript
id    stroke
15304  0.23
15305  0.55
15306  0.98
etc.
```


## Acquirements

Outliers and NULL values were checked, only "bmi" column had some NULL values and they were dropped. Variables and their relationships, and correlations were inspected with different plots. In previous versions of work, the RandomForestClassifier was used as an algorithm. However, StratifiedKFold gave better results than RandomForestClassifier. Therefore, StratifiedKFold used and tuned.

Here are the steps that are taken in this analysis period:

- Reading Related Files
- Controlling Variables whether They Contain Null or Not
- Merging Train and Original Dataset
- Separating Numericals and Categoricals In Order to Visualise
- Interpretting the Variables with Describe Method
- Plotting Sides
- Model Creation and Separation of Dependent/Independent Variables
- Model Parameter Tuning
- Inspection of ROC Curve and Variable Importances Plot
- Submission of File

The score is found : 87.8%

