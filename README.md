# Constructing acccurate predictions of impressions for an advertisement from the Snapchat Political and Advocacy ads library 

## Background 

The Snap Inc. Political and Advocacy Ads Library provides the public with access to political, issue related, and advocacy Ads that are shown on Snapchat. This library was created to give visibility into Snapchat's political and advocacy-related advertisements. The Political and Advocacy Ads Library is an important step in efforts to increase the level of transparency around political and issue advertising on Snapchat. All political, issue, and advocacy Ads are publicly available, along with relevant information on impressions, spend, and paying entities. Information on the organization that created the Ad, impressions, spend, targeting criteria, and the creative are all available. This analysis goes over the attached data to tackle following questions/concepts: 

1. What is the best way to predict impressions based on the data given?
2. Analyze the relationship among impressions received and money spent in the scope of the last four years 

Source: https://www.snap.com/en-US/political-ads 


## Business Question or Hypothesis 

Can you predict the number of impressions for an advertisement for any of the years of given data?

## Data Question 

Can multiple regression model tell me which variables will be the best predictors of impressions for an advertisement for any of the years of given data?

## Analysis

First, all worksheets were combined into one document and attached to this repository. 

Given metrics that could be used to perform multiple regression were: Currency Code, Spend, Start/ End Date, Gender, age brackets and etc. 

**Regression 1:** First, I decided to test if **duration** of how long the ad has been running could be a good predictor for impressions. 
  Therefore, Duration column was created (Times were omitted from dates and I took the difference of the End Day and Start Day. If end day was blank, meaning the ad is still running, I used the function =TODAY() to set the end date as the date of analysis performed) 
  Simple Linear Regression was performed and following reslts were obtained:
  
  ![Simple Linear Regression,Duration](https://github.com/DurdonaG/linear_regression_snapchatdata/blob/main/Analyzed%20Data%20and%20Results/Screen%20Shot%202021-03-04%20at%208.48.50%20AM.png)
  
  ###### Interpretation:
  Least square estimate of Duration is given as a coefficient. Our **null hypothesis**: Duration is not useful (or significant) in predicting impressions. **Alternative Hypothesis**: Duration is useful (or significant) in predicting impressions.
  Significance F Value 0.697 indicates that there are 697 chances in 1000 that my independent variable is not useful in predicting Y which is a pretty high number. 
  Since it is > than 0.05, we fail to reject null hypothesis. 

**Regression 2:** Now, we take money spent and duration as independent variables to predict impressions. Following results were obtained: 

![Simple Linear Regression,Duration and Money Spent](https://github.com/DurdonaG/linear_regression_snapchatdata/blob/main/Analyzed%20Data%20and%20Results/image.png)

###### Interpretation:
  Least square estimate of Duration and Money spent are given as coefficients. Our **null hypothesis**: Duration and Money spent are not useful (or significant) in predicting impressions. **Alternative Hypothesis**: Together all independet variables are useful (or significant) in predicting impressions.
  Significance F Value 9.18E-136,extremely small, so we reject null hypothesis.  
  Now, when we look at the p- values individually, we can tell that Duration is not significant in predicting impressions. 
  
**Regression 3:**  This time, currencies, duratiion, and money spent were used as independent variables. Dummy variables were created for the currencies: USD, EUR, GBP, CAD. Following results were obtained: 
![Simple Linear Regression: Currency, duration, money spent](https://github.com/DurdonaG/linear_regression_snapchatdata/blob/main/Analyzed%20Data%20and%20Results/Screen%20Shot%202021-03-04%20at%209.15.41%20AM.png)

###### Interpretation:
Best fitting estimate of the multiple regression equation: Y = -146982.14 +352.19A + 213.63B +45182.79C + 442058.17D + 697291.07E +329993.72F
ANOVA:  **Null hypothesis**: The hypothesis of no linear regression: together all independent variables are not useful (or significant) in predicting Y. **Alternative Hypothesis**: Together all independet variables are useful (or significant) in predicting Y.

Since Significance f value is 2.14E-142, which is less than .05, we reject the null hypothesis and conclude that All independent variables are useful in predicting Y. 
*R squared value* 0.643 indicates that 64.3% of the variation in Y is explained by our equation. Therefore, 35.7% of the variation in Y is unexplained by the multiple linear regression model. 

*Standard error* value of 642495.8 indicates that approximately 68% of the prediction for Y are accurate within one standard error. 

Remark: Even though, p values are greater than 0.05 for some currencies, because other currencies are significant, we know there is significant currencies so we leave USD, eUR, and CAD. 

## Relating back to Business Question: ##

After doing several multiple regressions, we can conclude that impressions can be predicted from Currencies, money spent, and duration, all independent variables taken togeteher. 

Based on my analysis it might be helpful to consider the target market of ads based on gender, age bracket and etc, but since the information in the spreadsheets was not complete for the aforementioned criteria, I did not include them into this anaysis. 













