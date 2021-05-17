# City Schools and Pandas
Continuing our work in Python, we will be utilizing tools within the Pandas library to better read CSV data and determine what story the data is telling with respect to school grades.

## Basis

With reports of academic dishonesty among ninth graders of Thomas High School, we are presented a problem of how to void the ninth graders’ scores without altering other high schoolers’ scores (“Module 4 Challenge”, 2021). Fortunately, via Pandas library tools, we can take out the dishonest scores from our analysis and still make findings on the other students’ scores.
## Part 1
Before we go ahead with replacing the ninth graders’ scores, we must meet a few prerequisites. Since we will be using the pandas library, we will **import pandas as pd** as well as install numpy for us to import and use later on (“Module 4 Challenge”, 2021). With that setup, we will be making good, frequent use of the Pandas **loc** method.

## Part 2
Since there are both reading and math scores in the data, we will focus on each set of scores at a time going forward. For instance, regarding ninth graders’ reading scores from Thomas High School, we can isolate and replace them with **loc** method, where we first specify in brackets the “grade” and “school_name” columns to match “9th” and “Thomas High School” respectively (“Module 4 Challenge”). In that same code, following a comma, we add a new column “reading_score” , close the bracket, and set the **loc** code expression equal to **np.nan**, allowing us to void the reading scores of Thomas High School’s ninth graders (“Module 4 Challenge”). We can do the same for math scores by simply specifying “math_score” instead of “reading_score” and setting “math_score” equal to **np.nan**. During this part of our work, we can use the **loc** method to pull up a DataFrame of our edited data by using a simpler version of our earlier working code that only has “grade” and “school_name” set for Thomas High School ninth graders (“Module 4 Challenge”). Once we check our **student_data_df** data, we can see that freshman scores for Thomas High School have been nullified, meaning we are one step closer to our school scores analysis.

## Part 3
Now that we have blotted out scores for Thomas High School freshmen, we will have to make some adjustments so that the scores are not counted in our student counts. One way we can do that is with the **loc** method to isolate data of Thomas High School freshman, but this time, we will assign the code a variable **thomas_freshman** so that we can apply the count() function in a manner similar our **student_count** variable to count all of the students (“Module 4 Challenge”, 2021). Afterwards, we subtract the Thomas High School freshman count from the total student count to arrive at a count of total academically honest students (“Module 4 Challenge”, 2021). With this new total, we can calculate new variables – **new_pass_math_percent**, **new_pass_reading_percent**, and **overall_new_passing** – to add into a new DataFrame **district_summary_df** (“Module 4 Challenge”). 

## Part 4
With our code framework in place, we can execute similar code to make our subsequent work a bit more efficient. As an example, to get the number of non-freshman students from Thomas High School, we can take our prior Thomas High School freshman code from Part 2 and then set “grade” *not* equal to “9th” using the **!=** syntax (“Module 4 Challenge”, 2021; “3.2.9”, 2021). To find students that pass math, reading, or both, we can adjust our column parameters accordingly inside the **loc** brackets and specify a score parameter to be at least 70 for passing (“Module 4 Challenge”). Afterwards, just as we did in Part 3, we can use variables like thomas_nonfreshman_math_count and apply count() to them to get the appropriate counts of non-freshman students from Thomas High School (“Module 4 Challenge”, 2021). With these particular counts having accounted for the voided freshman scores, we can calculate academically honest passing percentages of Thomas High School. To add these new percentages to our **per_school_summary_df** DataFrame, we use the **loc** method to specify the appropriate column and high school row names (“pandas.DataFrame.loc”, 2021) and – akin to what we did in Part 2 – set that intersection equal to the appropriate percentage (“Module 4 Challenge”, 2021). With that, we can turn our attention towards our school performance analysis.

## Part 5


## References

3.2.9 Membership and Logical Operators. (2021). Bootcamp Spot. Retrieved May 13, 2021, from https://
	courses.bootcampspot.com/courses/577/pages/3-dot-2-9-membership-and-logical-operators

4.9.1 Find the Highest-Performing Schools. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/pages/4-dot-9-1-find-the-highest-performing-schools

4.9.2 Find the Lowest-Performing Schools. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/pages/4-dot-9-2-find-the-lowest-performing-schools

4.10.1: Create Grade-Level DataFrames. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186366

4.10.2: Score Averages Grouped by School Name. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186367

4.10.3: Combine each grade level Series into a DataFrame. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186368

4.10.4: Format the Averages and Remove the Index Name. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186369

4.11.4: Create a DataFrame for the Scores by School Spending. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186375

4.12.4: Create a DataFrame for the Scores by School Size. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186381

4.13.2: Create a DataFrame for the Scores by School Type. Bootcamp Spot. Retrieved May 14, 2021, from https://	courses.bootcampspot.com/courses/577/modules/items/186385

Module 4 Challenge. (2021). Bootcamp Spot. Retrieved May 13, 2021, from https://	courses.bootcampspot.com/courses/577/assignments/11855

pandas.DataFrame.loc. (2021). the pandas development team. Retrieved May 13, 2021, from https://  pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html
