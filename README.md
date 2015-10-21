# flightdelayvisual

This visual provides flight delay statics for top 50 airport in US. I choose flight dataset from http://stat-computing.org/dataexpo/2009/the-data.html. I downloaded dataset from 1999-2008, and finally picked year 2008 as my target dataset.  I would like to create a exploratory visualization for readers to see flight delay situation in airports and flight routes which can help them to plan their air travel. I selected 50 US airport by air traffic so that the visual is not too crowd on the US map. I processed the data set to calculate number of arrival, departure delays, arrival delay average, departure delay average for those airport and each direct routes connecting those airports. Based I those data, I created a formula to calculate flight delay index for each airport and their  connecting routes including all those factors. 

Here is my firsts version: http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V1.html, actually is my first version that I felt that I can show to public. I initially only want to show the delay situation for airports. I got my son,  my wife even my mother-in-law to be my first readers and gave me feedback. Here are some of their feedbacks:
1) The liked my US map presentation. They could intuitively tell that the bigger is the circle is, the bigger the airport is. And they also noticed that most of the top airport are distributed on two coast, especially east coast. 
2) They had some trouble to get what color represented until they moved the mouse over the some green one and red one and compare details. Then the realized that green is good and red is bad and yellow is in between.
3) They raised some minor issue about text size and format, nothing major.
And I showed to one of my colleague, he liked overall, but he felt that user case was not strong enough. He said if he was the traveler, he would like to see how likely that his flight will be delayed. So I came back to process original dataset more to collect delay statics for  direct routes between top 50 airports. And learned and tried many times,   finally, that I was able to interactively show the delay situation visually by the lines connecting from selected airport to all other top airports. It came my second major version: http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V2.html

I posted this version to class forum. Teja, on the coach kindly gave me lots of very good suggestions:
1) Are these the top 50 airports by air traffic?
2). Please mention if the color of each datapoint or arc represent a certain type of delay. A color scale would also be a useful addition. It is also unclear what the size of each datapoint circle represents. 
3) The details of the data points are hidden by the arcs between airports. You also might want to rethink the text color for this. One solution could be to display the airport details outside the map
4) Do the colors for the airports represent the same information as the flight delay index? Also, this seems to be a continuous color scale rather than just having the 3 colors displayed in the legend?
Based on his feedback I created the third major version, adding  brief description and legend and improved legend several times:
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V3.html

Got more feedback after first submission of this project to UDACITY review team: this visual is  more explorary than explanary, some story line is needed here. So I divided the US map into 4 regions: Northeast, South, MidWest and West. And I would like to tell the geographic impact to flight delay. Here is the the forth version:
http://tigerhead.github.io/flightdelayvisual/FlightDelayVisual_V4.html


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

