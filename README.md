# MechaCar Statistical Analysis
> ## Overview
A few weeks after starting his new role, Jeremy is approached by upper management to review the production data for insights that may help the manufacturing team from suffering from production troubles. We will be analyzing a dataset for a new MechaCar with 50 different prototypes.

## Results

> ### Linear Regression to Predict MPG

![image](https://user-images.githubusercontent.com/124399950/222401824-0f309086-d3c7-454e-88f7-f7684079ed48.png)

Residual standard error: 8.774 on 44 degrees of freedom  
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825  
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11 

These result suggest that *vehicle length* and *ground clearance* have the most significant impacts on mpg. 

The overall *P-value* of the model is *5.35e-11.* This is smaller than the significance level of 0.05 and thus calls to **reject the null hypothesis** which assumes that the slope is **not** zero
the results suggest that the variables available can effectively predict the MPG of the prototype MechaCars.

The **R-squared** value in its turn is *0.7149* and assumes that around 72% of MPG predictions will be determined by this model. Jeremy then assumes that this model does effectively predict mpg of MechaCar prototypes.



> ### Summary Statistics on Suspension Coils

Total summary  


![image](https://user-images.githubusercontent.com/124399950/222401979-90134ddd-21c9-47bb-94d4-0df387305ee7.png)

Lot Summary  

![image](https://user-images.githubusercontent.com/124399950/222402053-94b065ae-601a-4077-bff2-b7e38ffb97de.png)

If our required metric of variation for PSI is to be less than 100, in aggregate across all the lots we would pass this metric (variance is 62 PSI), but lot 3 fails this metric (variance is 170 PSI). Lot 3 has too much variation and should be reconsidered. 

> ### T-Test on Suspension Coils

1 sample T-test  

![image](https://user-images.githubusercontent.com/124399950/222402174-bb38861a-b1a9-42d5-82af-a9514ee83607.png)

1 sample T-test Lot1 population mean

![image](https://user-images.githubusercontent.com/124399950/222402238-53084004-cb84-43ed-94ee-f6e4eca8569f.png)

1 sample T-test Lot2 population mean

![image](https://user-images.githubusercontent.com/124399950/222402302-50334d13-3536-489c-b9db-659d1da4b3f5.png)

1 sample T-test Lot3 population mean

![image](https://user-images.githubusercontent.com/124399950/222402342-8b74bbe2-647d-4c3c-9ef2-1e306d588a76.png)

For a single sample T-test comparing lots 1 and 2 to the population mean we so no statistically significant difference in the means (Lot1 P=1.5 e-11; Lot2 p=0.0006). 
However we do see a statistically significant difference in the means between lot3 and the population (p=0.1589)

Again, this points to something peculiar happening with lot3 having significant variation of the mean PSI ratings. 

> ### Study Design: MechaCar vs Competition
Some of the main metrics I would want to consider for a consumer are the fuel efficiency and horsepower as a function of total vehicle cost. 
A lower cost for higher horsepower and higher fuel efficiency is desirable. 

To compare these we can get the pierson correlation coeficients for the relationship between the MechaCar cost vs. fuel efficiency and compare that to the competition cost vs fuel efficiency. In addition to the pierson coeeficient we will want to know what the slope relationship is. 
as stated above a lower cost for a higher fuel efficiency (if cost is the independant variable, then a smaller slope coeficient is better), and having a higher pierson correlation would help to validate this. 

We can also use a 2 sample t-test to see if there is a statistically significant difference in the average values of fuel efficiency and horsepower of the two fleets. If they are statisitically significant then we may be able to use this information to support claims that the MechaCar has better performance. 
If they are not statistically different we can use that to help refute a competitor claim that their fleet is better (the null hypothesis is likely true and the cars are roughly the same or no different). 
We would need similar data for both manufacturers, and we would want it on a large quantity of samples (either individual units or a large number of models). we would likely want at least 100, and may not need more than 1000 to have a strong claim. 



