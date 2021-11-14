# Module 3 - Common RS Indices and Environmental Variables

**What will you learn from this module?**

- What are some common RS indices and environmental variables and their role in land use planning and environmental assessment,
- Generate, visualize, and download these indices from Google Earth Engine.

## 1. RS Indices
**Remote sensing indices** (or spectral indices) are arithmentic combinations of reflectance at two or more bands that help provide measurable estimates of the relative abundance of indicators of interest. Vegetation indices (such as the normalized difference vegetation index: NDVI) are the most widely known, but indices can be formulated for tracking burn areas, exposed soil or built-up areas.
- Spectral/Image indices are generally calculated using simple mathematical transformations (addition, subtraction, division) conducted on satellite bands of specific wavelength regions. Values of image indices can range from -1 - +1 (normalized difference indices), to arbitrary scales for other ratio-based indices. See <a href="https://www.usgs.gov/core-science-systems/nli/landsat/landsat-surface-reflectance-derived-spectral-indices?qt-science_support_page_related_con=0#qt-science_support_page_related_con">this link</a> for a good introduction to indices that can be obtained using Landsat data.

- Some commonly used RS indices include
      <blockquote>
      Normalized Difference Vegetation Index (NDVI)<br>
      Enhanced Vegetation Index (EVI)<br>
      Soil Adjusted Vegetation Index (SAVI)<br>
      Modified Soil Adjusted Vegetation Index (MSAVI)<br>
      Normalized Difference Moisture Index (NDMI)<br>
      Normalized Burn Ratio (NBR)<br>
      Normalized Burn Ratio 2 (NBR2)<br>
      Normalized Difference Snow Index (NDSI)<br>
      </blockquote>
  
  
- The Table below provides reflectances used to calculate the above indices and their uses.
<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135870925-6baf5423-4762-4bff-9a59-3d30d189d039.png" width="700">
</p>

- For example, NDVI is a combination of reflectances in the red and NIR wavelengths as shown in the Figure below. Healthy vegetation reflects more solar radiation in the NIR wavelength than unhealthy vegetation. Thus, the NDVI for healthy vegetation is higher. 
<p align="center">
<img src="https://user-images.githubusercontent.com/84922404/135468275-adaf7a44-b8f7-4d4e-9276-625a7a59f9d4.png" width="400">
</p>

:pushpin: A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). 

## 2. Sources for Preprocessed Indices for Regional-scale Applications
- The Table below provides the spatial and temporal resolutions of the RS indices and environment variables, along with their sensors/sources.

|  RS Indices and Environmental Variables     | Sensor(s)   | Temporal Resolution     | Spatial Resolution
|------------------------------|----------------------|------------------|---------------------------|
|     EVI                     |MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_EVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_EVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_EVI#:~:text=These%20composites%20are%20created%20from,following%20year%20by%203%20days.) (8-Day EVI Composite generated from GEE)|16-Day; 8-Day|1 km; 30 m
|     NDVI                    |     MODIS ([MOD13A2.006 Terra Vegetation Indices](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD13A2)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T1_8DAY_NDVI), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T1_8DAY_NDVI), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDVI_) ([8-Day NDVI Composite generated from GEE])    | 16-Day; 8-Day | 1 km; 30 m
|     NDWI                    |    MODIS ([Terra Daily NDWI](https://developers.google.com/earth-engine/datasets/catalog/MODIS_MOD09GA_006_NDWI)); Landsat 8 ([8-Day NDWI Composite](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T1_8DAY_NDWI) generated from GEE)    | Daily; 8-Day | 463 m; 30 m
|     Precipitation            |     Global Precipitation Measurement ([IMERG](https://developers.google.com/earth-engine/datasets/catalog/NASA_GPM_L3_IMERG_V06)) | Hourly | 10 km
|     Land Surface Temperature         |  MODIS ([MOD11A1.006 Terra Land Surface Temperature and Emissivity](https://developers.google.com/earth-engine/datasets/catalog/MODIS_006_MOD11A1)); Landsat [5](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LT05_C01_T2_SR), [7](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LE07_C01_T2_SR), [8](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C01_T2_SR) (Surface Reflectance Tier 1); | Daily; 16-Day | 1 km; 30 m

## 3. Other Environment Variables
- These provide vital information on environmental conditions impacting land cover changes. They are commonly used to monitor and predict weather events and measure variability
- Commonly used variables include
      <blockquote>
      Precipitation <br>
       Downward Solar Radiation (DSR) <br>
       Land Surface Temperature (LST) <br>
      </blockquote>
 
 - **Precipitation** product is retrieved from backscatter observed by two RADAR operating at wavelengths of 0.84 cm and 2.2 cm. Remotely sensed precipitation helps understand distribution and trends of rainfall across space and time. Models can be used analyze precipitation data and make predictions. <br>
- **Solar radiation** product is retrieved using optical and infrared spectral channels, as well data regarding (reflectance) and atmospheric composition. <br>
- **LST** product is obtained from emission observations in ther TIR wavelengths. It acts as an indicator for temperature trends such as urban heat islands (UHIs) and climate change. In addition it is used to predict other parameters such as evapotranspiration and vegetation health.

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

