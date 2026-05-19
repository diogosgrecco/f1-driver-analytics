# F1 Driver Head-to-Head Analytics 🏎️
 
<img width="1907" height="1073" alt="image" src="https://github.com/user-attachments/assets/1156e020-8402-454e-a6ed-9d9a4393ea0b" />



[**📥 Download Power BI File**](https://github.com/diogosgrecco/f1-driver-analytics/raw/refs/heads/main/F1%20-%20Dashboard%20V2.pbix)
> **Note:** You will need Power BI Desktop installed to view the interactive `.pbix` file.

---

## 📊 Project Overview
This project is a high-performance Head-to-Head (H2H) Comparison Tool designed to analyze Formula 1 driver performance across multiple seasons. Unlike standard reports, this dashboard utilizes a custom-built UI inspired by F1 pit-wall telemetry and broadcast graphics, focusing on clarity, symmetry, and "at-a-glance" insights.

## 🛠️ Tech Stack & Skills
Tools: Power BI Desktop, Azure Databricks, Python/PySpark

Data Engineering (ETL): Engineered an automated data pipeline in Databricks utilizing a Medallion Architecture (Bronze, Silver, Gold layers). Extracted and transformed raw Formula 1 data ingested from the Ergast REST API.

Data Modeling: Designed a highly optimized Star Schema in Power BI, establishing robust relationships between dimension tables (Drivers, Circuits, Constructors) and fact tables (Race Results, Qualifying) to ensure efficient data refresh and query performance.

DAX & Analytics: Authored advanced DAX measures to handle complex logic, dynamic filtering contexts, and custom conditional formatting to drive interactive visual insights.
