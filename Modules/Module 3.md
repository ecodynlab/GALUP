# Module 3 - Common RS Indices and Environmental Variables

**What will you learn from this module?**

- Common indices and environmental variables and their roles in remote sensing data

- Working with examples of these indices in Google Earth Engine

## 1. What are Indices and Variables?
**Remote sensing indices** serve the purpose of providing measurable indicators of environmental conditions and changes. 
- These indices can be calculated using measurable wavelength data, which is often provided by satellites or sensors. 
- There are distinct "bands" that are provided by that satellites that represent the specific wavelengths, such as near infrared (NIR) or shortwave infrared (SWIR). 

**Environmental variables** also provide key data for land-based analysis. 
- These can be gathered from various satellites that read climatic and ecological conditions and subsequently communicate these as datasets. 
- The table below outlines common variables and indices, the sensors from which they are acquired, and the resolutions.

| Environmental Variables and Indices    | Sensor(s)   | Temporal Resolution     | Spatial Resolution
|------------------------------|----------------------|------------------|---------------------------|
|     EVI                     |MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_EVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_EVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_EVI#:~:text=These%20composites%20are%20created%20from,following%20year%20by%203%20days.) (8-Day EVI Composite generated from GEE)|16-Day; 8-Day|1 km; 30 m
|     NDVI                    |     MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_NDVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_NDVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDVI_) ([8-Day NDVI Composite generated from GEE])    | 16-Day; 8-Day | 1 km; 30 m
|     NDWI                    |    MODIS ([Terra Daily NDWI](https://developers.google.com/earth-engine/datasets/catalog/MODIS_MOD09GA_006_NDWI)); Landsat 8 ([8-Day NDWI Composite](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDWI) generated from GEE)    | Daily; 8-Day | 463 m; 30 m
|     Precipitation            |     Global Precipitation Measurement ([IMERG](https://developers.google.com/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_V06)) | Hourly | 10 km
|     Land Surface Temperature         |  MODIS ([MOD11A1.006 Terra Land Surface Temperature and Emissivity](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD11A1)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T2_SR), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T2_SR), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T2_SR) (Surface Reflectance Tier 1); | Daily; 16-Day | 1 km; 30 m


## 2. Formulation, Purpose, and Significance
:pushpin: A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). 
- These provide vital information on environmental conditions and can be useful in monitoring land cover changes. 
  - Some commonly used indices include
      > enhanced vegetation index (EVI)<br>
      > normalized difference vegetation index (NDVI)<br> 
      > soil adjusted vegetation index (SAVI)<br> 
      > normalized burn ration (NBR)<br> 
      > normalized difference water index (NDWI) <br>

<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135870925-6baf5423-4762-4bff-9a59-3d30d189d039.png" width="700">
</p>

- An example of NDVI calculation and application is given in the image below:
<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135468275-adaf7a44-b8f7-4d4e-9276-625a7a59f9d4.png" width="400">
</p>

  - Environmental variables are commonly utilized to 
      >predict weather events <br>
      >monitor climate <br> 
      >measure variability<br>

Variables such as **precipitation**, **solar radiation**, and **land surface temperature (LST)** are frequently used in environmental analysis.
- **Precipitation** is used in remote sensing to first understand precipitation trends and then analyze data to predict temporal and spatial occurrences of rainfall changes or extremes.
- **Solar radiation** data are important for analysis of ecological systems and vegetation trends.
- **LST** acts as an indicator for temperature trends such as urban heat islands (UHIs) and climate change, and it can also be modeled to help predict other environmental parameters such as evapotranspiration and vegetative growth.


## Exercise and Post-Module Survey (required)
This video may be useful in completing the exercises:
<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/484d4b1a68194a6cbf85b4f6d97c29cd1d" target="_blank" rel="noopener">
    <img src="https://user-images.githubusercontent.com/84922404/141213294-7439b0d8-13c8-4e75-84e6-ecf7de7cf994.png" alt= "GEE Tutorial" width="800">
  </a>
</p>

1. Please complete and submit [Exercise 1](https://github.com/ecodynlab/GALUP/blob/main/Exercises/M3_exercise1.md) for Module 3.
2. Please complete and submit [Exercise 2](https://github.com/ecodynlab/GALUP/blob/main/Exercises/M3_exercise2.md) for Module 3.
3. Submit the Post-Module [survey](https://ufl.qualtrics.com/jfe/form/SV_bpjF7THHLlhtWCO). 

</p>


##
**Next Section:**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; **Previous Section:**

<a href="Module 4.md" title="Module 4">Module 4</a> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="Module 2.md" title="Module 2">Module 2</a>

