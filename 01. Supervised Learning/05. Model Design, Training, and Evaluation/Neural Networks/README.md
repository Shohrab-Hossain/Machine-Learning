# Neural Network


<br> <br>

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\NN-logo.gif" alt="Logo" width="60%"/>
</p>




<br> <br> 



**Table of content**

------

[TOC]



<br> 

# 1. Introduction to Neural Network

A **neural network** is an adaptive system that learns by using interconnected nodes or neurons in a layered structure that resembles a *human brain*. A neural network can learn from data—so it can be trained to recognize patterns, classify data, and forecast future events.

A neural network breaks down the input into layers of abstraction. It can be trained using many examples to recognize patterns in speech or images, for example, just as the human brain does. Its behavior is defined by the way its individual elements are connected and by the strength, or weights, of those connections. These `weights` are automatically adjusted during training according to a specified learning rule until the artificial neural network performs the desired task correctly.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\NN-intro.jpg" alt="Logo" width="60%"/>
</p>




<br> <br> <br> <br> 



# 2. Perceptron Model

**Perceptron** is a building block of a Neural Network. The basic structure of a perceptron is shown in the below figure.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Perceptron.png" alt="Logo" width="50%"/>
</p>





<br> <br> <br> 


## 2.1. Components of a Perceptron

Perceptron contains three main components - input, weight-bias, and activation function.

<br> <br> 

### 2.1.1. Input

Input is the set of features that are fed into the model for the learning process. It is the primary component of Perceptron which accepts the initial data into the system for further processing. Each input node contains a real numerical value. Inputs are represented as `X`.

<br> <br> 

### 2.1.2. Weight

Its main function is to give importance to those features that contribute more towards the learning. It does so by introducing scalar multiplication between the input value and the weight matrix. For example, a negative word would impact the decision of the sentiment analysis model more than a pair of neutral words.

Weight parameter represents the strength of the connection between units. This is another most important parameter of Perceptron components. Weight is directly proportional to the strength of the associated input neuron in deciding the output. Weights are represented as `W`.


<br> <br> 


### 2.1.3. Bias

The role of bias is to shift the value produced by the activation function. Its role is similar to the role of a constant in a linear function.

Further, Bias can be considered as the line of intercept in a linear equation. Biases are represented as `b`.



<br> 

The relation between input (X), weight (w), and bias (b) gives `z` as stated below, 

<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\z-equation.png" alt="Logo" width="45%"/>
</p>



<br> <br>


### 2.1.4. Activation Function

<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Activation-Function-logo.jpg" alt="Logo" width="60%"/>
</p>


<br> <br> 

Activation Function is the final and important component that help to determine whether the neuron will fire or not. Activation Function can be considered primarily as a step function. The purpose of an activation function is to add non-linearity to the neural network.

<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Activation-Function.png" alt="Logo" width="45%"/>
</p>


<br> <br> 

#### 2.1.4.1. Importance of Activation Function

Let’s suppose we have a neural network working *without* the activation functions. 

In that case, every neuron will only be performing a linear transformation on the inputs using the weights and biases. It’s because it doesn’t matter how many hidden layers we attach in the neural network; all layers will behave in the same way because the composition of two linear functions is a linear function itself.

Although the neural network becomes simpler, learning any complex task is impossible, and our model would be just a linear regression model.


<br> <br> 


#### 2.1.4.2. Types of activation function

Activation functions are of different types, some are linear and some non-linear. All the types of the activation function are stated [here](https://github.com/Shohrab-Hossain/Machine-Learning/blob/main/01.%20Supervised%20Learning/05.%20Model%20Design%2C%20Training%2C%20and%20Evaluation/Neural%20Networks/Types%20of%20activation%20function.md).


<br> <br> 


#### 2.1.4.3. How to choose the right Activation Function?

<br> 

You need to match your activation function for your output layer based on the type of prediction problem that you are solving—specifically, the type of predicted variable.

Here’s what you should keep in mind.

As a rule of thumb, you can begin with using the ReLU activation function and then move over to other activation functions if ReLU doesn’t provide optimum results.

<br> <br> 

And here are a few other guidelines to help you out.

1. ReLU activation function should only be used in the hidden layers.
2. Sigmoid/Logistic and Tanh functions should not be used in hidden layers as they make the model more susceptible to problems during training (due to vanishing gradients).
3. Swish function is used in neural networks having a depth greater than 40 layers.

Finally, a few rules for choosing the activation function for your output layer based on the type of prediction problem that you are solving :

1. **Regression **- Linear Activation Function
2. **Binary Classification**—Sigmoid/Logistic Activation Function
3. **Multiclass Classification**—Softmax
4. **Multilabel Classification**—Sigmoid

The activation function used in hidden layers is typically chosen based on the type of neural network architecture.

1. **Convolutional Neural Network (CNN)**: ReLU activation function.
2. **Recurrent Neural Network**: Tanh and/or Sigmoid activation function.


<br> <br> 


Here is a cheat sheet to consolidate all the knowledge on the Neural Network Activation Functions that discussed above - 

<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\activation-function-cheat-sheet.jpeg" alt="Logo" width="85%"/>
</p>



<br> <br> 



<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Activation-Function-Cheat-Sheet-Equation.png" alt="Logo" width="80%"/>
</p>



<br> <br> <br> <br> 




## 2.2. How perceptron works

Perceptron receives inputs (X) first, and then multiplies them with their weights (w). After that sum up the multiplies and add bias (b), which gives z. Later this z passes to a activation function, which generates the output Y.



In the below illustration, here is a perceptron receiving four inputs. The corresponding weights and biases are calculated to produce `z`. The activation function is a Binary Step Function, which gives output 1 or 0. Suppose output 1 means Blue class and 0 means Red class. 

Now for some inputs the perceptron generates output 1, meaning it predicts Blue class, and for other inputs it predicts Red class. The line shows the predicted class.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Perceptron-Learning.gif" alt="Logo" width="60%"/>
</p>


<br> <br> 

One important observation is the perceptron predicts same output for same inputs. Which means any time for the same input the perceptron is predicting the same class, again and again. The problem is, if the prediction is not good enough then the perceptron should learn how to predict better next time. But as we saw, it keeps predicting the same results all the time. To solve this problem all we need to do is to change the weights and biases after each misprediction. And for that we need to know how much error is there in any prediction and depending on that we will adjust the weights and biases. 

<br> <br> 


<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Perceptron-Learning-Block.png" alt="Logo" width="75%"/>
</p>


<br> <br> 

To accomplish this, a cost function is used to calculate the error in a prediction, and a backpropagation happens that updates the wights and biases based on the cost function. In this way, after each prediction the perceptron will be able to predict more accurately. 


<br> <br> <br> <br> 




## 2.3. Multi-Layer Perceptron (MLP)

In a multilayer perceptron model there is layers of perceptron. In simple terms, multi-layered perceptron can be treated as a network of numerous artificial neurons overhead varied layers, the activation function is no longer linear, instead, non-linear activation functions such as Sigmoid functions, Tanh, ReLU activation Functions, etc are deployed for execution.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\mlp-logo.png" alt="Logo" width="65%"/>
</p>



<br> <br> 


A multi-layered perceptron model executes in two stages; the **forward stage** and the **backward stages**. In the *forward stage*, activation functions are originated from the input layer to the output layer, and in the *backward stage*, the error between the actual observed value and demanded given value is originated backward in the output layer for modifying weights and bias values.


<br> <br> 


### 2.3.1. Components of MLP

When multiple neurons are stacked together in a row, they constitute a layer, and multiple layers piled next to each other are called a multi-layer neural network.

The main components of this type of structure discussed below.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\MLP-Terminology.png" alt="Logo" width="75%"/>
</p>



<br> <br> 


#### a. Input Layer

The data that we feed to the model is loaded into the input layer from external sources like a CSV file or a web service. It is the only visible layer in the complete Neural Network architecture that passes the complete information from the outside world without any computation.

<br> <br> 


#### b. Hidden Layer

The hidden layers are what makes deep learning what it is today. They are intermediate layers that do all the computations and extract the features from the data.

There can be multiple interconnected hidden layers that account for searching different hidden features in the data. For example, in image processing, the first hidden layers are responsible for higher-level features like edges, shapes, or boundaries. On the other hand, the later hidden layers perform more complicated tasks like identifying complete objects (a car, a building, a person).

<br> <br> 

#### c. Output Layer

The output layer takes input from preceding hidden layers and comes to a final prediction based on the model’s learnings. It is the most important layer where we get the final result.

In the case of classification/regression models, the output layer generally has a single node. However, it is completely problem-specific and dependent on the way the model was built.



<br> <br> <br> <br> 



# 3. How Neural Network Learns

First, we multiply our data with a randomly chosen weight and add a randomly chosen bias. We need **the bias and the weight** so that we can influence the result produced by the neuron. This is crucial to learning.

Next, we send the result through a non-linear **activation function**. The activation function transforms our input into a value in a specific range (usually between 0 and 1).

Now, we compare the output produced by the nonlinear activation function to the expected output. We measure the difference using a **cost function**. The larger the discrepancy between the produced and the expected output, the larger the imposed *cost*.

Finally, we send the information on how far off the produced result is from the expected back to the beginning. We use this information to slightly adjust the weight and the bias. Through a process called **backpropagation**, which is based on the *chain rule* of differentiation, we can gradually *adjust* the weights and biases in the desired direction. 

Then we repeat the process with the updated weights and biases until our produced output is reasonably close to the expected output.


<br> <br> 

<p align=center>
  <img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\NN-Propagation.webp" alt="Logo" width="45%"/>
</p>



<br> <br> <br> 


## 3.1. Cost Function













