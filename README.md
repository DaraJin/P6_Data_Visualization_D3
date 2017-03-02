
# Data Visualization for Flight Records

This [data set](http://stat-computing.org/dataexpo/2009/the-data.html) contains all flight records in 2008.[More details](https://www.transtats.bts.gov/Fields.asp?Table_ID=236)

## Summary

This chart shows the how flights delayed in 2008 by different timing and top 5 busiest carriers. The average delayed time is calculating total delayed time divided by total flights. Readers can click bars in the right to interact with the main chart. 

## Design

### What to show?

#### Carrier, Month, DayofMonth, Median of Daily Delayed Time, Mean Delayed Time per Month

The main plot of the story is about how the flight delays by time. I would like to present both a big picture and details to readers, thus I used two variables for time (i.e. Month, DayofMonth). I decided to use main chart to show how the day varies and a interactive bar chart on the right side of the screen to show the trends by month. line to indicate the trends. The filghts' identity were claimed by carriers as show on the left.

There were several statistics to choose from for Daily status. Ratio of delayed flights, mean of delayed time and the median. Considering the distribution of flights per day, the median is more robust and better describe the overall picture than the mean. Before conclusion, I drawed scatter plot and boxplot to see the distribution of a day. Result showed that there were lots of outliers that would raise the overall delay time if summarized by mean. In terms of ratio, it is less effective in explaining the whole picture. It's hard and less meaningful to draw a proper boundary of delayed and not-delayed. When choosing statistics for month status, mean works better since it contains all flights including extreme cases and reflect the data in a month as a whole. The different choices of day and month statistics result from the different distributions.

### How to show it?

The main plot is about day of month. I use line chart to show the trends. Flights from different carriers were identified by colors. The left chart is bar plot shows the mean of flight delay.

The bar plot also provide interactive function for readers to discover on their own. Readers can choose to see the time of interests such as holidays.

The animation helps reader to see the trends between month as the y-axis can strech and shrink by month. Readers can also pause it if it's annonying.

## Feedback

### Readers' Takeaways

1. There are peaks where carriers often delay during summer and winter.
2. From Dec 15- De 30, delays seems to be a common occurrence for majority of the airlines.
3. Southwest Airlines delayed a lot compared to others and US Airways did well in avoid delay. There're certain patterns on how the variable fluctuate.

### Problems & Suggestions

I collected feedbacks from 4 persons. Here are the key points:

1. For individual trends for airlines, a lot of the line are bunched together.
2. Can not see clearly which carrier did better than others and which worse. 
3. The whole picture is not clear as don't know the ratio of delayed flights. Why choose mean and median?
4. How is statistics calculated? 
5. Title doesn't reflect the plot of the story.
6. The automate animation is sometimes annoying.

### Revise

Problem 1, 2, 3: The median was used to be the observed statistics instead of mean and ratio, reasons are discussed above. 

Problem 4: Extra information was added in the chart below the main title.

Problem 5: Renamed the title.

Problem 6: The chart allows to pause the animation. No revise is made.

### Resource

1. https://discussions.udacity.com/c/nd002-p6-data-visualization-with-d3-js
2. https://github.com/PMSI-AlignAlytics/dimple/wiki
3. http://dimplejs.org/advanced_examples_viewer.html?id=advanced_storyboard_control
