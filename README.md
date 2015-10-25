# Flight Delay Visual


##Summary
This visual provides some points: 

1) Airports in Northeast region has the  worst flight delay while airports in West region does the best, and le airports in Midwest and South region are in between correlated to their geographic locations. 

2) Nearly half of top 50 airports are located in two coast line  which is related to its geographic advantage.

3) The largest airport are inland not on coat line,  4 out of TOP 5: ATL, ORD, DFW,  DEN are inland.

Additionally, reader can also explore flight delay statistics for each of those airport  and check delay situation for each flight route departing from selected airport

##Design
 I chose flight dataset from http://stat-computing.org/dataexpo/2009/the-data.html. I downloaded dataset from 1999-2008, and finally picked year 2008 as my target dataset. I would like to reveal top 50 airport geographic distribution and the geographic  location impact to flight delay.  I thought about bar chart, line chart, pie chart, those charts could show the delay data like delay percentage between different airports simple and clearly but couldn't visualize the geographic location and delay relationship effectively.  Putting airports on a US map would make user to see the distribution and  discover relation between flight delay and geographic location in a glimpse. So I finally chose to draw a US map representation. Each circle represents a airport. The size of the circle represents the traffic of the airport(annual departure and arrival flights) .  A formula was invented to calculate flight delay index for each airport and their  connecting routes including following those factors: total number of flight, total number of arrival delay, total number of departure delay, delay time. Color of each airport circle, which is based on the normalized flight delay index, represents how good or bad the delay situation for that airport.  I had my first based on this design: version:  ://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V1.html
 
Based on feedback to version 1, I processed original dataset more to collect delay statics for  direct routes between top 50 airports.   I added code to interactively show the delay situation for flight routes departing from selected airport. It came my second major version: http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V2.html

Based on his feedback I created the third major version. I realized without a legend that some reader couldn't get the meaning of the circle size and color. And adding  brief description would also help reader to get the intension of the visual. So I added a brief description of the visual, and added legends to show relationship between size of circle and airport traffic(total number of flights) and relationship between color and delay situation. So here is version 3: http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V3.html

From the feedback from Teja and Review team after my first submission. I realized that I headed the wrong direct in my design. I missed the story here. I went back to Teja's suggestion,  I digged back to the data, and found I could use my visual to reveal the relationship between airport flight delay situation and its geographic location. I found that most airports in the West region are greenish, and all the airport on in Northeast are reddish. Airports in South and Midwest are yellowish. So that can be the story that I can tell here. So I modify the map to divide US into 4 Census Bureau-designated regions to show this relationship in verion 4: http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V4.html

To lead the reader to find out that airports in West region has best delay situation and Northeast does the worst easier,  animation was created to show airports in each region from West to East. And reader can select each region through a series of buttons. As bonus,  when reader move mouse on certain airport circle, fight delay statistics for the airport and departing route delay situation(displaying by the color of the route line) will pop up.  Here is version 5:
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V5.html

## Feedback 

###I. Feedback on version 1  
My son:
 The map looks amazing. There were lots of dots on two coasts and very few in the middle. 

My Wife:
1) I don't know that Atlanta is the biggest airport in US until I saw your map.

2) What does the color means here?

One of my colleague:

1) I can see the airports distribution clearly and I can bigger circle means bigger airport.

2) Does the color means the how good or bad the delay is in the airport?

3) I am not sure what else I can get out of it other than distribution and airport traffic

4) More interaction and more information about like flight route may be helpful? 
And I showed to one of my colleague, he liked overall, but he felt if the visual could have more user interaction to reveal more information like the flight route delay situation for each airport . 

###II. Feedback on version 2: 

I posted version two to class forum. Teja, one of the coach kindly gave me lots of very good feedback:

1) Are these the top 50 airports by air traffic?

2). Please mention if the color of each data point or arc represent a certain type of delay. A color scale would also be a useful addition. It is also unclear what the size of each data point circle represents. 

3) The details of the data points are hidden by the arcs between airports. You also might want to rethink the text color for this. One solution could be to display the airport details outside the map

4) Do the colors for the airports represent the same information as the flight delay index? Also, this seems to be a continuous color scale rather than just having the 3 colors displayed in the legend?

###III Feedback on version 3

I submitted the project to see where I could improve.Got more feedback after first submission of this project to UDACITY review team:

Currently, this chart is exploratory rather than explanatory. It's exploratory because the viewer is presented with all of the data, and the viewer can explore around and try to make conclusions about the data for himself. For this chart to be explanatory, you as chart maker need to tell a story about the data. You need to find something interesting and force the viewer to see what it was that you found interesting about the chart.

###IV Feedback on version 4
From one of my friends:

I can see more green dots on West side and more orange and red dot on North and East part but it took me a while to figure it out. I wish that I could have more leading clue.


## References:
http://bost.ocks.org/mike/map/

http://bost.ocks.org/mike/bubble-map/

https://github.com/mbostock/d3/wiki/Selections

https://www.dashingd3js.com/svg-basic-shapes-and-d3js

http://christophergandrud.github.io/d3Network/

http://bl.ocks.org/WilliamQLiu/76ae20060e19bf42d774

https://github.com/mbostock/d3/wiki/API-Reference

http://stackoverflow.com/questions/16421298/add-a-circle-to-a-d3-js-map

http://stackoverflow.com/questions/19993809/d3-js-plot-point-on-map

http://www.jeromecukier.net/blog/2011/08/11/d3-scales-and-color/

https://github.com/mbostock/d3/wiki/Ordinal-Scales

http://synthesis.sbecker.net/articles/2012/07/16/learning-d3-part-6-scales-colors

