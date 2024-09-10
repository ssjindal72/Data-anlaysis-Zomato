# Data Analysis of Zomato Dataset using SQL

## Project Overview

Zomato is an Indian multinational restaurant aggregator and food delivery company. This project aims to analyze a Zomato dataset containing over 9000 rows of restaurant data, including details such as `RestaurantID`, `Restaurant_name`, `City`, `Location`, `Cuisines`, and more. The goal is to gain insights into their business and restaurant trends by performing data exploration and analysis using SQL.

## Dataset Overview

The dataset consists of:
- **Number of Rows**: 9000+
- **Key Columns**: `RestaurantID`, `Restaurant_name`, `City`, `Location`, `Cuisines`, `Votes`, `Rating`, `CountryCode`, `Has_Table_booking`, `Has_Online_delivery`, etc.

## Steps Performed

### Data Exploration with SQL

1. **Checked Table Structure**
   - Retrieved all column names, data types, and constraints for the `ZomatoData1` table.
   
2. **Duplicate Value Check**
   - Checked for duplicate entries in the `[RestaurantID]` column.

3. **Data Cleaning**
   - Removed unwanted columns that were not useful for analysis.

4. **Table Merging**
   - Merged two tables (`ZomatoData1` and `ZOMATO_COUNTRY`) and added a new column `Country_Name` using `CountryCode` as the primary key.

5. **Correcting Misspelled Data**
   - Identified and corrected misspelled city names using the `REPLACE` function.

6. **Rolling Count**
   - Counted the number of restaurants using a rolling count/moving count with SQL window functions.

7. **Aggregated Data**
   - Calculated the `MIN`, `MAX`, and `AVG` for key columns like `Votes`, `Rating`, and `Currency`.

8. **Created New Rating Categories**
   - Added a `RATE_CATEGORY` column to classify restaurants based on their ratings.

### Data Insights and Analysis

After exploring the data, the following insights were discovered:

1. **Country Distribution**
   - **90.67%** of the dataset consists of restaurants listed in **India**, followed by **USA (4.45%)**.

2. **Online Delivery Availability**
   - Out of 15 countries, only 2 countries offer online delivery options:
     - **28.01%** of restaurants in **India**.
     - **46.67%** of restaurants in **UAE**.

3. **Indian Restaurant Analysis**
   - Since most of the data pertains to India, further analysis focused on Indian restaurants:
     - **Connaught Place (New Delhi)** has the highest number of listed restaurants (**122**), followed by **Rajouri Garden (99)** and **Shahdara (87)**.
     - The most popular cuisine in Connaught Place is **North Indian**.

4. **Table Booking Facility**
   - Only **54 out of 122 restaurants** in Connaught Place offer table booking facilities.
   - Restaurants with table booking facilities have an average rating of **3.9/5**, while those without have an average rating of **3.7/5**.

5. **Best Moderately Priced Restaurant**
   - The best moderately priced restaurant (with an average cost for two < 1000, rating > 4, votes > 4, and offering both table booking and online delivery) is **India Restaurant** in **Kolkata, India** (RestaurantID: **20747**), offering Indian cuisine.
