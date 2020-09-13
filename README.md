# Surfs_up

## Overview
In this challenge, we pulled data from an SQLite data base and created summary statistics comparing the month of June to the month of December.

### Analysis
Do this, we first imported the required dependencies including the numpy, datetime, pandas, and sqlalchemy dependencies. We then initiated an engine to alter the sqlite database into a structure that we could query. Then, we reflected the database and its tables into a new model and assigned the tables for "Measurement" and "Station" to two variables. To finish preparation to query the database we initiated a session from sql alchmey to link python and the database.

To query the SQLite database, we used the session object along with its query, filter, and extract methods to gather all temperatures from the Measurement table that were in a given month. Then, I used numpy's "ravel" function convert the gathered temperatures for a given month into a list which I then passed into a dataframe. Lastly, to get the summary statistics, I used the describe method on the newly created dataframe holding the monthly temperature values.

## Results
* Average temperature between the two months was only marginally different at 75 degrees for June and 71 degrees for December. 
* The minimum temperature in December was 56 degrees while in June it was 64 degrees.
* The max however was virtually the same between the two months, being 85 in June and 83 in December.


## Summary
One could be forgiven for expecting a starker average temperature difference between the months of June and December. However, given the tropical climate, it is not surprising that this is the case, and bodes well for the surf shop's prospects. Similarly, even colder winter months like December reach high up into the 80's throughout the year as demonstrated by the max recorded temperature and the average temperature. Furthermore, while it can get much colder in December on occassion than in June as evidenced by the disparities in the two months minimum temperature, it still only gets down to the temperature of 56 degrees, with the temperature being below 65 degrees only 25% of the time in even the coldest month.


### Conclusion
In conclusion, the data supports the notion that the surf shop will do just fine not just in the Summer but throughout virtually the entire year as far as temperature is concerned. 
