# A_B_Testing


## Business Value

A-B testing plays a critical role in decision making process across industries. It is a method of comparing and testing the effectiveness and benefits of two different busines strategies. It can be considered as a experiment where two or more strategies are tested for a set period of time and then the experiment results are evaluated to find the strategy that has an edge over the other. 

In a typical A/B testing setting, we would create and test two or more versions of the marketing strategies for their effectiveness in achieving the marketing goal. 

__Hypothesis Testing__

It is important to test for our hypothesis and seek for statistically significant differences among the test group. The t-test compares the two averages and examines whether they are significantly different from each other or not. 

There are two important statistics in a t-test, the t-value and the p-value. 
t-value measures the degree of difference relative to the variation in the data, larger the t-value more is the difference in the two groups.
P-value measures the probability that the results will occur by chance, smaller the p-value, more statistically significant difference there will be between the two groups.  

The equation to compete t-value is:

![](Data%20Visualization/t%20value.PNG)

where M1 and M2 are the average of the group 1 and 2. S1 and S2 are the standard deviations of the group 1 and 2 and N1 and N2 are number of samples in group 1and 2 respectively.

## Problem Statement

To determine the statitically significant most effective promotion out of the three promotions group undertaken for the marketing campaign.

## Data

__Data Sample__

![](Data%20Visualization/Data%20Sample.PNG)

Each row of data represents a sales transaction for the attributes mentioned in the columns of the data table.

__MarketID__ : Unique identifier for for each market 

__MarketSize__ : Size of the market area by sales 

__LocationID__ : Identifier for the location of the store

__AgeOfStore__ : Number of years the store has been operating at the location

__Promotion__ : Promotion type (1/2/3) being run at this store

__Week__ : Number of weeks the promotion has been running

__SalesInThousands__ : Total sales amount in thousands of dollars for specific location, promotion and week. 


## Approach

+ Importing Necessary Dependencies

+ Loading Data

+ Data Exploration and Visualization
	
+ Hypothesis testing

## Evaluation

We formulate the hypothesis:

Null Hypothesis: Two groups of promotion data show no statistically significant difference in Sales Amount

Alternate Hypothesis: Two groups of promotion data show statistically significant difference in Sales Amount

We take threshold value of t-value and p-value to be 5% i.e 0.05

When the t-value of our test is greater than the threshold t-value and p-value of our test is less than threshold p-value, we can reject the null hypothesis and acceot that the the two groups show statistically significant difference in sales due to the the effect of promotions.

## Data Exploration and Visualization

__Sales Distribution Across Different Promotions__

![](Data%20Visualization/Sales%20promotion.png)

__Number of Stores in each Market__

![](Data%20Visualization/Market%20Size.PNG)

__Market Size Breakdown Across Promotions__

Unstacked

![](Data%20Visualization/Market%20Size%20Breakdown.png)

Stacked

![](Data%20Visualization/Mkt%20Size%20Promotion%20Breakdown.png)

__Distribution of Age of Store__

![](Data%20Visualization/Overall%20Age%20Distribution.png)

__Store Age Distributions Across Different Promotions__

![](Data%20Visualization/Age%20distribution%20of%20Store%20across%20promotions.png)

__Promotion Across Week__

![](Data%20Visualization/Promotion%20across%20week.png)

## Hypothesis Testing

### Computing t-value and p-value

We find that the means for Promotion 1 is 58.09, Promotion 2 is 47.32 and Promotion 3 is 55.36.

On calculating t-value and p-value while taking into consideration Promotion 1 and Promotion 2 we find the t-value is 6.42 and p-value is 4.143296816749853e-10. 

On calculating t-value and p-value while taking into consideration Promotion 1 and Promotion 3 we find the t-value is 1.5560224307759116
 and p-value is 0.12058631176433687.

## __Conclusion__

For Promotion 1 vs Promotion 2 t-value is greater than threshold t-value and p-value is less than threshold p-value. Therefore we can accept that there is statistically significant change in sales amount due to promotion 1 over promotion 2 i.e Promotion 1 performs better to drive up sales amount as against Promotion 2
 
However we cannot say the same for Promotion 1 over Promotion 3 as it doesn't satisfy both our conditions p-value is greater than the threshold p-value. So we coclude that Promotions 1 and 3 outperform the Promotion 2 but difference in average sales amount due to Promotions 1 and Promotions 3 is not statistically significant.
