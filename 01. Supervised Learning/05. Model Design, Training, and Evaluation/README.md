<h1 align='center'>
  Model Design, Train, and Evaluation
</h1>

<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\model-design-logo.png" alt="Logo" width="80%"/>
</p>






**Table of content**

---

[*Model Design, Train, and Evaluation(#types-of-supervised-learning-models)*]()

- [Types of Supervised Learning Models](#types-of-supervised-learning-models)
  - [Neural Networks](#neural-networks)
  - [Support Vector Machine](#support-vector-machine)
  - [Decision Tree](#decision-tree)
  - [Random Forest](#random-forest)
  - [K Nearest Neighbor](#k-nearest-neighbor)
  - [Linear Regression](#linear-regression)
  - [Logistic Regression](#logistic-regression)
- [Model Evaluation Metrices](#model-evaluation-metrices)
  1. [Bias Variance Trade Off](#1-bias-variance-trade-off)
     - [Validation Curves](#a-validation-curves)
  2. [Metrices to Evaluate Classification Model](#2-metrices-to-evaluate-classification-model)
     - [Confusion Matrix](#a-confusion-matrix)
       - [Accuracy](#Accuracy)
       - [Precision](#Precision)
       - [Recall](#Recall)
       - [F1 Score](#F1-score)
  3. [Metrices to Evaluate Regression Model](#metrices-to-evaluate-regression-model)
     - [Explained Variance](#explained-variance)
     - [Mean Squared Error](#mean-squared-error)











## Types of Supervised Learning Models

Under the umbrella of supervised learning fall: Classification, and Regression.


<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Supervised Learning Models.png" alt="Model Design, Train, and Evaluation" width="60%"/>
</p>








### Neural Networks

A Neural Network is essentially a network of mathematical equations. It takes one or more input variables, and by going through a network of equations, results in one or more output variables.

The blue circles represent the **input layer, **the black circles represent the **hidden layers,** and the green circles represent the **output layer.** Each node in the hidden layers represents both a linear function and an activation function that the nodes in the previous layer go through, ultimately leading to an output in the green circles.






<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Network Diagram.png" alt="Model Design, Train, and Evaluation" width="65%"/>
</p>










### Support Vector Machine

A Support Vector Machine is a supervised classification technique that can actually get pretty complicated but is pretty intuitive at the most fundamental level.

Let’s assume that there are two classes of data. A support vector machine will find a **hyperplane** or a boundary between the two classes of data that maximizes the margin between the two classes (see below). There are many planes that can separate the two classes, but only one plane can maximize the margin or distance between the classes.




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Support Vector Machine Diagram.png" alt="Model Design, Train, and Evaluation" width="30%"/>
</p>








### Decision Tree

**Decision trees** are a popular model, used in operations research, strategic planning, and machine learning. Each square above is called a **node**, and the more nodes you have, the more accurate your decision tree will be (generally). The last nodes of the decision tree, where a decision is made, are called the **leaves** of the tree. Decision trees are intuitive and easy to build but fall short when it comes to accuracy.




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Decision Tree Diagram.png" alt="Model Design, Train, and Evaluation" width="75%"/>
</p>








### Random Forest

Random forests are an ensemble learning technique that builds off of decision trees. Random forests involve creating multiple decision trees using bootstrapped datasets of the original data and randomly selecting a subset of variables at each step of the decision tree. The model then selects the mode of all of the predictions of each decision tree. What’s the point of this? By relying on a “majority wins” model, it reduces the risk of error from an individual tree.

For example, if we created one decision tree, the third one, it would predict 0. But if we relied on the mode of all 4 decision trees, the predicted value would be 1. This is the power of random forests.




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Random Forest Diagram.png" alt="Model Design, Train, and Evaluation" width="80%"/>
</p>








### K Nearest Neighbor

The K-Nearest-Neighbour algorithm estimates how likely a data point is to be a member of one group or another. It essentially looks at the data points around a single data point to determine what group it is actually in. For example, if one point is on a grid and the algorithm is trying to determine what group that data point is in (Group A or Group B, for example) it would look at the data points near it to see what group the majority of the points are in.




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\K Nearest Neighbor Diagram.png" alt="Model Design, Train, and Evaluation" width="50%"/>
</p>








### Linear Regression

Linear regression is the most basic type of regression. Simple linear regression allows us to understand the relationships between two continuous variables. The idea of linear regression is simply finding a line that best fits the data. 

Extensions of linear regression include multiple linear regression (eg. finding a plane of best fit) and polynomial regression (eg. finding a curve of best fit).




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Linear Regression Diagram.png" alt="Model Design, Train, and Evaluation" width="65%"/>
</p>










### Logistic Regression

Logistic regression focuses on estimating the probability of an event occurring based on the previous data provided. It is used to cover a binary dependent variable, that is where only two values, 0 and 1, represent outcomes.

Logistic regression is similar to linear regression but is used to model the probability of a finite number of outcomes, typically two. There are a number of reasons why logistic regression is used over linear regression when modeling probabilities of outcomes. In essence, a logistic equation is created in such a way that the output values can only be between 0 and 1 (see below).




<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Logistic Regression Diagram.png" alt="Model Design, Train, and Evaluation" width="65%"/>
</p>








## Model Evaluation Metrices

Common metrics used to evaluate models are discussed below.



### 1. Bias Variance Trade Off

The ultimate goal of any machine learning model is to learn from examples and generalize some degree of knowledge regarding the task we're training it to perform. Some machine learning models provide the framework for generalization by suggesting the underlying structure of that knowledge. For example, a linear regression model imposes a framework to learn linear relationships between the information we feed it. 

However, sometimes we provide a model with too much pre-built structure that we limit the model's ability to learn from the examples - such as the case where we train a linear model on a exponential dataset. In this case, our model is **biased** by the pre-imposed structure and relationships. Models with high bias pay little attention to the data presented; this is also known as **underfitting**.

On the other extreme, sometimes when we train our model it learns *too much* from the training data. That is, our model captures the noise in the data in addition to the signal. This can cause wild fluctuations in the model that does not represent the true trend; in this case, we say that the model has high **variance**. In this case, our model does not generalize well because it pays too much attention to the training data without consideration for generalizing to new data. In other words, we've **overfit** the model to the training data.

In summary, a model with high bias is limited from learning the true trend and underfits the data. A model with high variance learns too much from the training data and overfits the data. The best model sits somewhere in the middle of the two extremes.





#### a. Validation Curves

The goal with any machine learning model is **generalization**. Validation curves allow us to find the sweet spot between underfitting and overfitting a model to build a model that generalizes well.

A typical validation curve is a plot of the model's error as a function of some model hyperparameter which controls the model's tendency to overfit or underfit the data. On this curve, both the training error and the validation error of the model are plotted. Using both of these errors combined, it can be diagnosed that whether a model is suffering from high bias or high variance.



<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Validation curve.png" alt="Model Design, Train, and Evaluation" width='85%'/>
</p>






### 2. Metrices to Evaluate Classification Model



#### a. Confusion Matrix

Four different results are possible when making classification predictions :

- **True positives** are when you predict an observation belongs to a class and it actually does belong to that class.
- **True negatives** are when you predict an observation does not belong to a class and it actually does not belong to that class.
- **False positives** occur when you predict an observation belongs to a class when in reality it does not.
- **False negatives** occur when you predict an observation does not belong to a class when in fact it does.

These four outcomes are often plotted on a confusion matrix.



<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\confusion matrix logo.png" alt="Model Design, Train, and Evaluation" width='70%'/>
<>/p


A confusion matrix is an N X N matrix, where N is the number of classes being predicted. Confusion matrices can be applied to binary classification and could be expanded to illustrate multi-class classification predictions. 



<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Confusion Matrix Details.jpeg" alt="Model Design, Train, and Evaluation" width='80%'/>
</p>






The three main metrics used to evaluate a classification model are accuracy, precision, and recall.



##### Accuracy

Accuracy is defined as the percentage of correct predictions for the test data. It can be calculated easily by dividing the number of correct predictions by the number of total predictions.


<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Accuracy.png" alt="Model Design, Train, and Evaluation" width='70%'/>
</p>




##### Precision

Precision is defined as the fraction of relevant examples (true positives) among all of the examples which were predicted to belong in a certain class.


<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Precision.png" alt="Model Design, Train, and Evaluation" width='40%'/>
</p>




##### Recall

Recall (or, Sensitivity) is defined as the fraction of examples which were predicted to belong to a class with respect to all of the examples that truly belong in the class.



<img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Recall.png" alt="Model Design, Train, and Evaluation" width='40%'/>





The following graphic does a phenomenal job visualizing the difference between precision and recall.


<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Precision vs Recall.png" alt="Model Design, Train, and Evaluation" width='45%'/>
</p






##### F1 Score

Ultimately, it's nice to have one number to evaluate a machine learning model just as you get a single grade on a test in school. Thus, it makes sense to combine the precision and recall metrics; the common approach for combining these metrics is known as the f-score.

<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\F1 Score.png" alt="Model Design, Train, and Evaluation" width='50%'/>
</p








### 3. Metrices to Evaluate Regression Model

Evaluation metrics for regression models are quite different than the above metrics we discussed for classification models because we are now predicting in a continuous range instead of a discrete number of classes. If your regression model predicts the price of a house to be £400K and it sells for £405K, that's a pretty good prediction. However, in the classification examples we were only concerned with whether or not a prediction was correct or incorrect, there was no ability to say a prediction was "pretty good". Thus, we have a different set of evaluation metrics for regression models.



#### Explained Variance

Explained variance compares the variance within the expected outcomes, and compares that to the variance in the error of our model. This metric essentially represents the amount of variation in the original dataset that our model is able to explain.


<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\ev.png" alt="Model Design, Train, and Evaluation" width='50%'/>
</p




#### Mean Squared Error

Mean squared error is simply defined as the average of squared differences between the predicted output and the true output. Squared error is commonly used because it is agnostic to whether the prediction was too high or too low, it just reports that the prediction was incorrect.

<p align=center>
  <img src="..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\MSE.png" alt="Model Design, Train, and Evaluation" width='35%'/>
</p








