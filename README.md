# pandas-challenge

## Introduction
You've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

## Part 1: District Summary

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:
- Total number of unique schools
- Total students
- Total budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

## Part 2: School Summary

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:
- School name
- School type
- Total students
- Total school budget
- Per student budget
- Average math score
- Average reading score
- % passing math (the percentage of students who passed math)
- % passing reading (the percentage of students who passed reading)
- % overall passing (the percentage of students who passed math AND reading)

## Part 3: Highest and Lowest Scores 

Create dataframes Summarizing School Performance.

- Highest-Performing Schools (by % Overall Passing)
  - Sort the schools by % Overall Passing in descending order and display the top 5 rows.
- Lowest-Performing Schools (by % Overall Passing)
  - Sort the schools by % Overall Passing in ascending order and display the top 5 rows.
- Math Scores by Grade
  - Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level at each school.
- Reading Scores by Grade
  - Create a DataFrame that lists the average reading score for students of each grade level at each school.
- Scores by School Spending
  - Create a table that breaks down school performance based on average spending ranges (per student).
  - Use the code provided below to create four bins with reasonable cutoff values to group school spending.
```
spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
```
  - Include the following metrics in the table:
    - Average math score
    - Average reading score
    - % passing math (the percentage of students who passed math)
    - % passing reading (the percentage of students who passed reading)
    - % overall passing (the percentage of students who passed math AND reading)
- Scores by School Size
  - Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).
  - Use the following code to bin the per_school_summary
```
size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
```
- Scores by School Type
  - Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.



## Sources
I ran into some issues witht the formatting provided in the starter file as you can see it is commented out. 
The error was '<' not supported between instances of 'int' and 'str'. tried to convert the columns into a different datatype using the astype and pd.to_numeric functions but it didn't work
After removing the formatting and running the cells again the pd.cut function ran without errors so I left the formatting out since it wasn't included in the rubric
Wanted to shout out this week's tutor, Limei for helping me out with the groupby section of the code. She led me in the right direction and got me to complete a section in multiple ways. I removed the extra code we worked on. The only code she really gave me was:
```
school_type = school_data.set_index(['school_name'])['type']
```
# Thanks again!
