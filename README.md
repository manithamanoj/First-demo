Performing analysis of the Kickstarter data
# Kickstarter Analysis
## Introduction

  Louise is an upcoming playwriter. She started a fundraising campaign of $12000 for her play Fever. She is close to its fundraising goal in a short amount of time. She wanted to know how different campaigns in the Kickstarter data fared in relation to their launch dates and their funding goals. With the help of Excel, we are going to analyze and visualize the campaign outcomes based on their launch dates and their funding goals using the Kickstarter dataset that we have already combed through.
## Purpose

  In this analysis we are trying to help Louise understand how different campaigns fared by answering the questions given below,
•	Do the launch dates have any impact on the success of the campaign?
•	How Does the goal amount impact on the success of a campaign?

## Data Description

 Our data is stored in columns A through N and rows 1 through 4115. So, we use the different features of excel to do this analysis.

# Field	Description
* ID-	Project ID
* Name-	Name of the project
* Blurb	-Description of the project
* Goal	-The Goal column tells us how much money each campaign will need to succeed
* Pledged	-The Pledged column tells us how much each campaign made
* Country-	The Country column lists the country in which the campaign was started
* Currency-	Country currency
* Launched_at-	When project was launched the campaign on Kickstarter
* Staff_pick-	Someone on the Kickstarter team loves your project
* Backers_count -	Number of people who have contributed to the project by paying an amount of money
* Category and Subcategory-	Category and Subcategory which groups a main category with all its subcategories




## Analysis and Challenges
  Outcomes Based on Launch Date Chart
     
 In the given data the launch dates and deadline are given in Unix time stamp. I changed that to human date and added two new columns “Date created conversion” and “Date ended conversion” From "Date Created Conversion". I extracted years from it and added new column “Years “ in the Kickstarter spreadsheet. I inserted a new pivot table in a new worksheet and renamed it as "Theater Outcomes by Launch Date”. I then dragged "Parent Category" and "Years" under the filters. The row label is populated with Date created conversion and that is the launch date. The column and values are populated with outcomes. I applied the filter to remove ‘live’ from the column labels. The "Parent Category" is filtered on "theater" and row label are sorted in ascending order. Next, I inserted a line chart to see the visual representation and gave the chart title as “Theater Outcomes based on Launch date”.

 ![image](https://user-images.githubusercontent.com/72629108/153688056-5e1c3ec8-24c9-460d-b71d-c479ae0c5baf.png)


 ##  Results from “Outcomes Based on Launch Date” Chart
   
 From the pivot chart, we can see that the project with month May as the launch date has the most successful campaign rate followed by June. The month December has the lowest success rate.




  ## Outcomes Based on Goals Chart
  For analyzing Outcomes based on goal, we are using “countif” function and “sum” function. Initially I created a new sheet and labelled it "Outcomes Based on Goals” in the Kickstarter sheet and then created the following columns,
•	Goal
•	Number Successful
•	Number Failed
•	Number Canceled
•	Total Projects
•	Percentage Successful
•	Percentage Failed
•	Percentage Canceled
    In the goal column, I created 12 ranges of dollar-amounts, so that the projects can be grouped based on their goal amount. I used countif function to populate “Number Successful," "Number Failed," and "Number Canceled" from Kickstarter sheet. I also applied the filters on the Kickstarter "outcome" column, the "goal" amount column using the goal ranges created, and the "Subcategory" column with value “plays”. I then applied the sum function to calculate Total projects for each outcome. I also calculated the percentage successful, percentage failed, and percentage cancelled for each dollar range. I created a line chart to visually understand the trend and titled the chat as "Outcomes Based on Goal". The chart helps to visualize the relationship between the goal-amount ranges on the x-axis and the percentage of successful, failed and canceled projects on the y-axis.

 ![image](https://user-images.githubusercontent.com/72629108/153688021-c67f6d26-0ac8-4aeb-8063-1f57523e300c.png)


## Result from Outcomes Based on Goals Chart
From the Chart, we can see that there is a higher chance of campaign failure, if the goal amount is high. For the goal amount given by Louise $12,000 the chart shows a success rate of 54.167%.

## Challenges
One challenge I faced was using the countif function, that was completely new to me. But after watching the video provided, I felt very comfortable to use it.

## Recommendations
We should have also created a chart that shows if demography has any impact on the theater outcomes. We can use a pie chart to easily compare the theater outcomes for each country.

Also, we should have checked the impact of staff_pick on outcome. For this, we can use Stacked Bar chart to represent the relation.

I am also not sure about the reliability of the statistics, since we are using different currencies to calculate the descriptive statistics. (As we are filtering by country it doesn’t matter here). It is better if we convert goal amounts and pledged amount to same currency, if we need to compare across countries.

