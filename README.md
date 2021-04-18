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
- pgAdmin 4 (Version 4.30)
- Visual Studio (Version 1.54.3)
- GitHub account

## Analysis/Workflow/Results
The final sql code was generated in our Employee_Database_challenge.sql file (https://github.com/austin020269/Pewlett-Hackard-Analysis/blob/main/Employee_Database_Challenge.sql) generated in pgAdmin and later saved in Visual Studio.

One of the initial spreadsheets created during this code was a query that: 
1. retrieved the emp_no, first_name, and last_name columns from the Employees table.
2. create a new table using the INTO clause.
3. joined both tables on the primary key
4. filtered the data on the birth_date column then ordered by the employee number
5. finally exported the file naming it retirement_titles.csv (seen below)

![alt text](https://github.com/austin020269/Pewlett-Hackard-Analysis/blob/main/retirement_titles.PNG)

Similar flows were utilized to produce the unique_titles.csv and retiring_titles.csv.

Our final code was used to produce the mentorship_eligibility.csv as per this flow:
1. retrieve the emp_no, first_name, last_name, and birth_date columns from the Employees table.
2. retrieve the from_date and to_date columns from the Department Employee table.
3. retrieve the title column from the Titles table.
4. retrieve the first occurrence of the employee number for each set of rows defined by the ON () clause.
5. create a new table using the INTO clause (this was the mentoer_eligibility.csv).
6. join the Employees and the Department Employee tables on the primary key.
7. join the Employees and the Titles tables on the primary key.
8. filter the data on the to_date column to get current employees whose birth dates are between January 1, 1965 and December 31, 1965.
9. order the table by the employee number.
10.export the Mentorship Eligibility table as mentorship_eligibilty.csv (seen below)

![alt text](https://github.com/austin020269/Pewlett-Hackard-Analysis/blob/main/mentorship_eligibility.PNG)

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
