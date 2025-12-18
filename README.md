# Curry Shots Analysis — Power BI Dashboard

## Project Overview
This Power BI project analyzes Stephen Curry’s shooting performance across NBA teams and shot ranges. The report leverages Power Query and DAX to transform raw data into actionable insights, presented through interactive dashboards.

## Dashboard Preview 
<img width="1330" height="749" alt="dashboard-preview2" src="https://github.com/user-attachments/assets/9ab86fe4-8aaf-4961-b454-d0b87c2f40bb" />
<img width="1329" height="744" alt="dashboard-preview1" src="https://github.com/user-attachments/assets/c73616e2-3f02-4be6-aac6-ccd2cfa8ee13" />

## Files Included
- Curry Shots Analysis.pbix 
- Excel Files - Data Source
  - CurryShots.csv
  - NBA_teamlist.csv
- Nba_court.jpg - Image for Visual
- dashboard-preview1 - Dashboard Screenshot
- dashboard.preview2

## Features / Highlights
- **KPI Summary**: Total FG Attempted, FG Made, Field Goal Percentage (FG%)
- **Franchise Analysis**: Top 3 opponent teams by total field goals made
- **Shot Distance Grouping**: FG% by predefined shot distance ranges
- **Shot Chart**: Make vs Miss visualized across court area (scatter plot)
- **Distance-wise Analysis**: Shot attempts by exact distance (0–40 ft) using clustered column chart
- **Interactive Filters**: Season-level filters to customize views

## Tools & Techniques
- Power BI Desktop
  - Power Query Editor
  - DAX (for KPIs and calculations)
  - Data Groups (grouping shot distance)
  - Dashboard design with consistent color, font, and layout
    
## Data Preparation 
### Steps performed in Power Query:
- Removed irrelevant columns
- Renamed columns for clarity and consistency
- Reordered and cleaned data types
- Created custom conditional column for shots: make or miss
- Split, merged, and transformed fields as needed – date column
- Merged with NBA_teamlist table to enrich team data
- Added custom index for row tracking
- Replaced null/wrong values for clean visuals

## DAX Measures & Functions
Custom calculations were made using key DAX functions:
| Function         | Purpose                                                                                   |
|------------------|-------------------------------------------------------------------------------------------|
| `CALCULATE()`     | Applies filters dynamically to compute context-specific values (e.g., FG by opponent)    |
| `MEDIAN()`        | Calculates the median shot distance for shot range analysis                              |
| `MAX()`           | Retrieves the maximum (longest) shot distance                                            |
| `DISTINCTCOUNT()` | Counts unique values like total opponents or number of games                             |
| `DIVIDE()`        | Performs division (e.g., FG% = FG Made / FG Attempted)    |

## Future Enhancements
- Add trend visuals across seasons or time periods
- Benchmark against league averages or other players
- Incorporate bookmarks for toggling between filters


