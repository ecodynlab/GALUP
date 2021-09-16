# Satellite Remote Sensing for Land-Use Planning

## Module 1 - Introduction to Remote Sensing 

_Remote sensing is the science and art of obtaining information about an object, area, or phenomenon through the analysis of data acquired by a device that is not in contact with the object, area, or phenomenon under investigation<sup>1</sup>._

Modern day remote sensing started with the advent of radar, sonar, and thermal infrared detection systems during WWII. Since then, detectors have been expanded to  run on most of the EM spectrum and variety of applications spanning from military use to agriculture. 

### 1. EM spectrum 
• **Electromagnetic spectrum** is the entire distribution of electromagnetic radiation according to frequency or wavelength. 

• **Observed energy** or **radiation** is primarily sensitive to molecular resonances in the to molecular resonances in the surface layer surface layer of target. 

• **Emitted**, **reflected**, and **backscattered radiation** is sensitive to temperature distribution, geometric, and electric properties of surface or volume. 

•**Near infrared (NIR)** is defined from 750 nm to 1400 nm and **shortwave infrared (SWIR)** from 1400 nm to 3000 nm.


<p align="center">
<img width="604" height="207" src="https://user-images.githubusercontent.com/87503837/132062813-8bd2faa0-336c-4fc7-b3f1-f8ae62822e9b.png">
</p>

The human eye is only able to detect wavelengths in the visible light range. However, many insects see in the 300 to 650 nm wavelength and can detect ultraviolet light because   they have special photoreceptors in their eyes.   

**Scattering in atm**

**Absorption in atm**

<br/>

| Band                         | Wavelength           |
|------------------------------|----------------------|
|     Blue                     |     0.45-0.51µm      |
|     Green                    |     0.53-0.59µm      |
|     Red                      |     0.64-0.67µm      |
|     Near Infrared            |     0.75-2.5µm       |
|     Short-wave   infrared    |     0.50-0.68µm      |
|     Cirrus                   |     1.36 -1.38µm     |
|     Thermal Infrared         |     10.60–12.51µm    |

<br/>

**1.1 Hyperspectral**

![image](https://user-images.githubusercontent.com/87503837/130195843-a8aea0e9-def9-40c4-80ce-b562fd56e918.png)

Spectral sampling: Multispectral sensors
![image](https://user-images.githubusercontent.com/87503837/133636464-24493df3-1c5d-405f-b7ec-10fe64cec5e7.png)

Spectral sampling: Hyperspectral sensors
![image](https://user-images.githubusercontent.com/87503837/133636485-93336e1a-214b-4897-b1ca-c1206879b4e1.png)


<br/>

### 2. Remote sensing systems and sensors
**2.1 Sensors:** 

• **Active sensors** consist of a transmitter and a receiver that may (monostatic system) or may not be (bistatic system) co-located. It transmits a known signal at a particular wavelength and receives some portion of the signal in the direction of a receiver. In case of a monostatic system, the received signal is called “backscatter”. Examples include a camera with the flash, Light Detection and Ranging (LIDAR), Synthetic aperture radar (SAR). 

• **Passive Sensors** consist of receiver that receives naturally occurring EM energy from a target at a particular wavelength and direction. Examples include a camera without the flash and radiometers.

<br/>

**Types of Detectors:** 

**Thermal detectors**

• absorb incident flux and undergo temperature changes

• the power in absorbed radiation is typically small, and so the detector itself should be small to have a low heat capacity

• Ex: Bolometer 

![image](https://user-images.githubusercontent.com/87503837/133616355-0ff8f5fd-2d57-4e97-b781-786353fa934e.png)

**External Photo-effect detectors**

• has photocathode where incident light is partially absorbed and generates photoelectrons

• Ex: Photomultiplier Tube (PMT)


<img src="https://user-images.githubusercontent.com/87503837/133625438-5593a350-5cd9-414a-bd1e-24f23e051fc4.png" width="500" height="320">

**Internal Photo-effect detectors**

• semiconductors in which the electons undergo internal energy level transitions when they absorb an electron

• consists of **photoconductive detectors** and **photovoltaic detectors**

• Ex: 

<img src="https://user-images.githubusercontent.com/87503837/133616643-ba9e4e28-2811-4d02-bc5a-987a549af606.png" width="350" height="320">


**2.2 Resolution:**

• **Spatial resolution** describes how far apart two targets have to be so that they are detected as separate signals. If the detectable distance is small, the resolution is called **high** or **fine** and if the detectable distance is large, the resolution is **low** or **coarse**. 

• **Temporal resolution** describes how often a sensor observes the same target. If the revisit time is small, i.e. the target is observed more frequently, the temporal resolution is considered high (e.g. SMAP at about 2-3 days). On the other hand if the revisit time is longer or infrequent, e.g. LandSat at about 16 days, the temporal resolution is low/coarse. Typically, finer spatial resolution is associated with infrequent coverage because it covers less area during each overpass. 

• **Radiometric resolution** describes the number of wavelengths observed. For example, multispectral sensors observe about 10s of bands (or wavelength regions) in the VI/NIR spectrum, providing discrete observations. In contrast, hyperspectral sensors or imaging spectrometers observe 100s of wavelengths in the VI/NIR spectrum and provide continuous observations.

(Include example file for demonstration?)

<br/>

**2.3 Satellite Systems**

•	**Geo-stationary/geo stationary/geo-synchronous** : continuous coverage of synchronous : continuous coverage of one region one region only (meteorological applications, high Earth (meteorological applications, high Earth orbit of ~36000 km; low/coarser spatial resolution; ~36000 km; low/coarser spatial resolution; e.g GOES, Japanese GOES, Japanese GMS, European GMS, European Metosat Metosat)

•	**Polar orbiting** : 100s km, low Earth orbit, high/fine spatial resolution; repeat global resolution; repeat global coverage; e.g. coverage; e.g. Landsat Landsat, Landsat Landsat TM, NOAA AVHRR, SSM/I TM, NOAA AVHRR, SSM/I) 

•	**Neither** - Tropical Rainfall Mapping Mission (TRMM), Tropical Rainfall Mapping Mission (TRMM), +/- 35deg

<br/>

**2.4 Graphics:**

**Data Sources**
| Topic                                         | Source                                                                                                                                   | Temporal range                 |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Administrative   boundaries                   | Global administrative   areas and boundaries (GADM)                                                                                      | 2020                           |
| Albedo                                        | MODIS/MCD43B3                                                                                                                            | 2001, 2005 ,2009,   2013, 2016 |
| Albedo                                        | MODIS/MCD43A3 v006                                                                                                                       | 2001, 2005 ,2009,   2013, 2016 |
| Evapotranspiration   (ET)                     | MODIS/MOD16A2 v006                                                                                                                       | 2001, 2005 ,2009,   2013, 2016 |
| Health -   stunting in children               | DHS UNICEF                                                                                                                               | 2000, 2015                     |
| Health -   wasting prevalence in children     | DHS UNICEF                                                                                                                               | 2000, 2015                     |
| Land cover                                    | LANDSAT/LT05/C01/T1_SR,   USGS Landsat 5 Surface Reflectance Tier 1, LANDSAT/LC08/C01/T1_SR, USGS   Landsat 8 Surface Reflectance Tier 1 | 1990-2020                      |
| Land cover-2                                  | MODIS                                                                                                                                    | 2001, 2005 ,2009,   2013, 2016 |
| Land surface   temperature                    | LANDSAT/LT05/C01/T1_SR,   USGS Landsat 5 Surface Reflectance Tier 1, LANDSAT/LC08/C01/T1_SR, USGS   Landsat 8 Surface Reflectance Tier 1 | 1990-2020                      |
| Land surface   temperature                    | MODIS                                                                                                                                    | 2000, 2005, 2010,   2015, 2019 |
| Micrometeorogical   dataset                   | Trans-African   HydroMeteorological Observatory, African Rainfall Climatology                                                            |                                |
| NDVI                                          | MODIS/MOD13A1.005                                                                                                                        | 2001, 2005 ,2009,   2013, 2016 |
| Normalized difference vegetation index (NDVI) | LANDSAT/LT05/C01/T1_SR,   USGS Landsat 5 Surface Reflectance Tier 1, LANDSAT/LC08/C01/T1_SR, USGS   Landsat 8 Surface Reflectance Tier 1 | 1990-2020                      |
| Population   (rural)                          | LandScanTM                                                                                                                               | 2000-2018                      |
| Population   (urban)                          | Africapolis                                                                                                                              | 1950-2020                      |
| Road   checkpoints                            | CILSS                                                                                                                                    | 2018                           |
| Roads                                         | Open Street Map                                                                                                                          | 2010-2020                      |
| Socio-economic   indicators                   | SEDAC, Government of   Ghana                                                                                                             | 2010-2020                      |
| Soil   properties - moisture                  | NASA-SMAP, NASA/JAXA   AMSR-E, AMSR2                                                                                                     | 2000 - 2020                    |
| Soil   properties                             | AfSoilGrids                                                                                                                              |                                |
| Topography                                    | USGS/SRTMGL1_003                                                                                                                         | 2000                           |
| Ts                                            | MODIS/MOD11A1 v006                                                                                                                       | 2001, 2005 ,2009,   2013, 2016 |
| NDVI                                          | MODIS/MOD13A1.005                                                                                                                        | 2001, 2005 ,2009,   2013, 2016 |
| Ts                                            | MODIS/MOD11A2 v006                                                                                                                       | 2001, 2005 ,2009,   2013, 2016 |
| Albedo                                        | MODIS/MCD43B3                                                                                                                            | 2001, 2005 ,2009,   2013, 2016 |

## Module 2 - Remote Sensing Applications using Google Earth Engine (GEE)
### 2.1 Setting up GEE
First, you must request to set up an account with Google Earth Engine (GEE). Start [here](https://earthengine.google.com/), and then click “Sign Up” at the top right of the page. It will ask for the institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).



### 2.2 Exploring GEE interface using RS concepts from Module 1
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

**2.2.1 Scripts** 

• The "scripts" tab contains the code files for past saved projects. To begin a new file, click the "NEW" button and choose the intended format supply a descriptive name.  You can also create a folder or repository if desired to organize projects. For the purposes of this workshop, we will create a folder titled “RS Workshop.” All files created and used during the workshop should be placed in this folder. 

**2.2.2 Docs**  

• Under the “Docs” tab, there is a comprehensive list of the various functions and algorithms available in GEE, along with explanations of their inputs and outputs. 

  • Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection. 
  
• GEE has further explanation and examples of how to use the "Docs" at this [link](https://developers.google.com/earth-engine/guides/getstarted#earth-engine-algorithms).

**2.2.3 Assets** 

• The “Assets” tab allows for user to load in their own images (GeoTIFF or TFRecord) or tables (shapefiles or CSVs). These will show up under the "Tasks" (10.) tab when uploading to show progress. The “Tasks” tab is also where any exports from GEE will run.

**2.2.4 Search Bar** 

• The search bar allows the user to find publicly available datasets to utilize for their own analysis. Use keywords such as satellite name or desired parameter to find a relevant dataset.

• Imports from the search bar or assets show up in an “imports” tab at the top of the code editor. You can change the automatically supplied name of the object (e.g. "imageCollection") to improve comprehensibility in your code (e.g. Landsat8Collection).

**2.2.5 Get Link**

• GEE contains a "get link" option in order to copy the code to share it with other users for collaboration.

**2.2.6 Save**

• To ensure that the code does not accidentally get deleted, there is a "save" option, which should be used when important changes have been made to the code.

**2.2.7 Run** 

• Once the script has been written and completed by the user, the "run" button is pressed to execute the code.

**2.2.8 Help** 

• For any issues or questions that may need to be resolved within GEE, there is a Help button.

**2.2.9 Feedback** 

• A feedback option is supplied to reach out directly to Google.

**2.2.10 Tasks**  

• Assets and exports from GEE will show up under the "Tasks" (10.) tab when uploading to show progress. 

**2.2.11 Console** 

• The “Console” contains anything that has been printed or any errors existing in the c

**2.2.12 Inspector** 

• The “Inspector” tab gives information about the map, such as coordinates or scale. Once images or image collections have been added to the map, these will also have details that show up under this tab.

**2.2.13 Layer manager**  

• Any layers that have been added to the map will appear listed under the "Layer Manager" (13.), where the user can turn layers on and off and adjust visualization parameters.

• Parameters can be established, typically as color palettes, by the user to visualize the data on the map. 

**2.2.14 Geometry tools** 

• Geometry tools allow the user to draw directly on the map to specify a region of interest to which analysis will be applied, which will also appear in the "imports" tab.

**2.2.15 Zoom**

• The user can zoom in and out on the map using the "zoom" feature.

### 2.3 Exercises in GEE to play with RS data  
<br>
Import a dataset (such as MCD12Q1.006 MODIS Land Cover Type Yearly Global 500m) and add layer on map 
Import a shapefile as an asset (e.g. Ghana)


## Module 3 - Common RS Indices and Environmental Variables
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

## Module 5 - Statistical Analysis of Spatio-Temporal RS Data 
### Spatial statistics
### Trend analysis
### Relationships
### Linkages
<br>

# Advanced concepts in remote sensing with application to LUCIS-OPEN 

## Module 6 - Weights 
## Module 7 - LUCIS-OPEN

# Citations
1. Remote Sensing and Image Interpretation, 7th Edition, Lillesand, Kieffer, Chipman
