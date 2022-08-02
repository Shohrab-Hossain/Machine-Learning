<br>

<h1 align='center'>

  Count and Visualize Missing Data

</h1>

<br>

This is the fundamental step in addressing missing data. The entire picture of missing data is provided by counting and visualizing, which also aids in choosing the best handling method. One of three methods can be used to count and visualize data -

<br>

## a. Using Custom Package

In this case, missing data are counted and visualized using a custom package named `mltoolsh`. Basic Python libraries like NumPy, Pandas, Matplotlib, Seaborn, etc. were used in the development of this package.

This package includes modules for missing data visualization and counting. The module's function is executed along with the necessary parameter (for example, the data frame), and the function counts and visualizes missing data after that.

<br>

**Pros and Cons**

Utilizing this software has the benefit of providing a stunning bar plot representation with a percentage count of missing data on top of each bar. However, the package can't be installed via *pip* or *conda* and must be downloaded independently from GitHub in order to be implemented.

<br>

> Documentation of [`mltoolsh`](https://github.com/Shohrab-Hossain/mltoolsh)


<br>



## b. Using Python Library

A python library named `Missingno` is used in this case to visualize the missing data. The library can plot bar plot and matrix plot, which gives a proper view about missing data.

<br>

**Pros and Cons**

This library offers a fluid representation in both a bar plot and a matrix plot, however it is unable to provide a count of the number of missing data.

<br>

> Documentation of [`Missingno`](https://github.com/ResidentMario/missingno)


<br>


## c. Using Seaborn

There are numerous built-in methods to view missing data in Seaborn. Using Seaborn, missing data can be immediately represented as a bar plot.

<br>

**Pros and Cons**

This library provides a lovely bar plot representation. It cannot, however, give a total of the number of missing data.

<br>

> Documentation of [`Seaborn`](https://seaborn.pydata.org/generated/seaborn.heatmap.html#seaborn.heatmap)


<br> <br>







