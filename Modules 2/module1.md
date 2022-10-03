# Module 1 - Time Series Analysis 


**What will you learn from this module?**
- Time Series Concept
- Time Series Basics
- Techniques for Time Series Analysis in GEE

## 1. Introduction to Time Series Analysis
**Time series analysis** looks at landscape change as a dynamic process over several months, years, etc. Mapping the environment at various timescales can provide information about land monitoring parameters like land cover change trends and patterns in vegetation growth. Time series of satellite observations are used to derive environmental parameters to evaluate environmental conditions. <br>

**Common Applications of Time Series Analysis:**
- Identifying urban expansion
- Land cover changes
- Mapping deforestation
- Monitoring post-fire conditions

<p align="center">
<img src="https://user-images.githubusercontent.com/85199074/193483159-0a7eff47-d4d5-4dd9-81a6-6275ad535ec3.png">
</p>
<sub> Large portions of Yellowstone National Park were destroyed by fires that were started by lightning and human related activities in the summer of 1988. Increased greenness is evident in NDVI estimates over a 30-year period, showing recovery of vegetation across the burn scar. - NASA.</sub>

([Source](https://earthobservatory.nasa.gov/world-of-change/Yellowstone))<br>


## 2. Basics of Time Series 
- **Spatial/geospatial data** is information about locations and shapes of objects in a geographic coordinate system and is represented as shapes in the form of points, paths and surfaces. <br>
- **Temporal data** is data that represents a state in time. <br>
- **Spatio-temporal** databases host data collected across both space and time that describe a phenomenon in a particular location and period of time. 

<p align="center">
<img src="https://user-images.githubusercontent.com/87503837/151854688-12a69e04-c870-4273-88e6-4c30e7b9d7d5.png">
</p>

([Source](https://doi.org/10.1186/s40965-017-0038-z))<br>
MODIS NDVI and EVI

**Imagery Collection Guide:**
- Images should be collected at same time of day and same month or season to avoid seasonal/phenological differences.
- To minimize differences in sun angle, images should be taken around the same time of day.
- Seasonal trends result from differences in precipitation and temperature.
- Be aware of different annual weather conditions – For example, drought years vs. non-drought years.

**Types of Time Series Analysis**
- **Annual Trends:**
It is a yearly assessment undertaken for as many years as possible (availability of data). It is particularly useful for land use/land cover analysis over long periods of time.

<p align="center">
<img src="https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs10708-020-10302-4/MediaObjects/10708_2020_10302_Fig3_HTML.png">
</p>
<sub> Mangalore Taluk Land Use/Land Cover (LULC) for the years 1972-2018. </sub>

([Source](https://link.springer.com/article/10.1007/s10708-020-10302-4))<br>

- **Seasonal Trends:**
It is driven by annual temperature and/or precipitation to assess variation between seasons. It can measure change within a year timeframe and is useful in comparison of seasonal variation between years.

<p align="center">
<img src="https://user-images.githubusercontent.com/85199074/193489786-81894af7-5381-425a-8a8f-e9ac3fb019b5.png">
</p>
<sub> Snow cover monitoring in the Himalayas </sub>

([Source](https://appliedsciences.nasa.gov/join-mission/training/english/arset-using-google-earth-engine-land-monitoring-applications))<br>
 
## 3. Time Series Analysis in GEE

GEE has a variety of functions useful for time series analysis:
- filtering and compilation of data across large datasets over time. Refer to ([GALUP Training Module 2- Introduction to GEE](https://github.com/SERVIR-WA/GALUP/blob/master/training/2_rs/module2.md))<br>
- analysis using map visualizations and user interface generated charts and graphs
<p align="center">
<img src="https://developers.google.com/static/earth-engine/images/Charts_image_collection_05.svg">
</p>
<sub> Example chart of time series NDVI data from MODIS plotted in GEE from 2010 to 2019. </sub>

([Source](https://developers.google.com/earth-engine/guides/charts_image_collection))<br>

## 4. Exercises and Post-training Survey

- Please complete the [Exercise 1]
- Please complete the [Exercise 2]

- Please take this [post-training survey]
  
- Please submit your exercises [here]

## 5. What's Next?

Module 3 - Landcover Change Detection

