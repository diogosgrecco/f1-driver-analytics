F1 Driver Head-to-Head Analytics 🏎️
 
<img width="1907" height="1073" alt="image" src="https://github.com/user-attachments/assets/1156e020-8402-454e-a6ed-9d9a4393ea0b" />


📥 Download Power BI File

📊 Project Overview
This project is a high-performance Head-to-Head (H2H) Comparison Tool designed to analyze Formula 1 driver performance across multiple seasons. Unlike standard reports, this dashboard utilizes a custom-built UI inspired by F1 pit-wall telemetry and broadcast graphics, focusing on clarity, symmetry, and "at-a-glance" insights.

🛠️ Tech Stack & Skills
Tool: Power BI Desktop

Data Modeling: Star Schema (Facts: Results | Dimensions: Drivers, Races, Teams)

UI/UX: Custom Grid Layout, Dark Mode Optimization, Container-based Design

Logic: Advanced DAX for dynamic filtering and conditional formatting.

🌟 Key Features
Independent Driver Comparison: Uses a disconnected table strategy to allow users to select and compare any two drivers on the grid independently.

F1 "HUD" Interface: A bespoke UI that moves away from "standard" Power BI defaults. Features include:

Centered "VS" centerpiece for visual balance.

Removed gridlines and axis clutter for a "Telemetry" feel.

Anchor points for driver photography to provide immediate context.

Dynamic Color Synchronization: Implemented logic to ensure that "Driver 1" and "Driver 2" maintain consistent theme colors across all visuals (Donuts, Bars, and KPIs) regardless of the selection.

Performance Metrics: * Qualy & Race Wins: Breakdown of dominance within the selected pair.

Average Starting Grid: Vertical analysis of qualifying performance.

Season Points: Clustered bar charts for direct points comparison.

💡 Technical Highlights (DAX)
To keep the UI clean, I implemented custom DAX logic for the dynamic coloring. Instead of manually coloring 20+ drivers, the dashboard automatically assigns colors based on the selection order:

Code snippet
// Example of the logic used for Dynamic Color Assignment
Driver Color = 
VAR FirstDriver = MINX(ALLSELECTED(dim_driver), dim_driver[Name])
RETURN
IF(SELECTEDVALUE(dim_driver[Name]) = FirstDriver, "#E10600", "#FFD700") 
📂 Project Structure
Plaintext
f1-driver-h2h-analytics/
├── data/
│   ├── driver_stats.csv       # Cleaned F1 results data
│   └── dim_drivers.csv        # Driver metadata and image links
├── screenshots/
│   └── dashboard_main.png     # High-res preview of the final UI
├── F1_H2H_Analytics.pbix      # The interactive Power BI file
└── README.md                  # Project documentation
