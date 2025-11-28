# Gradient Descent with Example | Step By Step

In Statistics, Machine Learning, and other data science field we optimize a lot of stuff when we fit a line with linear Regression, we optimize the Intercept and Slop

When we use logistic Regression, we optimize Squiggle

And when we use T-SNE, We optimize cluster 

The Cool thing is that Gradient Descent can optimize all these things and much more 

So if we learn how to optimize this line using Gradient Descent

So let’s start with a simple dataset On the x-axis, we have weight And on the y-axis we have heights 

If we fit  a line to the data

And some tell us that they weight 1.5

We can use the line to predict that they will be 1.9 tall 

So let's learn how Gradient Descent can fit a line to data by finding the optimal values for the intercept and the slop

Actually, we will start by using Gradient Descent to find the intercept, and then once we understand how Gradient Descent work, we will use it to solve for the intercept and the slop.

So for now, let is just plug in the least-squares estimate for the slope, 0.64.

And we will use Gradient Descent to find the optimal value for the intercept 

The First thing we do is pick a random value for the intercept. This is just an initial guess that give Gradient Descent something to improve upon. In this case, we use 0, but any number will do 

And that give us the equation for this line 

In this example, we will evaluate how well this line fits the data with the sum of the squared Residual 

________________________

Actually, we'll start by using gradient descent to find the intercept.

Then once we understand how gradient descent works we'll use it to solve for the intercept and the slope.

So for now let's just plug in the least squares estimate for the slope 0.64.

And we'll use gradient descent to find the optimal value for the intercept the first thing we do is pick a random value for the intercept this is just an initial guess that gives gradient descent something to improve upon in this.

Case: we'll use 0 but any number will do.

And that gives us the equation for this line.

In this example, we will evaluate how well this line fits the data with the sum of the squared residuals note in machine learning lingo the sum of the 

Squared residual is a type of loss function.

we'll talk more about loss functions towards the end of the video we'll start by calculating this residual this data point represents a person with weight 0.5 and height 1.4 

we get the predicted height of the point on the line by plugging weight equals 0.5 into the equation for the line and the predicted height is 0.32

The residual is the difference between the observed height and the predicted height.

so we calculate the difference between 1.4 and 0.32 and that gives us 1.1 for the residual.

we'll keep track of the sum of the squared residuals up here here's the square of the first residual the second residual is 0.4 and the third residual is 1.3 in the end 3.1 is the sum of the squared residuals now just for fun we can plot that value on a graph this graph has the sum of squared residuals on the y-axis and different values for the intercept on the x-axis this point represents the sum of the squared residuals when the intercept equals zero however if the intercept equals 0.25 then we would get this point on the graph and if the intercept equals 0.5 then we would get this point and for increasing values for the intercept, we get these points.

of the points that we calculated for the graph this one has the lowest sum of squared residuals.

but is it the best we can do?

what if the best value for the intercept is somewhere between these values?

A slow and painful method for finding the minimal sum of the squared residuals is to plug and chug a bunch more values for the intercept.

Don't despair gradient descent is way more efficient gradient descent only does a few calculations far from the optimal solution.

And increases the number of calculations closer to the optimal value in other words gradient descent identifies the optimal value.

By taking big steps when it is far away and baby steps when it is close so let's get back to using gradient ascent to find the optimal value for the intercept starting from a random value in this case the random value was zero.

when we calculated the sum of the squared residuals.

The first residual was the difference between the observed height.

which was 1.4

and the predicted height.

which came from the equation for this line.

so we replace predicted height with the equation for the line since the individual weighs 0.5 we replace weight with 0.5 

so for this individual this is their observed height and this is their predicted height note we can now plug in any value for the intercept and get a new predicted height. 

Now let's focus on the second data point just like before the residual is the difference between the observed height which is 1.9 and the predicted height which comes from the equation for the line and since this individual weighs 2.3 we replace weight with 2.3 now let's focus on the last person again the residual is the difference between the observed height

which is 3.2 and the predicted height which comes from the equation for the line and since this person weighs 2.9 we'll replace weight with 2.9 

Now we can easily plug in any value for the intercept.

And get the sum of the squared residuals.

Thus we now have an equation for this curve. 

and we can take the derivative of this function and determine the slope at any value for the intercept.

so let's take the derivative of the sum of the squared residuals with respect to the intercept the derivative of the sum of the squared residuals with respect to the intercept equals the derivative of the first part.

plus the derivative of the second part plus the derivative of the third part.

let's start by taking the derivative of the first part first we'll move this part of the equation up here so that we have room to work to take the derivative of this we need to apply the chain rule so we start by moving the square to the front and multiply that by the derivative of the stuff inside the parentheses these parts don't contain a term for the intercept so they go away.

then we simplify by multiplying two by negative one and this is the derivative of the first part so we plug it in now we need to take the derivative of the next two parts i'll leave that as an exercise for the viewer bam let's move the derivative up here so that it's not taking up half the screen now that we have the derivative gradient descent will use it to find where the sum of squared residuals is lowest.

**Gradient Decent Part 1/2 | Session 01 | Izhar Ul Haq**

note if we were using least squares to solve for the optimal value for the intercept we would simply find where the slope of the curve equals zero.

in contrast gradient ascent finds the minimum value by taking steps from an initial guess until it reaches the best value.

this makes gradient descent very useful when it is not possible to solve for where the derivative equals zero and this is why gradient descent can be used in so many different situations.

bam remember we started by setting the intercept to a random number in this case that was zero.

so we plug zero into the derivative and we get negative 5.7 so when the intercept equals 0 the slope of the curve equals negative 5.7.

Note the closer we get to the optimal value for the intercept the closer the slope of the curve gets to zero

this means that when the slope of the curve is close to zero.

then we should take baby steps because we are close to the optimal value.

and when the slope is far from zero.

then we should take big steps because we are far from the optimal value.

however if we take a super huge step.

then we would increase the sum of the squared residuals so the size of the step should be related to the slope since it tells us if we should take a baby step or a big step but we need to make sure the big step is not too big.

gradient descent determines the step size by multiplying the slope.

by a small number called the learning rate note we'll talk more about learning rates.

later when the intercept equals 0 the step size equals negative 5.7 with the step size we can calculate a new intercept the new intercept is the old intercept minus the step size so we plug in the numbers and the new intercept equals 0.57 bam in one big step we moved much closer to the optimal value for the intercept.

going back to the original data and the original line with the intercept equals 0.

we can see how much the residuals shrink when the intercept equals 0.57.

now let's take another step closer to the optimal value for the intercept to take another step we go back to the derivative and plug in the new intercept and that tells us the slope of the curve equals negative 2.3.

Now let's calculate the step size by plugging in negative 2.3 for the slope and 0.1 for the learning rate ultimately the step size is negative 2.3 and the new intercept equals 0.8 now we can compare the residuals when the intercept equals 0.57 to when the intercept equals 0.8.

overall the sum of the squared residuals is getting smaller.

notice that the first step was relatively large compared to the second step.

now let's calculate the derivative at the new intercept and we get negative 0.9 the step size equals negative 0.09 and the new intercept equals 0.89 now we increase the intercept from 0.8 to 0.89 then we take another step and the new intercept equals 0.92 and then we take another step and the new intercept equals 0.94 and then we take another step and the new intercept equals 0.95.

notice how each step gets smaller and smaller the closer we get to the bottom of the curve. 

after six steps the gradient ascent estimate for the intercept is 0.95 note the least squares estimate for the intercept is also 0.95.

so we know that gradient descent has done its job but without comparing its solution to a gold standard how does gradient descent know to stop taking steps.

gradient descent stops when the step size is very close to zero the step size will be very close to zero.

when the slope is very close to zero in practice the minimum step size equals 0.001 or smaller so if this slope equals 0.009 then we would plug in 0.009 for the slope and 0.1 for the learning rate and get 0.0009 which is smaller than 0.001 so gradient descent would stop that said gradient descent also includes a limit on the number of steps it will take before giving up in practice the maximum number of steps equals 1000 or greater.

so even if the step size is large if there have been more than the maximum number of steps gradient descent will stop okay.

let's review what we've learned so far.

the first thing we did is decide to use the sum of the squared residuals as the loss function to evaluate how well a line fits the data.

then we took the derivative of the sum of the squared residuals in other words we took the derivative of the loss function.

then we picked a random value for the intercept in this case we set the intercept to be equal to zero then we calculated the derivative when the intercept equals zero.

plug that slope into the step size calculation and then calculated the new intercept the difference between the old intercept and the step size.

lastly we plugged the new intercept into the derivative and repeated everything until step size was close to zero.

double bam now that we understand how gradient descent can calculate the intercept let's talk about how to estimate the intercept and the slope.

just like before we'll use the sum of the squared residuals as the loss function this is a 3d graph of the loss function for the different values for the intercept and the slope this axis is the sum of the squared residuals this axis represents different values for the slope and this axis represents different values for the intercept we want to find the values for the intercept and slope that give us the minimum sum of the squared residuals.

so just like before we need to take the derivative of this function and just like before we'll take the derivative with respect to the intercept but unlike before we'll also take the derivative with respect to the slope we'll start by taking the derivative with respect to the intercept just like before we'll take the derivative of each part.

and just like before we'll use the chain and move the square to the front and multiply that by the derivative of the stuff inside the parentheses [Music] since we are taking the derivative with respect to the intercept we treat the slope like a constant and the derivative of a constant is zero.

so we end up with negative one just like before then we simplify by multiplying two by negative one and this is the derivative of the first part so we plug it in likewise we replace these terms with their derivatives so this whole thing is the derivative of the sum of squared residuals with respect to the intercept now let's take the derivative of the sum of the squared residuals with respect to the slope just like before we take the derivative of each part and just like before we'll use the chain rule to move the square to the front and multiply that by the derivative of the stuff inside the parentheses since we are taking the derivative with respect to the slope we treat the intercept like a constant and the derivative of a constant is zero.

so we end up with negative 0.5 then we simplify by moving the negative 0.5 to the front note i left the 0.5 in bold instead of multiplying it by 2 to remind us that 0.5 is the weight for the first sample and this is the derivative of the first part so we plug it in likewise we replace these terms with their derivatives again 2.3 and 2.9 are in bold to remind us that they are the weights of the second and third samples here's the derivative of the sum of the squared residuals with respect to the intercept and here's the derivative with respect to the slope note when you have two or more derivatives of the same function they are called a gradient.

we will use this gradient to descend to the lowest point in the loss function which in this case is the sum of the squared residuals thus this is why the algorithm is called gradient ascent.

bam just like before we'll start by picking a random number for the intercept in this case we'll set the intercept to be equal to zero and we'll pick a random number for the slope in this case we'll set the slope to be 1. thus this line with intercept equals 0 and slope equals 1 is where we will start.

now let's plug in 0 for the intercept and 1 for the slope.

and that gives us two slopes.

now we plug the slopes into the step size formulas and multiply by the learning rate which this time we set to 0.01 note the larger learning rate that we used in the first example doesn't work this time even after a bunch of steps gradient ascent doesn't arrive at the correct answer.

this means that gradient descent can be very sensitive to the learning rate.

the good news is that in practice a reasonable learning rate can be determined automatically by starting large and getting smaller with each step so in theory you shouldn't have to worry too much about the learning rate anyway we do the math and get two step sizes now we calculate the new intercept and new slope by plugging in the old intercept and the old slope and the step sizes and we end up with a new intercept and a new slope this is the line we started with.

and this is the new line after the first step now we just repeat what we did until all of the step sizes are very small or we reach the maximum number of steps.

this is the best fitting line with intercept equals 0.95 and slope equals 0.64 the same values we get from least squares.

double bam we now know how gradient descent optimizes two parameters the slope and the intercept if we had more parameters.

then we just take more derivatives and everything else stays the same triple bam note the sum of the squared residuals is just one type of loss function.

however there are tons of other loss functions that work with other types.

of data regardless of which loss function you use gradient descent works the same way.

step 1 take the derivative of the loss function for each parameter in it in fancy machine learning lingo take the gradient of the loss function 

step 2 pick random values for the parameters step 

3 plug the parameter values into the derivatives ahem the gradient

step 4 calculate the step sizes 

step 5 calculate the new parameters now go back to step 3 and repeat until step size is very small or you reach the maximum number of steps one last thing before we're done in our example we only had three data points so the math didn't take very long but when you have millions of data points it can take a long time so there is a thing called stochastic gradient descent that uses a randomly selected subset of the data at every step rather than the full data set this reduces the time spent calculating the derivatives of the loss function that's all stochastic gradient descent sounds fancy but it's no big deal hooray we've made it to the end of another exciting stat quest if you like this stat quest and want to see more please subscribe and if you want to support statquest well consider buying one or two of my original songs or buying a stack quest t-shirt or hoodie the links to do this are in the description below alright until next time quest on 

====================================================================

References: 

StatQuest With Josh Stamm | Gradient Descent, Step-by-Step
