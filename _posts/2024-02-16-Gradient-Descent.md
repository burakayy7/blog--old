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

```
import pandas as pd
import matplotlib.pyplot as plt
import random
x = [i for i in range(-110, 120, 10)]
y = [3*i-5 for i in x]
y = [i+(random.random()*250) for i in y]
df = pd.DataFrame({'a1': x, 'a2': y})
plt.scatter(df.a1, df.a2, color="black")
```
![image](https://github.com/burakayy7/blog/assets/120507146/2188ce3a-3389-4903-a13c-547e5c2bd87e)


