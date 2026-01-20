## Zomato-Analysis-PowerBI
This project analyzes Zomato restaurant data using Power BI, focusing on data modeling, calendar table creation, DAX calculations, and KPI-driven dashboard development. The objective is to derive actionable business insights related to restaurant growth, pricing, ratings, and service availability.
## 🛠️ Tools & Technologies
- Power BI Desktop
- Power Query (ETL)
- DAX (Data Analysis Expressions)
- Data Modeling
- Interactive Dashboards
## 💰 Currency Conversion (USD)
Avg Cost for Two (USD) = DIVIDE ( Zomato[Average_Cost_for_two], Zomato[Exchange_Rate] )

📊 Key Measures (DAX)
## Total Restaurants
Total Restaurants = COUNTROWS ( Zomato )
## Restaurants by City & Country
Restaurants Count = COUNT ( Zomato[RestaurantID] )
## ⭐ Ratings Analysis
Restaurants by Rating = COUNT ( Zomato[Average_Rating] )
## 💵 Price Bucket Analysis
Price Bucket =SWITCH (TRUE (),

    Zomato[Avg Cost for Two (USD)] <= 10, "Low",
    
    Zomato[Avg Cost for Two (USD)] <= 30, "Medium",
    
    Zomato[Avg Cost for Two (USD)] <= 60, "High",
    
    "Premium"
)
## 📅 Restaurants Opened Over Time
Restaurants Opened = COUNT ( Zomato[RestaurantID] )
## 🍽️ Table Booking %
Table Booking % = DIVIDE (CALCULATE ( COUNT ( Zomato[RestaurantID] ), Zomato[Has_Table_booking] = "Yes") ,COUNT ( Zomato[RestaurantID]))
## 🚚 Online Delivery %
Online Delivery % =
DIVIDE (
    CALCULATE ( COUNT ( Zomato[RestaurantID] ), Zomato[Has_Online_delivery] = "Yes" ),
    COUNT ( Zomato[RestaurantID] )
)
## DASHBAORD
| ![PowerBI DB](https://github.com/user-attachments/assets/490e8e34-0ce1-4462-bb40-6201a5d0aa06)
## Conclusion
This project demonstrates strong capabilities in Power BI, DAX, data modeling, and business intelligence. It transforms raw Zomato data into meaningful KPIs and interactive dashboards that support data-driven decision-making.



