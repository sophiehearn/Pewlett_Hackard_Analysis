# Pewlett Hackard Upcoming Employee Retirement and Mentorship Analysis

## Overview

Pewlett Hackard has a significant number of employees who will soon reach retirement age. In order to better prepare, they have requested a summary of employees who are eligible for retirement based on age. The summary also includes the titles of those eligible for retirement to help with hiring of new employees. Lastly, in order to ease the hiring burden and fill positions from within, a file with employees eligible for mentorship was also created.  

## Results

* There are 72,458 positions filled by employees nearing or at retirement age.
* 7 different roles need to be filled: Senior Engineers, Senior Staff, Engineer, Staff, Technique Leader, Assisant Engineer, and Manager.
* The majority (over 50,000) of these positions are for Senior Engineers or Senior Staff.
* There are comparatively few roles for mentoship - only 1549 employees are eligible based on birth date.

## Summary 

Pewlett Hackard will need to commit to hiring a significant number of new employees to begin to fill these upcoming vacancies. As it stands, the employee mentorship program has potential to help fill a small number of these positions. 
To help determine how many mentees will potentially fill these vacancies, we can run a quick count, similar to our `retiring_titles` table: 
```
SELECT COUNT (me.title), me.title
FROM mentorship_eligibility as me
GROUP BY me.title
ORDER BY COUNT (me.title) DESC
```
The result is: 
We can see that the 