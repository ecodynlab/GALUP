# Introduction to Remote Sensing Concepts

## Module 1 - Basic Remote Sensing 
### EM Spectrum 
• **electromagnetic spectrum** is the entire distribution of electromagnetic radiation according to frequency or wavelength. 

•**Observed energy** or **radiation** is primarily sensitive to molecular resonances in the to molecular resonances in the surface layer surface layer of target. 

•**Emitted**, **reflected**, and **backscattered radiation** is sensitive to temperature distribution, geometric, and electric properties of surface or volume. 

![image](https://user-images.githubusercontent.com/87503837/130260547-5c76cddd-c913-4adb-b183-c50604eee563.png)

The human eye is only able to detect wavelengths in the visible light range. However, many insects see in the 300 to 650 nm wavelength and can detect ultraviolet light because   they have special photoreceptors in their eyes.   


![image](https://user-images.githubusercontent.com/87503837/130195843-a8aea0e9-def9-40c4-80ce-b562fd56e918.png)




### Satellite Imagery 
•	Geo-stationary/ geo stationary/ geo-synchronous : continuous coverage of synchronous : continuous coverage of one region one region only (meteorological applications, high Earth (meteorological applications, high Earth orbit of ~36000 km; low/coarser spatial resolution; ~36000 km; low/coarser spatial resolution; e.g GOES, Japanese GOES, Japanese GMS, European GMS, European Metosat Metosat)   
•	Polar orbiting (100s km, low Earth orbit, high/fine spatial Polar orbiting (100s km, low Earth orbit, high/fine spatial resolution; repeat global resolution; repeat global coverage; e.g. coverage; e.g. Landsat Landsat, Landsat Landsat TM, NOAA AVHRR, SSM/I TM, NOAA AVHRR, SSM/I)  
•	Neither Neither - Tropical Rainfall Mapping Mission (TRMM), Tropical Rainfall Mapping Mission (TRMM), +/- 35deg 

### Bands (move to EM spectrum)
### Hyperspectral (move to EM spectrum)
resolution

graphics
### Environmental Data  
(move after GEE)
<br>

## Module 2 - GEE (software and implementing RS intro)
### Setting up GEE
First, you must request to set up an account with Google Earth Engine (GEE). Start [here](https://earthengine.google.com/), and then click “Sign Up” at the top right of the page. It will ask for the institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).



### Exploring interface using the theoretical concepts above
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

The "scripts" (1.) tab contains the code files for past saved projects. To begin a new file, click the "NEW" button and choose the intended format supply a descriptive name.  You can also create a folder or repository if desired to organize projects. For the purposes of this workshop, we will create a folder titled “RS Workshop.” All files created and used during the workshop should be placed in this folder. 

Under the “Docs” (2.) tab, there is a comprehensive list of the various functions and algorithms available in GEE, along with explanations of their inputs and outputs. GEE has further explanation and examples of how to use the "Docs" at this [link](https://developers.google.com/earth-engine/guides/getstarted#earth-engine-algorithms).

The “Assets” (3.) tab allows for user to load in their own images (GeoTIFF or TFRecord) or tables (shapefiles or CSVs). These will show up under the "Tasks" (10.) tab when uploading to show progress. The “Tasks” tab is also where any exports from GEE will run.

The “Inspector” (12.) tab gives information about the map, such as coordinates or scale. Once images or image collections have been added to the map, these will also have details that show up under this tab.

The “Console” (11.) contains anything that has been printed or any errors existing in the code.

The search bar (4.) allows the user to find publicly available datasets to utilize for their own analysis. Use keywords such as satellite name or desired parameter to find a relevant dataset.

Imports from the search bar or assets show up in an “imports” tab at the top of the code editor. You can change the automatically supplied name of the object (e.g. "imageCollection") to improve comprehensibility in your code (e.g. Landsat8Collection). Geometry tools (14.) allow the user to draw directly on the map to specify a region of interest to which analysis will be applied, which will also appear in the "imports" tab.

Bands in datasets (e.g. Landsat) allow for calculation of these remote sensing variables:

Parameters can be established, typically as color palettes, by the user to visualize the data on the map.

Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection. Any layers that have been added to the map will appear listed under the "Layer Manager" (13.), where the user can turn layers on and off and adjust visualization parameters. The user can zoom in and out on the map using the "zoom" feature (15.).

Once the script has been written and completed by the user, the "run" button (7.) is pressed to execute the code. To ensure that the code does not accidentally get deleted, there is a "save" (6.) option, which should be used when important changes have been made to the code. There is also a "get link" option (5.) in order to copy the code to send it to other users for collaboration.

For any issues or questions that may need to be resolved within GEE, there is a Help button (8.) as well as a Feedback option (9.) to reach out directly to Google.

### Exercises in GEE to play with RS data  
<br>
Import a dataset (such as MCD12Q1.006 MODIS Land Cover Type Yearly Global 500m) and add layer on map 
Import a shapefile as an asset (e.g. Ghana)


## Module 3 - Commonly Used Indices and Variables for Environmental Analysis
Remote sensing indices serve the purpose of providing measurable indicators of environmental conditions and changes. These indices can be calculated using measurable wavelength data, which is often provided by satellites or sensors. There are distinct "bands" that are provided by that satellites that represent the specific wavelengths, such as near infrared (NIR) or shortwave infrared (SWIR).

Environmental variables also provide key data for land-based analysis. These can be gathered from various satellites that read climatic and ecological conditions and subsequently communicate these as datasets.

### Formulation, use/purpose, and significance
A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). Some commonly used indices include albedo, enhanced vegetation index (EVI), and normalized difference vegetation index (NDVI). Additionally, environmental variables These provide vital information on environmental conditions and can be useful in monitoring land cover changes.

Environmental variables are commonly utilized to predict weather events, monitor climte, and measure variability. Variables such as precipitation, solar radiation, and land surface temperature (LST) are frequently used in environmental analysis.
### Exercises in GEE to play with indices  
Look at MODIS vegetation dataset (MOD13A2.006 Terra Vegetation Indices 16-Day Global 1km) to see NDVI and EVI values
Use Landsat dataset to calculate Albedo or NDVI

## Module 4 - Land Cover Classification
### Using indices – simple classification; accuracy & metrics
### Exercises in GEE to play with classification & temporal changes in indices for different classes (Ag/Forest/Urban)
<br>

## Module 5 - Statistics 
### Spatial statistics
### Trend analysis
### Relationships
### Linkages
<br>

# Advanced concepts in remote sensing with application to LUCIS-OPEN 

## Module 6 - Weights 
## Module 7 - LUCIS-OPEN
