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
Price Bucket =
SWITCH (
    TRUE (),
    Zomato[Avg Cost for Two (USD)] <= 10, "Low",
    Zomato[Avg Cost for Two (USD)] <= 30, "Medium",
    Zomato[Avg Cost for Two (USD)] <= 60, "High",
    "Premium"
)



