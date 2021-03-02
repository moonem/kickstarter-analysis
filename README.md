# An Analysis of Kickstarter Campaigns
Performing analysis on Kickstarter data to uncover trends. A large data-set having kickstarter campaign data from 21 countries, in 9 catagories (i.e. film & video, food, games, journalism, music, photography, publishing, technology and theater) and 41 sub-categories have been analyzed, sorted and filtered to observe categorical outcomes of various campaigns in the U.S. The followin stacked bar-graph shows summarizes the outcomes of various categories. It seems that "theater" has the most successfull outcomes, although "music" seems to have highest successful-to-failed ratio.

![Parent Category Outcomes](/images/ParentCategoryOutcomes.png). 

Louise has interest to see more details on "plays" sub-category under "theatre" category within the U.S. only. So, the dataset has been filtered to show a focused data subset to support Louise's intention. This analysis will help Louise get in-depth view of the campaign on "plays", for example, observing the goal and pledged amount for both successful and failed campaigns. Following table summerized the key findings on *goal* and *pledged* amount for *successful* and *failed* U.S. kickstarters on plays sub-category.

![US_play_Goal_Pledged](/images/US_play_Goal_Pledged.png). 

Based on these statistics, we can determine the following:
•	The mean of each distribution is around the 3rd quartile, so the data follows similar distributions in each subset.
•	The standard deviations are larger than the mean, which means everything below the mean is considered "close" to the center.
•	Some large values are driving all of these distributions. The standard deviations are all roughly twice the IQR in each distribution, except in the failed Kickstarters, where the standard deviation is closer to three times the IQR. There must be some failed Kickstarters with really high goals.

As we have 9 years' (2009 to 2017) of data on the launch date and duration of the campaigns on "play", we can generate a trend graph to observe if there is any help based on launching the campaign on any particular month(s). The following graph shows that May-June had been good months to start a campaign, although May-to-July also shows a rising trend for "failed" campaigns also. This information doesn't seem to be a core decision making factor, but it helps in addition to the other supporting findings.

![OutcomesBasedOnLaunchDate](/images/OutcomesBasedOnLaunchDate.png). 

While Louise is committed to creating a play in the U.S., she's also interested in researching musicals in Great Britain for a future project with an estimated budget of £4,000. To present Louise with the big picture, a box plot is created using statistical computations.
![GB_Musical_Campaign](/images/GB_Musical_Campaign_Box&Whisker_plot.png).

From the above plot, we can see that the mean campaign goal is around £4,000. This is outside of the range of outliers for amount pledged, so Louise should probably try to get her play produced for less than £4,000. Half of the campaign goals are less than £2,000, which is just over the 3rd quartile for amounts pledged.
