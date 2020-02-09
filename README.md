# School_District_Analysis
This repository contains data and programming regarding the school district project.  In this report, I will present a comparative analysis of major academic performance indicators, using data from all the schools and grades and then removing suspect scores from the 9th grade of Thomas High School, one of the charter schools. As the reader will note, the removal of these math and reading scores had a substantial impact at the school, school type level and at the school spending level.  The impact was not as great at the district level, given that many schools and grades are included in the district level data.
## Resources
- School and student level data was provided in a .csv file structure
- Pandas and Numpy dependencies were used to augment Python data analysis
- Jupyter Notebook was used to write and debug code.

# Findings
## District Summary
In examining the district summary data, there was a small negative effect of removing the 9th grade data of Thomas High School.  This is the first level when we begin to notice that the scores at that level were likely inflated--most likely the math scores were the major contributor to score inflation.
- Average Math Scores: moved from 79 to 78.9 (.1 point) as a result of this change.
- Average Reading Scores did not change
- % Passing Math moved from 75% to 74% (delta: 1 percentage point)
- % Passing Reading moved from 86% to 85% (1 percentage point)
- % Overall Passing moved from 65% to 64% (1 percentage point)

### Conclusion at District level
The 9th grade scores of Thomas High School support the assertion that score inflation occurred--while we cannot be certain the scores were tampered with, the data points to that possibilty

## School Level
At the school level, it makes sense to focus only on Thomas High, since the scores at other schools were not affected. When looking at average scores the impact was not as great as when looking at the % who passed math, reading and overall. Here is the summary:
- Average math at Thomas decreased from 83.42 to 83.35
- Average reading at Thomas slightly increased from 83.84 to 83.89 (less than .1 point)
- Average percent passing Math at Thomas greatly decreased from 93.3% to 66.9% (26.7 percentage points)
- Percent passing Reading at Thomas decreases from 97.3% to 69.7% (27.6 percentage points)
- Average percent overall passing both Math and Reading decreased from 90.9% to 65.1% (25.8 percentage points)
### Performance Rankings
As a result of the removal of suspect scores, Thomas High was no longer in the top 5 schools by performance, thus, we have further evidence of score inflation at the 9th grade level within Thomas High.

## Scores by Spending Level
When looking at the overall passing percentages by spending level, there is an effect at the per capita levels of $630-644, which may be an artifact of the spending level for Thomas High (at this same level).  With the removal of the 9th grade scores, the overall passing percentage decreased from 62.9% to 56.4% (6.5% decrease).

## Scores by School Type
There were two school types in the data set: District and Charter schools. Generally, the Charter schools demonstrated higher academic performance, even with the removal of the suspect 9th grade Thomas High scores.  Because Thomas was not a District school type, there would not be any expected effect on the district-type schools.  For the Charter, therefore, the changes were as follows:
- Average math scores declined from 83.47 to 83.46 (only very slight .1 point).
- Average reading scores were slightly higher: 83.89 compared to 83.9 (.1 point)
- % Passing math declined from 93.6 to 90.3 (3.3 percentage points)
- % Passing reading declined from 96.6% to 93.1% (3.5 percentage points)
- % Overall passing decreased from 90.4% to 87.2% (3.2 percentage points)

## Scores by School Size
An additional analysis was conducted by creating a new DataFrame to examine key performance indicators by school size.  For this, I used a similar procedure as used for per capita spending levels.  Examination of the data and experimentation of the most equitable categorization yielded four categories based on size.  The smallest school had 427 students and the largest 4,976 students.  I created four categories with the following bins: 0-1500 (3 schools, "small"), 1501-2840 (6 medium sized schools), 2841-4260 (3 large schools) and finally, 4261-4976 (3 very large schools). Removal of the 9th grade Thomas High scores did not affect performance.

However, it must be noted that there is a substantial difference in performance based on school size, with the large and very large schools show much lower performance on all key indicators.  Refer to the Jupyter Notebook section that presents the analysis by school size.
