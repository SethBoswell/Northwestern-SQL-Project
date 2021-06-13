# Pewlett-Hackard-Analysis
Project Folder for Pewlett-Hackard Analysis

## Overview of Analysis

### Background Context
Pewlett-Hackard (PH) is a large organization with thousands of employees, many of them on the verge of retirement. Unfortunately, the company's employee data was spread across six different CSV files, all containing various information on the employees' departments, birth dates, hire dates, salaries, titles, etc. Using Postgres and SQL queries, I helped Bobby, an HR analyst at Pewlett-Hackard, import the data into Postgres and establish links between the different CSV files using a variety of different joins. The objective was to create a list of employees who are elible for retirement. Included below is an image of this list. 

Because there was so many employees from this list, I helped Bobby provide a breakdown of the number of employees retiring from each department, which I have included below.


The department code corresponds to these departments:

In addition, I used SQL joins, filters, and conditional expressions to create a variety of tables that map out the employees that are eligible to retire from different departments (Sales and Development), a list of people in management and their corresponding employee information, as well as a list of general information about each employee in one table, including salary information.

### Challenge
Following the construction of the tables detailed above, I was finally tasked with two more assignments: determining the number of employees retiring for each employee title and identifying employees who are eligble for a "mentorship program" in which they will work part-time to help train new employees joining the company. To be considered eligible, an employee had to have been born 1965. Below, I will provide a bulleted list of four major results from the analysis and then provide a summary of how many roles will need to be filled as a result of employees retiring, as well as if there are enough employees eligible for the mentorship program to train these new hires.

## Results
Included below is an image of the number of employees retiring based on title:

I have three main points from this analysis:
- There are a total of 90,398 employees eligible for retirement. Since there are 300,024 total employees, this is approximately 30% of the workforce.
- The Senior titles, Senior Engineer and Senior Staff, comprise approximately 64% of all retirees, with Senior Engineers taking up 32.5% and Senior Staff taking up 31%. This suggests that hiring should focus on roles that will be able to fill in Engineering or general Staff roles, either at the senior level or entry level (and then promote current employees) to fill these voids. 
- Technique Leaders are only 5% of the employees eligible for retirement and there are only 2 managers retiring. This indicates that hiring should not be focused on bringing in new management or leaders to replace the retirees. 

Furthermore, below is an image of the list of employees who are eligible for the mentorship program:

The main point I have from this analyis is:
- There are only 1549 employees eligible for this program. If we wanted to replace all 90,398 employees, each mentor would have to teach a class of almost 60 new hires! 

## Summary
### Questions
1.) Based on the above analysis, there are 90,398 employees who are eligible for retirement. If the goal is to replace all of these employees to keep the company workforce at the same level, all 90,398 employees will need to be replaced by new hirers over the coming years.

2.) Since there are only 1,549 employees eligible for the mentorship program, each mentor would be required to mentor almost 60 new hires. Although the amount of training may vary by title, this seems like too many new hires for each mentor, so PH will likely have to come up with additonal training resources besides the mentorship program.
### Additional Analysis
Since we have a breakdown of the number of eligble retirees by title and discovered they are mainly Senior Engineers and Staff, I wanted to determine if the mentors mainly had these titles as well so they can mentor the new engineers and general staff members. I have included the results of this query below:

As you can see, there are 724 employees considered to be either Senior Staff or Staff, which accounts for 47% of the mentors. There are also 748 employees considered to either be a Senior Engineer, Engineer, or Assistant Engineer that could help train the new engineers. This accounts for 48% of the mentors. Thankfull, because a large proportion of the mentors have roles that are suitable to provide instruction to the new hirers, the vast majority of the mentors will be able to be used as a resource.


The final table I created by querying PH's employees database sums the salaries of all retirees across the different titles. See below for the results:


The table shows that the total estimated cost savings is: 22,814,009,389. Senior Engineers account for 32.5% of these cost savings, followed by Senior Staff at 31%. This suggests that, although it may be a bad thing that so many Senior Staff and Engineers are leaving the company, PH will also see significant cost savings as a result of lower salaries costs from highly-payed employees leave for retirement. 



