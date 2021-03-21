# MechaCar_Statistical_Analysis
Module 15: Statistics and R

## Overview
In this challenge we help AutosRUs and develop an analysis for their newest car prototype. The company is having issues with the production and it is blocking the manufacturing progress. 
The goal of this week is to create analysis to help AutosRUs'upper management with actionable insights to improve the manufacturing cycle. 

## Summary:
Please find below the summary of the statistical analysis performed in this challenge. 

### Linear Regression to Predict MPG
 
* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    
    Considering the significance level (alpha) as 0.05 (the probability thershold of usualness) and the p-values from the regression testing (table below), the only variables lower than 0.05 were the vehicle_lenght and the ground_clearance variables, so we can reject the null hypotesis and infer that the observed difference is significant.

    All the other variables: vehicle_weight, spoiler_angle and AWD have p-values above alpha, so we retain the null hypothesis, and the observed difference is due to random chance. 

    ![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression_summary_stats.JPG)

* Is the slope of the linear model considered to be zero? Why or why not?

    Based on the linear coeficients stated below, the slope of the linear model is not considered to be zero. Since some of the indenpendent variables influenced the miles per gallon (mpg), the slope is not zero.

    ![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression.JPG)

* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

    To quantify how well the linear model can be used to predict future observations, we use the r-squared value. The r-squared (r2) value is also known as the coefficient of determination and represents how well the regression model approximates real-world data points. In this analysis our r2 is 0.7149, meaning that roughly 71% of all miles per galon predictions will be correct when using this linear model, so we can infer that the model is effective for the prediction of mpg. 

    ![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/linear_regression_summary_stats_r2.JPG)

### Summary Statistics on Suspension Coils

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

    Analyzing the summary data below, the PSI variance is 62.29, lower than the 100 from the specifications, so the manufacturing data meet this design specification.

    ![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/total_summary.JPG)

    In addition to that, when we analyze the data broken down by the manufacturing lot, we can see that the variance in Lot 3 exceeds the threshold from the design expetations since 170.27 is higher than 100. 
    This can indicate that the manufacturing issue is due to production problems in the lot 3. Lot 1 and 2 pass the design specifications. 

    ![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/lot_summary.JPG)
    
### T-Tests on Suspension Coils

T-tests were performed to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.
Using a significance level (alpha) of 0.05 (the probability thershold of usualness) and analyzing the p-values from the t-test below, all of them are way larger than alpha, so the null hypotesis is true and the observed difference is due to random chance and are not statistically different from the population mean of 1,500 pounds per square inch.

T-test results: full sample

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_full_sample.JPG)

T-test results: Lot 1

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot1.JPG)

T-test results: Lot 2

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot2.JPG)

T-test results: Lot 3

![ScreenShot](https://github.com/liviamiyabara/MechaCar_Statistical_Analysis/blob/main/Resources/t_test_lot3.JPG)

## Study Design: MechaCar vs Competition

By using R and its statistical tools, a study could be performed to compare the performance of MechaCar vehicles and other manufacturers. 

* What metric or metrics are you going to test?

    Since the goal of the study is to show differentiators from MechaCar and competitors, one analysis could be comparing the brand of the vehicle with the maintenance costs.

* What is the null hypothesis or alternative hypothesis?

    The null hypothesis is that the observed differences in maintance cost between OEMs (Original Equipment Manufacturer) is due to random chance and there is no significant difference between the groups.

* What statistical test would you use to test the hypothesis? And why?

    I would use the ANOVA test since:
      * The dependent value is numerical and continuous (maintenance cost), and the independent variable is categorical (car manufacturer)
      * The dependent variable is considered to be normally distributed
      * The variance among each group should be very similar

* What data is needed to run the statistical test?
    
    Ideally a large sample is prefferable with a good distribution of different car types (SUV, pick up, sedan, etc) and age, we will need the information from the car manufacturer and also the total maintenance costs from the car owner 