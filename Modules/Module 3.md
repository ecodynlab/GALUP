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
A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). These provide vital information on environmental conditions and can be useful in monitoring land cover changes. Some commonly used indices include enhanced vegetation index (EVI), normalized difference vegetation index (NDVI), soil adjusted vegetation index (SAVI), normalized difference built-up index (NDBI), and normalized difference water index (NDWI).

| Index   | Formulation | Use/Purpose  | Source
|-----------|-------------|--------------|-----------|
|NDVI|((NIR - Red) / (NIR + Red)) | Measure and monitor vegetation greenness| [2] 
|EVI| 2.5 * ((NIR - Red) / (NIR + 6.0 * Red - 7.5 * Blue + 1))| Measure and monitor vegetation greenness, corrects for light distortions in NDVI | [3]
|SAVI| ((NIR - Red) / (NIR + Red + 0.5)) * (1 + 0.5) | Correct NDVI for soil brightness influence | [4]
|NDBI| (SWIR - NIR) / (SWIR + NIR) | Map urban built-up areas | [5]
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
