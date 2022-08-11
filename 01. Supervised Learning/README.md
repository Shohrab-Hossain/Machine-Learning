# Supervised Learning



<img src="..\readme-lib\01. Supervised Learning\supervised-ml-logo.png" alt="Logo" width="50%" style="min-width:180px;"/>







**Table of content**

---

[TOC]





## Introduction to Supervised Learning

**Supervised learning** involves learning a function that maps an input to an output based on example input-output pairs. In this  learning, the machine is taught by example. The operator provides the machine learning algorithm with a known dataset that includes desired inputs and outputs, and the algorithm must find a method to determine how to arrive at those inputs and outputs. While the operator knows the correct answers to the problem, the algorithm identifies patterns in data, learns from observations and makes predictions. The algorithm makes predictions and is corrected by the operator – and this process continues until the algorithm achieves a high level of accuracy/performance.



<img src="..\readme-lib\01. Supervised Learning\spervised-learning-block-diagram.png" alt="Feature Engineering Process" width='60%'/>







## Supervised Learning Steps

The steps involved in supervised learning are :





<img src="..\readme-lib\01. Supervised Learning\Supervised Learning Steps.png" alt="Feature Engineering Process" width='35%'/>







### 1. Exploratory Data Analysis

Exploratory Data Analysis refers to the critical process of performing initial investigations on data so as to discover patterns,to spot anomalies,to test hypothesis and to check assumptions with the help of summary statistics and graphical representations.



### 2. Missing Data Handling

Missing data means absence of observations in columns. It appears in values such as “0”, “NA”, “NaN”, “NULL”, “Not Applicable”, “None”. The cause of it can be data corruption ,failure to record data, lack of information, incomplete results ,person might not provided the data intentionally ,some system or equipment failure etc. There could any reason for missing values in your dataset. One of the biggest impact of Missing Data is, It can bias the results of the machine learning models or reduce the accuracy of the model. So, It is very important to handle missing values.



### 3. Feature Engineering

Feature engineering is the process of selecting, manipulating, and transforming raw data into features that can be used in supervised learning. In order to make machine learning work well on new tasks, it might be necessary to design and train better features. As you may know, a “feature” is any measurable input that can be used in a predictive model — it could be the color of an object or the sound of someone’s voice. Feature engineering, in simple terms, is the act of converting raw observations into desired features using statistical or machine learning approaches.



### 4. Data Splitting and Feature Scaling

The **train-test data split** procedure is used to estimate the performance of machine learning algorithms when they are used to make predictions on data not used to train the model. It is a fast and easy procedure to perform, the results of which allow you to compare the performance of machine learning algorithms for your predictive modeling problem. Although simple to use and interpret, there are times when the procedure should not be used, such as when you have a small dataset and situations where additional configuration is required, such as when it is used for classification and the dataset is not balanced.

**Feature scaling** is a method used to normalize the range of independent variables or features of data. In data processing, it is also known as data normalization and is generally performed during the data preprocessing step.



### 5. Model Design, Train, and Evaluation

Supervised learning can be achieved using different models. Model is designed and then trained using processed data. After the training the trained model is evaluated using validation data. There are many evaluation matrices available that are used to evaluate model predictions.







## Performance Optimization

The model is initially trained using some arbitrary parameters. However, it's possible that the trained model won't perform well with these model parameters. Thus, hyper-parameter tuning is utilized to identify those hyper-parameters that will result in optimal results. There are numerous methods for tuning hyper-parameters. 





<img src="..\readme-lib\01. Supervised Learning\Performance Optimization.png" alt="Feature Engineering Technique" width='50%'/>







