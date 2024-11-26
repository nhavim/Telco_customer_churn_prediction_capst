# Expresso_customer_churn_classification

## Overview
The Telco-Churn-Classification challenge involves creating a machine learning model for an African telecom company to predict customer churn. Churn refers to customers becoming inactive and not making any transactions for 90 days. By identifying these potential churners, the company can take proactive steps to retain them and boost customer satisfaction.
![image](https://github.com/user-attachments/assets/ba9bdc86-477c-4dfd-bba3-0cd21dab825d)

The solution proposed from this project will help the Telco serve its customers better by identifying customers that are at risk of churning.

# Project Objective 
* Predict Customer Churn: Develop a machine learning model to accurately predict which customers are likely to become inactive or leave the service.
* Identify Key Drivers: Analyze data to identify the main factors that contribute to customer churn, such as usage patterns, customer demographics, and service issues.
* Enhance Customer Retention: Use insights from the model to design targeted retention strategies aimed at reducing churn and improving customer satisfaction.
* Improve Decision-Making: Provide actionable insights to help the company make data-driven decisions regarding customer service, marketing, and product development.
* Optimize Resource Allocation: Focus retention efforts and resources on customers who are most at risk of churning, thereby maximizing the efficiency of retention campaigns.
* Increase Revenue: By reducing churn, the company can maintain a stable customer base, leading to increased revenue and profitability.

## Project Summary
|  Code   |  Project name          |  Published Article |  Deployed App     | Streamlit App                                  |
|:----:|:----:|:----:|:------:|:-----:|
|Capstone | Churn Prediction Classification with FastAPI and Streamlit| [Medium Article](---)     |  [FastAPI](https://abubakari-expresso-churn-prediction-fastapi.hf.space/docs) | [Streamlit App](https://abubakari-expresso-churn-prediction-streamlit.hf.space/)

## Project Setup
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

## Data

The data for this project comprises a diverse collection of sepsis cases obtained from various sources [Zindi](https://zindi.africa/competitions/customer-churn-prediction-challenge-for-azubian)

## Data Fields

|   Column Name   |  Data Features  |	Description                                                                                            |
|:---:|:---:|:---|
| REGION          | 	Categorical	  |    The location of each client                                                                         |
| TENURE	        |   Numeric	      |    Duration with the network                                                                           |
| MONTANT         |   Numeric	      |    Top-Up Amount                                                                                       |
| FREQUENCE_RECH	|   Numeric	      |    The number of times a customer refilled                                                             |
| REVENUE	        |   Numeric	      |    Monthly income of each client                                                                       |
| ARPU_SEGMENT	  |   Numeric	      |    Income over 90 days divided by 3                                                                    |
| FREQUENCE       |   Numeric	      |    Number of times the client has made an income                                                       |
|  DATA_VOLUME	  |   Numeric	      |    Number of connections                                                                               |
|  ON_NET	        |   Numeric	      |    Inter Expresso call                                                                                 |
|  ORANGE	        |   Numeric	      |    Calls to Orange                                                                                     |
|  TIGO	          |   Numeric	      |    Calls to Tigo                                                                                       |                 |
|  ZONE1	        |   Numeric	      |    Calls to Zone1                                                                                      |
|  ZONE2          |   Numeric       |    Calls to Zone2                                                                                      |
|  MRG	          |   Categorical	  |    A client who is going                                                                               |
|  REGULARITY	    |   Numeric	      |    Number of times the client is active for 90 days                                                    |
|  TOP_PACK       | 	Categorical   |    The most active packs                                                                               |
|  FREQ_TOP_PACK  |   Numeric	      |    Number of times the client has activated the top pack packages                                      |
|  CHURN	        |   Binary	      |   Target variable to predict - Churn (Positive: customer will churn, Negative: customer will not churn)|

## Exploratory Data Analysis
The exploratory data analysis (EDA) on telco customer churn can provide valuable insights into the factors that influence customer churn rates such 

* Univariate analysis: At this phase, each variable in the dataset is thoroughly examined. Summary statistics such as mean, median, standard deviation, and quartiles were calculated to understand the central tendency and spread of the data.
  An example is the visualization of the churn variable below.

  ![image](https://github.com/user-attachments/assets/7cae1def-41b9-4481-a64c-5fc585d1274a)


  * Bivariate analysis: This phase examines the relationship between pairs of variables to identify and explore potential churn indicators.
  ![image](https://github.com/user-attachments/assets/e719ac7c-7f50-41e3-8d5a-82e1e61c1319)


  * Multivariate analysis
 ![image](https://github.com/user-attachments/assets/f063365c-aae1-467e-ad33-dca9d96b8756)


## Hypothesis
![image](https://github.com/user-attachments/assets/c52ffc5e-3544-48c9-84b1-b4030a365986)

Hypotheses were developed based on prior knowledge and existing research. Depending on the nature of the variables, statistical tests such as t-tests, chi-square tests, or ANOVA were employed to test these hypotheses. The outcomes of these tests either validated or refuted the hypotheses, offering further insights into the relationships between the variables.

* Hypothesis 1: Higher plasma glucose levels (PRG) are associated with an increased risk of developing sepsis.

* Hypothesis 2: Abnormal blood work results, such as high PL, SK, and BD2 values, indicate a higher likelihood of sepsis.

* Hypothesis 3: Older patients are more likely to develop sepsis than younger patients.

* Hypothesis 4: Patients with higher body mass index (BMI) values (M11) have a lower risk of sepsis.

* Hypothesis 5: Patients without valid insurance cards are more likely to develop sepsis.

These hypotheses alongside the EDA, contribute to a deeper understanding of the dataset and provide valuable insights for further analysis and model development.

### Business Question
 *  1. What is the overall churn rate for the telecom company during the observed period?
![image](https://github.com/user-attachments/assets/24967b33-6986-4467-8730-82f51364cf2c)


 *  2. Are there any specific regions or geographic areas with a higher churn rate than others?
![image](https://github.com/user-attachments/assets/a19c0660-53e5-4fce-b302-d7409801f314)

 *  3. Do customers who have been with the network for a longer tenure exhibit lower churn rates?
    
![image](https://github.com/user-attachments/assets/84dc8478-140f-4f74-85ad-88280307e54a)

 *  4. Is there a correlation between top-up amount (MONTANT) and churn rate?
![image](https://github.com/user-attachments/assets/9b39a1b9-2e02-4910-b11f-baceb1f4feba)

 *  5. Are customers who frequently activate specific top-pack packages (TOP_PACK) less likely to churn?
 ![image](https://github.com/user-attachments/assets/c8149bc8-4ee9-448b-a25d-33bec3e5fbb5)

# Modelling

During the modeling phase, the evaluation of models took into consideration the imbalanced nature of the data. The main metrics used to assess model performance were the F1 score and AUC score, which provide a balanced assessment for imbalanced datasets.

The following models were evaluated:

Logistic Regression
Decision Tree
Random Forest
Gaussian Naive Bayes
Gradient boosting
Cat boost
XGBoost
ComplementNB
These models were evaluated based on their AUC and log loss scores, providing insights into their performance on the imbalanced dataset. Below is the results;

## AUC score comparison of all models
![image](https://github.com/user-attachments/assets/004c2555-23db-4f10-a2df-02b1b30abf33)

## Logloss comparison
![image](https://github.com/user-attachments/assets/fc587fe3-b03f-46ce-a3cb-167e0a271ef1)

Given the imbalanced nature of our dataset, we assessed the models' performance using the AUC metric.

Logistic Regression and GradientBoosting models emerged as the 🏆 top-performing models, achieving the highest AUC scores.
ComplementNB consistently demonstrated high performance across different conditions.
GaussianNB had a relatively lower AUC score and higher log loss compared to other models.
XGBoost, CatBoost, and Random Forest models showed improved performance compared to previous conditions.
Decision Tree model performed relatively poorer in terms of AUC score.

# Deployment

## Fastapi deployment
Make sure you have FastAPI and any necessary dependencies installed. You can install FastAPI using pip:
pip install fastapi
Open a terminal or command prompt and navigate to the directory where your main.py file is located.

Run the FastAPI application using the uvicorn command, specifying the module and application name:

uvicorn main:app --reload
After running the command, you should see an output indicating that the FastAPI application is running and listening on a specific address (e.g., http:localhost:8000). This address represents the API endpoint where you can access your application.

Open a web browser or use an API testing tool (e.g., Postman) to interact with your deployed FastAPI application. Use the API endpoint provided in the terminal to make requests and receive responses.

## API Documentation
The API documentation provides details about the available endpoints, request and response formats, and example usage. You can access the documentation by visiting the /docs endpoint after starting the server (http://localhost:8000/docs).

## Containerized deployment
To.  run the Docker container based on the provided Dockerfile, follow these steps:

* 1. Make sure you have Docker installed on your system.

* 2. Create a new file named Dockerfile (without any file extension) in the root directory of your project.

* 3. Copy the content of the Dockerfile you provided into the newly created Dockerfile.

* 4. Open a terminal or command prompt and navigate to the directory where the Dockerfile is located.

* 5. Build the Docker image by running the following command:

docker build -t your-image-name.
* 6. Replace your-image-name with the desired name for your Docker image. The . at the end denotes the current directory as the build context.

* 7. Once the image is built, you can run a Docker container based on that image using the following command:

docker run -d -p host-port:container-port your-image-name
Replace host-port with the port number on your host machine that you want to map to the container's port, and replace container-port with the port number specified in the Dockerfile's EXPOSE instruction (in this case, it's 8000).

For example, if you want to map the container's port 8000 to port 8080 on your host machine, the command would be:

docker run -d -p 8080:8000 your-image-name
* 8. After running the command, the Docker container will start, and your FastAPI application will be running inside the container.

* 9. You can access your application by visiting http://localhost:host-port in your web browser or using an API testing tool.

For example, if you mapped the container's port 8000 to your host's port 8080, you would access the application at http://localhost:8080.

## Streamlit deployment
Navigate to the cloned repository and run the command:

pip install -r requirements.txt
To run the demo app (being at the repository root), use the following command:

streamlit run streamlit_app.py
App Execution on Huggingface
Here's a step-by-step process on how to use the Streamlit App on Huggingface:

![image](https://github.com/user-attachments/assets/71e9dff0-8a68-44db-bb88-a8ed12689a0e)
### How to Use
* 1. Select your model of choice on the left sidebar.
* 2. Adjust the input parameters based on customer details
* 3. Click the "Predict" button to initiate the prediction.
* 4. The app will simulate a prediction process with a progress bar.
* 5. Once the prediction is complete, the results will be displayed below.
![image](https://github.com/user-attachments/assets/bb232c58-8a09-4a4f-b3a0-244dfad25321)

![image](https://github.com/user-attachments/assets/f192d1c2-c0c4-4b6c-bfe0-6c63c25e8351)

![image](https://github.com/user-attachments/assets/5be660c5-9afe-460f-880b-de6c5f0b9119)

### Fastapi on Huggingface
Here's a step-by-step process on how to use the [FastAPI](https://abubakari-expresso-churn-prediction-fastapi.hf.space/docs) on Huggingface:

![image](https://github.com/user-attachments/assets/5d34596e-2711-406e-b803-109a047750dd)

# Contribution
Get involved! Contribute to Expresso Churn classification project on GitHub and be part of a community that's changing the game!

## How to Contribute

* 1. Fork the repository on GitHub
* 2. Choose an issue to work on from our issue tracker
* 3. Submit a pull request with your changes
* 4. Join our community chat to discuss your contribution

We look forward to collaborating with you!

# Author
Nathaniel Havim          [LinkedIn](https://www.linkedin.com/in/nathaniel-havim/) 
Data Analyst
Azubi Africa
