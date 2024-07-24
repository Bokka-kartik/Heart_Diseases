Predicting Heart Disease Using Logistic Regression

Heart disease is a significant global health concern, responsible for millions of deaths each year. Early prognosis and risk assessment play a crucial role in managing cardiovascular health. In this context, logistic regression—a popular machine learning technique—can help us predict the risk of coronary heart disease (CHD) based on various patient characteristics.

Here’s a step-by-step breakdown of how we approach heart disease prediction using logistic regression:

Data Preparation:
We start with a dataset. In one example, researchers used data from an ongoing cardiovascular study in Framingham, Massachusetts. The goal was to predict whether a patient has a 10-year risk of future CHD.
The dataset includes over 4,000 records and 15 attributes. These attributes fall into three categories:
Demographic Factors:
Sex (Gender): Male or female (nominal).
Age: Continuous (although recorded ages are truncated to whole numbers).
Behavioral Factors:
Current Smoker: Whether the patient is a current smoker (nominal).
Cigarettes Per Day: Average number of cigarettes smoked per day (can be considered continuous).
Medical History:
Blood Pressure Medication (BPMeds): Whether the patient was on blood pressure medication (nominal).
Prevalent Stroke: Whether the patient had previously experienced a stroke (nominal).
Prevalent Hypertension (prevalentHyp): Whether the patient was hypertensive (nominal).
Diabetes: Whether the patient had diabetes (nominal).
Current Medical Measurements:
Total Cholesterol Level (totChol): Continuous.
Systolic Blood Pressure (sysBP): Continuous.
Diastolic Blood Pressure (diaBP): Continuous.
Body Mass Index (BMI): Continuous.
Heart Rate: Continuous.
Glucose Level: Continuous.
Target Variable:
10-Year Risk of CHD (CHD): Binary (1 for “Yes,” indicating risk; 0 for “No”).
Handling Missing Values:
Before modeling, we need to address any missing values in the dataset. Checking for missing values using heart_df.isnull().sum() helps ensure data quality.
Logistic Regression Model:
Logistic regression is a binary classification algorithm. It estimates the probability of an event (in this case, CHD risk) based on input features.
We fit a logistic regression model to our data, considering the relevant features.
The model learns the relationship between these features and the likelihood of CHD risk.
Model Evaluation:
We assess the model’s performance using metrics like accuracy, precision, recall, and the confusion matrix.
Cross-validation techniques help validate the model’s generalization ability.
Interpreting Coefficients:
Logistic regression provides coefficients for each feature. These coefficients indicate the impact of each feature on the log-odds of CHD risk.
Positive coefficients increase the log-odds (and thus the risk), while negative coefficients decrease it.
Predictions:
Once the model is trained, we can make predictions for new patients.
Given a set of patient characteristics, the model estimates the probability of CHD risk.
