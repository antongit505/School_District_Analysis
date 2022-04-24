# School_District_Analysis

## Overview

A chief data sciencetist for a city school district who's responsible for analyzing information from a variety of sources and a variety of formats request our help<br />.
She's tasked with preparing  all standarized test data for analysis, reporting and presentation to provide insights about performance trends and patterns. These insights are used to inform discussions and strategic decisions at the school and district level. <br/>
We'll be helping Maria analyize data on student funding and students standarized test scores.
The tasks is to aggregate the data and showcase trends in school performance. This analysis will assist the school board and superintendent in making decisiones regarding the school budgets and priorities.

Two datasets were provided, the first one contains information about students and has 39,169 rows and the second one contains information of the schools and only has 15 rows.<br/>
We'll be using pandas library and jupyter notebook to perform this analysis, also we'll use the read_csv method to read the file as a DataFrame.

When we display the students dataframe the names were displayed with errors.<br/>
The student dataset needed to be cleaned because some names had prefixes and suffixes, like *["Dr. ", "Mr. ","Ms. ", "Mrs. ", "Miss ", " MD", " DDS", " DVM", " PhD"]* .  <br/>
For this task we use a For loop to iterate through the student's names and replace the prefixes and suffixes with nothing and the DataFrame is ready for analysis.

![](resources/extra_resources/read_csv.PNG)

A previous analysis was performed, but we received information from the school board that students from __9th grade__ at the __Thomas High School__ appear to have been altered, therefore, we'll run the analysis again not considering that part of the information.

We will replace the reading and math scores for 9th grade at Thomas High School with 'NaN' values, this task was performed using *.loc* property from pandas library and the *.nan* method from the numpy library.

![](resources/extra_resources/reading_math_nan.PNG)

To check if only 9th graders from Thomas High School were modified a comparisson was made as follows:

![](resources/extra_resources/nan_check.PNG)


## Results

As mentioned earlier, a previous analysis was performed and since some information was modified we'll analyze how this modifications affected the results obtained.

* __How is the district summary affected?__<br/>
    As we can see the district summary was barely affected, since the 461 students represent approximately 1% of the total of students from all high schools.<br/>

    ![](resources/extra_resources/district_summary_canvas.PNG)

    ![](resources/extra_resources/district_summary_challenge.PNG)

* __How is the school summary affected?__<br/>
    When the math and reading scores from 9th graders of Thomas High School were put as NaN the averages from math and reading barely changed, this could be because   these student's grades were closed to the mean (~83).<br/>
    On the other hand, a drastic change in percentages happens, this means that most of the 9th graders passed both subjects and when calculations were performed not considering them, the numbers dropped. 

    ![](resources/extra_resources/district_summary_canvas.PNG)

    ![](resources/extra_resources/district_summary_challenge.PNG)

* __How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?__<br/>
    When the calculations were performed again but not considering the quantity of 9th grade students from Thomas High School neither their scores, the school district summary showed numbers close to the original summary where we consider the quantity of 9th grade students from Thomas High School.

    ![](resources/extra_resources/school_summary_without_9th.PNG)    

* __How does replacing the ninth-grade scores affect the following:__ <br/>

    - __Math and reading scores by grade__<br/>
    Regarding the performance in math and reading by grade, we notice that for 9th grade there's no information and for the rest of the grades the scores remain the       same. The images from below shows on the left the original dataframe and in the right is the dataframe not considering the 9th grade students from Thomas High          School.
    With the new dataframe an evaluation in performance could not be made since we don't have enough information and it could lead to wrong decisions regarding priorities and affect other schools budgets.

    ![](resources/extra_resources/math_scores_canvas_challenge.PNG)
    > **Math Scores**

    ![](resources/extra_resources/reading_scores_canvas_challenge.PNG)
    > **Reading Scores**

    - __Scores by school spending__<br/>
    The amounts were affected by decimals but when rounding the changes are not significant since they don't affect the result.<br/>
    We can check this in the images below.

    ![](resources/extra_resources/scores_by_spending_canvas.PNG)
    > **Score by spending considering 9th THS**

    ![](resources/extra_resources/scores_by_spending_challenge.PNG)
    > **Score by spending not considering 9th THS**
    

    - __Scores by school size__<br/>
    This is the same case as the scores by school spending, there's no changes.

    ![](resources/extra_resources/scores_by_size_canvas.PNG)
    > **Score by size considering 9th THS**

    ![](resources/extra_resources/scores_by_size_challenge.PNG)
    > **Score by size not considering 9th THS**
    

    - __Scores by school type__<br/>
    There's no changes in scores by school type.

    ![](resources/extra_resources/scores_by_type_challenge.PNG)<br/>
    > **Score by type considering 9th THS**

    ![](resources/extra_resources/scores_by_type_challenge.PNG)<br/>
    > **Score by type not considering 9th THS**




## Summary

The changes for math and reading scores by grade, scores by school spending, scores by school size and scores by school type are not significant when comparing with the original information.<br/>
But with this information a decision regarding budget or priorities for schools wouldn't be accurate because there's still missing information of the real performance from the 9th grade students from THS. <br/>
The real information is needed to make decisions.





