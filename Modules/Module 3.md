## Module 3 - Common RS Indices and Environmental Variables

What will you learn from this module?

• Some common indices and environmental variables and their roles in remote sensing data

• 

## 
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

<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135870925-6baf5423-4762-4bff-9a59-3d30d189d039.png" width="700">
</p>

An example of NDVI calculation and application is given in the image below:
<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135468275-adaf7a44-b8f7-4d4e-9276-625a7a59f9d4.png" width="400">
</p>

Environmental variables are commonly utilized to predict weather events, monitor climate, and measure variability. Variables such as precipitation, solar radiation, and land surface temperature (LST) are frequently used in environmental analysis.

* Precipitation is used in remote sensing to first understand precipitation trends and then analyze data to predict temporal and spatial occurrences of rainfall changes or extremes.
* Solar radiation data are important for analysis of ecological systems and vegetation trends.
* Land surface temperature (LST) acts as an indicator for temperature trends such as urban heat islands (UHIs) and climate change, and it can also be modeled to help predict other environmental parameters such as evapotranspiration and vegetative growth.


### 3.2 Exercises in GEE to play with RS data 
#### 3.2.1 Exercise 1
1. Using the script ["05_time_series"](https://github.com/ecodynlab/GALUP/wiki/Scripts#05_time_series), alter the variables "ST_DATE" and "END_DATE" to reflect a period of interest (try 1-2 years), and there will be three regions of interest to examine.
2. These regions will be designated by pre-set coordinates in the script labeled with four corners of a rectangle (e.g. xMin1,yMin1,xMax1,yMax1). However, you must comment out whichever two variables of "REG_GH" you do not want to analyze during a trial with "//" and keep the variable of interest for that region's trial.
3. Run the script, and for each region, take a screenshot of the time-series graph of NDVI values over the course of the given time period within the specified region. Submit the screenshot <a href="https://github.com/ecodynlab/GALUP/issues/new" title="here">here</a>\.
4. Questions: Do you notice any distinct patterns in NDVI levels over the course of the year(s)? What differences do you notice in NDVI between the regions? Input your answers in this **form**.

#### 3.2.2 Exercise 2
1. From the script "06_indices_images", choose two indices and specify them as the variables "IMG1" and "IMG2", respectively.
2. Choose a chosen time period (about 1 year) and over a chosen geometry (using the polygon tool). Tip: choose a smaller geometry size so that the image is not too large and will take less processing time.
3. Run the script export the images that show up under the "tasks" bar to Google Drive.
4. Download the images from Google Drive (they should be .tif files), and open QGIS. Upload the images as rasters to QGIS.
5. Look at the "Properties" of each image, and change the symbology to effectively visualize each index (e.g. green colorbar for NDVI, blue for NDWI, etc.).
6. Upload the images <a href="https://github.com/ecodynlab/GALUP/issues/new" title="here">here</a>\.

##
**Previous Section:** 

<a href="Module 2.md" title="Module 2">Module 2</a>

