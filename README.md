
# Data Visualization for Flights Delay Records

This [data set](http://stat-computing.org/dataexpo/2009/the-data.html) contains all flight records in 2008.[More details](https://www.transtats.bts.gov/Fields.asp?Table_ID=236)

## Summary

This interactive visualization shows the how flights of top 5 busiest carriers delayed in 2008 in United States by time. The daily metric is the ratio of flights delayed more than 15 minutes each day. The monthly metric is the mean of flights delayed > 15mins per day by month.

## Design

### The Story to Tell

The information I'd like to convey is how flights delay varies by date and by different carrier. By showing the visualization work, I hope readers can have the basic idea on how flights delay and if possible, it may help readers to manage the travel schedule properly.

### Choosing Metric

#### Carrier, Month, DayofMonth, Ratio, Mean

I assumed year 2008 is a good reflection of a common year for reference. (This may not be true since it's about 8 years ago.)
While travelling, passengers may be concerned about the scheduel and would like to avoid unexpected change which might result in ruining the whole arrangement. Thus, it's important for passengers to know how likely, and how long the flights will delay. I chose 15-minute-delay on destination arrival as the boundry for readers to know the probability of delay longer than that. 

Apart from the daily metric, the mean of the numbers of 15-minute-delay flights per day for every month. This can show how the delay varies month by month.

### Visualization

The main plot is about day of month. I use area chart to show the trends by day and the comparison between carriers. Flights from different carriers were visually encoded by colors.

The bar plot also provide interactive function for readers to navigate on their own. Readers can choose to see the time of interests such as holidays.

There is a briefing before the chart for readers to understand the basic information and background.

## Feedback

### Readers' Takeaways

1. There are peaks where carriers often delay during summer and winter.
2. From Dec 15- De 30, delays seems to be a common occurrence for majority of the airlines.
3. Southwest Airlines delayed a lot compared to others and US Airways did well in avoid delay. There're certain patterns on how the variable fluctuate.

### Problems & Suggestions

I collected feedbacks from 4 persons. Here are the key points:

1. The whole picture is not clear as don't know the ratio of delayed flights. Why choose mean and median?
2. Can not see clearly which carrier did better than others and which worse. 
3. How is statistics calculated? 
4. Title doesn't reflect the plot of the story.
5. The automate animation is annoying.

### Reflection & Revise

##### Problem 1

I used mean and median as metrics.

There were several statistics to choose from for Daily status. Ratio of delayed flights, mean of delayed time and the median. Considering the distribution of flights per day, most flights delayed less than 15 minutes, however, there are some extreme cases when flights delayed for a very long time. It was not outliers as it happens commonly at night everyday. These extreme cases will raise the mean as a whole. The median is more robust and better describe the overall picture than the mean. Here comes my first mistake. If I choose median, then I excluded all delay records passengers care about. Delay(>15mins) cases are not very common, it can not be reflect by median. The ratio is a good choice because it caught what passengers most care about and providing them the sure data on how likely they might delayed for more than 15mins.

The revise was that I changed the metric from mean, median to ratio and mean.

###### Problem 2

I used line to show the trends by date. But the line bunched togather and hard to distinct one from another. I changed the line to area format.

###### Problem 3

Added some information in the briefing.

###### Problem 4 

Changed the title to reflect the message I'd like to deliver.

###### Problem 5

Cancelled the automate animation.

### Resource

1. https://discussions.udacity.com/c/nd002-p6-data-visualization-with-d3-js
2. https://github.com/PMSI-AlignAlytics/dimple/wiki
3. http://dimplejs.org/advanced_examples_viewer.html?id=advanced_storyboard_control
