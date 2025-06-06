# Cleaning the shorebird survey data - Snow, Cover, and Land Data 
*This is an assignment for UCSB's MEDS program EDS 213 class.*

## About

This repository contains notebooks for cleaning snow survey data and exploring snow species data. The `data-cleaning-practice.qmd` begins the cleaning 

## The data set

ARCTIC SHOREBIRD DEMOGRAPHICS NETWORK [https://doi.org/10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W)

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the [course data repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-spring-2024-class-data) for full metadata information about this data set.



## Data & File Overview

| File and Folder Path                            | Description                                   |
| ----------------------------------------------- | --------------------------------------------- |
| `data/raw/01_ASDN_Readme.txt`                   | Full ASDN metadata information                |
| `data/raw/ASDN_Snow_species.csv`                | Raw species data from ASDN                    |
| `data/raw/ASDN_Snow_survey.csv`                 | Raw snow survey data from ASDN                |
| `data/processed/all_cover_fixed_YosRamirez.csv` | Cleaned `.csv` version of snow cover data     |
| `eds213_data_cleaning_assign_YosRamirez.qmd`    | Quarto notebook for snow cover data cleaning  |
| `eds213_data_cleaning_assign_YosRamirez.html`   | Rendered HTML output from `.qmd`              |
| `data-cleaning-practice.qmd`                    | Quarto notebook for practice data cleaning    |
| `README.md`                                     | Project documentation                         |
| `bren-meds213-data-cleaning.Rproj`              | RStudio project                               |
| `docs/`                                         | Folder for published outputs or documentation |

Relationship between files, if important:

Additional related data collected that was not included in the current
data package:

Are there multiple versions of the dataset?

## DATA-SPECIFIC INFORMATION FOR: all_cover_fixed_YosRamirez.csv

Number of Variables: 11
Number of Rows: 42830

| Variable Name | Description                        | Unit and Value Lables      | 
| ------------- | ---------------------------------- | -------------------------- |
| `Site`        | Field site abbreviation            | text                       | 
| `Year`        | Year of observation                | YYYY integer               | 
| `Date`        | Date of survey                     | DD-MM-YY text              | 
| `Plot`        | Plot ID within site                | text                       | 
| `Location`    | Sub-location or site grid cell     | text                       | 
| `Snow_cover`  | Percent of snow cover observed     | Percent (%) 0 - 100        | 
| `Water_cover` | Percent of water cover             | Percent (%) 0 - 100        | 
| `Land_cover`  | Percent of land cover              | Percent (%) 0 - 100        | 
| `Total_cover` | Sum of snow, water, and land cover | Percent (%) 0 - 100        | 
| `Observer`    | Initials of observer               | text                       | 
| `Notes`       | Additional field notes             | text                       | 

Missing data codes: <list code/symbol and definition>

Specialized formats or other abbreviations used:

## SHARING/ACCESS INFORMATION

Licenses/restrictions placed on the data:

Links to publications that cite or use the data:

Links to other publicly accessible locations of the data:

Links/relationships to ancillary data sets: <any supplementary data sources 
that support analysis or classification of the datasets, eg., plant taxonomy table.)>

Was data derived from another source? If yes, list source(s): <list citations 
to original sources>

Recommended citation for the project:

