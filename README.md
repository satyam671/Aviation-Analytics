# Aviation Analytics: Elevating Airline Profitability Through Data-Driven Insights
![Aviation Thumbnail](https://github.com/user-attachments/assets/d9e5a2b8-a136-435f-b879-8a61c1f70169)
## Project Introduction

From runway to revenue, and turbulence to triumph, This project harnesses the power of big data analytics to transform underperforming flights. By navigating the currents of passenger demand and addressing key airline challenges, It aims to propel aviation success, chart new heights in occupancy rates, and elevate customer satisfaction.


Through this data-driven approach, It break through the clouds of uncertainty, paving the way for optimized airline operations and enhanced profitability. This repository showcases my work in leveraging advanced analytics to revolutionize airline performance.

Join me on this journey as we soar to new analytical heights in the aviation industry!

## Objectives

1. Boost Occupancy Rates:
Our primary goal is to increase the average profit per seat and improve overall occupancy. This strategy aims to mitigate current industry challenges and enhance airline profitability.

2. Refine Pricing Strategies:
We'll develop a dynamic pricing model that responds to evolving market conditions and changing consumer preferences. This approach seeks to attract new customers and retain existing ones in a competitive market.

3. Elevate Customer Experience:
From booking to arrival, we're focused on creating a seamless and enjoyable journey for our passengers. By enhancing the overall customer experience, we aim to differentiate ourselves in the market and foster customer loyalty.

4. Optimize Underperforming Routes:
Through data-driven analysis, we'll identify and address factors contributing to underperforming flights. By improving these routes, we aim to boost overall airline profitability and operational efficiency.

## Project Details
![slide_3](https://github.com/user-attachments/assets/568e624c-ffe8-4aea-8e06-a14621ecb14a)
### Data Sources and Technologies Used


This project utilizes a SQLite database containing comprehensive airline data. To analyze this data, I've leveraged several powerful Python libraries within a Jupyter Notebook environment:

- **sqlite3**: For establishing and managing the database connection
- **pandas**: For data manipulation and analysis
- **seaborn** and **matplotlib**: For creating insightful data visualizations
- **warnings**: For managing warning messages during the analysis process

### Methodology

1. **Database Connection and Data Extraction**

    Using sqlite3, I established a secure connection to the SQLite database. This allowed me to extract the necessary data for analysis.

```python
import pandas as pd
import sqlite3
# Connect to the database
connection = sqlite3.connect('travel.sqlite') 
cursor = connection.cursor()
cursor.execute("select name from sqlite_master where type='table';") 
```
2. **Data Exploration and Cleaning**

   With pandas, I performed initial data exploration to understand the structure and content of our dataset. This phase included:
   - Checking for missing values
   - Identifying and handling outliers
   - Ensuring data types are appropriate for analysis

```python
# Read data into a pandas DataFrame
aircrafts_data = pd.read_sql_query("select * from aircrafts_data", connection)
airports_data = pd.read_sql_query("select * from airports_data", connection)
boarding_passes = pd.read_sql_query("select * from boarding_passes", connection)
bookings = pd.read_sql_query("select * from bookings", connection)
flights = pd.read_sql_query("select * from flights", connection)
seats = pd.read_sql_query("select * from seats", connection)
ticket_flights = pd.read_sql_query("select * from ticket_flights", connection)
tickets = pd.read_sql_query("select * from tickets", connection)
```
3. **In-depth Data Analysis**

   Leveraging pandas' powerful data manipulation capabilities, I conducted various analyses to address our project objectives:
   - Analyzed occupancy rates across different routes and periods
   - Investigated pricing patterns and their impact on bookings
   - Explored factors influencing customer satisfaction

4. **Data Visualization**

   Using Seaborn and Matplotlib, I created a variety of visualizations to better understand and communicate our findings:
   - Heat maps to show occupancy rates across different routes and times
   - Line charts to visualize pricing trends
   - Bar charts to compare customer satisfaction across different factors

### Comprehensive Data Analysis and Insights

#### Basic Analysis:> Initial Insights: Understanding Aircraft and Revenue Trends

The core data analysis provides insights into several key areas: the number of aircraft with over 100 seats, the trends in ticket sales and revenue generation over time, and the average fare for each aircraft under different pricing scenarios. These insights will be instrumental in devising strategies to boost occupancy rates and refine pricing models for each aircraft. Table 1 presents the aircraft with more than 100 seats, along with their specific seat counts.
                                               
 ![table 1](https://github.com/user-attachments/assets/76b65adb-5109-4bdb-87f4-b84af8a44e11)

#### Visualization and Analysis:> Visual Trends: Ticket Reservations and Revenue

To better understand the trend in ticket reservations and the corresponding revenue, we used a line chart visualization. The chart reveals a steady increase in ticket purchases from June 22nd to July 7th, followed by a stable pattern from July 8th until August, with a notable peak on one day when the most tickets were sold. It's important to highlight that the company's revenue from these bookings is directly linked to the number of tickets sold. Consequently, the overall revenue trend mirrors the pattern of ticket purchases over the analyzed period. These findings indicate that further investigation into the factors behind the peak in ticket bookings could help boost overall revenue and optimize operational strategies.

![figure 1](https://github.com/user-attachments/assets/e2d795ef-7391-4098-b3cc-64c8ad6e6016)
                                                
![figure 2](https://github.com/user-attachments/assets/de2ef9bf-99e3-4b98-be66-2f0d34c6cbe7)

#### Expense Analysis:> Cost Comparisons: Ticket Pricing Across Classes

After calculating the typical expenses for various ticket conditions for each aircraft, we created a bar graph to visually compare the data. Figure 3 displays data for three fare categories: business, economy, and comfort. Notably, only the 773 aircraft offer the comfort class, whereas the CN1 and CR2 aircraft only offer the economy class. Across all aircraft, business class costs are consistently higher than those for economy class under various pricing scenarios. This trend is evident regardless of the fare conditions for each aircraft.
                                                
![figure 3](https://github.com/user-attachments/assets/61065575-af39-43c8-9b47-ecd172f2555e)

#### Occupancy Rate Analysis:> Seat Utilization: Assessing Occupancy Rates

To maximize profitability, airlines need a thorough analysis of their income streams. Key metrics to consider are each aircraft's average revenue per ticket and total annual income. This data helps airlines identify the most profitable aircraft types and routes, enabling them to adjust their operations accordingly. Additionally, this analysis can reveal opportunities for pricing optimization and resource allocation to more lucrative routes.

Figure 4 shows each aircraft's total income, total tickets sold, and average revenue per ticket. The aircraft with the highest overall income is the SU9, which also has the lowest prices for both business and economy classes, likely attracting more passengers due to its affordability. Conversely, the CN1 generates the lowest overall income, possibly due to offering only economy class at the lowest prices or having fewer amenities or subpar conditions.

Another crucial metric is the average occupancy per aircraft. This measure allows airlines to evaluate seat utilization and identify opportunities to increase occupancy rates. Higher occupancy rates can reduce operating costs associated with empty seats and boost revenue and profitability. Factors influencing occupancy rates include customer satisfaction, scheduling, and pricing policies. Figure 5 shows the average number of booked seats per aircraft. The occupancy rate is calculated by dividing the number of reserved seats by the total number of seats. A higher occupancy rate means more passengers have reserved seats on the flight.
                            
![figure 4](https://github.com/user-attachments/assets/36fa1748-421d-4384-a102-161d76e772a1)

#### Exploring the Benefits of Increasing Occupancy Rates:> Revenue Potential: Impact of Enhanced Occupancy Rates

To further investigate the potential benefits of improving occupancy rates, airlines can calculate the potential increase in annual revenue by raising the occupancy rate of each aircraft by 10%. This analysis can help determine whether boosting occupancy is a feasible strategy with a positive financial impact. By optimizing pricing strategies and operational factors, airlines can enhance occupancy rates and revenue while offering better value and service to customers. The figure below illustrates the increase in total income with a 10% rise in occupancy rates, showing that the growth will be gradual. Hence, airlines should focus more on effective pricing tactics.

### Key Insights and Findings

1. **Occupancy Rate Analysis**
   - Identified peak travel times with the highest occupancy rates
   - Discovered routes with consistently low occupancy, presenting opportunities for optimization

2. **Pricing Strategy Insights**
   - Found optimal price points that maximize both occupancy and revenue
   - Uncovered seasonal pricing trends that can inform future strategies

3. **Customer Experience Factors**
   - Identified key factors contributing to high customer satisfaction
   - Pinpointed areas for improvement in the customer journey

4. **Route Optimization Opportunities**
   - Discovered underperforming routes and analyzed contributing factors
   - Proposed data-driven strategies for improving these routes


### Conclusion

For airlines aiming to maximize profitability, it is essential to analyze revenue metrics such as total annual revenue, average revenue per ticket, and average occupancy per aircraft. By examining these metrics, airlines can pinpoint areas for improvement and adjust their pricing and route strategies accordingly. A higher occupancy rate is crucial for increasing profitability, allowing airlines to maximize revenue while minimizing the costs associated with empty seats. Pricing adjustments are necessary for aircraft where tickets are not being purchased due to either too low or too high prices. Airlines should set fair prices based on the aircraft’s condition and amenities, avoiding excessively low or high rates.

Moreover, improving occupancy rates should not compromise passenger safety or satisfaction. Airlines must balance the goal of increasing profits with providing high-quality service and adhering to safety regulations. Airlines can achieve long-term success in a highly competitive industry by adopting a data-driven approach to revenue analysis and optimization.

This project demonstrates the power of data analytics in driving airline profitability and enhancing customer satisfaction. By leveraging Python's data science libraries and SQL database connectivity, we've uncovered valuable insights that can directly inform business strategies.

### Future Work

Moving forward, potential areas for expansion include:
- Implementing machine learning models for predictive analytics
- Integrating real-time data for more dynamic insights
- Developing an interactive dashboard for ongoing monitoring and analysis

Through this work, we've shown how data-driven decision-making can elevate an airline's performance, charting a course for success in the competitive aviation industry.


