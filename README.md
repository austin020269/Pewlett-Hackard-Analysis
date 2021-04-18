# Pewlett-Hackard-Analysis

Module 7 - University of Texas Data Analytics Bootcamp - Spring/Summer 2021

## Project Overview
Pewlett-Hackard asked us to analyze their current employees for retirmenet eligibility.  This was done by generating a database of company information that showed the entity-relationships between the various data sources as follows.

![alt text](https://github.com/austin020269/Pewlett-Hackard-Analysis/blob/main/EmployeeDB.png)

## Resources
Pewlett - Hackard provided us with six data spreadsheets summarizing personnel employment and department information according to the  following:
- departments.csv - identifying the department code for each department
- dept_manager.csv - identifying the depertment code for each employee and their start and end dates.
- employees.csv - identifying the employee number, first and last names, birth date, gender and hire date.
- salaries.csv - identifying the employee number and his/her salary and their start and end dates.
- titles.csv - identifying the employee number, their title and their start and end dates.
- dept_emp.csv - identifying the employee number, the department code they work in, and their start and end dates.

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
