---
navigation: true
cover: 'assets/images/'
title: Gradient Descent & Linear Regression
date: 2024-02-16
class: post-template
---
In this post I will be introducing the math behind Gradient Descent and how it works!

I was first introduced to Gradient Descent when I had to implement autoregressive models from scratch. To learn this, I first tried to implement a Linear Regression. 

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

Here is how the Linear Regression Algorithm works:

First, start off with a random set of m (this is often referred to as the weight because is has a scaling affect) and b (which is referred to as the bias because it will shift, or apply a bias, to our line). For simplisity sake, we can also start off with m and b equaling zero.

```python
m = 0
b = 0
```
Then we take our first point in the data set and take the gradient.


