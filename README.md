# Hospitality Analysis Dashboard

## Overview  
AtliQ Grand is a chain of five-star hotels operating across india for 20 years. Due to increasing competition and ineffective decision making the company has been loosing market share and revenue in luxury/business hotel segment. To overcome this the interactive Power BI dashboard is created that analyze key business metrics such as revenue, booking, occupancy rate, Average daily rate and ratings by customers across cities and properties. It also track weekly performance to uncover trends, monitor room utilization and evaluate booking platform effectiveness helping to improve business and make strategic decisions.

---

## Tools & Technologies  

| Category | Tools Used |
|-----------|-------------|
| **Visualization** | Power BI |
| **Data Transformation** | Power Query Editor |
| **Calculations** | DAX (Data Analysis Expressions) |

---

## Dataset
The dataset consists of multiple CSV files, including bookings, hotels, rooms, and dates, which provide detailed information on reservation data, room categories, and guest details for analysis.
Firstly, Data loaded into Power BI from excel files and the validated. Then established a relationship between tables and created key metrics using DAX

---

## Key DAX Measures  
- **Total Revenue** = SUM(fact_bookings[revenue_realized]) 
- **Total Bookings** = COUNT(fact_bookings[booking_id]) 
- **Occupancy Rate** = DIVIDE([Total Successful Booking], [Total Capacity], 0)
- **Cancellation Rate** = DIVIDE([Total Cancelled Bookings], [Total Bookings], 0)
- **Realisation %** = 1 - ([Cancellation Rate] + [No Show Rate %])

---

## Dashboard Design  
**Tool:** Power BI  

### Key Visuals:  
- KPI Cards – Total Revenue, Revenue Loss, RevPAR, Total Booking, Cancellation Rate
- Donut Chart – Occupancy % by day type
- Bar Charts – Revenue Analysis by month, city, property, room category
- Line Chart - Trends by Weeks 
![Hospitality_Domain_Dashboard](/Hospitality%20Analysis.pdf)

---

## Results & Insights
- **Overall Performance:** Total bookings stand at 135K, generating ₹1,708.8M in revenue, with an overall occupancy rate of 57.87% and an average guest rating of 3.6, stating moderate performance with room for improvement in guest experience.  
- **Revenue Analysis:** Mumbai generated the highest revenue of 669 million, with Atliq Exotica being the major contributor by generating 212.4 million from 13,480 total bookings.
Banglore experience lowest occupancy % and lowest guest rating but high reveneue suggesting high pricing. 
- **By Properties:** AtliQ Exotica(320.3M) and AtliQ Palace(304.1M) are top performing  properties by revenue. AtliQ Seasons perform weakest(66.1M, 44.62% occupancy, rating 2.29) requires immediate attension
- **Weekly Trend:** RevPAR and occupancy fluctute across weeks, but at peak around week W22-W27
- **Room Category Performance:** mid to high segment rooms are most preferred ad RT2 and RT3 room types generate high revenue. Presidential rooms contribute least to revenue, which suggest low demand for ultra premium rooms.    
- **Bookings by Platform:** Most bookings are made through MakeYourTrip and Others platform, while Direct offline booking is least preferred option, indicating strong reliance on online channels.
