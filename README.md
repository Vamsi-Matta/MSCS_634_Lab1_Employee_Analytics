# MSCS_634_Lab1_Employee_Analytics
# Employee Performance Analytics Using Python

## Student Information

Name: Vamsi Matta  
Course: Advanced Big Data and Data Mining (MSCS-634)  
Assignment: Lab 1  

## Project Overview

This lab analyzes an employee performance dataset using Python in Jupyter Notebook. The goal is to explore how workforce-related information can be cleaned, visualized, summarized, and prepared for deeper analysis.

The lab focuses on practical data analysis activities such as viewing the dataset, creating charts, handling missing information, identifying abnormal salary values, reducing unnecessary data, scaling numerical fields, and generating statistical summaries.

## Dataset Description

The dataset contains employee information from multiple departments. The main fields include department, years of experience, training hours, completed projects, performance score, satisfaction level, and monthly salary.

This dataset was selected because employee analytics is a realistic business use case. Organizations often analyze this type of information to understand workforce performance, employee development, salary distribution, and operational trends.

## Lab Activities Completed

### Data Collection

The employee dataset was loaded into a Pandas DataFrame. The first few records were displayed to confirm that the file was imported correctly and that the column structure was readable.

### Data Visualization

Several visualizations were created to explore the dataset:

- A pie chart was used to show employee distribution by department.
- A line plot was used to compare performance scores across employees.
- A histogram was used to observe the salary distribution.
- A scatter plot was used to compare training hours with performance score.
- A box plot was used to visually inspect salary spread and possible outliers.

These visualizations helped reveal department representation, salary concentration, performance variation, and possible relationships between training and performance.

### Data Preprocessing

The dataset contained missing values in Training_Hours and Satisfaction_Level. These were handled using median and mean replacement methods. This allowed the dataset to remain complete without deleting useful employee records.

Outlier detection was performed on Monthly_Salary using the Interquartile Range method. One unusually high salary value was identified and removed to avoid distortion in salary-based analysis.

Data reduction was also applied by sampling the dataset and removing Employee_ID because it is only an identifier and does not provide analytical value.

Performance scores were scaled using Min-Max scaling, and monthly salary values were grouped into salary bands for easier interpretation.

### Statistical Analysis

The lab included general dataset exploration using info() and describe(). Central tendency measures were calculated for Performance_Score, including minimum, maximum, mean, median, and mode.

Dispersion measures were calculated for Monthly_Salary, including range, quartiles, IQR, variance, and standard deviation. A correlation matrix was also generated to compare relationships among numerical fields.

## Key Findings

- The dataset contains employees from multiple departments, allowing department-based workforce review.
- Performance scores vary across employees, showing differences in employee output.
- Training hours appear useful for comparing development effort with performance results.
- Monthly salary contained one unusually high value that was detected through the IQR method.
- Removing the salary outlier made the salary analysis more balanced.
- Scaling made performance scores easier to compare in normalized form.
- Salary bands made compensation easier to interpret at a summary level.
- Correlation analysis helped identify relationships among employee metrics.

## Challenges and Decisions

One challenge was choosing how to handle missing values without reducing the dataset size. Median replacement was used for Training_Hours because it is more stable when values vary. Mean replacement was used for Satisfaction_Level because it is a continuous rating field.

Another decision was how to handle the extreme salary value. Since it was far beyond the normal salary range, it was treated as an outlier and removed before final statistical analysis.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Visual Studio Code

## Conclusion

This lab demonstrates how Python can be used to perform the main stages of data analysis, including exploration, visualization, preprocessing, and statistical evaluation. The employee dataset showed how raw organizational data can be converted into useful insights through structured analysis.