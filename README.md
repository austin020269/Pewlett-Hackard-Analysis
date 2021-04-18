# Pewlett-Hackard-Analysis

Module 7 UT Data Analytics Bootcamp - Spring 2021

## Project Overview
We were provided ride and city data by PyBer, a ride sharing app company.  The ride-share data spanned a timeframe from January to early May 2019.  Our final projaect was to provide a ride sharing summary dataFrame by city type, a multiple-line chart of total fares for each city type and a final report documenting the work done.  During this study we also created various bubble charts and pie charts to gain familiarity with the data as shown below in our PyBer.ipnyb code (https://github.com/austin020269/PyBer_Analysis/blob/main/PyBer.ipynb) in Jupyter Notebook.

![alt text](https://github.com/austin020269/PyBer_Analysis/blob/main/analysis/code.PNG)
![alt text](https://github.com/austin020269/PyBer_Analysis/blob/main/analysis/Bubble.PNG)

![alt text](https://github.com/austin020269/PyBer_Analysis/blob/main/analysis/Pie.PNG)

## Resources
Data Sources provided to analyze and minipulate included:
- ride_data.csv - showing city, date, fare amount and the ride_id
- city_data.csv - showing city, driver_count and city type (urban, suburban or rural)

Software utilized for this study included: 
- Python 3.7.6 
- Conda 4.9.2 
- Jupyter Notebook 6.1.4
- GitHub account

## Analysis and Workflow
The following flow was generated in our PyBer_Challenge_starter_code_final.ipynb (https://github.com/austin020269/PyBer_Analysis/blob/main/PyBer_Challenge_starter_code_final.ipynb) Jupyter Notebook file.

The ride share data frame was created by:
- retrieving the total number of rides, the total number of drivers and the sum of the fares for each city type.
- calculating the average fare per ride and average fare per driver for each city type.

![alt text](https://github.com/austin020269/PyBer_Analysis/blob/main/analysis/dataframe.PNG)

The mullti-line chart showing total fares for each city type was created by:
- creating a new dataframe showing the sum of the fares for each date.
- resetting the index on the dataframe.
- creating a pivot table with the date as the index, the columns ='type', and values='fare' to get total fares for each city.
- creating dataframe from the pivot table. 
- setting the "date" index to datetime datatype.
- creating a new dataFrame by week 'W' and get the sum of the fares for each week.
- plot the new dataframe using the df.plot() function. 

![alt text](https://github.com/austin020269/PyBer_Analysis/blob/main/analysis/Fig8.png)


## Summary

Some observations we can make about the pyber_summary_df dataframe include:
- there are more rides in urban cities than suburban or rural cities
- there are more drivers in urban cities
- fares and fares per ride are more expensive in rural cities, probably due to the length of the ride
- fares per ride are cheaper in urban cities

Some observations we can make from the Total Fare by City Type chart include: 
- the overall trends for each city type are relatively similar.
- their data never interesect each other
- an overall upward jump in fares in each city type in mid-February
- an overall upward trend in each city type in January
