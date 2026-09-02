**Intelligent Customer Churn Risk Prediction and Behavioural Segmentation System**
**Project Overview**

Customer churn is an important business problem in which customers discontinue using a company's products or services. Identifying customers who are likely to churn in advance allows organizations to take suitable retention actions and improve customer satisfaction.

This project develops an Intelligent Customer Churn Risk Prediction and Behavioural Segmentation System using Machine Learning. The system combines supervised learning for churn prediction with unsupervised learning for customer segmentation.

The system predicts whether a customer is likely to Churn or Not Churn, assigns a churn-risk level, groups customers into behavioural segments using K-Means clustering, and provides retention recommendations for high-risk customer groups.

**Objectives**

The main objectives of this project are:

To analyse customer information and identify factors related to churn.

To preprocess and prepare customer data for machine learning.

To build and compare multiple supervised machine learning models.

To predict whether a customer is likely to churn.

To evaluate classification models using multiple performance metrics.

To identify meaningful customer groups using K-Means clustering.

To use PCA for visualizing customer segments.

To identify high-risk customer groups.

To provide suitable customer retention recommendations.

**Key Features**

Customer data preprocessing

Missing-value handling

Categorical feature encoding

Feature scaling

Exploratory Data Analysis

Customer churn prediction

Multiple machine learning algorithms

Model performance comparison

Confusion matrix analysis

Hyperparameter tuning

K-Means customer segmentation

Elbow Method and Silhouette Score analysis

PCA-based cluster visualization

Churn probability estimation

Low, Medium, and High risk classification

High-risk customer identification

Retention recommendations

**Dataset**

The project uses the Telco Customer Churn dataset.

Dataset Source: Kaggle – Telco Customer Churn Dataset

The dataset contains customer demographic information, service details, account information, billing information, and the target variable Churn.

The dataset contains:

7,043 customer records
21 attributes
Target variable: Churn

**Important attributes include:**

Gender

Senior Citizen

Partner

Dependents

Tenure

Phone Service

Internet Service

Online Security

Online Backup

Device Protection

Tech Support

Streaming Services

Contract

Paperless Billing

Payment Method

Monthly Charges

Total Charges

Churn

The customerID attribute is removed during preprocessing because it is an identifier and does not provide useful predictive information.

**Technologies Used**

Programming Language

Python

Development Environment

Google Colab

Jupyter Notebook

Libraries

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Joblib

Machine Learning Methodology

**The project follows an end-to-end machine learning workflow:**

Customer Dataset

       ↓

Data Inspection

       ↓

Data Preprocessing

       ↓

Exploratory Data Analysis

       ↓

Train-Test Split

       ↓

Supervised ML Models

       ↓

Model Evaluation

       ↓

Best Model Selection
   
       ↓

Churn Probability Prediction
 
       ↓

K-Means Customer Segmentation
    
       ↓

PCA Visualization
     
       ↓

Risk Identification

       ↓

Retention Recommendations

**Data Preprocessing**

The following preprocessing operations are performed:

Dataset structure and data types are inspected.

Missing values are identified and handled.

TotalCharges is converted into numerical format.

customerID is removed as an irrelevant identifier.

Categorical variables are encoded using appropriate encoding techniques.

Numerical features are scaled where required.

The target variable Churn is converted into a binary representation.

The dataset is divided into training and testing sets using a stratified split.

**Exploratory Data Analysis**

EDA is performed to understand customer behaviour and identify patterns related to churn.

The analysis includes:

Overall churn distribution

Tenure distribution

Monthly charge analysis

Customer service usage

Contract-related patterns

Comparison of churn across important customer characteristics

Visualizations are generated using Matplotlib and Seaborn.

**Supervised Machine Learning Models**

Four classification algorithms were implemented and compared:

Logistic Regression

Gaussian Naive Bayes

Support Vector Machine (SVM)

Decision Tree

**The models were evaluated using:**

Accuracy

Precision

Recall

F1-Score

ROC-AUC

Confusion Matrix

Model Performance

**The obtained classification results are:**

Model	Accuracy	Precision	Recall	F1-Score	ROC-AUC

Logistic Regression	0.8055	0.6572	0.5588	0.6040	0.8419

Naive Bayes	0.6948	0.4589	0.8639	0.5980	0.8074

SVM	0.7913	0.6418	0.4840	0.5518	0.7905

Decision Tree	0.7289	0.4896	0.5063	0.4974	0.6573

**Best Model**

Logistic Regression was selected as the final churn classification model because it achieved the highest F1-score among the evaluated models.

Accuracy: 80.55%

Precision: 65.72%

Recall: 55.88%

F1-Score: 60.40%

ROC-AUC: 84.19%

The model provides a balanced performance between identifying churners and avoiding excessive false predictions.

**Hyperparameter Tuning**

Hyperparameter experimentation was performed for the Decision Tree model using GridSearchCV.

The best configuration obtained was:

max_depth = 5

min_samples_split = 2

**The tuned Decision Tree achieved:**

Accuracy: 79.84%

Precision: 63.47%

Recall: 56.68%

F1-Score: 59.89%

ROC-AUC: 82.97%

**Customer Segmentation**

K-Means clustering is used to divide customers into meaningful behavioural groups.

The Elbow Method and Silhouette Score were used to determine an appropriate number of clusters.

The final implementation uses 3 customer segments.

**Cluster Results**

Cluster	Customers	Average Tenure	Average Monthly Charges	Churn Rate

Cluster 0	1,526	30.55 months	21.08	7.40%

Cluster 1	3,189	15.30 months	67.86	44.03%

Cluster 2	2,328	56.95 months	89.15	15.12%

**Segment Interpretation**

**Cluster 0 – Low-Charge Stable Customers**

These customers have relatively low monthly charges and a low churn rate. They represent a comparatively stable customer group.

**Cluster 1 – Short-Tenure High-Risk Customers**

This group has relatively shorter tenure and higher monthly charges. It has the highest churn rate of 44.03%, making it the most important segment for targeted retention strategies.

**Cluster 2 – Long-Tenure Premium Customers**

These customers have longer tenure and higher monthly charges while maintaining a comparatively lower churn rate. They represent valuable long-term customers.

**Churn Risk Analysis**

The system also converts predicted churn probabilities into configurable risk categories:

Probability < 0.30       → Low Risk

0.30 – < 0.60            → Medium Risk

Probability ≥ 0.60       → High Risk

These thresholds are project-defined rules used to support customer prioritization.

High-risk customers can then be analysed together with their behavioural segments to identify groups requiring immediate attention.

**Retention Recommendations**

Based on the churn prediction and customer segmentation results, the system can support targeted retention strategies such as:

Provide personalized offers to high-risk customers.

Improve onboarding and early-stage customer engagement.

Offer suitable contract incentives.

Provide proactive technical support.

Identify dissatisfaction among short-tenure customers.

Maintain engagement with valuable long-term customers.

Prioritize customers belonging to high-churn behavioural segments.

The short-tenure, high-risk segment is particularly important because it combines relatively shorter customer relationships with a significantly higher observed churn rate.

**PCA Visualization**

Principal Component Analysis (PCA) is used to reduce the dimensionality of the processed customer data to two principal components.

This allows the customer clusters to be visualized in a two-dimensional space and provides a clearer understanding of the separation and distribution of the identified customer segments.
