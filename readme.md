# Airline on-time performance
## by Ha Nguyen


## Dataset

The dataset consitst of 7009724 unique records about flights in the United States in 2008, including date of flight, actual and scheduled arrival time, carriers, 
airport code, arrival and departure delays time, and reasons for delays. 4 duplicated records have been removed and one new atribute - 
Date in the full format yyyy-MM-DD has been created. The five reasons in seperated columns have been transformed to 2 new atributes: Reason and Time.
The interest variable I would like to look at is ArrDelay which stands for arrival delay time. 
The dataset can be found [here](https://community.amstat.org/jointscsg-section/dataexpo/dataexpo2009),
with feature documentation available [here](https://www.transtats.bts.gov/nosessionvar.asp).


## Summary of Findings

In the exploration, I found that there wasn't any strong relationship between numeric variables, so I look into the trend of delay time in qualitative
variables. 
Although total time of 5 reasons is equal to the arrival delay time, the correlation between them was not strong. The reason might be there are many records
that didn't have value in any reason, and especially WeatherDelay and SecurityDelay, most of the point is 0. Of the 5 reasons, CarrierDelay, NASDelay and 
LateAircraftDelay are the reasons with longest delay time and WeatherDelay and SecurityDelay are the reasons that rarely happended and also had short delay 
time.
For the pattern across time, I found that in the first half of the year, the delay time was quite stable, it decreased in the last 3 months and suddenly 
increased in the end of the year. There was also clearly pattern in the scheduled arrival time, the delay time is the shortest for the flight arrived from 
7 A.M. to 10 A.M. then gradually increase and become the longest in the midnight scheduled flights.
In multivariate exploration section, I looked more deeply in the relationship between delay time that has been seperated by 5 reasons and other categorical 
features and the same pattern as above was found, CarrierDelay, NASDelay and LateAircraftDelay are most often happened reasons for all carriers. But there 
was one exceptional case, OH which had WeatherDelay as the most often reason. The trend across time stay unchange for the 3 most often reason while 
SecurityDelay and WeatherDelay is quite stable by time. And finally with scheduled arrival time, while LateAircraftDelay happended more in the early and late 
flights, NASDelay and CarrierDelay have the opposite pattern, which happened more in middle of the day.

## Key Insights for Presentation

For the presentation, I focus on just the arrival delay time seperated by five reason of Delay: CarrierDelay, WeatherDelay, NASDelay, SecurityDelay, 
LateAircraftDelay. I start by introducing the distribution of total arrival delay time, followed by the pattern in each reason distribution, then use bar
plot to see the comparison of delay time by reason.

Afterwards, I use multivariate plot to introduce pattern of delay time by reason and other category features. To start,
I use the cluster bar plots of reason and delay time across unique carriers. I don't look at the airport because the number of unique value is too large
and there is not any interesting finding. Next, the pattern of delay time by reason across month is demonstrated by a line plot and the relationship between
delay time by reason and scheduled arrival time is plotted by cluster bar plot. For the three multivariate plot, I have to specify the color palette with
category order to make sure that the color of each reason is stay the same across different plots.
