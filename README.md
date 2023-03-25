# An Analysis of NYC Citi Bike Rentals

## Overview
### Purpose and Background
Python and Tableau were used to create a "story" with data collected from Citi Bike rental stations around NYC boroughs (mainly Manhattan) in 2019. Viuailzations were made to help support an entrepreneurs pitch of a similar bike service in Des Moines.

### Method and Results
#### Deliverable 1: Import, Clean, Rearrange, Export with Python

After importing the published data into a Pandas dataframe in Python, I changed the datatype of the **tripduration** column from seconds (integer) to date and time (datetime). While converting a delta variable to a date and time is not visually useful in its raw form, it would manipulte the column to bin by hours and minutes in Tableau rather than having to create a complicated calculated field. I exported the data from Python after this was complete and uploaded it to Tableau.

#### Deliverable 2: Tableau Visualizations
##### Who Rides the Longest?
My first dashboard made use of the tripduration, gender, and count (of all rows) columns in the dataset. I created two linegraphs that display number of yearly rides based on ride time in minutes. One side shows total riders, and the ther is broken up by gender. It is filterable by length in hours, but not many people rode longer than 45 minutes in 2019. The legend also includes a gender filter and gender color key.

<p align="center">
  <img width=auto height=auto src=images/page1.png>
  </p>
  
- 146,752 checkouts occurred with a length of approximately 5 minutes in 2019, the most frequent ride duration that year.
- 108,087 of these checkouts were reportedly completed by men, while 33,041 were reportedly completed by women.

##### When Are Rides Most Frequent?
My second dashboard made use of the gender, usertype, starttime, and count (of all rows) columns in the dataset. I created three heatmaps that equate color intensity to trip frequency. One map has weekday and hour of starttime as its axes, one map is arranged by hour of starttime, weekday, and gender, and the final map utilizes usertype rather than hour of starttime. The maps are filterable by gender, and the legend also includes color keys for each map's color intensity-value comparison.

<p align="center">
  <img width=auto height=auto src=images/page2.png>
  </p>
  
- The greatest amount of checkouts occur at 6pm on Thursday, averaging 44,905 average rides for 2019.
- 30,749 of these checkouts were by men, and 11,336 by women.
- Male subscribers made up the largest demographic of riders on Thursdays, with a total of 259,316.

##### Where Are Most People Beginning Their Rides?
My third and final dashboard made use of the latitude, longitude, starttime, gender, and count (of all rows) columns in the dataset. I created two geographical maps of the greater NYC area. One map shows average trip frequency for each station, and the other shows the gender breakdown for each station per hour on average. The maps are both filterable by hour of the day with a handy slider in the legend (which can also play an automatic animation).The legend also includes color keys for user count and gender (different for each map).

<p align="center">
  <img width=auto height=auto src=images/page3.png>
  </p>
  
- 5pm at Pershing Square North station is when / where the highest number of checkouts occurred on average in 2019.
- Very few stations had more women than men renting bikes.
- The most rides occur in the heart of Manhattan in the afternoon and early evening.

#### Deliverable 3: Tableau Story
A Tableau Story was created using the three dashboards created for deliverable 2. The finished product is shown below:

[link to dashboard](https://public.tableau.com/app/profile/max.dorris/viz/NYC_Citi_Bikes_16796136311070/BIKERENTALSINNYC?publish=yes "Link to the Dashboards")

### Conclusion
While my visualizations turned out nicely and effectively tell us about the state of Citi Bike ride sharing in NYC in 2019, I am not sure that they tell the best story for our entrepreneur's objective. To better persuade investors, we will need to draw more comparisons between the two cities by relating the captured habits of New York users to potential users in Des Moines. This is virtually impossible with our current dataset, other than merely assuming that "of course a scaled down version of NYC's success could exist in other smaller cities." Projecting in this manner is obviously not the best approach to protecting the future of her startup, and I would suggest she research / compare Des Moines's incomes, commute distances, current public transportation routes, and remote worker concentration to that of New York City as well.