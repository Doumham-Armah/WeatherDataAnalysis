# WeatherDataAnalysis

I first used SQL on the workspace provided. I downloaded a csv file with only the data on Istanbul since that is where I live. I also downloaded all the data for the global temperatures. After that, I used pandas and opened these 2 csv files as 2 DataFrames. I ran the following SQL queries to get the csv files:
select * 
from global_data
For the global data

AND

select * 
from city_data
where city = 'Istanbul'
For Istanbul’s data

In addition, I used the method df.rolling() with a window size of 7 to calculate the moving average for each 7 data points at a time with df.rolling(7). This method calculates the moving average by taking 7 values at a time and sliding down by one for each new data point. I added the moving average for each DataFrame in a column called it MA.
Finally, I drew a line plot with x = 'year', y='MA' for each DataFrame. I also generated line plots before creating a moving average column to see the effect the moving average has on smoothing out the curve and showing the general trend. I added color='green' and linewidth=3 as parameters to the line plot to make sure the line is visible. I also added the correct x and y labels to each plot along with an appropriate title.



For Istanbul, the temperature ranges between 12.5 - 15 over the years while it ranges between 7 and 10 globally. Which means Istanbul is hotter than the rest of the world.
Right now, Istanbul is hotter than the rest of the world at 15 degrees while the world is at 9.5-10 degrees.
Both Istanbul and the world went through a drastic dip in temperature around the year 1820.
The spikes and dips in temperature are more dramatic in Istanbul when compared to the rest of the world especially after the year 1850.
Obviously both Istanbul and the world are getting hotter.
v
