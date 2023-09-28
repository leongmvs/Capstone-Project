# HealthCare_Predictive_Analysis_On_Heart_Diseases

## Role & Objectives
As a Data Analyst working on the project for Parkway Pantai, a private healthcare provider. My objective of this project is to develop a machine learning model that can effectively predict the presence or absence of heart disease based on various medical and lifestyle factors.

## Details
Heart disease is a leading cause of mortality worldwide. Early detection and accurate prediction of heart disease can significantly improve patient outcomes by enabling timely intervention and preventive measures. As health care trends evolve quickly over the years, staying updated with evolving healthcare trends and technologies is crucial to effectively analyze and interpret data

## Folder Overview

.\
├── cardio_data.csv\
├── Data_Disctionary.pdf\
├── eda.ipynb\
├── P2 Healthcare PA.pdf\
├── README.md\
├── requirements.txt\

## Feature Preprocessing Summary
- Date Type to change from "Object" to "Datetime"
- Country is in nominal, require check for unique values
- ID not necessary, to be drop
- To convert Age from "days" to "years"
- Negative value present in blood pressure, to convert to positive values
- Outliers present in blood pressure, necessary to remove
- Outliers present in height & weight, necessary to remove
  
## EDA Findings
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/9b7b34f6-2cae-4a5c-860a-a8440c4e2813)
- To identify bell curve as left or right skewed, usually it represent a biasness in the data
---
  
 ![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/6468582b-369e-4f5f-bfb0-9352b2fe3275)
- High correlation between heart disease and these parameters: ap_hi, ap_lo, current_age, cholesterol, weight
---
  
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/784ddf9b-3b89-4b64-866e-7982dcc6216f)
- Trend 1: The taller you are, the heavier you would be
- Trend 2: In each height category, those with heart disease tend to weigh heavier than those without
- Trend 3: A lot outliers between the height 140 -180cm
---
  
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/fb680aff-efe0-4b79-9404-9803931fe07b)
- There is a significant number of ppl from the height group in red. Hence, this might shift the biasness of the data towards the majority. Even though height does not have any corelation to heart disease, but from the previous graph we can tell that the height and weight ratio might have a high corelation to heart disease
---
  
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/6e42ebd5-451f-43ea-9973-e67dc235b6e9)
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/7557e5fe-7b63-4af3-aa11-df2ead617946)
- Did not notice any obvious trend despite blood pressure having a high correlation to heart disease
---
  
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/3a52bada-26a3-445e-9d90-e0ce386110a6)
- To check if the targeted variable is evenly distributed
---
  
## Model Choices
- Random Forest
- Logisitc Regression
- Decision Tree
- KNN

# Model Evaluation

Models are evaluated based on testset MSE between predictions and true values. Model with the lowest testset MSE is evaluated as the best model.

Model: Random Forest
Accuracy: 0.72
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/8a5d58f2-dd73-4de7-b058-52d661dccdeb)

---

Model: Logistic Regression
Accuracy: 0.71
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/56d35755-01a2-4692-9be8-9b05cef60ad1)

---

Model: Decision Tree
Accuracy: 0.63
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/fa300a37-d39e-4f0d-9bfc-d2a75908ff6d)

---

Model: KNN
Accuracy: 0.69
![image](https://github.com/leongmvs/Capstone-Project/assets/145515502/5bb253db-7a6f-467e-86ab-dbda20ffd098)

---
# Conclusion & Takeaways
Utilizing the machine learning model, it becomes evident that the random forest model achieves the highest level of accuracy. Through the exploratory data analysis (EDA), we have identified the pivotal factors contributing to heart disease. Understanding these key contributors empowers us to advocate preventive measures more effectively, thereby reducing the incidence of heart diseases within the population. With the developed ML model, early detection of heart disease is achievable, leading to enhanced patient outcomes through timely intervention and preventive strategies.

In summary, the main insights from this project are as follows:
Given additional time and a deeper understanding, my focus would involve fine-tuning the model parameters, specifically:

- Refining the height-to-weight ratio
- Investigating the correlation between systolic and diastolic measurements

I firmly believe that implementing these enhancements will considerably elevate the predictive capabilities of the machine learning model.

---
# Created By:
- Name: Leong Wan Ning
- Email: Maeris3939@gmail.com
- Phone: +65 9339 3907
