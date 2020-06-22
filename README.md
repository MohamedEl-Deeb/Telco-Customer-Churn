
# Capstone Project
## Project: Telco Churn Predication 

### Install

This project requires **Python 3.x** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/)
- [pandas_profiling](https://github.com/pandas-profiling/pandas-profiling)
- [imblearn](https://github.com/scikit-learn-contrib/imbalanced-learn)
- [xgboost](https://xgboost.readthedocs.io/en/latest/)
- [scikitplot](https://scikit-plot.readthedocs.io/)

You will also need to have software installed to run and execute an [iPython Notebook](http://ipython.org/notebook.html)

I recommend installing [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 


### Run

In a terminal or command window, navigate to the top-level project directory `finding_donors/` (that contains this README) and run one of the following commands:

```bash
ipython notebook finding_donors.ipynb
```  
or
```bash
jupyter notebook finding_donors.ipynb
```

This will open the iPython Notebook software and project file in your browser.

### Domain Background 

With the wide spread of smart phones telco companies are now a more important than ever and have a high number of customer but as the telco market matures and big companies compete in prices, service and quality of service every little advantage is needed for any company and since customers are the most important aspect that drives these companies it is highly important to retain customers in the company hence a churn model to help telco companies predict which customers are in danger of leaving the company is of extreme importance now more than ever. 

The primary motivation behind this model is the dire need of businesses to retain existing customers, coupled with the high cost associated with acquiring new ones. A review of the field has revealed a lack of efficient, rule-based Customer Churn Prediction (CCP) approaches in the telecommunication sector in my country. 

### Problem Statement 
Given a dataset of customer features, an algorithm needs to be developed to classify whether a customer will churn or not and try to determine what are the most contributing features in their churn while also investigating the reason behind the churn of said customers and if possible introduce a solution for different types of churn for the business. 

**Datasets and Inputs **
I will be using the Telco Customer Churn “Focused customer retention programs” Dataset [See here] from Kaggle. This was uploaded for examining customer retention and predicting churn and will be well suited to this study. The data contains more than 7043 row each row represents a customer and 21 features including the target label as a flag. 

- `customerID`: A unique identifier for each cutomer
- `gender`: Whether the customer is a male or a female
- `SeniorCitizen`: Whether the customer is a senior citizen or not (1, 0)
- `Partner`: Whether the customer has a partner or not (Yes, No)
- `Dependents`: Whether the customer has dependents or not (Yes, No)
- `tenureNumber of months the customer has stayed with the company 
- `PhoneService`: Whether the customer has a phone service or not (Yes, No)
- `MultipleLines`: Whether the customer has multiple lines or not (Yes, No, No phone service)
- `InternetServiceCustomer’s internet service provider (DSL, Fiber optic, No)
- `OnlineSecurity`: Whether the customer has online security or not (Yes, No, No internet service) 
- `OnlineBackup`: Whether the customer has online backup or not (Yes, No, No internet service)
- `DeviceProtection`: Whether the customer has device protection or not (Yes, No, No internet service)
- `TechSupport`: Whether the customer has tech support or not (Yes, No, No internet service)
- `StreamingTV`: Whether the customer has streaming TV or not (Yes, No, No internet service)
- `StreamingMovies`: Whether the customer has streaming movies or not (Yes, No, No internet service)
- `ContractThe contract term of the customer (Month-to-month, One year, Two year)
- `PaperlessBilling`: Whether the customer has paperless billing or not (Yes, No)
- `PaymentMethod`: The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
- `MonthlyCharges`: The amount charged to the customer monthly • TotalCharges`: The total amount charged to the customer

**Target Variable**
- `Churn`: Whether the customer churned or not (Yes or No)

An imbalance can be observed in the target label as the number of lost customers are 1890 rows while the number of non-churn customers are 5174 rows

### Solution Statement 

The proposed solution is to create classification model to classify customers whether they are going to churn or not and try to profile the churn types. I am going try different models using methods to tune these models and try to address the imbalance problem in the data using techniques such as SMOTE. 

### Benchmark Model 

Looking on some kernels on kaggle it can be observed that accuracy ranges from 84% to 73% with kernels using relatively simple models as logistic regression (See here)  an accuracy of 75% and sensitivity of 75%, other tree based models were used and they perform rather well.

### Evaluation Metrics

This study will be evaluated with regards to the model ability to accurately predict the customers that are in danger of churning I will use both F-Score and sensitivity to evaluate my model since the business is mainly concerned with lost customer since the lost customers present a threat to revenue and the cost of regaining a customer is always greater that the cost of keeping one. 
