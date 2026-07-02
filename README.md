# esports Performance Analytics Dashboard

## Project Overview
This project is an interactive business intelligence dashboard built in **Power BI** to analyze competitive gaming telemetry. Instead of traditional business sales data, this project applies data analytics methodologies to unstructured tactical shooter data to extract insights regarding combat efficiency, win rates, and player progression over time.

## Tech Stack & Tools
* **Data Visualization & BI:** Power BI
* **Data Transformation:** Power Query
* **Calculations:** DAX (Data Analysis Expressions)
* **Source Data:** Excel (.xlsx)

## Key Features & Visualizations
* **Dynamic KPI Cards:** Instant visibility into overall Average Win Rate, K/D Ratio, and Headshot Percentage.
* **Time-Series Performance Tracking:** A categorical line chart visualizing K/D Ratio progression across distinct time periods, overriding default continuous axis limitations.
* **Combat Volume Analysis:** A clustered column chart comparing high-impact moments (Total Aces vs. Total Clutches) side-by-side.
* **Damage Consistency:** A smoothed area chart mapping Average Damage Per Round (DPR) to visualize combat effectiveness over time.
* **Interactive Filtering:** A dedicated slicer allowing users to filter the entire dashboard by specific time periods.

## Data Engineering & DAX Implementation
To ensure a scalable and professional backend, the project utilizes a dedicated measure table architecture. Custom DAX measures include:
* `Average Win Rate = AVERAGE('Match_Data'[winrate])`
* `Average K/D Ratio = AVERAGE('Match_Data'[kd_ratio])`
* `Total Aces = SUM('Match_Data'[aces])`
* `Average DPR = AVERAGE('Match_Data'[damage_round])`
