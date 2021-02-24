# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this data analysis was to show how fundraising campaigns for theaters and plays fared in relation to their launch dates and their fundraising goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Using a pivot table, I was able to create a dotted line chart that shows the number of successful, failed, and canceled theater fundraising campaigns by month. I did this to see if there were any months that were better than others to launch a fundraising campaign.

![Theater Outcomes Based on Launch Date](./Resources/Theater_Outcomes_vs_Launch.png)

Based on the chart, we can see that theater fundraising campaigns are most successful in May and June, and least successful at the beginning and end of the year.

### Analysis of Outcomes Based on Goals
To see how the fundraising campaigns of plays fared in relation to their fundraising goals, I created a line chart showing the percentage successful, failed, and canceled based on the fundraising goals.
To create the line chart, I first created a table with:

- the goals separated into 12 different categories (i.e. Less than 1000, 1000 to 4999, 5000 to 9999, etc. up to Greater than 50000);
- the number successful, failed, and canceled with their respective percentages using a COUNTIFS formula;
- and the total number of campaigns for each goal.

For example, to find out how many plays were successful with a goal of less than 1000, I used the following formula:

```
=COUNTIFS(Kickstarter!D:D,"<1000",Kickstarter!R:R,"plays",Kickstarter!F:F,"successful")
```

Using the table, I was able to create the line chart showing the outcomes based on the goals.

![Outcomes Based on Goal](./Resources/Outcomes_vs_Goals.png)

Based on the chart, we can see that as the goal increases, the less successful the play fundraising campaign becomes, with an exception of goals between $35000 to $39999 and $40000 to $44999. 

### Challenges and Difficulties Encountered
While I did not encounter any challenges or difficulties during this data analysis, there were a couple areas that could have been potentially problematic. One of these areas could have been with creating the pivot table for the Theater Outcomes Based on Launch Date chart. Knowing which fields to put for the columns, rows, and values while also regrouping the dates can be complicated. The COUNTIFS formulas for the Outcomes Based on Goal chart could also be potentially difficult since there are three variables to work with and having to make sure that the formulas work and are correct.

## Results
- We can conclude that a theater fundraising campaign launched in either May or June are the most successful. This might be because with summer nearing, warmer weather, and school letting out, more people have an interest in going to the theater, and in turn, supporting them. This is also a period where many people are receiving their tax returns and they might feel more generous in supporting theaters.
- We can also conclude that as the goal of a play fundraising campaign increases, the greater the chance the fundraising campaign will fail. Goals with less than $1000 were 76% successful and goals that were between $1000 and $4999 were 73% successful. On the other hand, goals between $45000 and $49999 were 0% successful and goals greater than $50000 were 17% successful. While goals between $30000 to $35000 and $40000 to $44999 were 67% successful, I believe these to be outliers. There are only six total projects with goals between $30000 to $35000 and three total projects with goals between $40000 to $44999. I would predict that if there were more data points in these goal ranges that they would follow the general downward trend.
- While the dataset is useful, it has its limitations. The most considerable limitation of the dataset is that it does not tell the specific amounts that people gave to each fundraising campaign. This data would have been useful as it could have given some insight in helping to determine the goal of a prospective campaign, and would have helped explain why there was an increase in successful campaigns with goals between $30000 to $35000 and $40000 to $44999.
- A table and graph that might have been useful to create is one based on location. The data included 21 countries from around the world and it would have been interesting to see if the success, fail, and cancel rate of fundraising campaigns is similar or vastly different between countries and different cultures. This could be visualized with a stacked bar chart. Other graphs that might have been helpful is the outcomes based on launch date and outcomes based on goals graphs but including all the categories in the dataset. This would have allowed for a comparison between the charts we have on data for plays and theaters with combined charts with all the categories and subcategories. This would help to see if the data trends in our data are unique to plays and theaters or if the trends are generally the same across all categories and subcategories.
