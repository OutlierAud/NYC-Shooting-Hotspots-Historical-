# The Geography of Gun Violence in New York City

## A 19-Year Temporal and Spatial Analysis of Shooting Incidents in NYC

This project examines when and where shooting incidents were recorded in New York City from **2006 to 2024** using the **NYPD Shooting Incident Dataset (Historic)**. It combines a citywide analysis of shooting patterns over time with maps and summaries by borough and police precinct.

## Research Question

**When and where were shootings recorded in New York City from 2006 to 2024, and where did incidents concentrate during the peak weekly time window?**

## Analysis

- Cleaned and validated the data, using distinct incident IDs to count shootings involving multiple victims once.
- Examined incident counts by year, month, day of the week, and hour of the day.
- Used a weekday-by-hour heatmap to identify the peak overnight window.
- Compared all-hours and peak-window incident counts by borough and precinct, including the share of each area's incidents that occurred during the peak window.
- Mapped all-hours and peak-window hotspots side by side using the same grid and colour scale.
- Examined annual patterns by borough and in the five precincts with the highest overall counts, and fitted a descriptive linear model of the citywide annual trend.

## Key Findings

- **The selected peak window spans two nights.** It runs from Friday at 10 p.m. through Saturday at 4:59 a.m. and from Saturday at 10 p.m. through Sunday at 4:59 a.m., in local NYC time.
- **Many of the same hotspots appear in both maps.** Peak-window incidents cluster in parts of Brooklyn, the South Bronx, and northern Manhattan, where the all-hours map also shows concentrations.
- **Recorded shootings declined overall.** A sharp increase in 2020 interrupted the longer-term decline, with spikes in several of the highest-count precincts. The downward trend resumed in 2023.

## Tools

- R and R Markdown
- tidyverse, ggplot2, and lubridate
- sf and tigris

## Files

- `NYPD_NYC_Temporal_and_Geographic_Analysis.Rmd` — R Markdown source for the combined temporal and geographic analysis. Open it in RStudio and select **Knit** to generate the HTML report.

## Data Source

The NYPD historical dataset includes incident dates, times, boroughs, precincts, and geographic coordinates. [NYPD Shooting Incident Data (Historic) · NYC Open Data](https://data.cityofnewyork.us/Public-Safety/ARCHIVED_NYPD-Shooting-Incident-Data-Historic-/833y-fsy8/about_data)

## Limitations

The analysis uses raw incident counts without adjusting for population or land area. The maps show where recorded incidents accumulated over the study period. They do not estimate individual risk.

The analysis excludes records with missing coordinates so the temporal and geographic comparisons use the same records. Unreported incidents and differences in NYPD recording practices may affect the observed patterns. Pooling 19 years of incidents may also obscure changes in hotspot locations over time.

The peak window was selected from the observed weekday-by-hour patterns. The analysis describes those patterns without drawing conclusions about their causes.