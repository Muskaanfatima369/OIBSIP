# Task 2 — Unemployment Analysis with Python

**Track:** Data Science
**Program:** Oasis InfoByte (OIBSIP)

## Objective
Perform exploratory data analysis on unemployment data to uncover regional and temporal trends, with a focus on the impact of the COVID-19 pandemic on unemployment rates in India.

## Dataset
"Unemployment in India" — sourced from Kaggle. Contains region, date, estimated unemployment rate (%), estimated employed count, and estimated labour participation rate (%).

## Approach
1. Loaded the dataset and cleaned column names (stripped leading/trailing whitespace)
2. Inspected shape, dtypes, and null values; converted Date to datetime (day-first format)
3. Computed region-wise and month-wise average unemployment rates
4. Plotted a time-series line chart of unemployment rate across 3 major states (Delhi, Maharashtra, Tamil Nadu)
5. Plotted a bar chart of the top 10 states by average unemployment rate
6. Built a correlation heatmap between unemployment rate, employment, and labour participation
7. Compared pre-COVID vs. post-COVID mean rates using a March 2020 cutoff (India's lockdown start)
8. Added written observations after each visualization

## Tech Stack
Python, pandas, matplotlib, seaborn, Jupyter Notebook

## Files
- `Unemployment_Analysis.ipynb` — full notebook with code, explanations, and results
- Screenshots — line chart, bar chart, and heatmap outputs

## Result

- **Time-series:** All three states show a sharp unemployment spike around April–May 2020, coinciding with India's COVID-19 lockdown. Tamil Nadu had the steepest and earliest spike (near 0% to ~50%), Delhi's spike was delayed but more sustained (peaking ~45%, staying elevated near 20% by July), and Maharashtra's spike was the most muted (~25% peak).
- **Top 10 states:** Tripura (~28%) and Haryana (~26%) have the highest average unemployment rates overall, though this reflects structural/baseline regional disparity rather than a COVID-specific effect.
- **Correlation:** Unemployment rate showed only a weak negative correlation (-0.22) with employed count, and near-zero correlation (0.00–0.01) with labour participation rate — suggesting unemployment shifts in this period were driven more by demand-side job losses than by people entering/leaving the labour force.
