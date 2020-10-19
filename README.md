# PyBer Analysis
 
## Overview
 
Using the Data provided by V. Isualize we created a ride sharing summary DataFrame organized by city type. Then utilizing the matplotlib library and the functions provided by matplotlib.pyplot we rendered charts and graphs to highlight and illustrate the data in a way that is easier to digest
 
## Results
 
### Dataframe based on city type:
 
![alt text](https://github.com/sebcampos/PyBer_Analysis/blob/master/analysis/PyBer_summary_df.png?raw=True)
 
 
### Line graph based on total fares by city type:
 
![alt text](https://github.com/sebcampos/PyBer_Analysis/blob/master/analysis/PyBer_fare_summary.png?raw=True)
 
 
When comparing the Rural, Suburban and Urban values we can see that Urban cities have the largest number of total rides, total drivers, and total fares followed by Suburban and finally Rural cities. But when we compare the average fare per ride and average fare per driver we see the opposite. Rural cities holding the highest values followed by Suburban and then Urban. This is due possibly to the logic that because the larger cities (Urban) have a larger amount of potential drivers only moving short distances within the city the average fare would be smaller. On the other hand a rural driver may be taking more trips to and from the suburban/urban areas covering more distance therefore accumulating a larger number of Average Fare per Driver and a larger number of Average Fare per Ride. 
 
 
 
## Summary
 
- If it is True that the average fare Rate per driver is larger  in Rural areas because the fares in this area tend to be higher it would make sense to include more drivers in these areas where we currently have the lowest amount of drivers. Pulling from the Suburban driver pool we could test this out by increasing the number of drivers and measuring the both the number and average of fares for this city type.
 
- The largest demand for rides appears to be in the Urban area by a large margin. Perhaps there is a larger demand than our current numbers are satisfying, to test this I would suggest pulling from the suburban to Urban and monitor for any significant fluctuations in total rides for urban fairs
 
- Perhaps rotating drivers and taking surveys from drivers we can collect more data either confirming or refuting these theories. Maybe a simple survey sent to their mobile devices would be quick and effective.
