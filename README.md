# R_Analysis

# Overview of Project

This special project is to find solution for the AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

The project output will help Jeremy and the data analytics team do the following:

     . Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
  
     . Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
  
      . Run t-tests to determine if the manufacturing lots are statistically different from the mean population
  
     . Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis,I will write a summary interpretation of the findings.
  
  The project consists of three technical analysis deliverables and a proposal for further statistical study. 

    1. Deliverable 1: Linear Regression to Predict MPG
    
    2. Deliverable 2: Summary Statistics on Suspension Coils
    
    3. Deliverable 3: T-Test on Suspension Coils
    
    4. Deliverable 4: Design a Study Comparing the MechaCar to the Competition
    
  # Resources Used
  
  . Data Source: MechaCar_mpg.csv and Suspension_Coil.csv
  
  . Data Tools: tidyverse, dplyr, ggplot2, geom_boxplot and MechaCarChallenge.RScript.
  
  . Software: RStudio and R
  
 ## Deliverable 1: Linear Regression to Predict MPG
 
    ### Deliverable Requirements:
    
    .  The MechaCar_mpg.csv file is imported and read into a dataframe
    
    .  An RScript is written for a linear regression model to be performed on all six variables
    
    .  An RScript is written to create the statistical summary of the linear regression model with the intended p-values
    
    .  There is a summary that addresses all three questions
    
   #### Results
   
   ##### linear regression
   
   ![image](https://user-images.githubusercontent.com/80365882/122660011-5c2daf80-d132-11eb-9867-7ddfdfbbdf71.png)
   
   ##### Summery
   
   mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)
   
   ![image](https://user-images.githubusercontent.com/80365882/122660032-939c5c00-d132-11eb-8356-1aa34644f6c0.png)

###### The results shows us:

    1.  The vehicle length and vehicle ground clearance have a significant impact on miles per gallon on the MechaCar prototype. 
    
    2. The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.
    
    3. This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. 

There is no significant impact on the removal of less independent variables (vehicle weight, spoiler angle, and All Wheel Drive),  but the r-squared value falls from 0.7149 to 0.674.

![image](https://user-images.githubusercontent.com/80365882/122988301-7051f680-d356-11eb-98a3-4d16b2f5c288.png)


##  Deliverable 2: Summary Statistics on Suspension Coils

THe requirements for Deliverable 2 results are:

     .  The Suspension_Coil.csv file is imported and read into a dataframe
     
     . An RScript is written to create a total summary dataframe that has the mean, median, variance, and standard deviation of the PSI for all manufacturing lots
     
     . An RScript is written to create a lot summary dataframe that has the mean, median, variance, and standard deviation for each manufacturing lot
     
     . There is a summary that addresses the design specification requirement for all the manufacturing lots and each lot individually
    
##### total_summary dataframe :

![image](https://user-images.githubusercontent.com/80365882/122989798-181bf400-d358-11eb-9c44-05ce299d41b3.png)

##### lot_summary dataframe:

![image](https://user-images.githubusercontent.com/80365882/122989924-397ce000-d358-11eb-9852-fdb8eaddd93d.png)


With the understanding that the design specifications for the MechaCar suspension coils mandate that the variance of the suspension coils cannot exceed 100 pounds per square inch (PSI), the variance of the coils is 62.29 PSI, which is well within the 100 PSI variance requirement.

 Lot 1 and Lot 2 are well within the 100 PSI variance requirement; with variances of 0.98 and 7.47 respectively. However, it is Lot 3 that is showing much larger variance in performance and consistency, with a variance of 170.29. It is Lot 3 that is disproportionately causing the variance at the full lot level.

##### This boxplot illustrates the differences between the lots:

![image](https://user-images.githubusercontent.com/80365882/122993552-4bf91880-d35c-11eb-82d8-e39b238299cc.png)


## Deliverable 3: T-Test on Suspension Coils

##### summary of the t-test results across all manufacturing lots

##### T-test for lot1

![image](https://user-images.githubusercontent.com/80365882/122995399-69c77d00-d35e-11eb-9bdf-213b3625036e.png)

From the above T-test results,the true mean of the sample is 1498.78, which we also saw in the total_summary dataframe above. With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.

##### T-test for lot-1

![image](https://user-images.githubusercontent.com/80365882/122995431-75b33f00-d35e-11eb-8a8e-9f004ef582d5.png)

##### T-test for lot-2

![image](https://user-images.githubusercontent.com/80365882/122995534-95e2fe00-d35e-11eb-993f-f61e005743ee.png)

##### T-test for lot-3

![image](https://user-images.githubusercontent.com/80365882/122995568-9ed3cf80-d35e-11eb-996b-f557222bed96.png)




 
 
 
  
