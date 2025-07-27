Uber Fares Dataset Analysis using Power BI
Overview
This project aims to analyze Uber ride fare data to uncover useful business insights using Python for data preparation and Power BI Desktop for data modeling and visualization.

Deliverables
Interactive Power BI Dashboard (

.pbix file) 

Project Report (this deck) 

Cleaned CSV dataset (

uber_features.csv) 

GitHub Repository 

Screenshots of key analyses and the dashboard 

Dataset
The dataset used for this analysis is the Uber Fares Dataset sourced from Kaggle.

Key Fields 

fare_amount

pickup_datetime

pickup_longitude

pickup_latitude

dropoff_longitude

dropoff_latitude

passenger_count

trip_distance_km (engineered feature)

Methodology
Data Understanding (Initial EDA) 

Initial Exploratory Data Analysis (EDA) involved:

Checking the data structure, data types, unique values, and missingness.

Calculating summary statistics (mean, median, standard deviation, IQR) for 

fare_amount and distance.

Identifying outliers and invalid coordinates.

Data Cleaning (Python / Jupyter) 

The following data cleaning steps were performed using Python in a Jupyter environment:

Removed or filtered impossible fares (e.g., negative, zero, or extremely high values).

Removed coordinates outside valid NYC bounds (if applicable).

Handled missing values by dropping or imputing them.

Feature Engineering 

New features were created from the pickup_datetime field:


hour 


day 


month 


weekday 

The enhanced dataset was then saved as a cleaned CSV file for import into Power BI.

Export to CSV 

The final cleaned and engineered DataFrame was exported to 

uber_features.csv.

Power BI – Data Import and Visualization 

The 

uber_features.csv file was imported into Power BI Desktop. Various visualizations were created to explore the data:


Fare Distribution: Histograms to inspect central tendency and skewness, and box plots to detect outliers.

Time-based Trends:

Average fare by hour (line chart).

Ride volume by hour, day, and month.

Day of week comparison (weekday vs. weekend rides/fare).


Fare vs. Distance (Correlation): A scatter plot of fare_amount vs. trip_distance_km to show correlation. This indicated a strong positive correlation, with potential heteroscedasticity at longer distances.



Busiest Periods Identification: Identified hours and months with the highest number of rides to segment peak vs. off-peak periods.

Dashboard Design & Interactivity 

The Power BI dashboard was designed with the following principles:


Clear Layout: KPIs positioned at the top, trends and distributions in the center, and filters at the bottom.


Slicers: Included slicers for month, weekday, and hour for interactive filtering.


Consistent Formatting: Applied a consistent theme, colors, and fonts.

Insights / Results 

Most Uber rides fall within the $5–$15 range, with some outliers exceeding $50.

The fare distribution is right-skewed, with a median fare around $8–$10.

Ride demand peaks during morning (6–9 AM) and evening (4–7 PM) commuting hours, and on weekends, especially Fridays and Saturdays.

Average fares increase late at night, possibly due to longer rides or surge pricing.

Monthly patterns indicate seasonal demand variations. Based on the provided image, 

April and May appear to have the highest ride volume. 

A strong positive correlation exists between fare and distance, meaning longer trips generally result in higher fares, though fare variability increases with distance.

Recommendations 

Based on the analysis, the following recommendations are proposed:

Implement dynamic or surge pricing during identified peak hours (6–9 AM, 4–7 PM) and on weekends.

Offer discounts or loyalty rewards during off-peak periods to help balance demand throughout the day.

Continuously monitor outlier fares and anomalies to maintain high data quality and accuracy.

Explore integrating external factors such as weather data and special event information for even deeper insights into ride demand and pricing strategies.


Conclusion 

The Power BI dashboard effectively visualizes fare distribution, time-based trends, and the relationship between fare and distance. These insights are valuable for informed decision-making regarding pricing strategies and operational optimizations.


