<br>

<h1 align='center'>
 Numeric Missing Data Handling
</h1>

<br>

After the data from the various visualizations have been counted up and analyzed, it is now important to process the missing data. In a data frame, numerical columns are common. Numerous approaches can be used to handle numerical missing data.


<br>


## a. Correlation

The column value that has a high correlation with the missing value-containing column is used in this method to handle the missing data. The most correlated column is chosen after calculating the correlations between the missing value column and the other numerical columns. After that, the aggregation mean is used to group the selected correlated column. which creates a data frame with the mean in the other columns and the correlated column with all of its unique values. The value from the created data frame is then used to replace the missing value.


<br>


## b. Interpolation

Interpolation can be used to fill in missing data. A built-in method called *interpolate* is available in Pandas and can be used to fill in missing data. This interpolate function provides multiple methods, including 'linear', 'pad', and others. Each strategy varies in how it interpolates the missing data.

<br>

> Documentation of [`Pandas interpolate()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.interpolate.html)


<br>


## c. Statistical Estimation

The objective of this imputation technique is to replace missing data with statistical estimates of the values that are missing. Imputation values that can be employed include Mean, Median, and Mode. First, the mean, median, or mode of the values in the column that contains missing values is calculated. The corresponding missing value of that column is subsequently replaced using the computed statistical guess.

<br>

> Documentation of [`Pandas fillna()`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.fillna.html)


<br> <br>









