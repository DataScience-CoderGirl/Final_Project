# Stroke Prediction

What if we could take a small amount of information about someone and tell them whether they were likely to have a stroke? Doctors could use a model like this to advise each patient of their risk and steps they could take to lower their odds of such an adverse health event. 

Using a dataset retrieved from https://www.kaggle.com/fedesoriano/stroke-prediction-dataset which contains just over 5,000 patients and eleven features we trained a variety of models in an attempt to optimize recall scores.  The data is highly imbalanced, with 248 patients that have had strokes and 4862 who have not.

In order to evaluate the usefulness of our models we decided that recall was the most important aspect of scoring for us to focus on.  The adverse effects of under-identifying potential stroke victims was much worse that the effects of over-identifying them.

In our initial modeling we used the dataset as it was provided, imbalanced.  Each of those models acheived very high accuracy simply by predicting that there would be zero stroke victims.

In order to better identify the minority group we used a combination of over and undersampling known as SMOTE.  With each model trained using SMOTE, recall went up considerably, while accuracy went down.

Attribute Information as listed on kaggle
1) id: unique identifier
2) gender: "Male" or "Female"
3) age: age of the patient
4) hypertension: 0 if the patient doesn't have hypertension, 1 if the patient has hypertension
5) heart_disease: 0 if the patient doesn't have any heart diseases, 1 if the patient has a heart disease
6) ever_married: "No" or "Yes"
7) work_type: "children", "Govt_jov", "Never_worked", "Private" or "Self-employed"
8) Residence_type: "Rural" or "Urban"
9) avg_glucose_level: average glucose level in blood
10) bmi: body mass index
11) smoking_status: "formerly smoked", "never smoked", "smokes" or "Unknown"*
12) stroke: 1 if the patient had a stroke or 0 if not
*Note: "Unknown" in smoking_status means that the information is unavailable for this patient

Project Contributors:
Sharon Bond
Mounika Ganta
Celia Watson

Acknowledgements per kaggle
(Confidential Source) - Use only for educational purposes
Kaggle contributor of dataset fedesoriano.