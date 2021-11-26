# Pyber_Analysis
Module  5 Challenge

## Overview of Project

CEO V.Isualize requested that I assist Omar in providing analysis on all ride-sharing data broken down by three city types, urban, suburban, and rural.  The analysis will contain information regarding total number of fares, total drivers, and total dollar amount of fares per city type.  Also, the analysis will contain the average per ride fare and the average fare per driver per city type. 

### Purpose

The metric and visualizations pulled from this analysis will be the primary source of information that will be utilized to identify any disparities in results across the multiple city types with regard to financial performance of each city type.  This information will be used to provide recommendations to the CEO of Pyber, V. Isualize for improvements to address any disparity that may be encountered during this analasys.

## Results

Using Pandas and Matplotlib Omar and I were able to create a summary table and a multiline graph by pulling data from two files provided, city_data.csv and ride_data.csv.  We were able to use these data sets and the cities into three city types, urban, suburban, and rural.  Not only were we able to segregate the data into three city types but, were able to take the data for each city type and provide more granularity around the data by calculating the following:

*total number of fares 
*total drivers
*total dollar amount of fares per city type
*average per ride fare
*average fare per driver per city type

### Code Used To Pull Required Data For PyBer Analysis

To pull data required to perform this analysis we merged two files, city_data and ride_data into a single data frame. Then we created multiple series by using code to pull specific data we would need to run calculations to be used for the data summary. 

*Creation of multiple Series code to be assembled inside of a data frame.

![SeriesDataforDataFrame](Resources/SeriesDataforDataFrame.png)

*Assembling of Series data into a data frame that will be used for data analysis.

![SeriesDataFramepreFormat](Resources/SeriesDataFramepreFormat.PNG)

*Formating of dataframe data output.

![SeriesDataFramepreFormat](Resources/SeriesDataFramepreFormat.PNG)

*Resulting table created from dataframe creation

![PyberSummary_df](Resources/PyberSummary_df.png)


### Analysis of District Summary

Upon running the District Analysis between data sets that include all students' scores and an analysis with scores that did not include math and reading scores for ninth graders at Thomas High School, the following can be observed:

* The Average Math Score dropped by .1% for the district when Thomas High School ninth graders scores were not calculated.
* The % Passing Math dropped by .2% for the district when Thomas High School ninth graders scores were not calculated.
* The % Passing Reading dropped by .1% for the district when Thomas High School ninth graders scores were not calculated.
* The % Overall Passing dropped by .3% for the district when Thomas High School ninth graders scores were not calculated.
* Special Note: To be consistent with formatting, the original full data output was re-formatted to include to the tenth decimal place.
* Please see images below for full District Analysis between full data set and data set where Thomas High School scores were not calculated.
 
![DistrictSumAllSchools](Resources/DistrictSumAllSchools.png)
![DistrictSumNaN9thTHS](Resources/DistrictSumNaN9thTHS.png)

### Analysis of School Summary

When eliminating Thomas High School ninth grade math and reading scores, it has a big impact on Thomas High Schools % Overall Passing data point by dropping it to 65.1%.  This is understandable as the scores were removed but the calculations were done on the entire student body.  However, when the analysis was performed only taking into consideration Thomas High Schools 10th, 11th, and 12th grade students scores and the respective student population, the changes observed were minimal when compared to the entire district.  More specific information is provided below:
 
 * % Overall Passing for Thomas High School students, excluding 9th grade was 90.63% when compared to the 90.95% average when the analysis was run including the suspect 9th grade data. While the district's % Overall Passing score was 65.2%
 * % Passing Reading showed a decline of .29% for Thomas High School students when the suspect ninth grade scores were removed when compared to the original data set.  
 * Average Math Scores and % Pass Math each showed less than .1% decline for the 9th grade excluded data set compared to the original data set.
 * Average Reading Scores showed less than .1% improvement for the 9th grade excluded data set compared to the original data set.
 * Please see a scaled down school summary below

![THS_Summary10th12thlGrades](Resources/THS_Summary10th12thlGrades.png)
![THS_SummaryAllGrades](Resources/THS_SummaryAllGrades.png)

### Overall Summary of Impact of Thomas High School analysis with removal of 9th grade scores
The overall impact to the District Analysis and School Analysis with the removal of Thomas High School 9th grade from the entire data set is minimal.  With 39,170 students in the district, the removal of the Thomas High School 9th grade population, which is only 461 students, from the data set has minimal impact.  In fact, using standard formatting of extending the accuracy of the output to either zero or one significant digit yielded no change at all.  The formatting had to be extended to two significant digits before yielding any differenece at all.  Below are two screen shots that show comparison of data sets with standard formatting as recommended through the exercise and then with the extension of accuracy to two significant digits.

![FormattedSpending](Resources/FormattedSpending.png)

As you can see above, there is no difference in the formatted data set with the removal of the 9th grade Thomas High School population from the data set. One would have to go to the unformatted data set as seen below to identify slight differences in results when comparison the reduced student data set to the full student population data set.

![UnformattedSpending](Resources/UnformattedSpending.png)

The remainder of this report will be analyzing the district performance when broken down by factors such as spending, size of school and type of school.

### Analysis of School Spending
After dividing the per capita spend into four brackets, one could make the determination that the amount of money spent per student does not necessarily yield better performance when it comes to student scores. In fact, in cases where the per capita spent was less than $584 dollars, the schools performed better in every category than those schools that spent more per student.  On the other end of the spectrum, schools that spent the most on a per capita basis performed worse than those that spent less on each category.  See screen snippet below:

![schoolspend](Resources/schoolspend.PNG)

### Analysis of School Size

When doing an analysis on school size and its impact on test performance, the following can be interpreted:
* Medium schools with 1000 - 2000 students had the highest overall percentage for passing and percentage passing reading
* Small schools with less than 1000 students were on par with medium schools for Average Reading Score, percentage passing math, but exceeded medium schools in Average Math Scores.
* Schools with more than 2000 students trailed the schools with smaller population sizes in every metric listed.
* Please see image below for reference.

![schoolsize](Resources/schoolsize.PNG)

### Analysis of School Type

This analysis was also separated out by reading and math scores performance when compared to school types. The two types of schools that were analyzed were Charter and District schools.  Looking at the snippet below, one could interpret the results as Charter schools tend to outperform District Schools in each category.  Charter schools performed better than District schools when it came to Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, % Overall Passing.

![schooltype](Resources/schooltype.PNG)

### Summary

After Assigning NaNs to the 9th grade population at Thomas High School the District Summary displayed the following changes
* The average math score dropped by .1% for the data set assigning Thomas High School ninth grade scores to NaN
* The average reading score remained unchanged when compared to the data set assinging Thomas High School ninth grade scores to NaN
* % Passing math dropped by .2% for the data set assigning Thomas High School ninth grade scores to NaN
* % Passing reading dropped by .1% for the data set assigning Thomas High School ninth grade scores to NaN
* The % Overall Passing dropped by .3% from 65.2% to 64.9% after assigning Thomas High School ninth grade scores to NaN
* Special note, analysis noted above was pulled from reports that was set to one significant digit.
 
Unfortunately, due to academic dishonesty, we do not have a complete data set to properly evaluate all students, at all grade levels, at all schools. Although the student population removed was only 461 of 39,170 students.  This removal of data could impact decisions about where resources should be distributed and potentially cause further harm to the school(s) that could ultimately be impacted.  I would have been interesting to see how the schools compared if data had not to be excluded or removed.
