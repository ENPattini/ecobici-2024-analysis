# Urban Mobility in Buenos Aires: Analysis with R & Tableau (Ecobici 2024)

This project analyzes over 3.2 million public bike trips from Buenos Aires' Ecobici system in 2024 to uncover usage patterns, peak demand, popular stations, and opportunities for sustainable urban mobility.


## Key Findings

- Strong commuting patterns: Evening peak (16–18 hs, up to 308k trips/hour) and secondary morning peak (7–10 AM).  
- Weekday average ~10,724 trips/day vs ~4,081 on weekends (ratio ~2.6:1).  
- Top origin stations (Constitución 35k, Pacífico 34k) and spatial heatmaps show concentrated demand in central areas (Microcentro, Palermo, Recoleta).  
- Morning origins cluster in residential/central zones, evening destinations disperse, confirming bidirectional commuting.  
- Trip durations: median ~16.1 min, average ~21.7 min — most under 30 min.  
- Gender distribution: Male ~60.8%, Female ~31.6%.  
- Seasonal peaks in late spring/early summer (October 335k), lowest in winter (July 215k).  
- Net flow extremes (e.g., Juan Manuel De Blanes +3,056, Cerrito -2,064) highlight rebalancing needs.


## Interactive Dashboard

Explore the full dataset interactively in Tableau Public:  
[View the Ecobici 2024 Dashboard](https://public.tableau.com/views/Ecobici2024-InteractiveUrbanBike-SharingInsights/Ecobici2024-UrbanBike-SharingInsights?:language=es-ES&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)


## Full Rendered Report

**Complete HTML Report** (with interactive heatmaps):  
[Open the Report Online](https://www.emilionahuelpattini.com/projects/ecobici-2024/urban-mobility-analysis.html)  
(Interactive version with zoom, pan, and tooltips. No download needed.)

**Alternative (offline download)**:  
Download the ZIP of the repo and open `outputs/urban-mobility-analysis.html` (requires `outputs/urban-mobility-analysis_files/` folder).

**Complete PDF Report** (printable version): 

[Download PDF Report](https://www.emilionahuelpattini.com/projects/ecobici-2024/urban-mobility-analysis.pdf)  
(Full report with all visuals and insights — static version, ~12 pages)


## Skills Demonstrated

- Data cleaning & preparation (R, tidyverse, lubridate)  
- Exploratory Data Analysis (temporal, spatial, demographic)  
- Visualization: ggplot2, leaflet (interactive heatmaps), Tableau  
- Business insights & actionable recommendations  
- Reproducibility & documentation


## Data Source

Official Buenos Aires open data portal (public & free): 

- Raw data: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas (download "ecobici_recorridos_realizados_2024.csv")  
- Processed data: The cleaned CSV (trips_clean_2024.csv) is not included due to GitHub size limits (>100 MB). You can recreate it by running the R Markdown report (urban-mobility-analysis.Rmd) or request it from me.


## How to Reproduce

1. Clone this repo.  
2. **Download the raw data** (not included due to size):  
   From the official source: https://data.buenosaires.gob.ar/dataset/bicicletas-publicas  
   Download "ecobici_recorridos_realizados_2024.csv" and place it in `data/raw/`.
3. Open `urban-mobility-analysis.Rmd` in RStudio.  
4. Install required packages (run once):  
   ```r
   install.packages(c("tidyverse", "lubridate", "scales", "leaflet", "leaflet.extras", "here"))
   ```
5. Knit to generate the report (HTML/PDF).
6. Tableau: Import `data/processed/trips_clean_2024.csv` to recreate or explore the interactive visuals (heatmaps, peak hours, etc.).
