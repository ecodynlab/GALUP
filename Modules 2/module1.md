# Module 1 - Time Series Analysis 
> **Instructor**: [Dr. Aditya Singh](https://abe.ufl.edu/people/faculty/aditya-singh/) (<ins>aditya01@<i></i>ufl.edu</ins>) <br>
> **Co-authors**: Silas Achidago (<ins>s.achidago@<i></i>ufl.edu</ins>) and Julie Peeling (<ins>juliepeeling@<i></i>ufl.edu</ins>)


**What will you learn from this module?**
- Time Series Analysis Concept and fundamentals
- Time Series Analysis Methods
- Techniques for Time Series Analysis in GEE

## 1. Introduction to Time Series Analysis
Geospatial **Time series analysis** techniques help monitor and quantify landscapes change across  across time and space. Mapping temporal changes can provide information on the rates, causes, and consequences or dynamic processes such as urbanization, land degradation, phenology, and trends in environmental parameters such as rainfall and temperature. <br>

**Common Applications of Time Series Analysis:**
- Identifying urban expansion,
- Mapping deforestation,
- Monitoring flood or fire-related damage,
- Indentifying regions experiencing changes in temperature or precipitation.

<p align="center">
<img src="https://www.mdpi.com/urbansci/urbansci-03-00026/article_deploy/html/images/urbansci-03-00026-g006.png">
</p>
<sub> Landcover changes for Greater Accra Metropolitan Area (GAMA) from the year 1991 to 2015.</sub>

([Source](https://www.mdpi.com/2413-8851/3/1/26#))<br>


## 2. Basics of Time Series Analysis
- **Spatial/geospatial data** is information on the location, shape, and extent of objects in a geographic space represented as points, paths, areas, or surfaces. <br>
- **Temporal data** are data that represent the state of a particular object at a given point of time. Temporal data collected over several intervals create time-series data.<br>
- **Spatio-temporal data** are data that describe the state of objects or processes across both space and time. 

<p align="center">
<img src="https://user-images.githubusercontent.com/87503837/151854688-12a69e04-c870-4273-88e6-4c30e7b9d7d5.png">
</p>

([Source](https://doi.org/10.1186/s40965-017-0038-z))<br>
MODIS NDVI and EVI

**Using Remote Sensing to Conduct Time Series Analyses:**
- In the context of remote sensing, time series analyses allow us to measure and quantify changes in spatio-temporal processes from space,
- For effective monitoring to occur, data need to: 1) have suitable spatial and spectral resolution to detect the phenomena, and 2) have a frequent-enough repeat interval to detect change.
- Assuming the object is detectable using a specific sensor, the timing of acquisition needs to be tuned to the rate of the process being studied. For example, discrete event detections (such as floods or fires) can be conducted by collecting images before and after that event has occurred. Images need to be spaced close in time for assessing rapidly changing phenomena, such as vegetation greenup after rain. For monitoring long-term changes, data can be aggregated over the time domain of interest, and then assessed on annual or monthly bases (urban expansion, temperature rise). 
- The availability of satellite data over different spatio-temporal resolutions therefore limits the kinds of proceses that can be studied.
- Some trends may need to be decomposed into their underlying components for generating insights into the dynamics. For example, temperature usually has a strong seasonal component in addition to potentially annual components in some regions.

**Types of Time Series Analysis**
- **Land cover trends:**
At the simplest, the relative change in the proportion of land cover types across time. When land cover maps are available, the user can calculate the proportions of landcover, and potentially aggregate them over administrative regions to generate a picture of differing trends in urbanization, agricultural expansion, or deforestation etc. Estimates of trends of land cover change are generally important for administrative and management applications.

<p align="center">
<img src="https://www.mdpi.com/land/land-09-00300/article_deploy/html/images/land-09-00300-g003.png">
</p>
<sub> Maps showing land cover change (LCC) characteristics in Kumasi (1986–2018)a. </sub>

([Source](https://www.mdpi.com/2073-445X/9/9/300/htm#))<br>

- **Seasonal/Annual Trends:**
Whereas land cover change can be considered a 'discrete' change in the state of a pixel or parcel of land, many processes vary continuously across both time and space. Temperature is a good example. Time series of temperature measurements can be analyzed for both seasonal variation (i.e. minimum/maximum annual temperature) or when strung together across many years, as annual trends (i.e. climate change).

<p align="center">
<img src="https://media.springernature.com/full/springer-static/image/art%3A10.1007%2Fs12665-022-10481-y/MediaObjects/12665_2022_10481_Fig9_HTML.png?as=webp">
</p>
<sub> Temperature analysis over the study period (1970–2020) in Southwestern Ghana </sub>

([Source](https://link.springer.com/article/10.1007/s12665-022-10481-y/figures/9))<br>

## 3. Methods for Change Mapping and Time Series Analysis
Several approaches can followed depending on the application context, for example:
- **Linear Models** - 
Linear time series analysis techniques are predicated on the assumption that the underlying process changes at a constant rate. For example, assessing the annual rate of change in land surface temperature across a city. In general, this involves fitting a straight line through time series of the observations of interest and evaluating the magnitude and direction of the slope of the fit.
- **Nonlinear Models** - 
Nonlinear time series models are employed when the time series cannot be adequately described by a straight line. For example, indicators of vegetation greenness usually have a strong seasonal component. Fitting a straight line through the data ignores intra-annual variations that might be important.
**Harmonic models**, also termed spectral analysis or Fourier analysis, allow the decomposition of the periodic signal into a series of sinusoidal functions, each defined by unique amplitude and phase values. See [this paper](https://www.isprs.org/proceedings/xxxiii/congress/part4/384_xxxiii-part4.pdf) for an excellent example.<br>
**Breakpoint Models** - Allow the automatic detection of breaks in time series data, and potentially the fitting of different linear and nonlinear models on either side of the break. 

## 4. Time Series Analysis in GEE

GEE has the functionality to derived both linear and harmonic trends from satellite imagery and environmental data. The techniques can be mixed and matched to model both simple trends, and to decompose complex trends into seasonal and annual components, and to detect and fit breakpoint models.
For the purposes of this training, we will focus on developing estimates of simple linear trends across regions. The user is directed to documentation on [**CCDC**](https://gee-ccdc-tools.readthedocs.io/en/latest/) for a more complex treatment of harmonic time series components for land cover mapping, and to [**LandTrendr**](https://emapr.github.io/LT-GEE/) for utilizing breakpoints for detection landcover change.
We will follow the following steps:
- a) Identify and collect a time series of interest,
- b) Find a location of interest, extract a time series and plot a chart,
- c) Export the chart in excel, and fit a linear trend to it,
- d) Fit linear trends to all pixels in the area of interest to assess rates of change.
To do this, follow the instructions on:
- Filtering and compilation of data across large datasets over time. Refer to ([GALUP Training Module 2- Introduction to GEE](https://github.com/SERVIR-WA/GALUP/blob/master/training/2_rs/module2.md))<br>
- Visualization of data, generate charts
<p align="center">
<img src="https://developers.google.com/static/earth-engine/images/Charts_image_collection_05.svg">
</p>
<sub> Example chart of time series NDVI data from MODIS plotted in GEE from 2010 to 2019. </sub>

([Source](https://developers.google.com/earth-engine/guides/charts_image_collection))<br>

**4.1 Video tutorial for the section 3.1** <br>

**4.2 Running Time Series Analysis**<br>
- In the following example, we will use GEE to run a Time Series Analysis and print a chart to show results for a selected area in Ghana. Please use the video tutorial in **Section 4.1** to follow along.

- Copy the script [Time Series Analysis (Linear Fit)](https://github.com/ecodynlab/GALUP/wiki/Scripts#05_linear_fit) and paste into the GEE code editor. This is the same script that will be used in Exercise with slight alterations necessary to complete the Exercise.
- The script includes:<br>
  a. Defining variables for dates of interest: **ST_DATE** and **EN_DATE** <br>
  b. Defining the region of interest using 4 coordinates: **Longitude_min**, **Latitude_min**, **Longitude_max**, **Latitude_max** or draw using drawing tools <br>
  c. Filtering the data product by the **region** and **dates of interest**. <br>
  d. Creating a function to add an **NDVI** band to an image collection. <br>
  e. Display the result. <br>
  f. Define the **chart** and **print**. <br>
   

## 5. Exercises and Post-training Survey

- Please complete the [Exercise 1](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise1.md)
- Please complete the [Exercise 2](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise2.md)

- Please take this [post-module survey]

## 6. What's Next?

Module 2 - [Change Detection](module2.md)

## 7. Other Useful Resources
 1. [Cloud-Based Remote Sensing with Google Earth Engine](https://www.eefabook.org/go-to-the-book.html)<br>
 2. [NASA ARSET: Time Series Analysis](https://www.youtube.com/watch?v=RqVselZ5hKM&t=3695s)<br>
