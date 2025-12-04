# 🚖 OLA Ride Analysis (Excel + SQL + Power BI)

This project is an end-to-end analysis of OLA ride booking data.  
The workflow includes **data cleaning using Excel**, **data analysis using MySQL**,  
and **interactive dashboard creation using Power BI** to uncover key insights related to  
rides, pricing, customer behavior, cancellations, and driver performance.

---

## 📌 Project Workflow

### **1️⃣ Data Cleaning – Excel**
- Checked for missing values  
- Removed duplicates  
- Standardized column names  
- Cleaned categorical values  
- Ensured numeric columns were properly formatted  

Excel file was then exported as **CSV** for SQL loading.

---

## **2️⃣ SQL Analysis – MySQL**

Performed detailed analysis using SQL queries.

### ✔ Key SQL Tasks:
- Successful ride extraction  
- Average ride distance  
- Top 5 customers  
- Customer vs driver cancellations  
- Ratings analysis  
- Payment method trends  
- Revenue calculation  
- Incomplete ride reasons  

All SQL questions with answers + screenshot images are stored in:

📁 **SQL/SQL_Queries.md**  
📁 **SQL/Screenshots_SQL/**

---

### ⭐ Example SQL Query:
```sql
SELECT vehicle_type, AVG(ride_distance) 
FROM ola_data
GROUP BY vehicle_type;
3️⃣ Power BI Dashboard
Interactive dashboards created using Power BI:

✔ Slicers
✔ KPI Cards
✔ Donut Charts
✔ Line Charts
✔ Bar Graphs
✔ Maps (If applicable)

Dashboard Covers:
Ride status analysis

Revenue trends

Driver ratings

Customer ratings

Vehicle performance

Payment mode comparison

Cancellation trends

Dashboard file + screenshots:

📁 PowerBI/Ola_Ride_Analysis.pbix
📁 PowerBI/Screenshots_PowerBI/

📊 Key Insights
🔹 Ride Analysis
A significant percentage of rides were completed successfully

Few customers contributed the highest number of bookings

🔹 Cancellation Patterns
Customer cancellations were more frequent than driver cancellations

Driver cancellations mainly due to personal / car-related issues

🔹 Ratings
Prime Sedan drivers received the highest average rating

Customer ratings varied based on ride type & distance

🔹 Financial Insights
Majority of revenue came from successful rides

UPI was the most preferred payment method

📁 Project Structure
sql
Copy code
Ola_Ride_Analysis/
│
├── SQL/
│   ├── Ola_project.sql
│   ├── SQL_Queries.md
│   └── Screenshots_SQL/
│        ├── q1.png
│        ├── q2.png
│        └── ...
│
├── PowerBI/
│   ├── Ola_Ride_Analysis.pbix
│   └── Screenshots_PowerBI/
│        ├── overview.png
│        ├── revenue.png
│        ├── ratings.png
│
├── Dataset/
│   └── ola_data.csv
│
└── README.md
🧠 Conclusion
This project showcases end-to-end data analytics skills:

✔ Excel (Cleaning & Preparation)
✔ SQL (Data Analysis & Business Insights)
✔ Power BI (Visualization & Dashboarding)

It demonstrates real-world problem-solving and insight generation.
