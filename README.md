# Curry Shots Analysis — Power BI Dashboard

This Power BI project analyzes Stephen Curry’s shooting performance across NBA teams and shot ranges. The report leverages Power Query and DAX to transform raw data into actionable insights, presented through interactive dashboards.

## Files Included
- Curry Shots Analysis.pbix
- Excel Files
  - CurryShots.csv
  - NBA_teamlist.csv
- Nba_court.jpg

## Power Query Editor (Data Preparation)
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


## Report Pages
### 1. Franchise-wise FG Analysis
-	Shows Curry’s field goal stats against different NBA teams
-	Visuals include:
    - KPI cards (Total FG Attempted, Made, FG%)
    - Top 3 opponent teams by total FGs made
    - Page-level filters (like season) enable custom views
### 2. Shot Range Analysis
- Groups FG attempts by shot distance
- Includes:
  - KPI cards (e.g., Longest & Median Shot Distance)
  - FG% by distance ranges
  - Shot chart (scatter plot: Make vs Miss across court)
  - Clustered column chart of shot attempts vs exact distance (0–40 ft)

## Key Insights
- Stephen Curry’s shot distances and field goal attempts vary by season, with a consistent trend of high-volume long-range shots (23ft+).
- The top 3 teams Curry scores most against update per selected season, revealing how matchups and performance evolve year by year.
- His highest accuracy often remains close to the basket (0–4 ft), though efficiency in long-range shooting varies season to season.

## Tools & Techniques
- Power BI Desktop
  - Power Query Editor
  - DAX (for KPIs and calculations)
  - Data Groups (grouping shot distance)
  - Dashboard design with consistent color, font, and layout

## Optional Enhancements
- Add trend visuals across seasons or time periods
- Benchmark against league averages or other players
- Incorporate bookmarks for toggling between filters


