# Introduction

Diabetes prediction ML models are crucial for early detection and prevention. By identifying individuals at high risk, timely interventions can be implemented to manage blood sugar levels, reduce complications, and improve overall health outcomes. In this project I am using Support Vector Machine (SVM) for predicting the likelihood of diabetes in individuals based on various health factors. I have built this model using diabetes dataset from the National Institute of Diabetes and Digestive and Kidney Diseases.

The data consists of the below columns that entail the health factors of each individual
- Pregnancies: Number of times pregnant
- Glucose: Plasma glucose concentration a 2 hours in an oral glucose tolerance test
- BloodPressure: Diastolic blood pressure (mm Hg)
- SkinThickness: Triceps skin fold thickness (mm)
- Insulin: 2-Hour serum insulin (mu U/ml)
- BMI: Body mass index (weight in kg/(height in m)^2)
- DiabetesPedigreeFunction: Diabetes pedigree function
- Age: Age (years)
- Label: Class variable (0 or 1)

# Data Cleaning and Preparation

Due to the presence of numerical columns with varying scales, I have scaled the data to prevent any one feature from dominating the model training process, ensuring all features contribute equally to the model's learning. 
My X variable consists of all health factors such as Glucose levels, BloodPressure, Skin Thickness, Insulin, etc 
which will be utilized to determine the Outcome (Y) - Diabetes (1) or Not Diabetes (0).

# Model Training 
Since this is a binary classification problem, I am using Support Vector Machine(SVM) for running the classification. Its strong performance in high-dimensional spaces and capacity to handle nonlinear relationships between features make it a valuable tool for identifying individuals at risk of diabetes.

# Model Performance
Recall is crucial in diabetes prediction because it measures the model's ability to correctly identify individuals who actually have diabetes. A high recall rate is essential to minimize false negatives, which means accurately detecting as many diabetic patients as possible. Early detection is vital for timely intervention and preventing severe complications associated with diabetes.

![ROC Curve](https://github.com/Sameeta9NK/PythonProjects/blob/main/Screenshot%202024-08-11%20112310.png)

An ROC AUC of ~80% for a diabetes classification model indicates a reasonably good performance. The model can distinguish between diabetic and non-diabetic individuals with moderate accuracy, but there's still room for improvement to increase sensitivity and specificity, especially in a critical application like diabetes prediction.

To prioritize recall in diabetes prediction, lower the classification threshold. This means more instances will be classified as positive (diabetic), increasing the chances of capturing true positives but also potentially leading to more false positives. The optimal threshold depends on the specific trade-off between recall and precision required for the application.


