# Types of activation function









**Table of content**

---

[TOC]







# 1. Types of activation function

Activation functions are of different types, some are linear and some non-linear. All the types of the activation function are stated below -



## a. Binary Step Function

Binary step function depends on a threshold value that decides whether a neuron should be activated or not. 

The input fed to the activation function is compared to a certain threshold; if the input is greater than it, then the neuron is activated, else it is deactivated, meaning that its output is not passed on to the next hidden layer.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Binary-Step-Function.jpg" alt="Logo" width="55%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Binary-Step-Function-Equation.png" alt="Logo" width="35%"/>





## b. Linear Activation Function

The linear activation function, also known as "no activation," or "identity function" (multiplied x1.0), is where the activation is proportional to the input.

The function doesn't do anything to the weighted sum of the input, it simply spits out the value it was given.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Linear-Activation-Function.jpg" alt="Logo" width="60%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Linear-Activation-Function-Equation.png" alt="Logo" width="22%"/>





## c. Sigmoid / Logistic Activation Function

This function takes any real value as input and outputs values in the range of 0 to 1. 

The larger the input (more positive), the closer the output value will be to 1.0, whereas the smaller the input (more negative), the closer the output will be to 0.0, as shown below.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Sigmoid-Activation-Function.jpg" alt="Logo" width="60%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Sigmoid-Activation-Function-Equation.png" alt="Logo" width="32%"/>





## d. Tanh Function (Hyperbolic Tangent)

Tanh function is very similar to the sigmoid/logistic activation function, and even has the same S-shape with the difference in output range of -1 to 1. In Tanh, the larger the input (more positive), the closer the output value will be to 1.0, whereas the smaller the input (more negative), the closer the output will be to -1.0.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Hyperbolic-Tangent.jpg" alt="Logo" width="55%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Hyperbolic-Tangent-Equation.png" alt="Logo" width="32%"/>



## e. ReLU Function

ReLU stands for Rectified Linear Unit. 

Although it gives an impression of a linear function, ReLU has a derivative function and allows for backpropagation while simultaneously making it computationally efficient. 

The main catch here is that the ReLU function does not activate all the neurons at the same time. 

The neurons will only be deactivated if the output of the linear transformation is less than 0.





<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\ReLU-Function.jpg" alt="Logo" width="50%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\ReLU-Function-Equation.png" alt="Logo" width="32%"/>



## f. Leaky ReLU Function

Leaky ReLU is an improved version of ReLU function to solve the Dying ReLU problem as it has a small positive slope in the negative area.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Leaky-ReLU-Function.jpg" alt="Logo" width="55%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Leaky-ReLU-Function-Equation.png" alt="Logo" width="35%"/>





## g. Parametric ReLU Function

Parametric ReLU is another variant of ReLU that aims to solve the problem of gradient’s becoming zero for the left half of the axis. 

This function provides the slope of the negative part of the function as an argument *a*. By performing backpropagation, the most appropriate value of *a* is learnt.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Parametric-ReLU-Function.jpg" alt="Logo" width="50%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Parametric-ReLU-Function-Equation.png" alt="Logo" width="35%"/>





## h. Exponential Linear Units (ELUs) Function

Exponential Linear Unit, or ELU for short, is also a variant of ReLU that modifies the slope of the negative part of the function. 

ELU uses a log curve to define the negative values unlike the leaky ReLU and Parametric ReLU functions with a straight line.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\ELU-Function.jpg" alt="Logo" width="55%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\ELU-Function-Equation.png" alt="Logo" width="35%"/>





## i. SoftMax Function

Before exploring the ins and outs of the SoftMax activation function, we should focus on its building block—the sigmoid/logistic activation function that works on calculating probability values. 



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\SOftmax-Function.jpg" alt="Logo" width="60%"/>







The output of the sigmoid function was in the range of 0 to 1, which can be thought of as probability. But this function faces certain problems.

Let’s suppose we have five output values of 0.8, 0.9, 0.7, 0.8, and 0.6, respectively. How can we move forward with it?

The answer is: We can’t.

The above values don’t make sense as the sum of all the classes/output probabilities should be equal to 1. 

You see, the Softmax function is described as a combination of multiple sigmoids. 

It calculates the relative probabilities. Similar to the sigmoid/logistic activation function, the SoftMax function returns the probability of each class. 



It is most commonly used as an activation function for the last layer of the neural network in the case of multi-class classification. 



Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Softmax-Function-Equation.jpg" alt="Logo" width="45%"/>





## j. Swish

It is a self-gated activation function developed by researchers at Google. 

Swish consistently matches or outperforms ReLU activation function on deep networks applied to various challenging domains such as *image classification*, *machine translation* etc. 

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Swish.jpg" alt="Logo" width="60%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Swish-Equation.png" alt="Logo" width="35%"/>





## k. Gaussian Error Linear Unit (GELU)

The Gaussian Error Linear Unit (GELU) activation function is compatible with BERT, ROBERTa, ALBERT, and other top NLP models. This activation function is motivated by combining properties from dropout, zoneout, and ReLUs. 

ReLU and dropout together yield a neuron’s output. ReLU does it deterministically by multiplying the input by zero or one (depending upon the input value being positive or negative) and dropout stochastically multiplying by zero. 

RNN regularizer called zoneout stochastically multiplies inputs by one. 

We merge this functionality by multiplying the input by either zero or one which is stochastically determined and is dependent upon the input. We multiply the neuron input x by 

m ∼ Bernoulli(Φ(x)), where Φ(x) = P(X ≤x), X ∼ N (0, 1) is the cumulative distribution function of the standard normal distribution. 

This distribution is chosen since neuron inputs tend to follow a normal distribution, especially with Batch Normalization.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Gelu.jpg" alt="Logo" width="60%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Gelu-Equation.png" alt="Logo" width="55%"/>





## l. Scaled Exponential Linear Unit (SELU)

SELU was defined in self-normalizing networks and takes care of internal normalization which means each layer preserves the mean and variance from the previous layers. SELU enables this normalization by adjusting the mean and variance. 

SELU has both positive and negative values to shift the mean, which was impossible for ReLU activation function as it cannot output negative values. 

Gradients can be used to adjust the variance. The activation function needs a region with a gradient larger than one to increase it.



<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Selu.jpg" alt="Logo" width="60%"/>







Mathematically it can be represented as:

<img src="..\..\..\readme-lib\01. Supervised Learning\05. Model Design, Training, and Evaluation\Neural Networks\Selu-Equation.png" alt="Logo" width="45%"/>







