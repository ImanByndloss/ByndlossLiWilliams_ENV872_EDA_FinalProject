# ByndlossLiWilliams_ENV872_EDA_FinalProject
ENV872 Course Project
## Summary


The purpose of this repository is to explore how species activity changes between Nashville parks. We focused on the Mills Creek, Bells Bend, and Beaman because they had similar timeframes for data collection. The goal of the study is to find if daily, monthly, and full study period activity are different between the parks and which park attributes might cause these changes. We looked at attribute affects on the two most common mammal species. The species data was collected using camera traps set out in the parks from 2019-2022. >

## Investigators

<Iman Byndloss, Leah Li, and Rachel Williams. Environmental Management students at Duke University.>

## Keywords

<Spatial analysis, Species Activity, Parks, Camera Traps>

## Database Information

<Camera trap data was collected on Wildlife Insights by Professor Malu Jorge's lab
at Vanderbilt University. Cameras were set up throughout Nashville Parks and data 
was collected on locations and species. The park data was spatial data collected
from Nashville Open Data set at the following link: https://datanashvillegov-nashville.hub.arcgis.com/datasets/13c1aa2bafdd43f4b3cd132e7256a172_0/explore?location=36.167341%2C-86.763938%2C9.17). This included information about park sizes and 
amenities. >


## Folder structure, file formats, and naming conventions 

<describe the folders contained in the repository, including what type of files they contain
Code: Contains Rmd files for Data Analysis, Data Exploration, and Data Processing. 
Data: Contains the processed and raw datasets used for analysis. Includes camera deployments, park properties (.cpg, .dbf, .prj, .shp, and .shx), and wildlife insights data from 2021-2022. All files except Parks_properties and the Parks_view .geojson file are .csv files. Also has a metadata Rmd file.
Tukey_Test_Results.csv: Excel file containing Tukey test results for the target parks.>

<describe the formats of files for the various purposes contained in the repository>

<describe your file naming conventions>

## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 
## Metadata for Wildlife Insights.csv

Wildlife insights: 

$Description
[1] "Dataset detailing camera trap data from 2021 to 2022."

$Columns
[1] "cluster.name"  "site.n"   "cam.n"  "deployment.id" "date.time"   "species"  

The columns include camera and site numbers, deployment ID, the date and time,
and species captured. 

$Data_Types
 cluster.name        site.n         cam.n deployment.id     date.time       species 
  "character"     "numeric"     "numeric"   "character"   "character"   "character" 

There are no relevent units to the data because most of it is categorical. 


## Metadata for All Deployments (2019-2022).csv

$Description
[1] "Dataset of deployment IDs with their start and end dates."

$Columns
[1] "deployment_id" "start_date"    "end_date" 

These columns include deployment ID, start date, and end date of deployment. 

$Data_Types
deployment_id    start_date      end_date 
  "character"   "character"   "character" 

There are no relevant units for this dataset. 

## Metadata for Park_Properties.shp



## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>