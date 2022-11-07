# Module 0 - A recap of Introduction to Satellite Remote Sensing I
## 1. What did we learn
### Definition
**Remote sensing** is the science and art of obtaining information about an object, area, or phenomenon through the analysis of data acquired by a device that is not in contact with the object, area, or phenomenon under investigation<sup>1</sup>. Modern day remote sensing started with the advent of radar, sonar, and thermal infrared detection systems during World War II. Since then, detectors have been expanded to obtain information from most of the bands in the EM spectrum, with a variety of applications spanning from military use to agriculture. <br> 

### Types of Resolutions: <br>
- **Spatial resolution** describes how far apart two targets have to be so that they are detected as separate signals.<br>
- **Temporal resolution** describes how often a sensor observes the same target . <br>
- **Radiometric resolution** describes the number of wavelengths observed. For example, in the Figures below, a multispectral sensor observing about 10s of discrete bands and a hyperspectral sensor observing 100s of bands in the optical/NIR region.<br>
 
<br/>

<p align="center"> <b> Spectral sampling: Multispectral sensors (left) and Hyperspectral sensors (right) </b> <p>

<p align="center"> 
<img src="https://user-images.githubusercontent.com/87503837/133636464-24493df3-1c5d-405f-b7ec-10fe64cec5e7.png" width="400" height="220"><img src="https://user-images.githubusercontent.com/87503837/133636485-93336e1a-214b-4897-b1ca-c1206879b4e1.png" width="400" height="220"> 
 </p>
 
<br/>

<p align="center"> 
  <img src = "https://user-images.githubusercontent.com/87503837/130195843-a8aea0e9-def9-40c4-80ce-b562fd56e918.png"/>
</p> <br/>

### Data Sources 
Satellite data can be obtained from multiple sources, some important repositories are:
- <a href="https://earthexplorer.usgs.gov/">USGS Earth Explorer</a>
- <a href="https://search.earthdata.nasa.gov/search?ac=true">NASA Earthdata Search</a>
- <a href="https://worldview.earthdata.nasa.gov/">NASA Worldview</a>
- <a href="https://scihub.copernicus.eu/dhus/#/home">Copernicus Open Access Hub</a>
<br>

## 2. Setting up GEE 
Please request an account with Google Earth Engine (GEE) as follows:
- Go to the GEE webpage [here](https://earthengine.google.com/)
- Select “Sign Up” at the top right of the page and input institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).

:pushpin: Approval may not happen immediately, so please be sure to sign up in advance of the workshop to provide a few days for completion.

## 3. Exploring GEE Interface

The video and Figure below show general interface functions for GEE. Further description of the components of the Figure can be found [here](https://github.com/SERVIR-WA/GALUP/wiki/GEE-Interface). 

<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/55447fcbfc2f487ebaae8d1258e829ca1d" target="_blank">
    <img src="https://user-images.githubusercontent.com/84922404/135470199-719878b5-7cb6-4a7a-aacd-e40881cda2e3.JPG" alt= "GEE Tutorial" width="800">
  </a>
</p>
  
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

:pushpin: In this workshop, we will be programming in the GEE [code editor](https://code.earthengine.google.com/) that uses the JavaScript language. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript Application Programming Interface (API).

## 4. RS Indices
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
  
  
- The Table below provides reflectances used to calculate the above indices. 


<p align="center">
<img src="https://user-images.githubusercontent.com/87503837/142231637-77253803-79a2-4f34-939a-f8d234d796bb.png" height="50%" width="50%">
</p>


:pushpin: A database of remote sensing indices and their respective sensors and areas of application are compiled [here](https://www.indexdatabase.de/). 
   

## 5. Exercises and Post-training Survey

- Please complete the [Exercise 0](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise0.md)

- Please submit your exercises [here]

## 6. What's Next?

Module 1 - [Time Series Analysis](module1.md)

## 7. Other Resources

Kindly refer to Workshop 2 - [Introduction to Satelite Remote Senisng I](https://github.com/SERVIR-WA/GALUP/tree/master/training/2_rs)
