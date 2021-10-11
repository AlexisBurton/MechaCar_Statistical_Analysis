# MechaCar Statistical Analysis
## Linear Regression to Predict MPG
Not knowing which vehicle characteristics contributed to MechaCar's fuel efficiency, we ran a multiple linear regression analysis to determine which characteristics were statistically significant. Using a significance factor of 0.05, we found that vehicle length and ground clearance contributed non-random variance to the fuel efficiency. This is somewhat contrary to conventional wisdom, which has vehicle weight and drive train being contributing factors to efficeinecy, so it is ceratinly worth investigating further.<br/>
Given a p-value very near to zero, we can conclude that the null hypothesis of there being no relationship between the characteristics and the fuel efficiency must be rejected. Therefore the slope of the model is not zero.<br/>
The linear model is somewhat effective in predicting the fuel efficiency. The R<sup>2</sup> value of 0.7149 indicates that it correctly predicts 71-72 percent of the time. However, since the Intercept also has a statistically significant amount on non-random variance, there are likely other vehicle characteristics not accounted for in the linear regression that also contribute to fuel efficiency.
<img src ="https://raw.githubusercontent.com/AlexisBurton/Src-images/master/15/Multiple-linear-regression.png">

## Summary Statistics on Suspension Coils
Looking at the suspension coil manufacturing as a whole, the coils seem to be within the design variance tolerance of 100 psi. When the individual manufacturing lots are evaluated, we find that Lots 1 & 2 have very little variance and Lot 3 is well outside of the design tolerance.<br/>
<img src ="https://raw.githubusercontent.com/AlexisBurton/Src-images/master/15/total-summary.png">
<img src = "https://raw.githubusercontent.com/AlexisBurton/Src-images/master/15/lot-summary.png">

## T-Tests on Suspension Coils
Running a T-test on the suspension coils, still using a .05 significance value, we find that the aggregated sample likely has a mean matching the population mean of 1,500 PSI.
<img src = "https://raw.githubusercontent.com/AlexisBurton/Src-images/master/15/t-test.png">
However, when we break the coils into manufacturing lots, we find that while Lots 1 & 2 likely have means matching the population, Lot 3 has only a 4.168% chance of matching the population mean, which falls under our limit of 5%.
<img src = "https://raw.githubusercontent.com/AlexisBurton/Src-images/master/15/t-test-by-lot.png">

## Study Design: MechaCar vs Competition
In order to quantify how MechaCar could perform against its competitors, we would have to think about how the customers perceive value. In today's environment, I beleive the initial cost, maintenance cost and fuel efficiency are most important to look at. We could run an ANOVA test across these variables with the null hypothesis that MechaCar performs the same as its competitors and an alternative that it does not. If the null hypothesis is rejected, we would then need to see if MechaCar performs better or worse than the competitiona and determine what we could do to improve it.