# Missing Data Handling



![Missing Data Logo](..\..\_Lib\images\01. Supervised Learning\02. Missing Data Handling\missing data logo.jpg)







**Table of content**

---

[TOC]





## Missing Data

Missing data (or missing values) is defined as the data value that is not stored for a variable in the observation of interest. The problem of missing data is relatively common in almost all research and can have a significant effect on the conclusions that can be drawn from the data.

Missing data present various problems. First, the absence of data reduces statistical power, which refers to the probability that the test will reject the null hypothesis when it is false. Second, the lost data can cause bias in the estimation of parameters. Third, it can reduce the representativeness of the samples. Fourth, it may complicate the analysis of the study. Each of these distortions may threaten the validity of the trials and can lead to invalid conclusions. [[Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3668100/)]



## Types of Missing Data

Rubin first described and divided the types of missing data according to the assumptions based on the reasons for the missing data. In general, there are three types of missing data according to the mechanisms of missingness. [[Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3668100/#B4)]

- Missing completely at random
- Missing at random
- Missing not at random




## Techniques for Handling the Missing Data

Missing data may be categorical, numerical, or in any other format. There are different handling techniques for each format. Some of the strategies are detailed in this article. 





![Missing Data Handling Technique](E:\My Drive\_ML\_AlgoDocs\Machine Learning\_Lib\images\01. Supervised Learning\02. Missing Data Handling\missing data handling.png)







### a. Count and Visualize Missing Data

This is the fundamental step in addressing missing data. The entire picture of missing data is provided by counting and visualizing, which also aids in choosing the best handling method. One of three methods can be used to count and visualize data -





#### Using Custom Package

In this case, missing data are counted and visualized using a custom package named `mltoolsh`. Basic Python libraries like NumPy, Pandas, Matplotlib, Seaborn, etc. were used in the development of this package.

This package includes modules for missing data visualization and counting. The module's function is executed along with the necessary parameter (for example, the data frame), and the function counts and visualizes missing data after that.



**Pros and Cons**

Utilizing this software has the benefit of providing a stunning bar plot representation with a percentage count of missing data on top of each bar. However, the package can't be installed via *pip* or *conda* and must be downloaded independently from GitHub in order to be implemented.



> Documentation of [`mltoolsh`](https://github.com/Shohrab-Hossain/mltoolsh)





#### Using Python Library

A python library named `Missingno` is used in this case to visualize the missing data. The library can plot bar plot and matrix plot, which gives a proper view about missing data.



**Pros and Cons**

This library offers a fluid representation in both a bar plot and a matrix plot, however it is unable to provide a count of the number of missing data.



> Documentation of [`Missingno`](https://github.com/ResidentMario/missingno)





#### Using Seaborn

There are numerous built-in methods to view missing data in Seaborn. Using Seaborn, missing data can be immediately represented as a bar plot.



**Pros and Cons**

This library provides a lovely bar plot representation. It cannot, however, give a total of the number of missing data.



> Documentation of [`Seaborn`](https://seaborn.pydata.org/generated/seaborn.heatmap.html#seaborn.heatmap)







###  b. Numeric Missing Data Handling

After the data from the various visualizations have been counted up and analyzed, it is now important to process the missing data. In a data frame, numerical columns are common. Numerous approaches can be used to handle numerical missing data.





#### Correlation

The column value that has a high correlation with the missing value-containing column is used in this method to handle the missing data. The most correlated column is chosen after calculating the correlations between the missing value column and the other numerical columns. After that, the aggregation mean is used to group the selected correlated column. which creates a data frame with the mean in the other columns and the correlated column with all of its unique values. The value from the created data frame is then used to replace the missing value.





#### Interpolation

Interpolation can be used to fill in missing data. A built-in method called *interpolate* is available in Pandas and can be used to fill in missing data. This interpolate function provides multiple methods, including 'linear', 'pad', and others. Each strategy varies in how it interpolates the missing data.



> Documentation of [`Pandas interpolate()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.interpolate.html)





#### Statistical Estimation

The objective of this imputation technique is to replace missing data with statistical estimates of the values that are missing. Imputation values that can be employed include Mean, Median, and Mode. First, the mean, median, or mode of the values in the column that contains missing values is calculated. The corresponding missing value of that column is subsequently replaced using the computed statistical guess.



> Documentation of [`Pandas fillna()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.fillna.html)







### c. Categorical Missing Data Handling

Most categorical data are texts that cannot be processed as numeric data. To manage data that forms categories, the following techniques are used -





#### Impute a New 'Missing' Category

This method creates an entirely new category by replacing all missing data with the word 'Missing'. The overall number of categories increases as a consequence of this approach. 





#### Frequent Category Imputation

This approach examines the missing data column first, then chooses the category that appears the most frequently. And then all the missing data are replaced by this frequent column. This approach reinforces the total number of categories the same while increasing the count of the most frequent category.







### d. Drop Missing Data

If missing data cannot be replaced, it may be dropped. Dropping can be done in either rows or columns. Drop in rows is applied if the number of missing values is very low, and drop in columns is applied if the number is high enough.



#### Drop in Rows

If there are only a few missing values, the entire row that contains even one of them can be deleted. In this technique the data frame's number of columns remains constant while the number of rows is decreased.





#### Drop in Columns

A column can be completely deleted if it has a lot of missing data. The data frame's number of columns is decreased but the number of rows is left unchanged by this column deletion.







### e. Use of Predictive Model

To prevent leaking, this should be done in conjunction with a cross-validation strategy. This can be quite useful and aid in the creation of the final model. A neural network is one of several possibilities for such a prediction model. Linear Regression, Random Forest, K Nearest Neighbor, Maximum Likelihood, etc. are a few examples of prediction models.

Using the values from the missing data column, a predictive model is trained using this method, where the targets are the values of the missing-value column and the training values are the values of the other columns. The predictive algorithm then uses the corresponding data to predict the missing value.

