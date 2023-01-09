# Module 16 Challenge: MechaCar Production Analysis - Statistics & R
## by Crystina Dang using R v4.2.2, RStudio v2022.12.0+353

## Introduction:
AutoRUs' newest prototype, the MechaCar, is under review for manufacturing issues and two datasets were collected. 

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. 

The Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.


## Part 1:
## Linear Regression to Predict MPG
A multiple linear regression model was used on the dependent variable fuel efficiency (mpg) and the independent variables vehicle length, vehicle weight, spoiler angle, ground clearance and all wheel drive (AWD). 

Vehicle length and ground clearance (as well as inteception) are the coefficients that are statistically unlikely to provide a non-random amount of variance to the linear model. The probability value is smaller than a normal significance level, providing sufficient evidence to reject the null hypothesis and that the slope is not zero. This linear model predicts fuel efficiency of the MechaCar prototypes effectively because of the high coefficient of determination (R-squared) of 0.7.


*Below is an image of the multiple linear regression output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/linear_reg.png)

*Below is an image of the multiple linear regression summary output:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/lr_summary.png)


## Part 2:
## Summary Statistics on Suspension Coils

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The specification is met for the lot total at 62.3, whereas manufacturing lot 3 does not meet the design specification at 170.3. As the mean is similar across all lots, the higher variance for lot 3 represents a larger distribution of data.

*Below is an image of the total_summary table:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/PSI.png)

*Below is an image of the lot_summary table:*
![This is an image](https://github.com/crystdang/MechaCar-Statistical-Analysis/blob/main/Images/Lots.png)


## Part 3:
## T-Tests on Suspension Coils

T-tests were performed to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch (PSI). Only lot 3 proved the two means are statistically different.


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

As the MechaCar is a new prototype, the statistical study for safety rating would be of great interest to a consumer. The metric that should be tested is whether all wheel drive is necessary and can be predicted from the MechaCar_mpg.csv dataset using a multiple linear regression model.

H0 : all of the independent variables will be statistically likely to provide random amount of variance to the linear model

Ha : one or more independent variable will be statistically unlikely to provide random amount of variance to the linear model
