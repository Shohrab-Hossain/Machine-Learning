<h1 align='center'>
  Feature Engineering 
</h1>

<br> <br>

<p align='center'>
  <img src="..\..\readme-lib\01. Supervised Learning\03. Feature Engineering\Feature-Engineering-logo.png" alt="Logo" width="75%" style="min-width:180px;"/>
</p>


<br> <br> <br>


## Feature Engineering

Feature engineering is the process of transforming raw data into features that better represent the underlying problem to the predictive models, resulting in improved model accuracy on unseen data. Feature engineering is a machine learning technique that leverages data to create new variables that aren’t in the training set. It can produce new features for both supervised and unsupervised learning, with the goal of **simplifying and speeding up data transformations** while also **enhancing model accuracy**.


<br> <br>


## Processes in Feature Engineering

Feature engineering consists of various process [[Link](https://towardsdatascience.com/what-is-feature-engineering-importance-tools-and-techniques-for-machine-learning-2080b0269f10)] -


<br> <br>

<p align='center'>
  <img src="..\..\readme-lib\01. Supervised Learning\03. Feature Engineering\Feature Engineering Process.png" alt="Feature Engineering Process" width='70%'/>
</p>

<br> <br> <br>


### Feature Creation

Creating features involves creating new variables which will be most helpful for our model. This can be adding or removing some features.

<br>

### Transformations

Feature transformation is simply a function that transforms features from one representation to another. The goal here is to plot and visualize data, if something is not adding up with the new features we can reduce the number of features used, speed up training, or increase the accuracy of a certain model.

<br>

### Feature Extraction

Feature extraction is the process of extracting features from a data set to identify useful information. Without distorting the original relationships or significant information, this compresses the amount of data into manageable quantities for algorithms to process.

<br>

### Exploratory Data Analysis

Exploratory data analysis (EDA) is a powerful and simple tool that can be used to improve your understanding of your data, by exploring its properties. The technique is often applied when the goal is to create new hypotheses or find patterns in the data. It’s often used on large amounts of qualitative or quantitative data that haven’t been analyzed before.

<br>

### Benchmark

A Benchmark Model is the most user-friendly, dependable, transparent, and interpretable model against which you can measure your own. It’s a good idea to run test datasets to see if your new machine learning model outperforms a recognised benchmark. These benchmarks are often used as measures for comparing the performance between different machine learning models like neural networks and support vector machines, linear and non-linear classifiers, or different approaches like bagging and boosting. To learn more about feature engineering steps and process, check the links provided at the end of this article. Now, let’s have a look at why we need feature engineering in machine learning.


<br> <br> <br>


## Techniques for Feature Engineering

There are different techniques available for Feature Engineering. Some of the strategies are detailed in this article. 


<br> <br>

<p align='center'>
  <img src="..\..\readme-lib\01. Supervised Learning\03. Feature Engineering\Feature Engineering Technique.png" alt="Feature Engineering Technique" width='90%'/>
</p>


<br> <br> <br>


### 1. Categorical Data Encoding

The implementation of categorical data encoding is achievable when the feature column is a categorical one. According to this method, each category was converted to a numeric number. Following is a discussion of numerous strategies for encoding categorical data -

<br> <br>

#### a. Using Pandas 'get_dummies()' function

The `get_dummies()` function converts each category to a new column and encode the value with 0 and 1. Which means this function creates new columns based on the categories.

Utilizing this function increases the number of columns but the encoded values of the encoded columns are remain 0 and 1.

<br>

> Documentation of [`get_dummies()`](https://pandas.pydata.org/docs/reference/api/pandas.get_dummies.html)

<br> <br>

#### b. Using Pandas 'replace()' function

The `replace()` function replaces each category with the user defined encoded value. Which means each category replaced to a unique numeric value defined by the user.

Utilizing this function keeps the number of columns same as before but the encoded values of the encoded column can be any number defined by the programmer.

<br>

> Documentation of [`replace()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.replace.html)

<br> <br>

#### c. Apply Custom Function

Categorical data can be encoded using a custom function. If necessary, new columns with new features can be constructed while encoding, and a custom function can encode the column to any numeric value. 

<br>

**Pros and Cons**

The ability to encode values to binary or any other numeric value is a benefit of employing custom functions, as is the ability to build new feature columns as needed. A dedicated function must be written for each custom encoding, which is the drawback of custom functions.


<br> <br> <br>


###  2. Date and Time Data Handling

In a data frame, the date and time are the most significant types of information. Using a built-in pandas function, this feature can be manipulated.

<br>

#### a. Using Pandas 'to_datetime()' function

This function converts a date and time string to date-time format. Then this date-time can be used to extract required date and time data.

<br>

> Documentation of [`to_datetime()`](https://pandas.pydata.org/docs/reference/api/pandas.to_datetime.html)


<br> <br> <br>


### 3. Textual Data Handling

In a data frame, textual data are common. This form of data can be an address, a zip code, or anything else. Contemporary Natural Language Processing techniques are capable of handling textual data.


<br> <br> <br>


---

<br>

## Table of content

<br>

[**Feature Engineering**](#feature-engineering)

- [Feature Engineering](#feature-engineering)
- [Processes in Feature Engineering](#processes-in-feature-engineering)
  - [Feature Creation](#feature-creation)
  - [Transformations](#transformations)
  - [Feature Extraction](#feature-extraction)
  - [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Benchmark](#benchmark)
- [Techniques for Feature Engineering](#techniques-for-Feature-engineering)
  1. [Categorical Data Encoding](#1-categorical-data-encoding)
      - [Using Pandas 'get_dummies()' function](#a-using-pandas-get_dummies-function)
      - [Using Pandas 'replace()' function](#b-using-pandas-replace-function)
      - [Apply Custom Function](#c-apply-custom-function)
  3. [Date and Time Data Handling](#2-date-and-time-data-handling)
     - [Using Pandas 'to_datetime()' function](#a-using-pandas-to_datetime-function)
  5. [Textual Data Handling](#3-textual-data-handling)

