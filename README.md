# Kickstarting with Excel

## Overview of Project
This project is to perform analysis on Kickstarter data to uncover trends and correlation among various factors. A large dataset having kickstarter campaign data from 21 countries, in 9 catagories (i.e. film & video, food, games, journalism, music, photography, publishing, technology and theater) and 41 sub-categories have been analyzed, sorted and filtered to observe categorical outcomes of various campaigns. Louise has interest in sub-category *plays* under category *theater*, and she wants to know how the other campaigns on *plays* performed in relation to their launch dates and their funding goals.

### Purpose
There are two purposes of this analysis, first – to observe the trend of theater outcomes based on launch date, that means, if there is any suitable time of the year to start a campaign to be successful. Second – to understand the relation of success-rate with the amount of campaign goal.

## Analysis and Challenges
Following paragraphs reveal more detail of this analysis.

### Analysis of Outcomes Based on Launch Date
As there is 9 years' (2009 to 2017) of data on the launch date and duration of the campaigns on play, a trend graph can be generated to observe if there is any useful information about launching the campaign on any particular month(s). 
A pivot table was created based on *Parent category* and *Years*,and filtered for category *theater* and three outcomes i.e. *successful*, *failed*, *canceled* - as shown in following table.

Table-1: *theater* campaign outcomes based on launch date

![Table 1](/images/Table_theater_vs_LaunchDate.png) 

Based on the filtered data from the pivot table a line-chart has been created to show the relation of outcomes for the *theater* campaign with the launch time in a year. The following line-chart shows that May-June had been good months to start a campaign. 

![Outcome vs Launch Date](/resources/Theater_Outcomes_vs_Launch.png). 

### Analysis of Outcomes Based on Goals
To analyze outcomes based on goals, a new table has been created on 12 different ranges of goal amount for sub-category *plays*. 

 Table-2: “plays” campaign outcome based on Goal amount
 
 ![Table 2](/images/Table_playOutcomes_vs_Goal.png) 

Number of successful, failed and canceled campaigns for *plays* sub-category has been populated using the **=COUNTIFS()** function. The following formula shows how the Number of Successful campaigns i.e. 341 was calculated from the *Kickstarters* sheet for goal range of $1000 to $4999.

=COUNTIFS(Kickstarter!$D:$D, ">1000", Kickstarter!$D:$D, "<=4999",Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays")

Based on the data in the above table, a line-chart has been created using the Goal column as ***x***-axis and percent values of successful, failed and canceled in the ***y***-axis. Since there was no canceled campaign in *plays* sub-category, it shows a 0% straight line on the ***x***-axis.

![Outcomes vs Goal](/resources/Outcomes_vs_Goals.png).

### Challenges and Difficulties Encountered
Choosing the proper items for Pivot table’s Row and Column, has been a little challenging for me. Actually, that’s the key part of a pivot table – to understand what we want to extract in relation to other available parameters.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  1) May-June had been good months to start a campaign.
  2) The line-chart shows that *failed* campaigns also follow quite similar trend like *successful* ones along the year. This information doesn't seem to be a core decision making factor, but it may help other supporting findings.

- What can you conclude about the Outcomes based on Goals?
Most of the successful campaigns in “plays” sub-category had goal amount less than $5000. 

- What are some limitations of this dataset?

  There could have more specific information in the Kickstarter dataset to identify the type of projects precisely. For example, people might be more interested in literary character based *plays* than musical or other types of *plays*. So, the success story of other campaigns in the same category (e.g. *plays*) may not exactly reflect the scenario as Louise is intending to get.
  
- What are some other possible tables and/or graphs that we could create?

The line-chart “Outcomes Based on Goal” seems not to convey the desired information efficiently, as the chart is created based on the percentage of outcomes within each goal-range, not based on actual number of campaigns. For example, in the goal-range of $40,000 to $44,999 there are only 3 projects in plays sub-category and 2 of them were successful, i.e. 67% successful. Whereas, in the goal-range of $1,000 to $4,999 there are 469 projects in plays sub-category and 341 of them were successful, i.e. 73% successful. Although 67% seems close to 73% in the chart, in terms of number of projects they don’t convey very useful message. Instead of “Outcomes based on Goal” chart the following chart based on actual project numbers could be more helpful for Louise to decide about the campaign goal amount.

![Number of Plays vs Goals](/images/NumberOfPlaysOutcome_vs_Goal.png) 

