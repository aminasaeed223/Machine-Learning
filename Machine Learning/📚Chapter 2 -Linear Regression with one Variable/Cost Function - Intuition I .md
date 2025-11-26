# 007_Cost Function - Intuition I (11 min)

## Table of Content
- Recap
- What the cost function is doing?
- Why we want the Cost function?
- Recap

---

## Recap
We want to fit a straight line to our data, so we had this formed as a hypothesis with these parameters theta zero and theta one, and with different choices of the parameters we end up with different straight line fits. So the data which are fit like so, and there's a cost function, and that was our optimization objective.

---

## Simplified Hypothesis for Visualization
So this tutorial, in order to better visualize the cost function J, I'm going to work with a simplified hypothesis function, like that shown on the right. So I'm gonna use my simplified hypothesis, which is just theta one times X. We can, if you want, think of this as setting the parameter theta zero equal to 0. So I have only one parameter theta one and my cost function is similar to before except that now H of X that is now equal to just theta one times X. And I have only one parameter theta one and so my optimization objective is to minimize J of theta one.

In pictures what this means is that if theta zero equals zero that corresponds to choosing only hypothesis functions that pass through the origin, that pass through the point (0, 0).

---

## What the Cost Function is Doing
Using this simplified definition of a hypothesizing cost function let's try to understand the cost function concept better.

It turns out that two key functions we want to understand:
1. The hypothesis function
2. The cost function

### Hypothesis
So, notice that the hypothesis, right, H of X. For a face value of theta one, this is a function of X. So the hypothesis is a function of, what is the size of the house X.

**Google Bard:** In machine learning, a hypothesis is a mathematical function or model that converts input data into output predictions. It is an explanation or solution to a problem based on insufficient data. A good hypothesis contributes to the creation of an accurate and efficient machine-learning model.

For example, let's say we have a dataset of houses with their respective prices. We want to build a machine learning model that can predict the price of a house given its features, such as the number of bedrooms, the square footage, and the location.

One possible hypothesis for this model could be the following linear regression equation:

