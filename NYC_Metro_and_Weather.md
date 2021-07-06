## Weather and New York City Subway Traffic

Matthew Rimol

---

### Abstract

The goal of this project was to perform exploratory data analysis on New York City Metro data and begin to understand how subway traffic is affected by weather. Using weather measurements collected from Central Park over a six month period from January 1 though June 30, 2016 I explored mainly how temperature affects subway traffic at different stations throughout the city. I scoped my analysis to explore a few stations that seemed to show some meaningful relationship with temperature. To visualize the data, I created charts plotting temperature and entries over the six month period.

---

### Data

Data provided from the New York City MTA was used to examine total entries per day for each different subway station. The weather data was originally collected by the National Weather Service and provided  temperature, precipitation, and snowfall, measured daily for the year 2016. I explored the time period from January 1, 2016 to June 30, 2016 in order to encompass multiple seasons.

After joining the two data sets on the primary key of date, I examined individual stations and how total entires varied with weather.  The analysis was scoped to weekend days only to try to capture more people in leisure activities and less commuters.

---

### Algorithms

**Data Cleaning**

- Scoped to time period 1/1/2016 through 6/30/2016
- Dropped unneeded columns
- Converted cumulative entires to daily entries for turnstiles, accounting for possible discrepancies
- Converted "T" in weather data (representing trace amounts of precipitation or snow) to small integer

**Aggregating into Data Frames to Explore**

- Grouped MTA data into daily entires per station on each day
- Merged weather data with MTA data using date as the primary key
- Filtered down data to just Saturdays and Sundays

**Exploration**

- Calculated some regression statistics to get a rough idea for what stations may be worth exploring first
- Explored temperature and entries as well the change in temperature and entires compared to one week prior (i.e. "last Saturday/Sunday")

**Visualization** (Matplotlib & Seaborn)

- Compared trends between daily entires and temperature as well as daily entries as a time series
- Explored how temperature and entries changed along the same time series
- Explored how significant changes in temperature impact entries

---

### Tools

- SQLite3 & SQLAlchemy - Data ingestion, initial exploratory queries
- Pandas - Data ingestion, data cleaning, analytics
- Numpy - Data manipulation
- Seaborn & Matplotlib - Visualizations

---

### Communication 

See presentation. Additionally, my Jupyter Notebook contains charts for other stations not in the presentation as well as algorithms to easily generate charts for any given station.