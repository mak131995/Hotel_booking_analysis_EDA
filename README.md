# Hotel_booking_analysis_EDA
# Objective
The objective of this project is to perform exploratory data analysis on a hotel booking dataset to gain insights into guest demographics, booking patterns, seasonality, and cancellations. The analysis aims to understand customer preferences, optimize revenue management, and improve marketing strategies for the hotel industry. By examining variables such as guest nationality, booking channels, lead time, and cancellation rates, the project seeks to provide actionable insights that can guide decision-making and enhance operational efficiency in the hotel booking process.

**Business Objectives :**

1. **Understanding Customer Preferences**: Gain insights into customer preferences, such as preferred room types, amenities, and booking channels, to tailor marketing strategies and enhance customer satisfaction.

2. **Optimizing Revenue Management**: Identify peak and off-peak seasons, length of stay patterns, and factors influencing cancellations to optimize pricing strategies, allocate resources effectively, and maximize revenue generation.

3. **Improving Operational Efficiency**: Identify areas for improvement in the booking process, such as reducing cancellations, streamlining check-in/check-out procedures, and optimizing staffing levels based on booking patterns.

4. **Enhancing Marketing Strategies**: Utilize customer demographic information, booking behavior, and seasonality trends to develop targeted marketing campaigns, promotions, and loyalty programs to attract new customers and retain existing ones.

5. **Identifying Market Trends**: Analyze market trends and competition by examining booking patterns, guest demographics, and customer preferences, to identify emerging trends, potential market opportunities, and areas for differentiation.

6. **Enhancing Customer Experience**: Gain insights into special requests, guest feedback, and preferences to improve overall customer experience, personalize services, and tailor offerings to meet specific customer needs.

7. **Mitigating Risks**: Identify potential risks and challenges in the booking process, such as high cancellation rates or seasonal fluctuations, and develop strategies to mitigate these risks through improved forecasting and operational planning.

8. **Data-Driven Decision Making**: Utilize data-driven insights from the analysis to guide strategic decision-making, enhance business planning, and support evidence-based decision-making across different departments within the hotel organization.

These business objectives aim to leverage the insights gained from the hotel booking analysis EDA to drive business growth, improve operational efficiency, enhance customer satisfaction, and gain a competitive edge in the hotel industry.

# Dataset 

**(1)- Hotel:** Type of hotel(City or Resort)

**(2)- is_cancelled:** If the booking was cancelled(1) or not(0)

**(3)- lead_time:** Number of days before the actual arrival of the guests

**(4)- arrival_date_year:** Year of arrival date

**(5)- arrival_date_month:** Month of arrival date

**(6)- arrival_date_week_number:** Week number of year for arrival date

**(7)- arrival_date_day_of_month:** Day of arrival date

**(8)- stays_in_weekend_nights:** Number of weekend nights(Saturday or Sunday) spent at the hotel by the guests.

**(9)- stays_in_weel_nights:** Number of weeknights(Monday to Friday) spent at the hotel by the guests.

**(10)- adults:** Number of adults among the guests

**(11)- children:** Number of children

**(12)- babies:** Number of babies

**(13)- meal:** Type of meal booked

**(14)- country:** country of the guests

**(15)-market_segment:** Designation of market segment

**(16)- distribution_channel:** Name of booking distribution channel

**(17)- is_repeated_guest:** If the booking was from a repeated guest(1) or not(0)

**(18)- previous_cancellation:** Number of previous bookings that were cancelled by the customer prior to the current booking

**(19)- previous_bookings_not_cancelled:** Number of previous bookins not cancelled by the customer prior to the current bookin

**(20)- reserved_room_type:** Code from room type reserved

**(21)- assigned_room_type:** Code of room type assigned

**(22)- booking_changes:** Number of changes made to the booking

**(23)- deposit_type:** Type of deposite made by the guest

**(24)- agent:** ID of travel agent who made the booking

**(25)- comapny:** ID of the company that made the booking

**(26)- days_in_waiting_list:** Number of the days the booking was in the waiting list

**(27)- customer_type:** Type of customer, assuming one of four categories

**(28)- adr:** Average daily rate

**(29)- required_car_parking_spaces:** Number of car parking spaces required bt the customer

**(30)- total_of_special_requesrs:** Number of special requests made by the customer

**(31)- reservation_statuse:** Reservation status(Canceled, check-out or no-show)

**(32)- reservation_status_date:** Date at which the last reservation status was updated
* Total number of rows in data: 119390
* Total number of columns: 32

# Data Cleaning and Feature Engineering Summary:

## 1. Duplicate Removal:
   - Action: Dropped all duplicate rows.

## 2. Handling Null Values:
   - Action: Replaced null values in columns 'company' and 'agent' with 0.
   - Action: Replaced null values in the 'country' column with 'others'.
   - Action: Replaced null values in the 'children' column with the mean of the column.

## 3. Data Type Conversion:
   - Action: Changed the data type of columns 'children', 'company', and 'agent' to int type.
   - Action: Changed the data type of the 'reservation_status_date' column to date type.

## 4. Outlier Removal:
   - Action: Identified one outlier in the 'adr' column and dropped it.

## 5. New Column Creation:
   - Action: Created a new column 'total_stay' by adding the 'stays_in_weekend_nights' and 'stays_in_week_nights' columns.
   - Action: Created a new column 'total_people' by adding the 'adults', 'children', and 'babies' columns.
# Exploratory Data Analysis:

Conducted Exploratory Data Analysis (EDA) and sought to address the following inquiries:

Q1) Who is the top booking agent based on the number of bookings?

Q2) Which room type is the most in demand, and which room type generates the highest average daily rate (ADR)?

Q3) What is the most preferred meal type among customers?

Q4) What percentage of bookings does each hotel receive?

Q5) Which channel is the most commonly used for booking hotels?

Q6) During which months are the hotels most busy?

Q7) Which country contributes the most guests to the hotels?

Q8) What is the average length of stay for guests at the hotels?

Q9) Which hotel appears to generate more revenue compared to others?

Q10) Which hotel has a higher lead time for bookings?

Q11) What is the preferred length of stay for guests in each hotel?

Q12) Which hotel has a higher booking cancellation rate?

Q13) Which hotel has a higher rate of returning customers for another stay?

Q14) Which channel is predominantly used for early hotel bookings?

Q15) Among the channels, which one has a longer average waiting time for bookings?

Q16) Which distribution channel brings better revenue-generating deals for hotels?

Q17) Among significant distribution channels, which one has the highest percentage of booking cancellations?

Q18) Does a longer waiting period or lead time lead to a higher cancellation rate for bookings?

Q19) Is not getting the same room type as demanded the main cause of booking cancellations?

Q20) Does not allotting the same room as demanded affect the average daily rate (ADR)?

Q21) What is the trend of bookings within a month?

Q22) Which types of customers are the primary contributors to hotel bookings?

Employed Matplotlib and Seaborn libraries for in-depth Exploratory Data Analysis (EDA) and utilized a diverse set of graphical representations, including:

*  Bar Plot: Visualized categorical data using bar plots.
* Histogram: Examined the distribution of numerical data through histograms.
* Scatter Plot: Investigated the relationship between two variables using scatter plots.
* Pie Chart: Represented proportions and relative sizes of categories using pie charts.
* Line Plot: Tracked trends and patterns over time using line plots.
* Heatmap: Visualized the correlation and intensity of numerical data with a heatmap.
* Box Plot: Identified the distribution, central tendency, and outliers in numerical data using box plots.

# Univariate Analysis Conclusions:

1. Booking Agent Analysis:
   - Conclusion: Agent no. 9 is the top performer, making the most bookings.

2. Room Type and ADR Analysis:
   - Conclusion 1: Room type A is the most demanded category.
   - Conclusion 2: Rooms H, G, and C have higher Average Daily Rate (ADR), suggesting potential for increased revenue. Hotels should consider expanding the availability of room types A and H to capitalize on this opportunity.

3. Meal Preference Analysis:
   - Conclusion: The majority of guests prefer the Bed and Breakfast (BB) meal type.

4. Hotel Distribution Analysis:
   - Conclusion: Approximately 60% of bookings are for City hotels, while 40% are for Resort hotels. As a result, City hotels experience higher activity compared to Resort hotels.

5. Booking Channels Analysis:
   - Conclusion: Guests use various channels for making bookings, with the most preferred being TA/TO (Travel Agency/Tour Operator).

6. Busiest and Profitable Months Analysis:
   - Conclusion: July and August are the peak months for both hotels in terms of bookings and profitability.

7. Guest Origin Analysis:
   - Conclusion: The majority of guests come from European countries, with Portugal being the highest contributor.

8. Preferred Stay Length Analysis:
   - Conclusion 1: The most common stay length is less than 4 days.
   - Conclusion 2: City hotels are favored for shorter stays, whereas Resort hotels are preferred for longer stays.

# Bivariate Analysis Conclusions:

1. Revenue Comparison:
   - Conclusion: City hotels have slightly higher Average Daily Rate (ADR) and more bookings than Resort hotels, resulting in higher revenue generation for City hotels.

2. Lead Time Analysis:
   - Conclusion 1: City hotels exhibit slightly higher median lead time than Resort hotels.
   - Conclusion 2: Both hotels generally experience significantly higher median lead time, indicating that customers plan their hotel visits well in advance.

3. Cancellation Rate:
   - Conclusion: Approximately 30% of City Hotel bookings are canceled.

4. Customer Retention Analysis:
   - Conclusion: Both hotels have a low percentage of customers who return for repeat stays, but Resort hotels show slightly higher repeat customer rates compared to City hotels.

5. Booking Channels:
   - Conclusion: TA/TO (Travel Agency/Tour Operator) is predominantly used for planning hotel visits well ahead of time.

6. Booking Confirmation Time:
   - Conclusion: While booking via TA/TO, customers may experience a slightly longer waiting time to confirm room bookings.

7. Revenue Generation by Channel:
   - Conclusion: The GDS (Global Distribution System) channel brings higher revenue-generating deals for City hotels. However, most bookings come via TA/TO. City hotels can focus on increasing their outreach on GDS channels to obtain more high-revenue deals.

8. Booking Cancellation by Channel:
   - Conclusion: TA/TO has the highest booking cancellation percentage, indicating that bookings made via TA/TO are 30% likely to be canceled.

9. Impact of Lead Time on Cancellations:
   - Conclusion: Longer lead time does not significantly affect the cancellation rate of bookings.

10. Room Demands and Cancellation:
    - Conclusion: Not getting the same room as demanded is not the primary cause of booking cancellations. A significant percentage of bookings are not canceled even after receiving a different room than requested.

11. Impact of Room Allocation on ADR:
    - Conclusion: Guests who did not get the same room as demanded tend to pay a slightly lower ADR.

12. Arrivals and ADR Variation:
    - Conclusion: Hotel arrivals increase on weekends, and the average ADR tends to rise towards the end of the month.

13. Booking Preferences:
    - Conclusion: Most bookings are made by couples, with two adults in the bookings.

# Summary of Conclusions:

1. Hotel Booking Distribution and ADR:
   - Approximately 60% of bookings are for City hotels, while 40% are for Resort hotels. City hotels are busier than Resort hotels. Additionally, the overall Average Daily Rate (ADR) of City hotels is slightly higher than Resort hotels.

2. Preferred Stay Length:
   - Most guests stay for less than 5 days in hotels. For longer stays, Resort hotels are preferred.

3. Booking Cancellation and Customer Retention:
   - Both hotels experience significantly higher booking cancellation rates. Only a small percentage (less than 3%) of guests return for another booking in City hotels, while 5% return for stays in Resort hotels.

4. Guest Origin:
   - The majority of guests come from European countries, with Portugal being the primary contributor.

5. Preferred Booking Channels:
   - Guests use different booking channels, with TA/TO being the most preferred method.

6. Revenue Generation and GDS Channel:
   - Hotels receive higher ADR deals via the GDS channel, suggesting a need to increase their popularity on this platform.

7. TA/TO Booking Cancellation:
   - Approximately 30% of bookings made via TA/TO are canceled.

8. Factors Affecting Booking Cancellations:
   - Not getting the same reserved room, longer lead time, and waiting time do not significantly impact booking cancellations. However, guests who receive different room allotments tend to have lower ADR.

9. Busiest and Profitable Months:
   - July and August are the busiest and most profitable months for both hotels.

10. Monthly ADR Trends:
    - ADR gradually increases towards the end of the month, with small sudden rises on weekends.

11. Preferred Guest Type:
    - Couples are the most common guests for hotels, suggesting that tailoring services to couples' needs can increase revenue.

12. Special Requests and Group Size:
    - More guests in a booking result in more special requests.

13. Booking Segments and Special Requests:
    - Bookings made via the complementary market segment and bookings with adults typically have a higher number of special requests.

14. Better Deals for Longer Stays:
    - Customers planning longer stays (more than 15 days) tend to get better deals in terms of lower ADR.

These conclusions highlight essential patterns and insights from the data analysis, offering valuable information for decision-making and potential areas of improvement for the hotels.

# Challenges Encountered:

1. Duplicate Data:
   - One of the primary challenges was dealing with a significant amount of duplicate data present in the dataset. Removing duplicates was essential to ensure data accuracy and prevent misleading analysis.

2. Data Type Format:
   - Another hurdle was the presence of data in incorrect data type formats. Correcting these formats and converting columns to appropriate data types were necessary for accurate analysis and visualization.

3. Visualization Techniques:
   - Selecting the most suitable visualization techniques was challenging. Ensuring that the chosen plots and graphs effectively represented the data and conveyed insights required careful consideration.

4. Handling Null Values:
   - The dataset contained a substantial number of null values, which posed challenges in data analysis. Deciding on appropriate strategies to handle these missing values, such as imputation or exclusion, was crucial for unbiased analysis.
