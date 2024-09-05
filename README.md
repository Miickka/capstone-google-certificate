# Google Data Analytics Professional Certificate Case study: How does a bike-share navigate speedy success?

### Introduction
Welcome to the Cyclistic bike-share analysis case study! In this case study, I am a junior data analyst working for a fictional company, Cyclistic, based in Chicago (USA). I was assigned with the question to answer: *How do annual members and casual riders use Cyclistic bikes differently?*

After downloading [the previous 12 months of data](https://divvy-tripdata.s3.amazonaws.com/index.html)*, I merged everything into a single .csv file containing more than **6 million rows**. In order to answer the business question, I've followed the data analysis process: *Ask, Prepare, Process, Analyze, Share, and Act*. I am working with using **Pandas (Python)** 

I had to produce a report with the following deliverables:

## 1. A clear statement of the business task
Identify how annual members and casual riders use differently the bikes provides by Ciclystic to have some insights about how to convince casual riders to become annual members. 

## 2. A description of all data sources used
The data used for analysis was initially located in a cloud, from which I downloaded Cyclistic’s trip records for the previous 12 months (July 2023 to July 2024) and stored them on my local computer. The data was organized by month in 13 separates .zip folders, which I extracted into .csv files and merged into a single file using a Python script with Pandas for easier analysis. To ensure the data’s credibility and integrity, I checked for missing values, duplicates, data type validation, consistency, referential integrity, statistical summaries, and anomalies. There were no duplicates, but some columns contained missing values, which will be dropped during the cleaning phase, and I had to convert several columns from object to string and datetime. Assessing data integrity was crucial in addressing potential biases and ensuring the data’s reliability. No anomalies or outliers were found, and privacy, security, licensing, and accessibility considerations were addressed.

## 3. Documentation of any cleaning or manipulation of data
To process the Cyclistic data, which included over 6 million rows from the past 12 months, I chose to use Pandas in Python because attempting to import the file into MySQL Workbench, Excel, or Google Sheets proved too cumbersome. Although R was an option, I opted for Python despite it not being covered in the Google Data Analytics Professional Certificate program, as it offered better handling of large datasets. To ensure data integrity, I followed standard steps and verified the dataset had no missing or duplicate entries. I cleaned the data by dropping unnecessary columns, creating a new 'ride_length' column by subtracting 'started_at' from 'ended_at' in HH:MM format, and adding 'Year' and 'Month' columns. Finally, I saved the cleaned dataset as a new .csv file and documented the entire cleaning process for future review and sharing.

## 4. A summary of your analysis
After cleaning the data and addressing issues such as negative ride lengths, unusually long rides, and zero-length rides, the clean dataset was saved for analysis. The analysis revealed that annual members accounted for 63.5% (4,113,411 rides) of all rides in the past 12 months, while casual riders made up 35.5% (2,369,932 rides). The average ride length was found to be 15 minutes, with casual members averaging 21 minutes per ride, exceeding the overall average, and annual members averaging 12 minutes. A seasonal trend was observed, with more rides in 2023 than in 2024 and a peak in July, followed by August and June, indicating that Cyclistic bikes are most used during the summer months. When examining usage by member type, it was found that casual riders' numbers tripled from winter to summer, preferring to ride on warm, sunny days, while annual members maintained consistent usage throughout the year, with slight peaks in winter. This suggests that annual members likely use the bikes for commuting, even in winter. The hypothesis that casual members ride more on weekends while annual members ride more during weekdays, especially on Tuesdays and Wednesdays, was confirmed, implying that annual members use the bikes for commuting, regardless of the season.

## 5. Supporting visualizations and key findings
Cyclistic Membership Trends: Key Findings (file attached)

## 6. Your recommendations based on your analysis
- Target Summer Users: Promote annual memberships during summer, when casual ridership triples. Highlight benefits like unlimited rides and savings during peak months.
- Seasonal Discounts: Provide summer discounts or"end of season" deals to entice casual riders to become annual members before the winter months.
- Weekend Membership Offers: Since casual riders are more active on weekends, create tailored membership options that emphasize weekend rides.
- Promote Year-Round Benefits: Market annual memberships as the best option for consistent commuters, even during winter. Emphasize the convenience of bike commutes in all weather.
- Loyalty Programs: Reward frequent casual riders with discounts on an annual membership after reaching a set number of rides.
- Email Campaigns: Target casual users with personalized promotions showing potential savings from switching to an annual plan based on their ride frequency.


*(Note: The datasets have a different name because Cyclistic is a fictional company. For the purposes of this case study, the datasets are appropriate and will enable you to answer the business questions. The data has been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement).) This is public data that you can use to explore how different customer types are using Cyclistic bikes. But note that data-privacy issues
prohibit you from using riders’ personally identifiable information. This means that you won’t be able to connect pass purchases to credit card numbers to determine if casual riders live in the Cyclistic service area or if they have purchased multiple single passes.
