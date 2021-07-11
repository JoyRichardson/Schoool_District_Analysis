# An Analysis of School District
## Overview
Maria is the Chief Data Scientist who prepares standardized tast data for analysis, reporting and performance trends.  She is responsible for analyzing data of funding and standardized test scores.  After our original analysis was provided, the school board discovered that the orignal .csv file might have been altered. 
### Purpose
Initially, we were asked to aggregate the data and showcase trends and school performances for the School Board/Superintendent to use in setting school budgets and priorities.  Now, we have been asked to replace the math and reading scores for the ninth grade at Thomas High School with NaNs while keeping the rest of the data intact, then repeat our analysis and report on how these changes affected the overall analysis.  This included tables with the following metric(s):
* District summary
* School summary
* Top five (5) performing schools based on overall passing rates
* Bottom five (5) performing schools based on overall passing rates
* Average math scores and percentages by student in each grade at each school
* Average reading scores and percentages by student in each grade at each school
* School performance based on budget per student
* School performance based on school size
* School performance based on school type
## Resources
Data:  .csv files:  students_complete, schools_complete, clean_students_complete, missing_grades<br/>
Software(s):  Python 3.7, Jupyter Lab 3.0.14, Pandas, NumPy
## Results 
NOTE:  In each section, the first screenshot is the original analysis (Original) and the second is after removal of the ninth grade at Thomas High School (Amended).

* How is the district summary affected?<br/>
(Original)
![](District_Summary_before.PNG)
(Amended)
![](District_Summary_after.PNG)
As shown above, the average math score dropped 0.10, which effectively had no change in the analysis results for the district.

* How is the school summary affected?<br/>
(Original)
![](School_Summary_before.PNG)
(Amended)
![](School_Summary2_after.PNG)
As shown above, only the Thomas High School results were affected.  Although the average math and reading scores were minimally affected, all other statistics were greatly changed due to the effect of NaNs = 0 in the percentage calculations.

* How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?<br/>

  Originally, Thomas High School ranked second in the District due to its high Overall Passing % of 91.  With the replacement of the 9th grade scores with zeroes, the Overall  Passing % dropped to 65, dropping the school from second to eighth place in the District.
  
* How does replacing the ninth-grade scores affect the following:<br/>
  * Math and reading scores by grade<br/>
    (Amended - Math)<br/>
    ![](Math_by_Grade_after.PNG)<br/>
    (Amended - Reading)<br/>
    ![](Reading_by_Grade_after.PNG)<br/>
    As shown above, the only change for both the math and reading scores for the 9th grade at Thomas High School is the original scores are replaced with NaN = 0.
        
  * Scores by school spending<br/>
    Thomas High School is in the spending bucket of "$630-644" in both analyses.  Removing the 9th grade students' scores reduced the passing percentages by an insignificant amount.
     
  * Scores by school size<br/>
    Thomas High School is in the "Medium (1000 - 2000)" size in both analyses.  Removing the 9th grade students' scores reduced the passing percentages by an insignificant amount.
    
  * Scores by school type<br/>
    Thomas High School is in the "Charter" type in both analyses.  Removing the 9th grade students' scores reduced the passing percentages by an insignificant amount.

## Summary
We have summarized the following changes in the updated analysis after the reading and math scores for the ninth grade at Thomas High School were replaced with NaNs.<br/>
1)  There were no significant changes in the analysis results for the district.
2)  Although the average math and reading scores were not significantly impacted, the replacement of grades with zeroes made a significant change in the passing percentages for Thomas High School.
3)  Thomas High School dropped from second to eighth in performance ranking in the District.
4)  Thomas High School remained in the same categories for scores by school spending, scores by school size, and scores by school type with minimal change.

