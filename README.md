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
1. First, I decided to test if **duration** of how long the ad has been running could be a good predictor for impressions. 
  1. Therefore, Duration column was created (Times were omitted from dates and I took the difference of the End Day and Start Day. If end day was blank, meaning the ad is still running, I used the function =TODAY() to set the end date as the date of analysis performed) 
  1. Simple Linear Regression was performed and following reslts were obtained:
  
  ![Simple Linear Regression,Duration](https://github.com/DurdonaG/linear_regression_snapchatdata/blob/main/Analyzed%20Data%20and%20Results/image.png)
  
  ######Interpretation: Least square estimate of Duration is given as a coefficient. Our **null hypothesis**: Duration is not useful (or significant) in predicting impressions. **Alternative Hypothesis**: Duration is useful (or significant) in predicting impressions.
  Significance F Value 0.697 indicates that there are 697 chances in 1000 that my independent variable is not useful in predicting Y which is a pretty high number. 
  Since it is > than 0.05, we fail to reject null hypothesis. 




4. Perform calculations and model-building to answer the data-related questions; A list of any data analysis or metrics that you explored and any resulting numbers, tables or visualizations that help convey the results + a brief description about what these mean
5. Relate the data findings back to your initial business question and outline what your linear regression model tells us about election ads, city government salaries, etc.;  A brief summary of how the numerical findings relate back to your initial question, what you can answer 

based on your data analysis, what additional data might be helpful for you to build on these findings, and why this is important for you 

NOTE: Depending on your question you do not have to format your README in this exact format (e.g. “Business Question”, “Data Question”, etc.) as long as you include all of the same relevant information.

Apply Excel Data Analysis ToolPak correlation and regression functions to model a simple and a multiple linear regression equation (with at least 2 independent variables) with a publicly available dataset.
Determine what linear regression statistics such as the R2 value, standard error, coefficients, p-value, and F significance mean for your specific data set, and interpret these results for a non-technical audience
Evaluate and interpret your linear regression models and explain to your audience (based on the dataset used and business questions posed) what these values mean and how your audience should consider these values for current and future operations.

Project Deliverables


Excel files of the original data used for your analysis
Excel files that contain your analysis. If this is too large to save in the GitHub repository, save this in a Google Drive and provide a link to the data in your README.
README.md file
Simple step-by-step descriptions on how you manipulated the Excel data 

Description 
Create a public GitHub repository that contains your written summary of the regression analysis and your Excel/CSV files used

Components
Excel files of the original data used for your analysis
Excel files that contain your analysis. If this is too large to save in the GitHub repository, save this in a Google Drive and provide a link to the data in your README.
README.md file
Simple step-by-step descriptions on how you manipulated the Excel data 
README components
A brief statement summarizing background information about your initial problem statement. Here you should also include any links to relevant outside sources.
A 1-sentence “Business Question” based on the background information that you intend to explore with data
A list of data sources with brief descriptions with links to either the original data sources or the Excel files in your GitHub repository
A list of any data analysis or metrics that you explored and any resulting numbers, tables or visualizations that help convey the results + a brief description about what these mean
A brief summary of how the numerical findings relate back to your initial question, what you can answer based on your data analysis, what additional data might be helpful for you to build on these findings, and why this is important for you 

NOTE: Depending on your question you do not have to format your README in this exact format (e.g. “Business Question”, “Data Question”, etc.) as long as you include all of the same relevant information.

Can you predict the number of impressions for an advertisement for any of the years of given data?

Can we predict impressions based on how much spent and age bracket 
how they vary over the year 

Analysis of the Snapchat Political and Advocacy ads library and prediction of the number of impressions for an advertisement for the given data
