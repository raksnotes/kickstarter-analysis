# kickstarter-analysis
Performing analysis on Kickstarter data to uncover trends 
# Kickstarting with Excel

## Overview of Project

### Purpose
## The purpose of this analysis is to visualize the outcomes of different campaigns considering their launch dates and campaign goal.  

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

# Deliverable 1: 
*First, in order to extract the year from the "Date Created Conversion" Column, I used the following formula: 

*YEAR(S:S), the S in this formula refers to the S Column in the Kickstarter worksheet, also known as the 'Data Created Conversion' Column.*

*In order to visualize theater outcomes by launch date, a PivotTable was created. Both the 'parent category' and 'years' columns were placed in the filters box, 'Parent Category' was set to theater, 'Years' was set to All. 'Outcomes' was set in descending order as column values, as well as placed into values in order to show the 'count of outcomes'.*

Theater outcomes were then plotted into a line chart with markers, showing the distinct comparison between successful, failed and canceled outcomes over time by month. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/116187123/203156341-6e526439-cf1f-4c33-92b1-9b064d9a4007.png)

### Analysis of Outcomes Based on Goals

# Deliverable 2: 

*The purpose of deliverable 2 was to visualize the different percentages of outcomes by the ranges of campaign goals.*

*First, I had to calculate the number of successful, failed and canceled outcomes by goal ranges.*

*To calculate this, a COUNTIFS formula was used in Excel, to extract the categories from the Kickstarter Dataset, and setting the appropriate criteria for each column. For example, if I want to calculate the number of successful outcomes, I would use a COUNTIFS statement that includes: the column range for goal, criteria for the goal, column range for outcome, criteria for the outcome, column range for the subcategory, criteria for the subcategory. *

*As part of this deliverable, inn order to achieve the number of successful outcomes for a goal range from 1000 to 4999, under the subcat plays, the syntax would be:* 
**'COUNTIFS(Kickstarter!D:D, ">=1000", Kickstarter!D:D, "<=4999", Kickstarter!F:F, "successful", Kickstarter!R:R, "plays")'**
*where Column D indicates the goal column, Column F indicates the outcome column and Column R indicates the Subcategory column which is indicated by the blue and yellow highlighted markup.*

![columns and headers](https://user-images.githubusercontent.com/116187123/203158172-322c5021-2be5-4074-abfa-7babc0a1abe0.png)


*it turned out that there were no canceled plays when the dataset was filtered to a specific goal range and when the subcategory was set to plays, so this would mean that the number of canceled plays is 0 and the percentage is 0% of canceled plays.* 

The line chart for Outcomes based on Goals is shown below: 

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/116187123/203156868-31b43699-e803-4a5f-bd2c-6f064a7ef541.png)


### Challenges and Difficulties Encountered
# Deliverable 1:
*When creating the Pivot table for Deliverable 1, row labels was set to 'Years', but the visualization required the launch date to be shown by monthly data.*

*This was a challenge that I had run into, since I did not have prior knowledge on how to change the way a value is grouped on Excel. In order to achieve this in the pivot table, I right clicked on one cell value that displayed year, clicked group, and then clicked month. This then grouped the row labels by month.*
![grouping](https://user-images.githubusercontent.com/116187123/203160064-5eef8cf2-4d5c-43cd-b6a4-82d59b5300b0.png)

# Deliverable 2:
*When calculating the number of successful and failed outcomes initially, I had trouble getting the right  line chart output; I had the right COUNTIFS formula, but the outcome wasn't coming out correctly. I went back to the formula and realized that in my criteria, I had forgotten an operator when referencing the first number of the goal range. For calculating a goal range from 10000 to 14999, I had put ">10000";"<=14999", however, it's a range so I would need to include the first number in the range when calculating the number of outcomes. So I was able to catch that error and change the criteria from ">10000" to ">=10000", then my line chart matched.* 

*It's always necessary to double check, a small error can create a big impact on the visualization of the data.*


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

## It is shown in the line chart that canceled outcomes were less than 20, and that there are significantly more successful theater outcomes than failed theater outcomes. The highest outcome seems to be approximately 115 successful outcomes, and the lowest outcome seems to be approximately 1 canceled outcome. 

- What can you conclude about the Outcomes based on Goals?
## I can conclude that the percentage of successful and failed outcomes has kind of a symmetrical change over time. 
## In a few data points but with different goal ranges, the percent of success and failure is the same. At the range 5000 to 9999 and the range 20000 to 24999, there is a 55 percent chance of success and a 55 percent chance of failure. 
## There is a 50 percent chance of success and failure, which is shown at the crossing point in the goal range 15000 to 19999. 

- What are some limitations of this dataset?
## When wanting to figure out the differences between campaign outcomes, sometimes when you filter the data, the list of subcategories don't match up for successful, failed and canceled. For example, in this data, the idea is to visually compare successful, failed and canceled plays, but there aren't any canceled plays. 
## When playing around with the outcomes and subcategories within the data, if I want to compare the number of successful to failed outcomes with the subcategory 'animation', that wouldn't be possible because there are only failed outcomes for 'animation' and not successful outcomes for 'animation'. 

- What are some other possible tables and/or graphs that we could create? 
## Other possible tables could be a bar chart to show the differences between the outcomes. I could only assume approximate values within a line chart or bar chart, however it may be easier to distinguish the visual differences of the outcomes with a higher bar in contrast to a higher line. 
## In reference to the percentage differences for deliverable 2, another possible graph/chart could be a pie chart. Differences in percentages are commonly shown with pie charts, it would be interesting to see the percentage of success versus the percentage of failure. 
