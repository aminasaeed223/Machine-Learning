# 6- Understanding the Linear Regression Cost Function

## Table of Content
- Overview of the Cost Function  
- Type of the Cost function  
- Understanding the Components of the Cost Function  

---

## 1- Overview of the Cost Function  

**Def:** In mathematical optimization and decision theory, a loss function or cost function (sometimes also called an error function) is a function that maps an event or values of one or more variables onto a real number intuitively representing some “cost” associated with the event.

**Def:** Also known as lost function or objective function, it measures the unhappiness with the job being done, that is, if the algorithm is very bad, its value will be high. Basically, it compares the correct category score with the other ones to say how satisfied it is. In machine learning, a cost function is a measure of how well a model performs. It is used to evaluate the model's predictions and to guide the learning process. The goal of the learning process is to minimize the cost function, which means finding the set of parameters that produces the best predictions.The cost function is typically a mathematical function that takes the model's predictions and the ground truth labels as input and outputs a single number. The lower the cost function value, the better the model's predictions.

**Def:** In machine learning, a “cost function” quantifies the difference between predicted and actual values. It measures how well a model performs by assigning a penalty for prediction errors. The goal during training is to minimize this cost function, adjusting model parameters to achieve accurate predictions. Common cost functions include mean squared error for regression and cross-entropy for classification tasks. A well-designed cost function guides the learning process, steering the model towards optimal performance.

The cost function is an important part of machine learning. It is used to evaluate the model's predictions and to guide the learning process. By choosing the right cost function, you can improve the performance of your machine learning models.

---

## 2- Type of the Cost function 

There are many different types of cost functions, each of which is used for a different type of machine learning problem. The two most common loss functions are hinge loss and cross-entropy.

### **Mean squared error (MSE) cost function**
Mean squared error (MSE) cost function is often used for regression problems. This is a common cost function for regression problems. It is calculated as the average of the squared errors between the model's predictions and the ground truth labels.

### **Cross-entropy cost function**
Cross-entropy cost function is often used for classification problems. This is a common cost function for classification problems. It is calculated as the sum of the probabilities of the incorrect labels, multiplied by the negative log of those probabilities.

### **Hinge loss**
This is a cost function that is often used for support vector machines. It is calculated as the sum of the absolute values of the differences between the model's predictions and the ground truth labels.

---

## 3- Understanding the Components of the Cost Function

This will let us figure out how to fit the best possible straight line to our data.

In linear regression, we have a training set like that shown here. Remember our notation M was the number of training examples. So maybe M=47. And the form of the hypothesis, which we use to make predictions, is this linear function. To introduce a little bit more terminology, these theta zero and theta one, right, these theta i's are what I call the parameters of the model.

### **Choosing Parameter Values**

How to go about choosing these two parameter values, theta zero and theta one. With different choices of parameters theta zero and theta one, we get different hypotheses and different hypothesis functions.

- If theta zero is 1.5 and theta one is 0, then the hypothesis function will look like this. Right, because your hypothesis function will be h(x) equals 1.5 plus 0 times x which is this constant value function, this is flat at 1.5.

- If theta zero equals 0 and theta one equals 0.5, then the hypothesis will look like this. And it should pass through this point (2, 1), says you now have h(x) or really some hθ(x) but sometimes I'll just omit theta for brevity. So, h(x) will be equal to just 0.5 times x which looks like that.

- And finally, if theta zero equals 1 and theta one equals 0.5 then we end up with a hypothesis that looks like this. Let's see, it should pass through the (2, 2) point like so. And this is my new h(x) or my new hθ(x). All right? Well you remember that this is hθ(x) but as a shorthand sometimes I just write this as h(x).

---

## **The objective function or Cost function for linear regression**

In linear regression, we have a training set, like maybe the one I've plotted here. What we want to do is come up with values for the parameters theta zero and theta one. So that the straight line we get out of this corresponds to a straight line that somehow fits the data well. Like maybe that line over there.

So how do we come up with values theta zero, theta one that corresponds to a good fit to the data?  
The idea is we're going to choose our parameters theta zero, and theta one so that h(x), meaning the value we predict on input x, is close to the values y for the training examples.

So we try to choose values for the parameters so that given the x's in the training set, we make reasonably accurate predictions for the y values.

### **Formalizing this**

We want to solve:

**minimize** over θ₀, θ₁  
the **sum of squared errors** between prediction and actual price.

Notation:  
(x(i), y(i)) = ith training example  
M = number of training examples

So the cost function is:

\[
\frac{1}{2M} \sum_{i=1}^{M} \left( h_\theta(x^{(i)}) - y^{(i)} \right)^2
\]

This is J(θ₀, θ₁).

This is the **Squared Error Cost Function** — the most commonly used one for regression tasks.

---

### **Mathematical detail**

J = (∑(y’−y)²) / n  

This squared-loss is widely used because it works well for most regression problems.

Our objective is to choose values of θ₀ and θ₁ to minimize the loss function.

---

## 4- Conclusion

Okay. So that's the cost function. So far we've just seen a mathematical definition of this cost function and in case this function J of theta zero theta one seems a little bit abstract, in the next videos we’ll go deeper into intuition.

**Remember, learning is a continuous process.  
So keep learning and keep creating and sharing with others! 💻✌️**

---

## **References**
1- Machine Learning (Andrew)  
2- Google Bar  
3- Easy Way to Understand and Visualize Loss and Cost Functions  
