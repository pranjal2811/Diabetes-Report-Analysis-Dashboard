# Diabetes-Report-Analysis-Dashboard
Hello, folks! My name is Pranjal Joshi, and I am delighted to present my project. This project involved a comprehensive analysis of a diabetes dataset, providing valuable insights into various health indicators and their relationship with diabetes outcomes.

# Project Overview
The core of this project was to analyze patient health data to identify patterns and contributing factors related to diabetes. The primary goal was to understand key metrics such as BMI, glucose levels, and their distribution across different age groups and outcome categories (diabetic/non-diabetic). This interactive dashboard serves as a vital tool for exploring health trends and potential risk indicators.

# Objectives
This project was developed with several key objectives to provide a comprehensive analysis of the diabetes dataset:

Assess Core Health Metrics: To understand average health indicators by calculating and displaying key metrics like Average BMI and Average Glucose levels across the dataset.

Categorize BMI Status: To classify individuals into distinct BMI categories (Underweight, Healthy, Overweight, Obese) to facilitate a segmented analysis of health status.

Quantify Diabetic Prevalence: To determine the proportion of diabetic individuals by calculating the Diabetic Count, NonDiabetic Count, and the overall Diabetic Percentage, along with the Total Records in the dataset.

Analyze Outcome Distribution: To visualize the distribution of diabetic and non-diabetic outcomes, providing an immediate understanding of prevalence.

Explore Health Trends over Pregnancies: To investigate the relationship between the number of pregnancies, health outcomes, and average blood pressure, identifying potential correlations.

Examine Age and BMI Impact on Outcome: To understand how different age ranges and BMI categories correlate with diabetes outcomes, identifying specific demographic and physical risk groups.

Enable Granular Filtering: To allow for dynamic filtering of data based on diet type, family history, and age categories, enabling targeted investigations into specific cohorts.

# Implementation Steps
I utilized Power BI Desktop for data loading, DAX calculations, and dashboard visualization. As the dataset comprised only one table (diabetes_dataset), no complex data modeling was required.

Data Loading and Preparation:

The diabetes_dataset was loaded into Power BI.

A calculated column named 'Age range' was created using bins to group individuals into meaningful age categories for analysis.

DAX Measure and Calculated Column Creation:
The following crucial DAX measures and the calculated column were created for dynamic analysis and categorization:

Average BMI = AVERAGE(diabetes_dataset[BMI])

Purpose: Calculates the average Body Mass Index across all individuals in the dataset.

Average Glucose = AVERAGE(diabetes_dataset[Glucose])

Purpose: Calculates the average glucose level across all individuals.

BMI Category = SWITCH(TRUE(), 'diabetes_dataset'[BMI] < 18.5, "Underweight", 'diabetes_dataset'[BMI] < 25, "Healthy", 'diabetes_dataset'[BMI] < 30, "Overweight", "Obese")

Purpose: This calculated column categorizes each individual's BMI into predefined health classifications based on standard ranges.

Diabetic % = DIVIDE([Diabetic Count], [Total Records])

Purpose: Calculates the percentage of individuals diagnosed with diabetes relative to the total number of records.

Diabetic Count = CALCULATE(COUNTROWS(diabetes_dataset), FILTER(diabetes_dataset, diabetes_dataset[Outcome] = 1))

Purpose: Counts the number of individuals where the Outcome column indicates a diabetic diagnosis (Outcome = 1).

NonDiabetic Count = CALCULATE(COUNTROWS(diabetes_dataset), FILTER(diabetes_dataset, Diabetes_dataset[Outcome] = 0))

Purpose: Counts the number of individuals where the Outcome column indicates a non-diabetic diagnosis (Outcome = 0).

Total Records = COUNTROWS(diabetes_dataset)

Purpose: Calculates the total number of records or individuals in the dataset.

Dashboard Visualizations:

KPI Cards: Display key summary metrics such as Total Records (1485), Diabetic % (1.00%), Average BMI (27), and Average Glucose (104.42), providing an immediate overview of the dataset's characteristics.

Donut Chart: Diabetic Count and NonDiabetic Count visually represents the proportion of diabetic versus non-diabetic individuals in the dataset, clearly showing the 1K (100%) distribution.

Line Chart: Count of Outcome and Average of Blood Pressure by Pregnancies plots the count of outcomes and average blood pressure against the number of pregnancies, enabling the identification of trends.

Bar Chart: Count of Age range by BMI Category and Outcome shows the distribution of individuals across different BMI categories within various age ranges, segmented by outcome. This chart provides insights into risk groups, with 'Overweight' and 'Obese' categories often having higher counts.

Interactive Filters: Slicers for Diet Type, Family History, and age categories allow users to dynamically filter the dashboard and explore specific demographic and lifestyle segments.

# Results and Conclusion
The Diabetes Report Analysis Dashboard provides a comprehensive and interactive view of the dataset:

Overall Health Overview: The dashboard quickly communicates key averages, showing an Average BMI of 27 and Average Glucose of 104.42. With 1485 Total Records, it reveals a Diabetic % of 1.00% (likely representing the proportion of records marked as diabetic, given the visual of 1K records).

Outcome Distribution: The visual representation of Diabetic Count and NonDiabetic Count clearly delineates the spread of outcomes within the dataset.

Risk Factor Insights: The analysis by Pregnancies and Blood Pressure highlights potential correlations between these factors and outcomes.

Targeted Risk Group Identification: The Count of Age range by BMI Category and Outcome chart is crucial for identifying specific age and BMI groups that are more prone to diabetes, such as individuals in the 'Overweight' and 'Obese' categories, which show higher counts (e.g., over 400 for 'Overweight'). This can inform targeted health interventions.

Custom Categorization: The 'Age range' calculated column and BMI Category measure effectively segment the data, enabling more granular and insightful analysis that would not be possible with raw data.

This project demonstrates proficiency in data analysis, DAX formula creation, and dashboard design using Power BI to transform health data into meaningful and easily digestible insights for understanding diabetes prevalence and risk factors.

# Tools and Technologies Used
Power BI Desktop: Core tool for dashboard development, data loading, calculated column creation, DAX measure implementation, and visualization.

DAX (Data Analysis Expressions): Utilized extensively for creating calculated measures (Average BMI, Average Glucose, Diabetic %, Diabetic Count, NonDiabetic Count, Total Records) and the BMI Category calculated column.

# Contact Information
Name: Pranjal Joshi 

GitHub: https://github.com/pranjal2811 

LinkedIn: https://www.linkedin.com/in/pranjaljoshi2811 

Email: pranjaljoshi2811@gmail.com 
