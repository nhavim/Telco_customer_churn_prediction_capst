# Telco_customer_churn_classification
![image](https://github.com/user-attachments/assets/d8a48d46-7a15-4aa4-ab4b-12067e237113)


## Overview
The Telco-Churn-Classification challenge involves creating a machine learning model for an African telecom company to predict customer churn. Churn refers to customers becoming inactive and not making any transactions for 90 days. By identifying these potential churners, the company can take proactive steps to retain them and boost customer satisfaction.

The solution proposed from this project will help the Telco serve its customers better by identifying customers that are at risk of churning.

# Project Objective 
* Predict Customer Churn: Develop a machine learning model to accurately predict which customers are likely to become inactive or leave the service.
* Identify Key Drivers: Analyze data to identify the main factors that contribute to customer churn, such as usage patterns, customer demographics, and service issues.
* Enhance Customer Retention: Use insights from the model to design targeted retention strategies aimed at reducing churn and improving customer satisfaction.
* Improve Decision-Making: Provide actionable insights to help the company make data-driven decisions regarding customer service, marketing, and product development.
* Optimize Resource Allocation: Focus retention efforts and resources on customers who are most at risk of churning, thereby maximizing the efficiency of retention campaigns.
* Increase Revenue: By reducing churn, the company can maintain a stable customer base, leading to increased revenue and profitability.

# Project Summary
|  Code   |  Project name                                             |  Published Article |  Deployed App                                                      | Streamlit App                                  |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
|Capstone | Churn Prediction Classification with FastAPI and Streamlit| [Medium Article](---)     |  [FastAPI](https://abubakari-expresso-churn-prediction-fastapi.hf.space/docs) | [Streamlit App](https://abubakari-expresso-churn-prediction-streamlit.hf.space/)

# Project Setup
To set up the project environment, follow these steps:

1. Clone the repository:
git clone my_github

https://github.com/aliduabubakari/Expresso-Telco-Churn-Classification.git

2. Install the required dependencies:
pip install -r requirements.txt

3. Create a virtual environment:
   * Windows:

python -m venv venv
venv\Scripts\activate
   * Linux & MacOS:

python3 -m venv venv
source venv/bin/activate

You can copy each command above and run them in your terminal to easily set up the project environment.

# Data

The data for this project comprises a diverse collection of sepsis cases obtained from various sources [Zindi](https://zindi.africa/competitions/customer-churn-prediction-challenge-for-azubian)

# Data Fields

|   Column Name   |  Data Features  |	Description                                                                                            |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
---------------------------------------------------------------------------------------------------------------------------------------------
| REGION          | 	Categorical	  |    The location of each client                                                                         |
|-----------------|-----------------|--------------------------------------------------------------------------------------------------------|
| TENURE	        |   Numeric	      |    Duration with the network                                                                           |
|-----------------|-----------------|--------------------------------------------------------------------------------------------------------|
| MONTANT         |   Numeric	      |    Top-Up Amount                                                                                       |
|-----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
| FREQUENCE_RECH	|   Numeric	      |    The number of times a customer refilled                                                             |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
| REVENUE	        |   Numeric	      |    Monthly income of each client                                                                       |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
| ARPU_SEGMENT	  |   Numeric	      |    Income over 90 days divided by 3                                                                    |
|:----------------|:---------------:|--------------------------------------------------------------------------------------------------------|
| FREQUENCE       |   Numeric	      |    Number of times the client has made an income                                                       |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  DATA_VOLUME	  |   Numeric	      |    Number of connections                                                                               |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  ON_NET	        |   Numeric	      |    Inter Expresso call                                                                                 |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  ORANGE	        |   Numeric	      |    Calls to Orange                                                                                     |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  TIGO	          |   Numeric	      |    Calls to Tigo                                                                                       |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  ZONE1	        |   Numeric	      |    Calls to Zone1                                                                                      |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  ZONE2          |   Numeric       |    Calls to Zone2                                                                                      |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  MRG	          |   Categorical	  |    A client who is going                                                                               |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  REGULARITY	    |   Numeric	      |    Number of times the client is active for 90 days                                                    |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  TOP_PACK       | 	Categorical   |    The most active packs                                                                               |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  FREQ_TOP_PACK  |   Numeric	      |    Number of times the client has activated the top pack packages                                      |
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|
|  CHURN	        |   Binary	      |   Target variable to predict - Churn (Positive: customer will churn, Negative: customer will not churn)|
|:----------------|:---------------:|:-------------------------------------------------------------------------------------------------------|


# Exploratory Data Analysis
The exploratory data analysis (EDA) on telco customer churn can provide valuable insights into the factors that influence customer churn rates such 

* Univariate analysis: At this phase, each individual variable in the dataset is thoroughly examined. Summary statistics such as mean, median, standard deviation, and quartiles were calculated to understand the central tendency and spread of the data.
  Example is the visualisation of the churn variable below.

  ![image](https://github.com/user-attachments/assets/7cae1def-41b9-4481-a64c-5fc585d1274a)


  * Bivariate analusis: This phase examines the relationship between pairs of variables to identify and explore potential churn indicators.
  ![image](https://github.com/user-attachments/assets/e719ac7c-7f50-41e3-8d5a-82e1e61c1319)


  * Multivariate analysis
 ![image](https://github.com/user-attachments/assets/f063365c-aae1-467e-ad33-dca9d96b8756)


# Hypothesis
![image](https://github.com/user-attachments/assets/c52ffc5e-3544-48c9-84b1-b4030a365986)

Hypotheses were developed based on prior knowledge and existing research. Depending on the nature of the variables, statistical tests such as t-tests, chi-square tests, or ANOVA were employed to test these hypotheses. The outcomes of these tests either validated or refuted the hypotheses, offering further insights into the relationships between the variables.

* Hypothesis 1: Higher plasma glucose levels (PRG) are associated with an increased risk of developing sepsis.

* Hypothesis 2: Abnormal blood work results, such as high values of PL, SK, and BD2, are indicative of a higher likelihood of sepsis.

* Hypothesis 3: Older patients are more likely to develop sepsis compared to younger patients.

* Hypothesis 4: Patients with higher body mass index (BMI) values (M11) have a lower risk of sepsis.

* Hypothesis 5: Patients without valid insurance cards are more likely to develop sepsis.

These hypotheses, along with the results of the EDA, contribute to a deeper understanding of the dataset and provide valuable insights for further analysis and model development.

## Business Question
 *  1. What is the overall churn rate for the telecom company during the observed period?
![image](https://github.com/user-attachments/assets/24967b33-6986-4467-8730-82f51364cf2c)


 *  2. Are there any specific regions or geographic areas with a higher churn rate compared to others?
![image](https://github.com/user-attachments/assets/a19c0660-53e5-4fce-b302-d7409801f314)

 *  3. Do customers who have been with the network for a longer tenure exhibit lower churn rates?
    
![image](https://github.com/user-attachments/assets/84dc8478-140f-4f74-85ad-88280307e54a)

 *  4. Is there a correlation between top-up amount (MONTANT) and churn rate?
![image](https://github.com/user-attachments/assets/9b39a1b9-2e02-4910-b11f-baceb1f4feba)

 *  5. Are customers who frequently activate specific top pack packages (TOP_PACK) less likely to churn?
 ![image](https://github.com/user-attachments/assets/c8149bc8-4ee9-448b-a25d-33bec3e5fbb5)

## AUC score comparism of all models
![image](https://github.com/user-attachments/assets/004c2555-23db-4f10-a2df-02b1b30abf33)

## Logloss comparism
![image](https://github.com/user-attachments/assets/fc587fe3-b03f-46ce-a3cb-167e0a271ef1)

