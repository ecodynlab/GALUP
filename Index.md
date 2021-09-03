# Introduction to Remote Sensing Concepts

## Module 1 - Basic remote sensing 
### 1. EM spectrum 
The **electromagnetic spectrum** is the entire distribution of electromagnetic radiation according to frequency or wavelength. **Observed energy** or **radiation** is primarily sensitive to molecular resonances in the to molecular resonances in the surface layer surface layer of target. **Emitted**, **reflected**, and **backscattered radiation** is sensitive to temperature distribution, geometric, and electric properties of surface or volume. 

<p align="center">
<img width="500" height="400" src="https://user-images.githubusercontent.com/87503837/130260547-5c76cddd-c913-4adb-b183-c50604eee563.png">
</p>

The human eye is only able to detect wavelengths in the visible light range. However, many insects see in the 300 to 650 nm wavelength and can detect ultraviolet light because   they have special photoreceptors in their eyes.   


![image](https://user-images.githubusercontent.com/87503837/130195843-a8aea0e9-def9-40c4-80ce-b562fd56e918.png)

**1.1. Bands**

**1.2 Hyperspectral**



### 2. Remote sensing systems and sensors
**2.1 Sensors:** 

**Active sensors** consist of a transmitter and a receiver that may (monostatic system) or may not be (bistatic system) co-located. It transmits a known signal at a particular wavelength and receives some portion of the signal in the direction of a receiver. In case of a monostatic system, the received signal is called “backscatter”. Examples include a camera with the flash, Light Detection and Ranging (LIDAR), Synthetic aperture radar (SAR). **Passive Sensors** consist of receiver that receives naturally occurring EM energy from a target at a particular wavelength and direction. Examples include a camera without the flash and radiometers. 



**2.2 Resolution:**

**Spatial** describes how far apart two targets have to be so that they are detected as separate signals. If the detectable distance is small, the resolution is called **high** or **fine** and if the detectable distance is large, the resolution is **low** or **coarse**. Temporal describes how often a sensor observes the same target.If the revisit time is small, i.e. the target is observed more frequently, the temporal resolution is considered high (e.g. SMAP at about 2-3 days). On the other hand if the revisit time is longer or infrequent, e.g. LandSat at about 16 days, the temporal resolution is low/coarse. Typically, finer spatial resolution is associated with infrequent coverage because it covers less area during each overpass.

• Radiometric
It describes the number of wavelengths observed. For example, multispectral sensors observe about 10s of bands (or wavelength regions) in the VI/NIR spectrum, providing discrete observations. In contrast, hyperspectral sensors or imaging spectrometers observe 100s of wavelengths in the VI/NIR spectrum and provide continuous observations.

**2.3 Graphics:**

### 3. Environmental data  
(move after GEE)
<br>

## Module 2 - GEE (software and implementing RS intro)
### Setting up GEE
First, you must request to set up an account with Google Earth Engine (GEE). Start [here](https://earthengine.google.com/), and then click “Sign Up” at the top right of the page. It will ask for the institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).



### Exploring interface using the theoretical concepts above
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:
![GEEinterface](https://user-images.githubusercontent.com/84922404/130262824-4a91fac4-631f-4393-a673-79a07018bb45.png)

The "scripts" tab contains the code files for past saved projects. To begin a new file, click the "NEW" button and choose the intended format supply a descriptive name.  You can also create a folder or repository if desired to organize projects. For the purposes of this workshop, we will create a folder titled “RS Workshop.” All files created and used during the workshop should be placed in this folder. 

Under the “Docs” tab, there is a comprehensive list of the various functions and algorithms available in GEE, along with explanations of their inputs and outputs. GEE has further explanation and examples of how to use the "Docs" at this [link](https://developers.google.com/earth-engine/guides/getstarted#earth-engine-algorithms).

The “Assets” tab allows for user to load in their own images (GeoTIFF or TFRecord) or tables (shapefiles or CSVs). These will show up under the "Tasks" tab when uploading to show progress. The “Tasks” tab is also where any exports from GEE will run.

The “Inspector” tab gives information about the map, such as coordinates or scale. Once images or image collections have been added to the map, these will also have details that show up under this tab.

The “Console” contains anything that has been printed or any errors exsting in the code.

The search bar allows the user to find publicly available datasets to utilize for their own analysis. Use keywords such as satellite name or desired parameter to find a relevant dataset.

Imports from the search bar or assets show up in an “imports” tab at the top of the code editor. You can change the automatically supplied name of the object (e.g. "imageCollection") to improve comprehensibility in your code (e.g. Landsat8Collection).

Bands in datasets (e.g. Landsat) allow for calculation of these remote sensing variables:

Can use parameters to visualize the data (use colors)

Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection

### Exercises in GEE to play with RS data  
<br>
Look at MODIS vegetation dataset (MOD13A2.006 Terra Vegetation Indices 16-Day Global 1km) to see NDVI and EVI values

Import MODIS classification and add layer on map (MCD12Q1.006 MODIS Land Cover Type Yearly Global 500m)


## Module 3 - Indices (Environmental Datasets and Variables)
Remote sensing indices serve the purpose of providing measurable indicators of environmental conditions and changes.
### Formulation, use/purpose, and significance
A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/).
### Exercises in GEE to play with indices  
<br>

## Module 4 - Classification
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
