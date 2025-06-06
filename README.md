# Cleaning the shorebird survey data - Snow, Water, and Land Cover Data 
*This is an assignment for UCSB's MEDS program EDS 213 class.*

## ABOUT

This repository contains notebooks for cleaning snow survey data and exploring snow species data. The `data-cleaning-practice.qmd` begins the cleaning process in a practice format, and explores the species data. The `eds213_data_cleaning_assign_YosRamirez.qmd` cleans the snow, water, and land cover data and saves a `.csv` for future use. 

## DATA SET

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

This repository is cloned from [MEDS 213 Course repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning) and conatins some of its orginal content. Credit is given to where it belongs. 

## DATA & FILE OVERVIEW

### File list

| File and Folder Path                            | Description                                   |
| ----------------------------------------------- | --------------------------------------------- |
| `data/raw/01_ASDN_Readme.txt`                   | Full ASDN metadata information                |
| `data/raw/ASDN_Snow_species.csv`                | Raw species data from ASDN                    |
| `data/raw/ASDN_Snow_survey.csv`                 | Raw snow survey data from ASDN                |
| `data/processed/all_cover_fixed_YosRamirez.csv` | Cleaned `.csv` version of snow cover data     |
| `eds213_data_cleaning_assign_YosRamirez.qmd`    | Quarto notebook for snow cover data cleaning  |
| `eds213_data_cleaning_assign_YosRamirez.html`   | Rendered HTML output from `.qmd`              |
| `snow_cover.csv`                                | Practice cleaning `.csv`                      |
| `species_presence.csv`                          | Species count `.csv`                          |
| `data-cleaning-practice.qmd`                    | Quarto notebook for practice and exploration  |
| `README.md`                                     | Project documentation                         |
| `bren-meds213-data-cleaning.Rproj`              | RStudio project                               |
| `docs/`                                         | Folder for published outputs or documentation |

### Relationship between files:
The notebook `eds213_data_cleaning_assign_YosRamirez.qmd` cleans the `ASDN_Snow_survey.csv` data and produces the `all_cover_fixed_YosRamirez.csv` cleaned dataset.

The notebook `data-cleaning-practice.qmd` produces `snow_cover.csv` from `ASDN_Snow_survey.csv` and `species_presence.csv` from `ASDN_Snow_species.csv`.

The `docs/` folder contains folders and files from different sources.

### Additional related data collected:  
No additional data collected

### Versions of the dataset:
There is only one version of the cleaned dataset `all_cover_fixed_YosRamirez.csv`

## DATA-SPECIFIC INFORMATION FOR 

**`all_cover_fixed_YosRamirez.csv`**

Number of Variables: 11

Number of Rows: 42830

### Variable list

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

### Missing data code list

| Code        | Meaning                  |
| ----------- | ------------------------ |
| *empty*     | not recorded             | *in `.csv`*
| `NA`        | not recorded             | *in `.csv`*
| `"."`       | missing or invalid entry |
| `"--"`      | missing or placeholder   |
| `"unk"`     | missing or unknown       |
| `"n/a"`     | not recorded             |

Note: the code for missing value `"."`, `"--"`, `"unk"` and `"n/a"` were turned to `NA` and are not in the cleaned data. Any cover greater than 100 was set to `NA`. A singular missing cover value was recovered by summing all 3 covers to 100. Remaining empty values were unable to be recovered. 

### Specialized formats or other abbreviations used:
None

## SHARING/ACCESS INFORMATION

### Licenses/restrictions placed on the data:
Creative Commons Attribution 4.0 International (CC-BY 4.0) Free to share and adapt data with appropriate credit.

### Links to publications that cite or use the data:
[NSF Arctic Data Center - ASDN data](https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W) by the [NSF Arctic Data Center](https://arcticdata.io) repository

### Links to other publicly accessible locations of the data:
[MEDS 213 Course repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning) 

### Links/relationships to ancillary data sets: 
None were used to clean the snow survey data

### Citations

Ruthrauff, D., et al. (2015). Arctic Shorebird Demographics Network. NSF Arctic Data Center. DOI: 10.18739/A2222R68W

### Recommended citation for the cleaned dataset

Ramirez, Y. (2025). Cleaned ASDN snow, water, and land cover data (Week 7 homework, EDS 213). GitHub repository.

