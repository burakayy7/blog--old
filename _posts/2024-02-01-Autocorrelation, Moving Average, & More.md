---
navigation: true
cover: assets/images/AutoCorr/ACmain.png
title: Autocorrelation, Moving Average, & More
date: 2024-02-01
class: post-template
---

A simple introduction to Autocorrelation, Moving Average, STL Decomposition, Seasonal Trends, and much more!

Today, I would like to teach you about Forecasting Principles, which include but aren't limited to, Autocorrelation, moving average filters, additive and multiplicative decomposition, STL decomposition, etc.

This became relevant when I started my research on forecasting epidemics like the COVID-19 pandemic. The ultimate question at hand would be something along the lines of, how many people will be hospitilized after t days and in which specific location. These statistics can be very useful when making political, societal, or economic based decisions. 

So one thing we can use to predict hospitilizations or really any dataset that contains some sort of repeated pattern, is something called autoregressive models. But to learn this, one first needs to know what autocorrelation is, and other statistical metrics. Thus, this post. 

****Disclaimer:** You can find most of the code refrenced here in my repo [here](https://github.com/burakayy7/ARIMA-model/blob/main/ARIMA_model.ipynb)


## What is Autocorrelation

Strictly speaking, autocorrelation refers to the amount a data point at time t, <u>depends</u> on the past _p-lagged values_. So, just how correlation measures the linear relationship between two variables, autocorrelation measues the linear relationship bewteen _lagged_ values in a time series dataset(so since it is based off it's own past values, can you see why it's called _auto_? And here time series refers to the fact that the dataset is a function of time, as in, it's order via time). By this _past p-lagged values_ I am simply refering to the past p values. For example, say p = 10, past p-lagged values would be the past p values from time t (so from x<sub>t-10</sub> to x<sub>t</sub>, which is a total of 11 values).  

r<sub>1</sub> represents the correlation bewtween y<sub>t</sub> and y<sub>t-1</sub>. Similarly, r<sub>2</sub> measures the relationship between y<sub>t</sub> and y<sub>t-2</sub>. So, to get into the math, here is the mathematical definition of autocorrelation for the value r<sub>k</sub>:

$$
r_k = \frac{\sum_{t=k+1}^T \left(y_t - \hat{y}) \cdot \right (y_t-k - \hat{y})}{\sum_{t=1}^T (y_t - \hat{y}^2)}
$$
(T is the length of our dataset)

where the numerator represents the [sample autocovariance](https://ccs.fau.edu/~bressler/EDU/STSA/Modules/IV.pdf) and the denominator represents the [variance](https://en.wikipedia.org/wiki/Variance). Here, r<sub>k</sub> measures the correlation between the past lagged values.  

And there are actually ways in which we can visualize these values.

### Visualizing Autocorrelation

Now, in CS, there are a ton of different types of graphes. And I won't get into them now since they are out of scope for this tutorial. So instead I will cheat and use libraries that do the math and code for us. 

Now, time to actually code! 
