# School District Analysis
Analysis of student funding and students standardized tests scores to make decisions regarding school budgets and priorities.We are using Python and Jupyter Notebook along with The Pandas Library. 
Deliverable 3 Instructions

For this part of the Challenge, write a report that summarizes your updated analysis and compares it with the results from the module.

The analysis should contain the following:

Overview of the school district analysis: 
Background
After the complete analysis of the school district student data,the grades of the ninth graders at Thomas High School have been changed. While administrators do not know the full extent of this academic integrity violation, they want to uphold the standards of state testing and have turned to us for help.After assessing the situation with the school superintendent and Maria, we decide the best approach is to:
Replace the ninth-grade math and reading scores from Thomas High School and Keep all other data associated with the ninth-grade students and Thomas High School intact.

Analysis is done in the Jupyter Notebook in the PyCitySchools_Challenge.ipynb file.

Objectives
The goals of this challenge are:
Filter DataFrames using logical operators.
Replace the incorrect values with NaN.
Explain how our PyCitySchools analysis changes after we handle the incorrect data.

Instructions
After creating a duplicate of PyCitySchools.ipynb and rename it PyCitySchools_Challenge_testing.ipynb; we corrected the students names so there are no professional prefixes or suffixes.
Also, replaced the reading and math scores for ninth graders at Thomas High School with NaN.
We used the pandas.DataFrame.loc to equate the math and reading scores of 9th graders from Thomas High School to np.nan.To use np.nan, we need to import Numpy.
Original District Summary DataFrame with the analysis in the module is as below:

![alt_text](https://github.com/RGK73/School_District_Analysis/blob/main/PNGs/Original%20Student%20Data.png)

After we replaced the reading and math scores for ninth graders at Thomas High School with NaN, DataFrame looks like as below:

![alt_text]("Clean Student Data_NaN.png")

After merging the clean student data with the school dataset and checking the column order for all the DataFrames and number formatting same as what was covered in this module, we started analysis on it.
After replacing the reading and math scores,and recreating the district and school summary DataFrames we have to analyse by answering the questions for each step.


Results: Using bulleted lists and images of DataFrames as support, address the following questions.

How is the district summary affected?
Before DATA Cleanup:
![alt_text]("Initial District Summary.png")
#Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
#79.0, 81.9, 75, 86, 65
After DATA Cleanup:
![alt_text]("District Summary After 9th grade NaN.png")
#Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing
#78.9, 81.9, 74.8, 85.7, 64.9
Observation: Slight downward change in district averages

How is the school summary affected?
Before DATA Cleanup: 
![alt_text]("original school listings by performance.png")
Thomas High School's % Overall Passing = 91, placing second
After DATA Cleanup: % Overall Passing = 65, placing eighth!
![alt_text]("Top Schools after NaN.png")
Observation: Overall ranking order change due to THOMAS HS, which slipped from second to eighth position.
How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

How does replacing the ninth-grade scores affect the following:
We have to analyse How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?
Before Cleanup:original math and reading scores were
![alt_text]("Math and Reading scores_original.png")
After Cleanup:
![alt_text]("Math and Reading scores after NaN.png")
Observation: It shows 9th grade column as NaN and rst of the grade scores remains the same.
After recalculating the high- and low-performing schools.Thomas High School ratinf clearly dropped from 2nd to 8th place.

Math and reading scores by grade
"%age passing" score is reduced as Total number of students (denominator) remains unchanged, but total passing value (numerator) is reduced by the number of removed 9th grade scores.
![alt_text]("top five schools_original.png")
![alt_text]("Top Schools after NaN.png")
![alt_text]("Bottom Five Schools.png")
![alt_text]("Bottom 5 Schools_NaN.png")
Thomas HS 9th grade math & reading scores set to "NaN"
Totals for passing math & reading across grades are reduced as all of 9th grade scores are equivalent to failing
Average scores calculation not significantly affected by removal of 9th grade scores, seems due to count() function NOT including 9th grade scores = nan
We cacluated number of students with a math grade
BEFORE cleanup: Thomas High School       1635
AFTER cleanup: Thomas High School       1174
![alt_text]("School Summary before academic integrity violation.png")
![alt_text]("School Summary After NaN.png")
From these two images, we conclude that there is hardly any effect on the scores for THS.

Scores by school spending
Thomas HS is in the spending bucket "$630-644"
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for spending bucket "$630-644" as follows
BEFORE: 73, 84, 63
![alt_text]
AFTER: 67, 77, 56
![alt_text]

Scores by school size
Thomas HS is in the "Medium (1000-2000)" size bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for size bucket "Medium (1000-2000)" as follows
BEFORE:94, 97, 91
![alt_text]
AFTER: 88, 91, 85
![alt_text]

Scores by school type
Thomas HS is in the "CHARTER" type bucket
Removing 9th grade scores reduces the "% Passing Math", "% Passing Reading" and "% Overall Passing" scores for type bucket "CHARTER" as follows
BEFORE:94, 97, 90
![alt_text]
AFTER: 90	93	87
![alt_text]

Summary: Summarize four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

