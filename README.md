# MechaCar_Statistical_Analysis

## Overview
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress.
The goal of this project is to:
* discover which variables predict the MPG for vehicle prototypes;
* collect summary statistics on the pounds per square inch (PSI) of suspension coils from the manufacturing lots;
* determine if manufacturing lots are statistically different from the mean population;
* design a study to compare the vehicle performance of MechaCar vehicles against vehicles from other manufacturers.
## Results
### Linear Regression to Predict MPG
![Img1_linear Regression](https://user-images.githubusercontent.com/108683284/210033876-97a49a41-048b-4c15-bb4a-168569be4c42.png)

The most significant variables in our dataset which show a non-random effect on the MPG of the MechaCar are the **Vehicle Length** and the **Ground Clearance**. As indicated by the yellow arrows in the image above, a linear regression model run on these variables against figures for MPG, resulted in p-values of 2.6x10<sup>-12</sup> and 5.21x10<sup>-8</sup>, respectively. The intercept was also statistically significant, indicating that there are likely other factors, not included in our dataset, that have a strong impact on the MPG. The slope of the linear model can not be considered to be zero, as the p-value of 5.35x10<sup>-11</sup>, indicated by the orange arrow above, is lower than even an extreme level of significance, and thus the null hypothesis must be rejected. This means that the relationship between our variables and the miles per gallon is subject to more than random chance. Although there are still unconsidered factors, this model does predict the mpg of the MechaCar prototype with some relative effectiveness. The r-squared value of 0.7149, indicates that the model is 71% accurate... though it could probably do better.

 ### Summary Statistics on Suspension Coil
![Img2_suspension_mean](https://user-images.githubusercontent.com/108683284/210034045-df7bef88-a1cb-4806-861d-752f8a445202.png)
![Img3_lot Stats](https://user-images.githubusercontent.com/108683284/210034062-7acb0424-5d47-43ec-8afa-7b92e6245368.png)
While the overall variance, as shown in the Total Summary data above, is under 100 psi and meets specifications, there is a problem with one of the individual lots. As shown in the Lot Summary stats, the variance for Lot 3 is well over the acceptable threshold, at 170.28.

 * The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

### T-Tests on Suspension Coil
![Img4_t-all lots](https://user-images.githubusercontent.com/108683284/210034225-fbccb283-877c-4019-8a69-74c329db3c00.png)

A review of the results of the T-test for the suspension coils across all manufacturing lots shows that they are not statistically different from the population mean, and the p-value is not low enough (0.0603) for us to reject the null hypothesis.
![Img5_t-lot1](https://user-images.githubusercontent.com/108683284/210034248-99e18040-64de-4785-9945-fd2a994aa660.png)

A review of the results of the T-test for the suspension coils for Lot 1 shows that they are not statistically different from the population mean, and the p-value is not low enough (1) for us to reject the null hypothesis.
![Img6_t-lot2](https://user-images.githubusercontent.com/108683284/210034312-02635e5f-734e-450e-b8f4-46912c92221d.png)

A review of the results of the T-test for the suspension coils for Lot 2 shows that they are not statistically different from the population mean, and the p-value is not low enough (0.6072) for us to reject the null hypothesis.
![Img7_t-lot3](https://user-images.githubusercontent.com/108683284/210034331-4ca90980-27d6-486b-abac-c4572b740b34.png)

A review of the results of the T-test for the suspension coils for Lot 3 shows that they are slightly statistically different from the population mean, and the p-value is just low enough (0.0417) for us to reject the null hypothesis. This lot may be need to be discarded, or at least more closely evaluated.


## Study Design: MechaCar vs Competition
There are many factors that consumers take into consideration when evaluating a car to purchase. However, in a world where ridesharing is becoming more ubiquitous and it's easy and cheap to get around in other people's vehicles, customers looking to purchase a car are looking for more than just a conveyance. They will be looking to buy a car that is an economical means to regularly transport themselves and their items on a reliable, regular basis.

To narrow down our test, we should evaluate MechaCar's carrying capacity, in cubic inches, in comparison to various competitors' vehicles.

Null Hypothesis: MechaCar prototypes' average carrying capacity is similar to competitor's vehicles in the same vehicle class
Alternate Hypothesis: MechaCar prototypes' average carrying capacity is statistically above or below that of competitor vehicles.

The best statistical test for this would be two-sample t-tests.
