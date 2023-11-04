# Employee Attrition Prediction

As Data Scientist consultants, our responsibility involves analyzing the factors that contribute to employee attrition within a company. We will create a machine learning model capable of predicting the likelihood of an employee leaving the company, and provide business recommendations based on the results of the predictions and analysis.


## About the Client 
### Sloth Company

Human resources are considered as an important aspect of an organization, and voluntary employee attrition has been identified as a key issue. Sloth Company one of the Biggest FMCG Company in Indonesia is concerned about this topic.
Based on data have been collected by their HR Department, Sloth Company want to identify whether an employee is likely to attrite so they can increase their ability to intervene on time and possibly provide a remedy to the situation to prevent attrition.
Sloth Company asked Data Dynasty to help them Predict and Identify which aspects drive the employee to attrite.

## What  is The Problem ?

Out of 1470 employees, 16.1% experienced attrition, which amounts to 237 employees. While the overall attrition rate of 16.1% may seem low, when referring to research from the Certified Human Resource Management Professional, a good attrition rate is considered to be no more than 10%. Thus, it can be concluded that the 16.1% attrition rate is indeed high.

Based on a study conducted by Raza, Munir, Almutairi, Younas, & Fareed in 2022, the cost of hiring a new employee is $4,129 per hire, according to the Society for Human Resource Management (SHRM). Therefore, when we calculate the total cost of attrition, which is 237 employees multiplied by $4,129, the cost amounts to $978,573. Hence, it can be concluded that high attrition leads to high recruitment costs.
#### Background 
Sloth Company want to know which aspects drive the employee to attrite.
####  Goals
Decrease the Attrition Rate from the target feature from 16,1%  to at least 10%. 
####  Objective 
Create a model to predict potential employee attrition and identify the aspects of employee attrition.
####  Business Metric
Attrition Rate (%)

## Exploratory Data Analysis
#### Attrition by Job Level
Majority of employees in the organization are at Entry Level or Junior Level. The Highest Attrition is at the Entry Level

#### Attrition by Over Time
Employees who overtime are more likely to  attrition compared to employees who do not overtime

#### Attrition by  Environment Satisfaction
Majority of employees rate organizational environment satisfaction High & Very High. However, there are still very high levels of attriton in this environment

## Data Preprocessing
Data Preprocesing Flow

 - Feature Selection
 - Feature Extraction
 - Feature Engineering
	 - Label Encoding 
	 - One Hot Encoding
 - Train Test Split
 - Handle Outlier in Data Train
 - Handling Imbalance Data Train

##  Modeling

Models tested:
 - Logistic Regression
 - AdaBoost
 - Random Forest
 -  XGBoost

After Hyperparameter tuning, the model with the highest Recall and fairly high accuracy is XGBOOST. Recall measures the ratio between the number of employees that are predicted to leave who actually leave the company, and the number of employees that are predicted to stay but actually end up leaving the company. Maximizing recall means minimizing the number of employees falsely predicted to stay.


## Feature Importance
Based on the feature importance plot, it can be determined that the most influential features on the model are JobLevel, Overtime, and Environment Satisfaction.

##  Recommendation
###  Recommendation HR

 - #### **Job Level and Overtime**
	 - Career Development
		 - Provide opportunities for advancement and Improve work efficiency
		 - Career development has a positive and significant effect on employee retention -Yadewani, D. (2021)
		 
- #### **Environment Satisfaction**
	 -  Improve environment facility
		 - Add and/or improve the quality of environmental facilities
		 - A positive work environment can help employees feel more motivated and productive, thereby reducing the likelihood of them leaving the organization. -Nam Choi, J (2019)

###  Recommendation Software Development
Creating a survey to predict whether an employee will experience attrition or not. If an employee is predicted not to experience attrition, they will remain with the company. However, if an employee is predicted to experience attrition, the next step is to provide treatment. After receiving treatment, employees who were initially predicted not to experience attrition will continue to stay with the company. Meanwhile, for employees predicted to experience attrition after receiving treatment, further analysis will be conducted.

## Business Impact
Before the model, there were 237 employees who experienced attrition. According to the confusion matrix results, it correctly detected 53 employees who were truly experiencing attrition (True Positives, TP), and 18 employees were incorrectly classified as not experiencing attrition when they actually were (False Negatives, FN).

Assuming that 50% of employees who were truly experiencing attrition do not experience attrition after the model (post-modeling), you can calculate the Attrition Rate as follows:

Attrition Rate = (0.5 * TP + FN) / Total

The number of employees experiencing attrition decreased by 90 after the model, resulting in a total of 147 employees experiencing attrition.

Before the model, the attrition rate was 16.1%, and it decreased by 6.1% after the model, resulting in an attrition rate of 10%.

Therefore, before the model, the company incurred a recruitment cost of USD 978,573. After the model, this cost decreased to USD 606,963, resulting in a cost saving of USD 371,610 for the company.
