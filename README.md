# PyCitySchools

## Overview

The purpose of this analysis is to use python and pandas to do two things.  First, exclude the scores for the 9th grade at Thomas High School by replacing them with "Nan".  Then perform an in-depth analysis on the rest of the data that remains.

## D1: Removing THS 9th Grade Reading & Math Scores

In deliverable one, I used the pandas loc method to selectively edit the 9th grade Thomas High School reading and math school. All of these scores were changed to 'Nan' values, which effectively excludes them from all further calculations in the analysis.

## D2:  

In this section, we reanalyzed the following metrics after excluding the 9th-graders test results:

- The District summary
- The school summary
- The top 5 and bottom 5 performing schools, based on the overall passing rate
- The average reading score for each grade level from each school
- The average math score for each grade level from each school
- The scores by school spending per student, by school size and by school type

### The District summary
Recalculated total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then recalculated the passing math and passing reading percentages and overall passing percentage. new student total

Using the new student total and recalculated math, reading and overall passing percentage, I created a new data frame and formatted the values accordingly as seen below district_summary_df

### The school summary
Using the same methods from previous examples I created a data frame, including the data metrics: School Type, total students, total school budget, per student budget, average math score, average reading score, passing math percentage, passing reading percentage and overall passing percentage. I formatted the school budget and per student budget to include the dollar sign and set the values to show to the hundreds place. You can see the data in the following screenshot. School Summary table

The top 5 and bottom 5 performing schools, based on the overall passing rate
To find the top 5 and bottom 5 performing schools, I recalculated the passing math percentage, passing reading percentage and overall passing percentage of Thomas High School and entered the new data into the school summary data frame.

After calculating the total number of students in 10th, 11th and 12th grade I calculated the number of those students who passed math and reading.

- Total number of students in 10th - 12th grade: 1174
- Passing reading: 1094
- Passing math: 1139 total student
Next I calculated the percentage of 10th to 12th graders who passed reading, math and the overall passing percentage by excluding the 9th grades data as seen below calculate percentage of passing tests 10th - 12th

Next to calculate the top 5 and bottom 5 I replaced the new data from Thomas High School in the per_school_summary_df by using the loc function and used ascending=False.head(5) to find the top five schools and ascending=True.head(5) to find the bottom five schools. top 5 and bottom 5 school

The Average math score and reading for each grade level from each school
I calculated the average math and reading score for each grade level with the new total student count and by creating a series of scores by grade level. series of scores by grade level math scorers by grade level

### Results
How is the district summary affected

- Original Data to After data clean up: Average Math Score 79.0 to 78.9, Average Reading Score stayed the same, % Passing Math went from 75 to 74, % passing reading went from 86 to 85, % Overall Passing 64 to 65 

How is the school summary affected?

- Thomas High School overall passing percent went from 90.95% down to 65.08% after removing 9th grades testing results. Going from placing 2nd to 8th.

How does replacing the ninth graders math and reading scores affect Thomas 
High Schools performance relative to the other schools?

- Thomas High School % passing math went from 93.27% down to 66.91% and their % passing reading went from 97.31% (which was 2nd best among all other schools) down to 69.66% 

How does replacing the ninth-grade scores affect the following?

- Math and reading score by grade: Math grade for 9th graders went from 80.34% down to 80.12% and reading also decreased.

Scores by school spending: Thomas High school was in the $630 to $644 spending range and was one of four high schools in that range, their % passing math was higher then the average prior to omitting the 9th grade test results and so reduced the averages for schools in that range when the test results dropped from 90.95% down to 65.08%
Scores by school type: Thomas High school, as it is a charter school, negatively affected the passing math percentage and passing reading percentage

- % passing math went from 73% down to 67%
- % passing reading went from 84% down t 77%
- % overall went from 63% down to 56%
Scores by school size:
Thomas High School is in the 1000 to 2000 range
- % passing math went from 94% down to 88%
- % passing reading went from 97% down to 91%
- % overall went from 91% down to 85%

## Summary

After excluding all the the test scores from Thomas High School(THS) 9th grade, several metrics for THS were negatively affected. In particular their ranking for overall percentage of passing students dropped from 2nd best to 8th worst.  They also dragged down the ratings for charter schools in their size range.

