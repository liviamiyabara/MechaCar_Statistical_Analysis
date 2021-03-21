# MechaCar_Statistical_Analysis
Module 15: Statistics and R

## Overview

## Summary

### Linear Regression to Predict MPG
 

* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
 Considering the significance level (alpha) as 0.05 (the probability thershold of usualness) and the p-values from the regression testing (table below), the only variables lower than 0.05 was the vehicle_lenght and the ground_clearance variable, so we can reject the null hypotesis and inffer that the observed difference is significant.

 All the other variables: vehicle_weight, spoiler_angle and AWD has p-values above alpha, so we retain the null hypothesis, and the observed difference is due to random chance. 

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression_summary_stats.JPG)

* Is the slope of the linear model considered to be zero? Why or why not?

Based on the linear coeficients stated below, the slope of the linear model is not considered to be zero. Since some of the indenpendent variables had an effect on the miles per gallon (mpg), the slope is not zero.

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression.JPG)

* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
To quantify how well the linear model can be used to predict future observations, we use the r-squared value. The r-squared (r2) value is also known as the coefficient of determination and represents how well the regression model approximates real-world data points. In this analysis our r2 is 0.7149, meaning that roughly 71% of all miles per galon predictions will be correct when using this linear model, so we can inffer that the model is effective for the prediction of mpg. 

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression_summary_stats_r2.JPG)