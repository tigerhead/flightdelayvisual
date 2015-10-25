# Flight Delay Visual

##Summary
This visual provides the distribution of top  50 US airports  in 4 Census Bureau-designated regions and an insight between flight delay in the airports  and their geographic locations, especial to its region: West, South, Midwest and East. From the visual, it is obvious that airports in Northeast region has the  worst flight delay while West region does the best. Additionally, reader can also explore flight delay statistics for each of those airport  and check delay situation for each flight route departing from selected airport.
##Design
 I choose flight dataset from http://stat-computing.org/dataexpo/2009/the-data.html. I downloaded dataset from 1999-2008, and finally picked year 2008 as my target dataset. I would like to reveal top 50 airport geographic distribution and the geographic  location impact to flight delay.  I thought about bar chart, line chart, pie chart, those charts could show the delay data like delay percentage between different airports simple and clearly but couldn't visualize the geographic location and delay relationship effectively.  Putting airports on a US map would make user to see the distribution and  discover relation between flight delay and geographic location in a glimpse. So I finally chose to draw a US map representation. Each circle represents a airport. The size of the circle represents the traffic of the airport(annual departure and arrival flights) .  A formula was invented to calculate flight delay index for each airport and their  connecting routes including following those factors: total number of flight, total number of arrival delay, total number of departure delay, delay time. Color of each airport circle, which is based on the normalized flight delay index, represents how good or bad the delay situation for that airport.  I had my first based on this design: version:  ://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V1.html
Based on feedback to version 1, I processed original dataset more to collect delay statics for  direct routes between top 50 airports.   I added code to interactively show the delay situation for flight routes departing from selected airport. It came my second major version: 
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V2.html
Based on his feedback I created the third major version. I realized without a legend that some reader couldn't get the meaning of the circle size and color. And adding  brief description would also help reader to get the intension of the visual. So I added a brief description of the visual, and added legends to show relationship between size of circle and airport traffic(total number of flights) and relationship between color and delay situation. So here is version 3: 
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V3.html
From the feedback from Teja and Review team after my first submission. I realized that I headed the wrong direct in my design. I missed the story here. I went back to Teja's suggestion,  I digged back to the data, and found I could use my visual to reveal the relationship between airport flight delay situation and its geographic location. I found that most airports in the West region are greenish, and all the airport on in Northeast are reddish. Airports in South and Midwest are yellowish. So that can be the story that I can tell here. So I modify the map to divide US into 4 Census Bureau-designated regions to show this relationship:
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V4.html

To lead the reader to find out that airports in West region has best delay situation and Northeast does the worst easier,  animation was created to show airports in each region from West to East. And reader can select each region through a series of buttons. As bonus,  when reader move mouse on certain airport circle, fight delay statistics for the airport and departing route delay situation(displaying by the color of the route line) will pop up.  Here is version 5:
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V5.html



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

