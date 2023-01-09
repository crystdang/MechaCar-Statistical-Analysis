# Module 16 Challenge: MechaCar Production Analysis - Statistics & R
## by Crystina Dang using R v4.2.2, RStudio v2022.12.0+353

## Part 1:
## Linear Regression to Predict MPG
A multiple linear regression model was used on the dependent variable fuel efficiency (mpg) and the independent variables vehicle length, vehicle weight, spoiler angle, ground clearance and AWD. 

Vehicle length and ground clearance (as well as inteception) are the coefficients that are statistically unlikely to provide a non-random amount of variance to the linear model. The probability value is smaller than a normal significance level, providing sufficient evidence to reject the null hypothesis and that the slope is not zero. This linear model predicts fuel efficiency of the MechaCar prototypes effectively because of the high coefficient of determination (R-squared) of 0.7.


*Below is an image of the multiple linear regression output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/linear_reg.png)

*Below is an image of the multiple linear regression summary output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/lr_summary.png)

## Part 2:
## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The specification is met for the total lot at 62.3, whereas manufacturing lot 3 does not meet the design specification at 170.3. As the mean is similar across all lots, the higher variance represents a larger distribution of data.

*Below is an image of the total_summary table:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/PSI.png)

*Below is an image of the lot_summary table:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/Lots.png)

## Part 3:
## T-Tests on Suspension Coils

T-tests were performed to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. Only lot 3 proved the two means are statistically different.


The t-test performed for all lots did not provide sufficient evidence to reject the null hypothesis as the probability value is higher than a normal significance level at 0.06.
*Below is an image of the t.test output for all lots:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/t.test_All.png)

The t-test performed for lot 1 did not provide sufficient evidence to reject the null hypothesis as the probability value is higher than a normal significance level at 1.
*Below is an image of the Lot 1 t.test output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/t.test_Lot1.png)

The t-test performed for lot 2 did not provide sufficient evidence to reject the null hypothesis as the probability value is higher than a normal significance level at 0.6.
*Below is an image of the Lot 2 t.test output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/t.test_Lot2.png)

The t-test performed for lot 3 did provide sufficient evidence to reject the null hypothesis as the probability value is lower than a normal significance level at 0.4.
*Below is an image of the Lot 3 t.test output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/t.test_Lot3.png)

## Part 4:
## Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

What metric or metrics are you going to test?

What is the null hypothesis or alternative hypothesis?

What statistical test would you use to test the hypothesis? And why?

What data is needed to run the statistical test?