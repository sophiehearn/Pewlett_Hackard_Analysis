# Pewlett Hackard Upcoming Employee Retirement and Mentorship Analysis

## Overview

Pewlett Hackard has a significant number of employees who will soon reach retirement age. In order to better prepare, they have requested a summary of employees who are eligible for retirement based on age. The summary also includes the titles of those eligible for retirement to help with hiring of new employees. Lastly, in order to ease the hiring burden and fill positions from within, a file with employees eligible for mentorship was also created.  

## Results

* There are 72,458 positions filled by employees nearing or at retirement age.
* 7 different roles need to be filled: Senior Engineers, Senior Staff, Engineer, Staff, Technique Leader, Assisant Engineer, and Manager.
* The majority (over 50,000) of these positions are for Senior Engineers or Senior Staff.
* There are comparatively few roles for mentorship - only 1549 employees are eligible based on birth date. Many of these are already in senior positions, so may not significantly contribute to the hiring issue.

## Summary 

Pewlett Hackard will need to commit to hiring a significant number of new employees to begin to fill these upcoming vacancies. As it stands, the employee mentorship program has potential to help fill a small number of these positions. 
To help determine how many mentees will potentially fill these vacancies, we can run a quick count, similar to our `retiring_titles` table: 
```
SELECT COUNT (me.title), me.title
FROM mentorship_eligibility as me
GROUP BY me.title
ORDER BY COUNT (me.title) DESC
```
The resulting count is: 

![Mentee Count](https://github.com/sophiehearn/Pewlett_Hackard_Analysis/blob/main/Images/Mentee_count.jpg?raw=true)

We can see that some of the individuals eligible for mentorship are already in senior roles. These employees may benefit from mentorship in a different way, but won't help offset the senior employees who are leaving. The mentorship should likely focus on the 400 Engineers and 317 Staff who could potentially be promoted to Senior Engineers and Senior Staff. 

Pewlett Hackard ultimately still has a lot of senior and non-senior roles it will need to fill in the upcoming years. But with this analysis, they'll be better equipped to understand where they need to start recruiting.