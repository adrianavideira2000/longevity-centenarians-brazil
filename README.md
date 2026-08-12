# Longevity and the Profile of Brazilian Centenarians: Exploring Potential Blue Zones Through Mortality Data

**Authors:** Adriana Videira, Maria Teresa Bispo & Sindy Silva

## Overview
This project explores Brazil's 2023 mortality microdata (SIM/DATASUS) to screen, in an 
exploratory way, for regions with a strong signal of extreme longevity (deaths at age 
100+), and to characterise the sociodemographic profile of these individuals — inspired 
by "Blue Zone" research on longevity hotspots.

> This is a screening of candidates, not a confirmation of Blue Zones.

## Structure
The analysis is split into two notebooks:

- **Part 1 – Data Collection** (`Elderly_Mortality_Brazil_Part1.ipynb`)  
  Downloads raw mortality microdata from DATASUS (SIM-DO, 2023, all Brazilian states) 
  using the `microdatasus` package, filters records for individuals aged 100+, processes 
  the raw SIM codes into readable categories, and exports the result to Excel.

- **Part 2 – Data Cleaning, Processing and Analysis** (`Elderly_Mortality_Brazil_Part2.ipynb`)  
  Imports the exported dataset, cleans and recodes variables (age, region, education, 
  cause of death), and produces:
  - Sociodemographic profiling (age, sex, race/colour, marital status, education, 
    place of death) overall and by region
  - Underlying causes of death by ICD-10 chapter
  - Geographic distribution of centenarian deaths (state, region, map)
  - A regional "intensity of extreme longevity" indicator (105+ and 110+ thresholds)
  - Statistical tests: Chi-square, Fisher's Exact Test, Shapiro–Wilk, Mann–Whitney U, 
    Kruskal–Wallis

## Data
Data source: **SIM/DATASUS** (Brazilian Mortality Information System), 2023, accessed 
via the `microdatasus` R package. The intermediate dataset produced in Part 1 
(`sim_100plus_brazil_2023.xlsx`) is included/required to run Part 2.

## Requirements
R packages: `microdatasus` (from GitHub), `dplyr`, `writexl`, `tidyverse`, `openxlsx`, 
`maps`, `scales`

## Notes
This project was completed as part of a group assignment (R Data Analysis course, 2026).
