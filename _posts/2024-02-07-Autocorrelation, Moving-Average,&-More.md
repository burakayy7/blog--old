---
navigation: true
cover: assets/images/AutoCorr/ACmain.png
title: Part 2 - Autocorrelation, Moving Average, & More
date: 2024-02-07
class: post-template
---

A simple introduction to Seasonal Trends, Decompositions, and many more! This is the second and last part of the lessons on Autocorrelation, Moving Averages, Trends, and Decompositions. For the code used in this tutorial, please view the previous post for the github link. 


## Seasonal Trends

If we want to understand what a _Seasonal Trend _ is, I think it's best if we first understand what we are refrencing when we mean a _trend._ So, look at this graph, 

![image](https://github.com/user-attachments/assets/e5a7cd20-7f87-4778-8ac0-a9a151f86df0)

as you can see, over time, the graph tends upwards. That simple relationship is what we mean when we talk about trends: <u>in which direction does the data tend?</u> If over time, it tends to increase, then we refer it to be a positive trend; if it tends to decrease over time, then we refer to it as a negative trend.

#### Seasonality in Data

These are patterns in the data which are affected by seasonal factors, such as the time of year, or day of weak. For example, we can observe that the sale of snow shovels will be a function of the time of year, whether it is winter or not. So over a 3 year period, we should expect a spike of sales every 12 or so months (which is the time between winters). 

Please observe this graph of the Monthly expenditure ($AUD) on corticosteroid drugs that the Australian health system had between 1991 and 2008: ![image](https://github.com/burakayy7/blog/assets/120507146/b79a4fc8-d835-491c-a551-c69c2fb192a2).

As you can see, there is a spike in the data every 12 months. 

If you run this piece of code, we can view the dates:
```python
  #installations
!pip install skforecast

import numpy as np
import pandas as pd

from skforecast.datasets import fetch_dataset

# Data download
# ==============================================================================
data = fetch_dataset(name='h2o_exog', raw=True) #this dataset is on australian health system, from 1991 to 2008. This is from Hyndman (2023) fpp3
#Monthly expenditure ($AUD) on corticosteroid drugs that the Australian health system had between 1991 and 2008. Two additional variables (exog_1, exog_2) are simulated.

# Data preparation
# ==============================================================================
data = data.rename(columns={'fecha': 'date'})
data['date'] = pd.to_datetime(data['date'], format='%Y-%m-%d')
data = data.set_index('date')
data = data.asfreq('MS')
data = data.sort_index()

#data = data.y

data
```
Then you can click the "Convert this data to an interactive table" button and see the entire dataset.
![image](https://github.com/user-attachments/assets/18b20d7d-ae68-4dbb-8748-3955b6d24741)

As you can see, the spike occurs around winter time. Now there is probably an entire medical reason for this (try to research and find the answer yourself), but that's outside the scope of this lesson. The first data is April 1st, and from the next April 1st, you can see that there is exactly one major spike in the data. The spike is a function of time, and this pattern is reoccuring. 

And that is the simple, introductory, definition to seasonality. 

And that's is simply what we are refering to when we say _Seasonal Trends._ Any patterns in data that has a repeated, predictable, and time-dependent factors, is a type of seasonal trend (can you see why we call it seasonal?).



#### Cycles

Similarly, cycles are when the data shows rises and falls that are not of a fixed frequency. This could be from economic activity. 

Cycles and Seasonality are often confused, and their main differentiation is if the pattern is of fixed frequency. 


## Decompositions

In this section, we will discuss two main ideas which are often closely related: transformations and decompositions. 

### Box-Cox Transformations

Transformations are useful when the data exhibits increases or decreases with the level of the series, such as logorithmic transformations. Transformations are often used to simplify the data before forecasting. Here we will dicuss a common one: the Bickel & Doksum Transformation which is actually a modified Box-Cox Transformation. Mathematically, it looks like this:

$$
w_t =
\begin{cases}
    \log(y_t) & \text{if } \lambda = 0, \\
    \frac{\operatorname{sign}(y_t) \cdot |\lambda - 1|}{\lambda} & \text{otherwise}.
\end{cases}
$$

Here, w<sub>t</sub> depends on \( \lambda \) (or lambda). So, if $\lambda$ is zero, the we will take the logarithm of y (which in Box-Cox is always a natural logarithm (i.e. to base _e_)), but if \( \lambda \) is anything else, w<sub>t</sub will be \( \frac{\operatorname{sign}(y_t) \cdot |\lambda - 1|}{\lambda} \).

### STL Decomposition


#### Additive and Multiplicative Decompositions
