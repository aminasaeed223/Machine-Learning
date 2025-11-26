
# 5_Model Representation

## Table of content
- Linear Regression problem  
- Machine learning notation  
- ML Notation  
- The overall process of Supervised learning  
- How hypothesis represent  
- Section 1- What is Model?  

---

## Section 1- What is Model?

Machine learning is process to build model from data. Model is function That take input data and there is output value that human care about, How the function evaluate input and output value, There is lot ways to represent that model.

The input data feed into model. The model is some function ( it may be logistic regression, Neural network, SVM etc.) and this model perform number of computation on input data, after doing this numerical Evalution and the output will be some desired output.

---

## Section 2- Linear Regression Problem

### Example 1

**formula:**

where,

- **y** = value that has to be predicted  
- **m** = slope of the line  
- **x** = input data  
- **c** = y-intercept  

With these values, we can predict y values such as.

here the blue points are the x values (the input data). now using the input data, we can calculate the slope and y coordinate such that our predicted line (red line)should cover most of the points. now using this line we can predict any values of y given its x values. Now one thing to note from linear regression is that it works with continuous data, But if we need linear regression for our classification algorithms, we need to further tweak our algorithm a bit.

first we need to define a threshold such that if our predicted value is lower than the threshold then it is of class1 otherwise class2. Now if you are thinking “oh that’s easy we have to define linear regression with threshold and vola it becomes classification algorithm,there is a trick in it. We have to define threshold value by ourselves, and for large datasets it will be impossible for us to calculate the threshold. Moreover, the threshold value once defined will be the same even if our predicted values change.

### Example 2

Let's use some motivating example of predicting housing prices. We're going to use a data set of housing prices from the city of Portland, Oregon. And here I'm gonna plot my data set of a number of houses that were different sizes that were sold for a range of different prices.

Let's say that given this data set, you have a friend that's trying to sell a house and let's see if friend's house is size of 1250 square feet and you want to tell them how much they might be able to sell the house for. Well one thing you could do is fit a model. Maybe fit a straight line to this data. Looks something like that and based on that, maybe you could tell your friend that let's say maybe he can sell the house for around $220,000. So this is an example of a supervised learning algorithm. And it's supervised learning because we're given the, quotes, "right answer" for each of our examples. Namely we're told what was the actual house, what was the actual price of each of the houses in our data set were sold for and moreover, this is an example of a regression problem where the term regression refers to the fact that we are predicting a real-valued output namely the price. And just to remind you the other most common type of supervised learning problem is called the classification problem where we predict discrete-valued outputs such as if we are looking at cancer tumors and trying to decide if a tumor is malignant or benign. So that's a zero-one valued discrete output.

---

## Section 3- Machine Learning Notation

More formally, in supervised learning, we have a data set and this data set is called a training set. So for housing prices example, we have a training set of different housing prices and our job is to learn from this data how to predict prices of the houses.

Let's define some notations that we're using throughout this course. We're going to define quite a lot of symbols. It's okay if you don't remember all the symbols right now but as the course progresses it will be useful [inaudible] convenient notation.

So I'm gonna use lowercase **m** throughout this course to denote the number of training examples. So in this data set, if I have, you know, let's say 47 rows in this table. Then I have 47 training examples and **m = 47**.

Let me use lowercase **x** to denote the input variables often also called the features. That would be the x is here, it would the input features.

And I'm gonna use **y** to denote my output variables or the target variable which I'm going to predict and so that's the second column here. [inaudible] notation,

I'm going to use **(x, y)** to denote a single training example. So, a single row in this table corresponds to a single training example, and to refer to a specific training example, I'm going to use this notation **x(i)** comma gives me **y(i)**.

And, we're going to use this to refer to the ith training example. So this superscript i over here, this is **not exponentiation** right? This (x(i), y(i)), the superscript **i** in parentheses that's just an index into my training set and refers to the ith row in this table, okay? So this is not x to the power of i, y to the power of i. Instead (x(i), y(i)) just refers to the ith row of this table.

So for example:  
- **x(1)** refers to the input value for the first training example → 2104  
- **x(2)** = 1416  
- **y(1)** = 460  

---

## Section 4- Overall process of supervised learning algorithm

So here's how this supervised learning algorithm works. We saw that with the training set like our training set of housing prices and we feed that to our learning algorithm. Is the job of a learning algorithm to then output a function which by convention is usually denoted lowercase **h** and **h** stands for hypothesis.

And what the job of the hypothesis is, is, is a function that takes as input the size of a house like maybe the size of the new house your friend's trying to sell so it takes in the value of x and it tries to output the estimated value of y for the corresponding house. So **h** is a function that maps from x's to y's.

People often ask me, you know, why is this function called hypothesis. Some of you may know the meaning of the term hypothesis, from the dictionary or from science or whatever. It turns out that in machine learning, this is a name that was used in the early days of machine learning and it kinda stuck. 'Cause maybe not a great name for this sort of function, for mapping from sizes of houses to the predictions, that you know.... I think the term hypothesis, maybe isn't the best possible name for this, but this is the standard terminology that people use in machine learning. So don't worry too much about why people call it that.

---

## Section 5- Mathematical detail of Linear Regression

Suppose we are given a dataset of  pairs of values. Each pair includes the value of our independent variable  and of our dependent variable :

We can hypothesize the following relationship between  and :

where:

- **θ₀** is the intercept, or the bias  
- **θ₁** is the regression coefficient, or the weight of x with respect to y  
- **ε** is the error in our prediction  

The goal of regression is finding the correct values for θ₀ and θ₁.

---

## Section 6- How do we represent the hypothesis?

**Def:** The hypothesis is noted **hθ** and is the model that we choose. For a given input data x(i) the model prediction output is **hθ(x(i))**.

When designing a learning algorithm, the next thing we need to decide is how do we represent this hypothesis h. For this and the next few videos, I'm going to choose our initial choice, for representing the hypothesis, will be the following. We're going to represent h as follows. And we will write this as:

**hθ(x) = θ₀ + θ₁x**

And as a shorthand, sometimes instead of writing, you know, h subscript theta of x, sometimes there's a shorthand, I'll just write as a h of x. But more often I'll write it as a subscript theta over there.

And plotting this in the pictures, all this means is that, we are going to predict that y is a linear function of x. Right, so that's the data set and what this function is doing, is predicting that y is some straight line function of x. That's **h(x) = θ₀ + θ₁x**, okay?

And why a linear function? Well, sometimes we'll want to fit more complicated, perhaps non-linear functions as well. But since this linear case is the simple building block, we will start with this example first of fitting linear functions, and we will build on this to eventually have more complex models and more complex learning algorithms.

Let me also give this particular model a name. This model is called **linear regression** or this, for example, is actually linear regression with one variable, with the variable being x. Predicting all the prices as functions of one variable X. And another name for this model is **univariate linear regression**. And univariate is just a fancy way of saying one variable. So, that's linear regression.

---

## References
1- All about Logistic regression in one article  
2- Introduction to Linear Regression - mathematics and application with Python

