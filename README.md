# ByndlossLiWilliams_ENV872_EDA_FinalProject
ENV872 Course Project
## Summary

<The purpose of this repository is to explore how species activity changes between Nashville parks. We focused on the Mills Creek, Bells Bend, and Beaman because they had similar time frames for data collection. The goal of the study is to find if daily, monthly, and full study period activity are different between the parks and which park attributes might cause these changes. We looked at attribute affects on the two most common mammal species. The species data was collected using camera traps set out in the parks from 2019-2022.>

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

Code: Contains Rmd files for Data Analysis, Data Exploration, and Data Processing. 
Data: Contains the processed and raw datasets used for analysis. Includes camera deployments, park properties (.cpg, .dbf, .prj, .shp, and .shx), and wildlife insights data from 2021-2022. All files except Parks_properties and the Parks_view .geojson file are .csv files. Also has a metadata Rmd file.
Tukey_Test_Results.csv: Excel file containing Tukey test results for the target parks.
Final_Report_files: Holds figure-latex folder with graphs from the final report. 
Files are in a pdf format.


## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

### Raw Data 

#### Wildlife Insights.csv
$Source
[1] "Prof. Malu Jorge's Lab at Vanderbilt University"

$Description
[1] "Dataset detailing camera trap data from 2021 to 2022."

$Columns
[1] "cluster.name"  "site.n"        "cam.n"         "deployment.id" "date.time"    
[6] "species"      

$Data_Types
 cluster.name        site.n         cam.n deployment.id     date.time       species 
  "character"     "numeric"     "numeric"   "character"   "character"   "character" 

$Summary_Stats
 cluster.name           site.n           cam.n       deployment.id       date.time        
 Length:26380       Min.   : 1.000   Min.   : 2.00   Length:26380       Length:26380      
 Class :character   1st Qu.: 2.000   1st Qu.:15.00   Class :character   Class :character  
 Mode  :character   Median : 3.000   Median :34.00   Mode  :character   Mode  :character  
                    Mean   : 3.601   Mean   :30.14                                        
                    3rd Qu.: 5.000   3rd Qu.:43.00                                        
                    Max.   :10.000   Max.   :51.00                                        
   species         
 Length:26380      
 Class :character  
 Mode  :character  

To briefly explain a couple components, the columns include cluster name (identifies park), camera and site numbers, deployment ID, combined date and time, and species captured.  It is important to note that date columns are incorrectly recognized as characters, which was corrected for in data processing. Also, there are no relevant units to the data because most of it is categorical. 


#### All Deployments (2019-2022).csv

$Source
[1] "Prof. Malu Jorge's Lab at Vanderbilt University"

$Description
[1] "Dataset of deployment IDs with their start and end dates."

$Columns
[1] "deployment_id" "start_date"    "end_date"     

$Data_Types
deployment_id    start_date      end_date 
  "character"   "character"   "character" 

$Summary_Stats
 deployment_id       start_date          end_date        
 Length:70          Length:70          Length:70         
 Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character 
 
 To briefly explain a couple components, the columns include deployment ID, start date, and end date of deployment. It is important to note that date columns are incorrectly recognized as characters, which was corrected for in data processing. Also, there are no relevant units for this dataset. 

#### Park_Properties.shp

$Source
[1] "Nashville Open Data Portal (https://data.nashville.gov/)"

$Description
[1] "Dataset of local park boundaries with relevant information."

$Columns
 [1] "Name"       "PARK_ID"    "Latitude"   "Longitude"  "YearEstabl" "Acres"      "DaysOpen"  
 [8] "Hours"      "Phone"      "Webstie"    "Address"    "Restroom"   "CommunityC" "NatureCent"
[15] "ADA"        "Concession" "DogPark"    "Baseball"   "BasketBall" "MountainBi" "Boating"   
[22] "Camping"    "DiscGolf"   "Fishing"    "GolfCourse" "Hiking"     "HistoricSi" "HorsebackR"
[29] "Lake"       "Picnic"     "PicnicShel" "Playground" "SchoolSite" "Soccer"     "SprayPark" 
[36] "SkatePark"  "Swimming"   "Tennis2"    "WalkJog"    "Email"      "Descriptio" "Status"    
[43] "Volleyball" "FootballMu" "CanoeLaunc" "CommunityG" "CommonName" "Classifica" "City"      
[50] "State"      "ZipCode"    "GlobalID"   "geometry"  

$Data_Types
$Data_Types$Name
[1] "character"

$Data_Types$PARK_ID
[1] "character"

$Data_Types$Latitude
[1] "numeric"

$Data_Types$Longitude
[1] "numeric"

$Data_Types$YearEstabl
[1] "numeric"

$Data_Types$Acres
[1] "numeric"

$Data_Types$DaysOpen
[1] "character"

$Data_Types$Hours
[1] "character"

$Data_Types$Phone
[1] "character"

$Data_Types$Webstie
[1] "character"

$Data_Types$Address
[1] "character"

$Data_Types$Restroom
[1] "character"

$Data_Types$CommunityC
[1] "character"

$Data_Types$NatureCent
[1] "character"

$Data_Types$ADA
[1] "character"

$Data_Types$Concession
[1] "character"

$Data_Types$DogPark
[1] "character"

$Data_Types$Baseball
[1] "character"

$Data_Types$BasketBall
[1] "character"

$Data_Types$MountainBi
[1] "character"

$Data_Types$Boating
[1] "character"

$Data_Types$Camping
[1] "character"

$Data_Types$DiscGolf
[1] "character"

$Data_Types$Fishing
[1] "character"

$Data_Types$GolfCourse
[1] "character"

$Data_Types$Hiking
[1] "character"

$Data_Types$HistoricSi
[1] "character"

$Data_Types$HorsebackR
[1] "character"

$Data_Types$Lake
[1] "character"

$Data_Types$Picnic
[1] "character"

$Data_Types$PicnicShel
[1] "numeric"

$Data_Types$Playground
[1] "character"

$Data_Types$SchoolSite
[1] "character"

$Data_Types$Soccer
[1] "character"

$Data_Types$SprayPark
[1] "character"

$Data_Types$SkatePark
[1] "character"

$Data_Types$Swimming
[1] "character"

$Data_Types$Tennis2
[1] "character"

$Data_Types$WalkJog
[1] "character"

$Data_Types$Email
[1] "character"

$Data_Types$Descriptio
[1] "character"

$Data_Types$Status
[1] "character"

$Data_Types$Volleyball
[1] "character"

$Data_Types$FootballMu
[1] "character"

$Data_Types$CanoeLaunc
[1] "character"

$Data_Types$CommunityG
[1] "character"

$Data_Types$CommonName
[1] "character"

$Data_Types$Classifica
[1] "character"

$Data_Types$City
[1] "character"

$Data_Types$State
[1] "character"

$Data_Types$ZipCode
[1] "character"

$Data_Types$GlobalID
[1] "character"

$Data_Types$geometry
[1] "sfc_MULTIPOLYGON" "sfc"             


$Summary_Stats
     Name             PARK_ID             Latitude       Longitude        YearEstabl  
 Length:198         Length:198         Min.   : 0.00   Min.   :-87.03   Min.   :   0  
 Class :character   Class :character   1st Qu.: 0.00   1st Qu.:-86.79   1st Qu.:1964  
 Mode  :character   Mode  :character   Median :36.12   Median :-86.73   Median :2000  
                                       Mean   :26.30   Mean   :-62.22   Mean   :1855  
                                       3rd Qu.:36.18   3rd Qu.:  0.00   3rd Qu.:2002  
                                       Max.   :36.34   Max.   : 86.90   Max.   :2021  
     Acres           DaysOpen            Hours              Phone             Webstie         
 Min.   :   0.10   Length:198         Length:198         Length:198         Length:198        
 1st Qu.:   0.10   Class :character   Class :character   Class :character   Class :character  
 Median :   6.01   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
 Mean   : 111.12                                                                              
 3rd Qu.:  21.75                                                                              
 Max.   :3765.79                                                                              
   Address            Restroom          CommunityC         NatureCent            ADA           
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
  Concession          DogPark            Baseball          BasketBall         MountainBi       
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
   Boating            Camping            DiscGolf           Fishing           GolfCourse       
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
    Hiking           HistoricSi         HorsebackR            Lake              Picnic         
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
   PicnicShel       Playground         SchoolSite           Soccer           SprayPark        
 Min.   : 0.0000   Length:198         Length:198         Length:198         Length:198        
 1st Qu.: 0.0000   Class :character   Class :character   Class :character   Class :character  
 Median : 0.0000   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
 Mean   : 0.5505                                                                              
 3rd Qu.: 0.7500                                                                              
 Max.   :13.0000                                                                              
  SkatePark           Swimming           Tennis2            WalkJog             Email          
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
  Descriptio           Status           Volleyball         FootballMu         CanoeLaunc       
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
  CommunityG         CommonName         Classifica            City              State          
 Length:198         Length:198         Length:198         Length:198         Length:198        
 Class :character   Class :character   Class :character   Class :character   Class :character  
 Mode  :character   Mode  :character   Mode  :character   Mode  :character   Mode  :character  
                                                                                               
                                                                                               
                                                                                               
   ZipCode            GlobalID                  geometry  
 Length:198         Length:198         MULTIPOLYGON :198  
 Class :character   Class :character   epsg:2274    :  0  
 Mode  :character   Mode  :character   +proj=lcc ...:  0  


## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>

The following can be found within the code folder in this repository:

1. Data_Processing.Rmd (data processing in which raw data was loaded in and processed data was externally saved)
2. Data_Exploration.Rmd (data exploration in which several visualizations of the data were created)
3. Data_Exploration.html (html version of above rmd file)
4. Data_Analysis.Rmd (data analysis in which processed data was analyzed through anovas and t-tests to answer research questions)
5. Data_Analysis.html (html version of above rmd file)
6. Final_Report.Rmd (final report containing summarized information on all other code files and additional comments)
7. Final_Report.html (html version of above rmd file)