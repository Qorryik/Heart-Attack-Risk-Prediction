# **HEART ATTACK RISK PREDICTION**

## 📌 Project Overview

This dataset contains patient health, lifestyle, medical, and demographic information related to heart attack risk. It includes clinical indicators such as age, cholesterol, blood pressure, and heart rate, lifestyle factors like exercise, diet, stress, and smoking, as well as medical history and socioeconomic attributes. With 8,763 records collected from patients worldwide, the dataset is designed for binary classification to predict the presence or absence of heart attack risk.

---

## 📂 Dataset Information

**Source:**
🔗 [https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset)

## 🧾 Column Description

| Column Name                     | Description                                              |
| ------------------------------- | -------------------------------------------------------- |
| Patient ID                      | Unique identifier for each patient                       |
| Age                             | Age of the patient                                       |
| Sex                             | Gender of the patient (Male/Female)                      |
| Cholesterol                     | Cholesterol levels of the patient                        |
| Blood Pressure                  | Blood pressure of the patient (systolic/diastolic)       |
| Heart Rate                      | Heart rate of the patient                                |
| Diabetes                        | Whether the patient has diabetes (Yes/No)                |
| Family History                  | Family history of heart-related problems (1: Yes, 0: No) |
| Smoking                         | Smoking status (1: Smoker, 0: Non-smoker)                |
| Obesity                         | Obesity status (1: Obese, 0: Not obese)                  |
| Alcohol Consumption             | Alcohol consumption level (None/Light/Moderate/Heavy)    |
| Exercise Hours Per Week         | Number of exercise hours per week                        |
| Diet                            | Dietary habits (Healthy/Average/Unhealthy)               |
| Previous Heart Problems         | History of heart problems (1: Yes, 0: No)                |
| Medication Use                  | Medication usage (1: Yes, 0: No)                         |
| Stress Level                    | Reported stress level (1–10)                             |
| Sedentary Hours Per Day         | Hours of sedentary activity per day                      |
| Income                          | Income level of the patient                              |
| BMI                             | Body Mass Index                                          |
| Triglycerides                   | Triglyceride levels                                      |
| Physical Activity Days Per Week | Number of active days per week                           |
| Sleep Hours Per Day             | Hours of sleep per day                                   |
| Country                         | Country of residence                                     |
| Continent                       | Continent of residence                                   |
| Hemisphere                      | Hemisphere of residence                                  |
| Heart Attack Risk               | Target variable (1: Yes, 0: No)                          |

---

## 🔍 Analysis Workflow

### 1. Hypothesis
* The risk of heart disease increases as a person gets older.
* Men tend to have a higher risk of heart attacks then women.
* Higher cholesterol levels are associated with a higher risk of heart attacks.
* High blood pressure (hypertension) is one of the main factors contributing to heart disease.
* A higher heart rate per minute is linked to an increased risk of heart attacks.
* People with diabetes have a higher risk of experiencing a heart attack.
* Individuals with a history of heart problems are more likely to experience another heart attack.
* Smoking and alcohol consumption increase the risk of heart attacks.
* More physical activity, such as higher exercise hours per week and more active days, helps reduce the risk of heart attacks.
* Getting enough sleep, not too little and not too much, can affect stress levels and indirectly influence heart attack risk.
* A high BMI, which indicates obesity caused by unhealthy eating habits, increases the risk of heart attacks.

### 2. Exploratory Data Analysis (EDA)

* Data consistency checks
* Handling anomalies and missing values
* Feature understanding

### 3. Data Visualization

Key questions explored:

* How does the risk of heart disease change as age increases?
* Is there a difference in heart attack risk between men and women across different age groups?
* How are cholesterol levels related to heart attack risk?
* Does higher blood pressure increase the likelihood of heart disease?
* Is a higher resting heart rate associated with an increased risk of heart attacks?
* Do people with diabetes have a higher heart attack risk compared to those without diabetes?
* How does a history of heart problems affect the risk of future heart attacks?
* How do smoking and alcohol consumption influence heart attack risk?
* Does increased physical activity, such as more exercise hours and active days per week, reduce heart attack risk?
* How do sleep duration and stress levels together influence heart attack risk?
* How does a high BMI, as an indicator of obesity, relate to heart attack risk?
* Which countries have the highest number of heart attack cases in the dataset?

### 4. Predictive Modeling

* Random Forest
* Logistic Regression
* Gradient Boosting

---

## 📊 Visualization Result

**FINAL CONCLUSION:**

Based on the overall data analysis, heart attack risk is influenced by multiple factors rather than a single variable. Demographic factors such as gender show a clear pattern, where men have a higher heart attack risk than women. Age alone does not consistently increase risk, although early middle age (36–45) appears to be a stage where risk factors start to accumulate.

Several medical and lifestyle factors are strongly associated with heart attack risk. High blood pressure, diabetes, smoking, and alcohol consumption show a clear relationship with increased risk and can be considered major contributing factors. High cholesterol also shows a positive association, although the difference is relatively small. On the other hand, resting heart rate, physical activity levels, BMI, and family history do not show a strong or clear relationship with heart attack risk in this dataset, even though some of these factors are known to be important in real-life medical contexts.

Sleep patterns show an indirect effect, where too little or too much sleep is associated with higher stress levels, which may contribute to heart attack risk. From a geographical perspective, Asia has the highest total heart attack risk at the continent level due to the combined contribution of many countries, while Germany has the highest total risk at the country level, highlighting the difference between aggregated and individual-level analysis.

Overall, this analysis suggests that heart attack risk is best understood as the result of a combination of medical conditions and lifestyle behaviors, rather than isolated factors alone.

---

## 🤖 Machine Learning Results

In this study, three classification models Logistic Regression, Random Forest, and Gradient Boosting were evaluated to predict heart attack risk using an imbalanced dataset. The results show that Logistic Regression and Gradient Boosting achieved high recall for the positive class after tuning; however, this was accompanied by very low precision and accuracy, indicating that the models tended to predict most samples as positive cases. This behavior led to a high number of false positives.

Random Forest produced more balanced results, with moderate recall, precision, and accuracy across both classes. Although its overall performance was not high, it demonstrated a better trade-off between detecting positive cases and avoiding excessive false positives.

Overall, increasing model complexity and applying advanced tuning techniques did not lead to a significant improvement in predictive performance. This suggests that the limited performance is mainly influenced by the overlap of features between classes and the imbalance of the dataset, rather than the choice of classification algorithm. Therefore, Random Forest is considered the most stable model in this study, while the results highlight the importance of data quality and feature relevance for improving prediction performance.
