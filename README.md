# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this data analysis was to show how fundraising campaigns for theaters and plays fared in relation to their launch dates and their fundraising goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
Using a pivot table, I was able to create a dotted line chart that shows the number of successful, failed, and canceled theater fundraising campaigns for plays by month.

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

Based on the chart, we can see that as the goal increases, the less successful the play fundraising campaign is, with an exception with goals between 35000 to 44999.

### Challenges and Difficulties Encountered

