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


## What is Autocorrelation

Strictly speaking, autocorrelation refers to the amount a data point at time t, <u>depends</u> on the past _p-lagged values_. By this _past p-lagged values_ I am simply refering to the past p values. For example, say p = 10, past p-lagged values would be the past p values from time t (so from x<sub>t-10</sub> to x<sub>t</sub>, which is a total of 11 values).  

So, to get into the math, here is the mathematical definition of autocorrelation:

$$
r_k = \frac{\sum_{t=k+1}^T \left(y_t - \hat{y}) \cdot \right (y_t-k - \hat{y}}{\sum_{t=1}^T (y_t - \hat{y}^2}
$$

