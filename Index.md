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
|     Near Infrared            |     0.75-1µm         |
|     Short-wave infrared 1    |     1-1.6µm          |
|     Short-wave infrared 2    |     1.6-2.5µm        |
|     Thermal Infrared         |     10.60–12.51µm    |

<br/>

**1.1 Hyperspectral**

![image](https://user-images.githubusercontent.com/87503837/130195843-a8aea0e9-def9-40c4-80ce-b562fd56e918.png)


**1.2 Exercises**

Download the following files and view them in QGIS. 

Start by creating a new project in QGIS. Next add the files by clicking the **Add Raster Layer** icon on the lefthand side of the interface. If you dont see the icon, right click the toolbar at the top of the page and make sure **Manage Layers Toolbar** is checked. Once you have added the two files, you should see them added as layer.  

What range of values do you see for the two files? 

<br/>

### 2. Remote sensing systems and sensors
**2.1 Sensors:** 

• **Active sensors** consist of a transmitter and a receiver that may (monostatic system) or may not be (bistatic system) co-located. It transmits a known signal at a particular wavelength and receives some portion of the signal in the direction of a receiver. In case of a monostatic system, the received signal is called “backscatter”. Examples include a camera with the flash, Light Detection and Ranging (LIDAR), Synthetic aperture radar (SAR). 

• **Passive Sensors** consist of receiver that receives naturally occurring EM energy from a target at a particular wavelength and direction. Examples include a camera without the flash and radiometers.

<br/>

<!--- 
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

<img align="center" src="https://user-images.githubusercontent.com/87503837/133616643-ba9e4e28-2811-4d02-bc5a-987a549af606.png" width="350" height="320">

-->

**2.2 Resolution:**

• **Spatial resolution** describes how far apart two targets have to be so that they are detected as separate signals. If the detectable distance is small, the resolution is called **high** or **fine** and if the detectable distance is large, the resolution is **low** or **coarse**. 

• **Temporal resolution** describes how often a sensor observes the same target. If the revisit time is small, i.e. the target is observed more frequently, the temporal resolution is considered high (e.g. SMAP at about 2-3 days). On the other hand if the revisit time is longer or infrequent, e.g. LandSat at about 16 days, the temporal resolution is low/coarse. Typically, finer spatial resolution is associated with infrequent coverage because it covers less area during each overpass. 

• **Radiometric resolution** describes the number of wavelengths observed. For example, multispectral sensors observe about 10s of bands (or wavelength regions) in the VI/NIR spectrum, providing discrete observations. In contrast, hyperspectral sensors or imaging spectrometers observe 100s of wavelengths in the VI/NIR spectrum and provide continuous observations.

Spectral sampling: Multispectral sensors

<img src="https://user-images.githubusercontent.com/87503837/133636464-24493df3-1c5d-405f-b7ec-10fe64cec5e7.png" width="500" height="320">

Spectral sampling: Hyperspectral sensors

<img src="https://user-images.githubusercontent.com/87503837/133636485-93336e1a-214b-4897-b1ca-c1206879b4e1.png" width="500" height="320">


<br/>

**2.3 Satellite Systems**

•	**Geo-stationary/geo stationary/geo-synchronous** : continuous coverage of synchronous : continuous coverage of one region one region only (meteorological applications, high Earth (meteorological applications, high Earth orbit of ~36000 km; low/coarser spatial resolution; ~36000 km; low/coarser spatial resolution; e.g GOES, Japanese GOES, Japanese GMS, European GMS, European Metosat Metosat)

•	**Polar orbiting** : 100s km, low Earth orbit, high/fine spatial resolution; repeat global resolution; repeat global coverage; e.g. coverage; e.g. Landsat Landsat, Landsat Landsat TM, NOAA AVHRR, SSM/I TM, NOAA AVHRR, SSM/I) 

•	**Neither** - Tropical Rainfall Mapping Mission (TRMM), Tropical Rainfall Mapping Mission (TRMM), +/- 35deg

<br/>

**2.4 Graphics:**


**2.5 Applications of Remote Sensing**
1. Land use/land cover mapping
2. Geological and soil mapping
3. Agriculture
4. Forestry
5. Rangeland
6. Water resource
7. Snow and ice
8. Urban and regional planning 
9. Wetland mapping
10. Wildlife ecology 
11. Archeological 
12. Environmental assesment and protection
13. Natural disaster assesement 

**Data Sources**
| Data type                                     | Source      |
|-----------------------------------------------|-------------|
| Albedo                                        | MODIS       |
| Evapotranspiration   (ET)                     | MODIS       |
| Land cover                                    | LANDSAT     |
| Land surface   temperature                    | MODIS       |
| NDVI                                          | MODIS       |
| Normalized difference vegetation index (NDVI) | LANDSAT     |
| Soil   properties - moisture                  | NASA-SMAP   |
| Soil   properties                             | AfSoilGrids |
| Topography                                    | USGS        |
| Ts                                            | MODIS       |
| NDVI                                          | MODIS       |
| Ts                                            | MODIS       |
| Albedo                                        | MODIS       |

A table of the bands from the Landsat satellite program are given below, with the differences between Landsat 5, 7, and 8 outlined. General uses for these bands are supplied, such as Land Use/Land Cover (LULC) and Land Surface Temperature (LST).

<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/134026792-d1f488cd-3630-4266-ad2f-ed7062e52982.png" width="500" height="600">
</p>
(M.U. Liaqat (February, 2016))


## Module 2 - Remote Sensing Applications using Google Earth Engine (GEE)
### 2.1 Setting up GEE
First, you must request to set up an account with Google Earth Engine (GEE):
* Start [here](https://earthengine.google.com/)
* click “Sign Up” at the top right of the page and input institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).



### 2.2 Exploring GEE interface using RS concepts from Module 1
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:

<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/55447fcbfc2f487ebaae8d1258e829ca1d">
    <img src="https://user-images.githubusercontent.com/84922404/135470199-719878b5-7cb6-4a7a-aacd-e40881cda2e3.JPG" alt= "GEE Tutorial" width="800">
  </a>
</p>
  
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

Further description of the components of the figure above:

**1. Scripts** 

• This tab contains the code files for past saved projects. To begin a new file, click the "NEW" button and choose the intended format supply a descriptive name.  You can also create a folder or repository if desired to organize projects. For the purposes of this workshop, we will create a folder titled “RS Workshop.” All files created and used during the workshop should be placed in this folder. 

**2. Docs**  

• Under the “Docs” tab, there is a comprehensive list of the various functions and algorithms available in GEE, along with explanations of their inputs and outputs. 

  • Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection. 
  
• GEE has further explanation and examples of how to use the "Docs" at this [link](https://developers.google.com/earth-engine/guides/getstarted#earth-engine-algorithms).

**3. Assets** 

• The “Assets” tab allows for user to load in their own images (GeoTIFF or TFRecord) or tables (shapefiles or CSVs). These will show up under the "Tasks" (10.) tab when uploading to show progress. The “Tasks” tab is also where any exports from GEE will run.

**4. Search Bar** 

• The search bar allows the user to find publicly available datasets to utilize for their own analysis. Use keywords such as satellite name or desired parameter to find a relevant dataset.

• Imports from the search bar or assets show up in an “imports” tab at the top of the code editor. You can change the automatically supplied name of the object (e.g. "imageCollection") to improve comprehensibility in your code (e.g. Landsat8Collection).

**5. Get Link**

• GEE contains a "get link" option in order to copy the code to share it with other users for collaboration.

**6. Save**

• To ensure that the code does not accidentally get deleted, there is a "save" option, which should be used when important changes have been made to the code.

**7. Run** 

• Once the script has been written and completed by the user, the "run" button is pressed to execute the code.

**8. Help** 

• For any issues or questions that may need to be resolved within GEE, there is a Help button.

**9. Feedback** 

• A feedback option is supplied to reach out directly to Google.

**10. Tasks**  

• Assets and exports from GEE will show up under the "Tasks" (10.) tab when uploading to show progress. 

**11. Console** 

• The “Console” contains anything that has been printed or any errors existing in the c

**12. Inspector** 

• The “Inspector” tab gives information about the map, such as coordinates or scale. Once images or image collections have been added to the map, these will also have details that show up under this tab.

**13. Layer manager**  

• Any layers that have been added to the map will appear listed under the "Layer Manager" (13.), where the user can turn layers on and off and adjust visualization parameters.

• Parameters can be established, typically as color palettes, by the user to visualize the data on the map. 

**14. Geometry tools** 

• Geometry tools allow the user to draw directly on the map to specify a region of interest to which analysis will be applied, which will also appear in the "imports" tab.

**15. Zoom**

• The user can zoom in and out on the map using the "zoom" feature.

### 2.3 Exercises in GEE to play with RS data 
#### Module 2 Exercise 1 ####
##### Description #####
In this exercise, we will cover satellite dataset visualization using Google Earth Engine.

##### Skills and Goals #####
* Understand how to import and filter a dataset in GEE

* Create a visual map using specific bands

* Identify satellite differences over various years and regions

##### Instructions #####
1. In Google Earth Engine, open the script "01_search_and_display."
2. Using the geometry tools, identify a region of interest (smaller than the size of a country) and draw a polygon around it. This will be imported into the code editor.
3. Choose two sets of dates over which satellite data will be collected: one set in the summer months (May through August) and one set in the winter months (December to March). Set the initial and end dates for each set to be about 3 months apart. 
5. Using the script as a guide, map the satellite images using your chosen region and dates of interest.
6. Questions: What differences do you notice between the data taken during the summer and winter? Change the cloud cover fraction filtered in GEE: what changes do you notice in the output? Change the band combinations in the visualization parameters (e.g. for Landsat 8 edit "bands: ['B5', 'B4', 'B3']" to "bands: ['B4','B3','B2']". What do you notice about the map output after this change?
7. Submit images/screenshots of your map.

##### Result #####
* Upon completion of the exercise, your submission should look similar to the file **here**.


## Module 3 - Common RS Indices and Environmental Variables
Remote sensing indices serve the purpose of providing measurable indicators of environmental conditions and changes. These indices can be calculated using measurable wavelength data, which is often provided by satellites or sensors. There are distinct "bands" that are provided by that satellites that represent the specific wavelengths, such as near infrared (NIR) or shortwave infrared (SWIR). 

Environmental variables also provide key data for land-based analysis. These can be gathered from various satellites that read climatic and ecological conditions and subsequently communicate these as datasets.

| Environmental Variables and Indices    | Sensor(s)   | Temporal Resolution     | Spatial Resolution
|------------------------------|----------------------|------------------|---------------------------|
|     EVI                     |MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_EVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_EVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_EVI#:~:text=These%20composites%20are%20created%20from,following%20year%20by%203%20days.) (8-Day EVI Composite generated from GEE)|16-Day; 8-Day|1 km; 30 m
|     NDVI                    |     MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_NDVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_NDVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDVI_) ([8-Day NDVI Composite generated from GEE])    | 16-Day; 8-Day | 1 km; 30 m
|     NDWI                    |    MODIS ([Terra Daily NDWI](https://developers.google.com/earth-engine/datasets/catalog/MODIS_MOD09GA_006_NDWI)); Landsat 8 ([8-Day NDWI Composite](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDWI) generated from GEE)    | Daily; 8-Day | 463 m; 30 m
|     Precipitation            |     Global Precipitation Measurement ([IMERG](https://developers.google.com/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_V06)) | Hourly | 10 km
|     Land Surface Temperature         |  MODIS ([MOD11A1.006 Terra Land Surface Temperature and Emissivity](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD11A1)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T2_SR), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T2_SR), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T2_SR) (Surface Reflectance Tier 1); | Daily; 16-Day | 1 km; 30 m


### 3.1 Formulation, use/purpose, and significance
A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). These provide vital information on environmental conditions and can be useful in monitoring land cover changes. Some commonly used indices include enhanced vegetation index (EVI), normalized difference vegetation index (NDVI), soil adjusted vegetation index (SAVI), normalized burn ration (NBR), and normalized difference water index (NDWI).

| Index   | Formulation | Use/Purpose  | Source
|-----------|-------------|--------------|-----------|
|NDVI|((NIR - Red) / (NIR + Red)) | Measure and monitor vegetation greenness| [2] 
|EVI| 2.5 * ((NIR - Red) / (NIR + 6.0 * Red - 7.5 * Blue + 1))| Measure and monitor vegetation greenness, corrects for light distortions in NDVI | [3]
|SAVI| ((NIR - Red) / (NIR + Red + 0.5)) * (1 + 0.5) | Correct NDVI for soil brightness influence | [4]
|NBR| (SWIR - NIR) / (SWIR + NIR) | Identify burned areas and measure burn severity | [5]
|NDWI| (Green-NIR)/(Green+NIR) |  Measure vegetation liquid water | [6]

An example of NDVI calculation and application is given in the image below:
<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135468275-adaf7a44-b8f7-4d4e-9276-625a7a59f9d4.png" width="400">
</p>

Environmental variables are commonly utilized to predict weather events, monitor climte, and measure variability. Variables such as precipitation, solar radiation, and land surface temperature (LST) are frequently used in environmental analysis.

* Precipitation is used in remote sensing to first understand precipitation trends and then analyze data to predict temporal and spatial occurrences of rainfall changes or extremes.
* Solar radiation data are important for analysis of ecological systems and vegetation trends.
* Land surface temperature (LST) acts as an indicator for temperature trends such as urban heat islands (UHIs) and climate change, and it can also be modeled to help predict other environmental parameters such as evapotranspiration and vegetative growth.


### 3.2 Exercises in GEE to play with RS data 
Look at MODIS vegetation dataset (MOD13A2.006 Terra Vegetation Indices 16-Day Global 1km) to see NDVI and EVI values
Use Landsat dataset to calculate Albedo or NDVI

## Module 4 - Land Cover Classification
### Using indices – simple classification; accuracy & metrics
### Exercises in GEE to play with classification & temporal changes in indices for different classes (Ag/Forest/Urban)
<br>

# Citations
1. Remote Sensing and Image Interpretation, 7th Edition, Lillesand, Kieffer, Chipman
2. https://earthobservatory.nasa.gov/features/MeasuringVegetation/measuring_vegetation_2.php
3. https://earthobservatory.nasa.gov/features/MeasuringVegetation/measuring_vegetation_4.php
4. usgs.gov/core-science-systems/nli/landsat/landsat-soil-adjusted-vegetation-index
5. https://www.usgs.gov/core-science-systems/nli/landsat/landsat-normalized-burn-ratio
6. Gao, Bo-cai. “NDWI—A Normalized Difference WATER Index for Remote Sensing of VEGETATION Liquid Water from Space.” Remote Sensing of Environment, vol. 58, no. 3, 1996, pp. 257–266., doi:10.1016/s0034-4257(96)00067-3. 
