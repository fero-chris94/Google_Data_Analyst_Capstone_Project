# Google_Data_Analyst_Capstone_Project
This repository contains the code and analysis for the Google Data Analyst Capstone Project. The project focuses on analyzing the usage patterns and behaviors of Cyclistic's annual members and casual riders in order to develop targeted marketing strategies to increase the conversion of casual riders into annual members.
## Project Objective
The objective of this project is to analyze the usage patterns and behaviors of Cyclistic's annual members and casual riders to identify any differences that can inform the development of targeted marketing strategies. The primary goal is to increase the conversion of casual riders into annual members in order to maximize the long-term growth and profitability of Cyclistic's bike-share program. Key stakeholders include Cyclistic's management team, finance analysts, annual members, casual riders, and the marketing analyst team. Success will be measured by the percentage of casual riders who convert to annual members and the effectiveness of the targeted marketing strategies in achieving this goal.

## Data Summary
Location and Organization of Data
The data used for this project is located on an AWS server and is easily downloadable. The data is organized by year and fiscal quarters and is stored in CSV files with the following file names:

- Divvy_Trips_2019_Q2
- Divvy_Trips_2019_Q3
- Divvy_Trips_2019_Q4
- Divvy_Trips_2020_Q1

The data includes columns such as trip_id, start_time, end_time, bikeid, tripduration, from_station_id, from_station_name, to_station_id, to_station_name, usertype, gender, and birthyear. It provides information about all the rides recorded on the Cyclistic bike-share program.

### Issues with Bias or Credibility
There do not appear to be any issues with bias or credibility in the data, as it comes from the company that manages the City of Chicago’s Cyclistic Bike Share program. The data is reliable, original, comprehensive, and current. However, the data does have some limitations due to data privacy issues that prohibit the use of personally identifiable information.

### Licensing, Privacy, Security, and Accessibility
The data is made accessible to the public by the City of Chicago, and all identifying information has been removed from the data to protect privacy. The data is stored in CSV files that are updated on a monthly basis, and the license governing the distribution of this data is available at https://ride.divvybikes.com/data-license-agreement.

### Verifying Data Integrity
The data is collected by Motivate, Inc., the corporation that manages the City of Chicago’s Cyclistic Bike Share program, and is published on a monthly basis. The data provided in this project has been downloaded directly from an AWS server, ensuring that the data was not altered during the transfer process.

### Answering the Business Question
The data helps answer questions related to the usage of the Cyclistic Bike Share program, such as how different types of riders use the program and where the most popular stations are located.

### Problems with the DataSet
There are some discrepancies in the structure of the dataframe, such as duplicate records and missing fields, that can be solved by data cleaning. Additionally, some values are missing from the data, which have been eliminated from the analysis. There are also some limitations due to data privacy issues that prohibit the use of personally identifiable information. Finally, there are some issues with the data, such as inconsistencies in the rideable type field and difficulties in mapping popular stations due to the use of latitude/longitude coordinates.

## Process and Clean
The project uses RStudio Desktop as the primary tool for data analysis, cleaning, summarization, and visualization. The necessary R packages, including tidyverse, skimr, lubridate, janitor, scales, and mapview, are loaded to perform various tasks.

The data is collected by reading CSV files for each quarter into separate data frames. The column names are checked for uniformity across all files, and any necessary renaming is performed to ensure uniformity.

The data wrangling process involves inspecting the data frames for any missing values, duplicate records, or other irregularities. Data types of certain variables are converted to ensure proper analysis. The four data sets are then combined into a single data frame.

Data cleaning steps include removing empty columns and rows, cleaning variable names, transforming data types, and removing unnecessary columns. The "member_casual" column is updated to replace "Subscriber" with "member" and "Customer" with "casual" for consistency.

Additional columns are added to the data frame to represent the date, month, day, and year of each ride, allowing for aggregation of ride data based on these factors.

To ensure data integrity, the data frame is inspected using the glimpse() function, and summary statistics are evaluated using the summary() function. Further modifications are made to remove unnecessary columns and transform the "ride_length" column from a factor to a numeric data type.

Finally, the cleaned data is saved as a CSV file and an RDS file for further analysis and visualization.

## Analysis and Visualisation
The project includes several analyses and visualizations to explore the data and answer the business questions. Here are some of the key analyses and visualizations performed:

- Time Analysis: Analyzing the number of trips, mean trip duration, and total trip duration by ride type and start hour. Visualizations include bar charts showing the number of trips per hour, average trip duration per hour, and total trip duration per hour, segmented by user type.
- Analysis of Days of the Week: Analyzing the number of trips, average trip duration, and total trip duration by day of the week and user type. Visualizations include bar charts showing the number of trips per day of the week, average trip duration per day of the week, and total trip duration per day of the week, segmented by user type.
- Analysis of Trip Time by Month: Analyzing the number of trips, average trip duration, and total trip duration by month and user type. Visualizations include bar charts showing the number of trips per month, average trip duration per month, and total trip duration per month, segmented by user type.
- Visualization of Most Popular Start and End Stations: Identifying and visualizing the most popular start and end stations, segmented by user type.

## Conclusions
Based on the analysis performed, the following conclusions can be drawn:

- Users with membership take more rides throughout the week compared to casual users.
- Casual users tend to take longer rides, indicating higher trip durations.
- Both casual and member users have peak usage during the 2nd and 3rd quarters of the year, coinciding with the favorable summer weather.
- Users with membership have higher usage during the weekdays, while casual users have higher usage during the weekends.
- The most popular station, especially for casual users, is Streeter Dr & Grand Ave.

## Recommendations
Based on the analysis and findings, the following recommendations are suggested:

- Implement rewards or incentives for users with memberships who take longer rides to encourage casual riders taking longer rides to convert to memberships.
- Offer discounts or promotions for members taking rides during the summer and weekends to encourage casual users to register for memberships.
- Target marketing campaigns at the Streeter Dr & Grand Ave station and related routes, as it has the highest trip volume for casual users.

Please refer to the Jupyter file provided in this repository forthe detailed code and visualizations generated during the analysis. The Jupyter file provides step-by-step explanations of the data cleaning process, data wrangling, and various analyses conducted. The visualizations help illustrate the patterns and trends discovered in the data.

Additionally, the repository includes a CSV file (cyclistic_data.csv) and an RDS file (cyclistics_data.rds) that contain the cleaned data, which can be used for further analysis or visualization in other software tools such as Excel, Tableau, or presentation software.

Feel free to explore the code, analysis, and visualizations in the Jupyter file to gain a deeper understanding of the project and its findings.
