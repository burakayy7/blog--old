---
navigation: true
cover: ![](https://github.com/burakayy7/blog/assets/120507146/9e45a485-6010-4d45-8113-2335d249d70f)
title: Gradient Descent & Linear Regression
date: 2024-02-16
class: post-template
---
In this post I will be introducing the math behind Gradient Descent and how it works!

I was first introduced to Gradient Descent when I had to implement autoregressive models from scratch. To learn this, I first tried to implement a Linear Regression. 


**Disclaimer: I will be using Python code in this tutorial found in my [repo](https://github.com/burakayy7/LinearRegression).**

Please follow along, I think it helps to see an example. Or better yet, create your own script by using the code in this post. 

Linear Regressions are brought up in the context of tring to find a line that best fits the trend of a data set.
For example, lets say we wanted to find the line which best represents this graph:

~~~python

import pandas as pd
import matplotlib.pyplot as plt
import random
x = [i for i in range(-110, 120, 10)]
y = [3*i-5 for i in x]
y = [i+(random.random()*250) for i in y]
df = pd.DataFrame({'a1': x, 'a2': y})
plt.scatter(df.a1, df.a2, color="black")
~~~
![image](https://github.com/burakayy7/blog/assets/120507146/2188ce3a-3389-4903-a13c-547e5c2bd87e)

Well, we know that the final equation will look something like this:
```
y = mx + b
```
So all we have to do is find the appropriate values for m and b. While we could go the trial-and-error method and try a bunch of values until the result _looks right_, we could also have a computer automate that process for us. 

### Here is how the Linear Regression Algorithm works:
1. Start with an initial line equation
2. Calculate how far you are from the expected value when you plug in a point, using the current m and b.
3. Then slightly adjust m and b in the _direction_ which will get us _closer_ to the expected value
4. Repeat steps 2 and 3 for a specified amount (this is referred to as the epoch size)


First, start off with a random set of m (this is often referred to as the weight because is has a scaling affect) and b (which is referred to as the bias because it will shift, or apply a bias, to our line). For simplisity sake, we can also start off with m and b equaling zero.

```python
m = 0
b = 0
```
Then we take our first point in the data set and plug it into our line equation. This should give us an output value. We can compare this with the expected value (since we know the point) by finding the error. Now, there are a variety of different error functions (referred to as the cost function, can you see why?) which can be used, and it will depend on your system. But for simplicity sake, I have chosen the _Mean Squared Error_ cost function. 

#### How does the Mean Squared Error Cost Function Work

So imagine we know the real value, say y_real. Then from some equation we get a computed value, say y_cal. We wish to know the error between these. The first thing that comes to mind is simply
```
error = y_real - y_cal
```
However, what if over time we got a bunch of negative and positive error values that when summed up (which will happen in our MeanSquaredError function because we will calculate the error across the entire dataset at once) would result in a value close to zero (the positive and negaitves would cancel)? This is where the _squared_ term comes in. By squaring the error value, we eliminate the posability of a negative value.
```python
error = (y_real - y_cal)**2
```
Next, we wish to know the error across the entire dataset, so the somewhat obvious method might be to take the average of all the errors between every point, this is the _mean_ term.

So now our algorithm is something like this:
```python
def mean_squared_error(m, b, points):
  total_error = 0
  for i in range (len(points)):
    x_i = points.iloc[i].a1
    y_i = points.iloc[i].a2
    total_error += (y_i - (m*x_i+b))**2
  return total_error/float(len(points)) #take the average
```
Here _points_ is a [Pandas DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html) and I just access the x and y components. And when calculating the error, I just simply calculate the value on the spot with ```total_error += (y_i - (m*x_i+b))**2``` ,adding it to a variable to then take the average.

Easy enough? If not, here is another resource: [for help](https://statisticsbyjim.com/regression/mean-squared-error-mse/)

Once we know our error, we wish to know how much we should adjust m and b according to this value. If we have a big error, maybe we should make a big change, but if it's small, a tiny change might be sufficient. 

This is when Gradient Descent comes in.

The underlining goal in the Linear Regression algorithm is to modify the weights and biases in such a way, that we get closer to our goal. But the question remains: How do we know how much we want to modify each value? 

### How does Gradient Descent Work

So let's observe our cost function:


$$
\text{error} = \sum_{i=0}^n (y_i - (m \cdot x_i + b))^2
$$


The first thing we wish to know, is how much our error will change with a small change in m. Then according to that value, we will adjust m to reduce 
