# Statistical & Machine Learning Explorations with Wolfram Demonstrations

**Author:** Vedant Zore (Roll No. 62)

**Date:** November 10, 2026

**Report File:** `62_VEDANT_ZORE_WOLFRAM_10_11_26`

## Overview

This repository documents an interactive exploration of three foundational concepts in statistics and machine learning using the **Wolfram Demonstrations Project**. By dynamically adjusting parameters in Wolfram Cloud notebooks, this study visualizes how theoretical formulas behave under different configurations:

1. **Critical Value** $z^*$ **for z-Scores for Confidence Levels**

2. **The Normal Distribution**

3. **Linear Regression**

## Table of Contents

* [1. Critical Value z\*for z-Scores for Confidence Levels](#1-critical-value-z-for-z-scores-for-confidence-levels)

* [2. The Normal Distribution](#2-the-normal-distribution)

* [3. Linear Regression](#3-linear-regression)

* [Tools & Resources](#tools--resources)

## 1. Critical Value $z^*$ for z-Scores for Confidence Levels

### Concept

In statistics, the critical value $z^*$ serves as the bridge between a chosen confidence level and the standard normal distribution. Used in both traditional significance testing and the construction of confidence intervals, $z^*$ marks the exact boundary on the bell curve that captures a specified central percentage of the distribution—such as $99\%$—while splitting the remaining probability equally into the two tails.

Calculated using the inverse cumulative distribution function (CDF) of the tail area, this value allows researchers to combine a sample mean and population standard deviation into a confidence interval that reliably estimates the true population mean.

### Experimental Observations

| Trial | Confidence Level | Unshaded Central Area | Critical Value ($z^*$) | 
| ----- | ----- | ----- | ----- | 
| **1** | $0.806$ | $0.81$ | $1.299$ | 
| **2** | $0.902$ | $0.90$ | $1.655$ | 
| **3** | $0.990$ | $0.99$ | $2.576$ | 

### Key Takeaway

As the desired confidence level increases, the unshaded central region expands toward the edges of the bell curve, pushing the critical value $z^*$ further away from the mean and reducing the shaded tail areas.

## 2. The Normal Distribution

### Concept

The normal distribution is one of the most fundamental probability distributions in statistics, characterized by its symmetric, bell-shaped curve. Its probability density function (PDF) is defined as:

$$
f(y) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{\frac{-(y-\mu)^2}{2\sigma^2}}
$$

The curve's exact shape and position are governed by two key parameters:

* **Mean (**$\mu$**):** Shifts the center of the distribution horizontally along the axis.

* **Standard Deviation (**$\sigma$**):** Controls the spread and height of the curve.

In the demonstration, a customized normal curve (blue) is compared directly against the **standard normal distribution** (red/magenta), where $\mu = 0$ and $\sigma = 1$.

### Experimental Observations

| Trial | Mean ($\mu$) | Standard Deviation ($\sigma$) | Visual Comparison to Standard Normal ($\mu=0, \sigma=1$) | 
| ----- | ----- | ----- | ----- | 
| **1** | $-1.15$ | $2.0$ | Shifted to the left; significantly wider and flatter peak. | 
| **2** | $0.35$ | $2.0$ | Shifted slightly to the right; wider and flatter peak. | 
| **3** | $0.35$ | $1.2$ | Shifted slightly to the right; narrower spread and taller peak, closely resembling the standard normal curve. | 

### Key Takeaway

Changing $\mu$ translates the curve without altering its shape, whereas increasing $\sigma$ flattens and widens the curve (since the total area under the PDF must always remain $1$).

## 3. Linear Regression

### Concept

Linear regression is a foundational statistical and machine learning technique used to model the relationship between variables by fitting a straight line to observed data. It is represented by the linear hypothesis:

$$
h_\theta(x) = \theta_0 + \theta_1 x
$$

The accuracy of the fitted line is evaluated using the Mean Squared Error (MSE) cost function:

$$
J(\theta_0, \theta_1) = \frac{1}{2m} \sum_{i=1}^{m} \left(h_\theta(x_i) - y_i\right)^2
$$

By tuning the intercept ($\theta_0$) and slope ($\theta_1$) parameters, we can observe the residual errors (vertical distances from data points to the line) and track the parameter pair's position on the cost function's contour landscape as it moves toward the global minimum (optimal solution).

### Experimental Observations

| Trial | Training Examples ($m$) | Intercept ($\theta_0$) | Slope ($\theta_1$) | Contour Lines | Cost Function $J(\theta_0, \theta_1)$ | 
| ----- | ----- | ----- | ----- | ----- | ----- | 
| **1** | $23$ | $4.25$ | $-0.74$ | $90$ | $67.5497$ | 
| **2** | $64$ | $4.25$ | $0.64$ | $49$ | $11.8832$ | 

### Key Takeaway

When the slope $\theta_1$ is misaligned with the positive trend of the dataset (Trial 1, $\theta_1 = -0.74$), the cost $J(\theta_0, \theta_1)$ is high ($67.5497$) and sits far from the center of the contour plot. Adjusting $\theta_1$ to better align with the data trend (Trial 2, $\theta_1 = 0.64$) significantly lowers the cost ($11.8832$), moving the red marker much closer to the optimal green solution at the center of the contour basin.

## Tools & Resources

* **Platform:** [Wolfram Demonstrations Project](https://demonstrations.wolfram.com/)