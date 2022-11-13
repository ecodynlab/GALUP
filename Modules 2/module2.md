# Module 2 - Change Detection

> **Instructor**: [Dr. Aditya Singh](https://abe.ufl.edu/people/faculty/aditya-singh/) (<ins>aditya01@<i></i>ufl.edu</ins>) <br>
> **Co-authors**: Silas Achidago (<ins>s.achidago@<i></i>ufl.edu</ins>) and Julie Peeling (<ins>juliepeeling@<i></i>ufl.edu</ins>)

**What will you learn from this module?**
- Introduction to change detection using remote sensing,
- Different ways change can be detected, choosing the best sensor combinations,
- Conducting change detection in GEE using a few common examples.

## 1. Introduction to Change Detection
**Change Detection** Is the generic term for utilizing remote sensing sensor(s) to detect, delineate, and measure the conversion of a landscape from one dominant type to another. Changes could be observed in the shape, size, or texture of patches of land depending on the magnitude of the change, and the characteristics of the sensor utilized. Examples include;
- Land degradation as a result of deforestation or overuse,
- Urban expansion,
- Flooding,
- Landscape scarring due to forest fires etc.

**Forms of Change** Landscape change can occur in many different ways, therefore, a detailed understanding of mechanism of change is required to determine the correct combination of techniques and sensors.

<p align="center">
<img src="https://user-images.githubusercontent.com/40871781/201491844-a3dd8fa8-2b9f-4ce4-b315-cd339e1d9c45.gif">
</p>
<sub align="center"> Continental-scale vegetation phenology tracked by MODIS.</sub> 

([Source](https://developers.google.com/earth-engine/tutorials/community/modis-ndvi-time-series-animation))<br>

- Directional change: e.g, Conversion of agriculture to urban: Needs high spatial resolution imagery, generally involving at least one band that can track vegetation (e.g. NIR)
- Cyclic change: e.g., Crop or grassland phenology: Needs high temporal resolution imagery so changes around critical growth stages can be captured, typically also using a vegetation tracking band (NIR),
- Multidirectional change: e.g., Deforestation folowed by forest regeneration: Needs moderate spatial and temporal resolution depending upon the magnitude of change. Having calendar-date imagery is useful when change needs to be tracked across multiple years.
- Between class changes: e.g., Forest to agriculture conversion: Typically needs high spatial and temporal resolution to be able to tell different growth stages apart,
- Within-class changes: e.g., Seasonal change in dominant grass species: Typically needs high spectral resolution to be able to tell different vegetation types apart

**Change Detection answers the questions;**
- How much and what kind of change has occurred?
- Where and when has change taken place?
- What are the trends in the change?

## 2. Change Detection Using Remote Sensing
At the most basic, remote sensing techniques track landscape change by tracking changes in spectral reflectance profiles of individual pixels. Differences in spectral characteristics inherent to different surfaces are exploited to differentiate between cover types. As an example, healthy vegetation has high reflectance in the near-infrared spectrum but low reflectance in the red spectrum. The widely used normalized difference vegetation index (NDVI = [NIR-Red]/[NIR+Red]) exploits these differences to track vegetation vigor. Moisture in vegetation also strongly absorbs shortwave radiation making these bands very useful for tracking water status in plants. Much like NDVI, differences in spectral characteristics can be exploited by combining different spectral bands into standardized indicies, with the bands determining which phenomenon can be best tracked. Note that change detection almost always requires imagery to be available at at least two different time periods.

<p align="left">
<img src="https://user-images.githubusercontent.com/85199074/194796915-95e941ba-75d1-4c58-aa52-2462e10d18ba.jpg">
</p>
<sub> Healthy vegetation has a large peak in the near infrared region, while soil or burned areas are much lower. Healthy vegetation also has low reflectance in the red and shortwave infrared regions in contrast with burned areas.</sub>

([Source](https://appliedsciences.nasa.gov/join-mission/training/english/arset-using-google-earth-engine-land-monitoring-applications))<br>

## 3. Change Detection Methods
**a**.  **Visual Analysis** - The first step in any change detection process - change can be detected through simple visual comparison using different combinations of bands followed by on-screen. While this technique is considered the most accurate becuase of direct human involvement, it is unsuitable for large areas as multiple digitizers can inject human bias into the process. Also, visual analysis cannot be relied upon when changes are subtle. 

**b**.  **Image Differencing** - When abrupt changes are expected, a simple differncing of bands, or selected image indices can often reveal areas of change. Image differencing is generally computed on a pixel-by-pixel basis and is executed across the full extent of two images. The pixel-based nature of image differencing allows for more precise identification of change. The difference image can then be scaled to ground observations using standard statistical techniques such as linear or logistic regression. This method is particularly useful for assessing change over continuous indices (such as those used to measure vegetation and soil). 
<p align="center">
<img src="https://user-images.githubusercontent.com/85199074/194987983-817db71d-207d-4624-a9bc-fcaf350750c9.png">
</p>

**c**.  **Image Sequences** - When subtle changes are expected, a large number of chronologically ordered inages are stacked, and trajectories of individual pixels are extracted. Once pixel-scale trajectories are available, users can fit a variety of statistical models to understand the process of change. For example for environmental data, fitting a linear trend to precipitation data stacked over long time periods can provide evidence of secular warming or cooling trends. Periodic data such as vegetation phenology can be studied using harmonic models to understand vegetation seasonality.

**d**.  **Change vectors** - When complex changes are expected, sets of spectral bands or vegetation indices can be studied for change simultaneously by considering each combination of index or bands as a N-dimensional vector. Changes in the direction of this vector computed via standard vector algebraic models can provide indicators of change in more than a single variable. 
 
## 4. Change Detection in GEE

For the purposes of this exercise, we will focus on 1) image differencing to detect change, and 2) assuming classified maps are available, tracking changes in proportions of pre-classified landcover - an important activity in many land use planning organizations. To do this, we will use three case studies:
**1** Detecting deforestation<br>
**2** Detecting flooding, and conducting damage assessments<br>
**3** Detecting land cover change using classified imagery<br>

### 4.1 Detecting deforestation
Copy the script [here](https://github.com/ecodynlab/GALUP/wiki/Scripts#05_basic_deforestation_assessment) and paste into GEE.
This exercise involves 6 distinct steps:
1. Selecting an area of interest:
   - Draw a rectangle on the map GUI where you suspect change to have occurred. For the purpose of this exercise we utilized the region spanning SW Kumasi to Ntobroso in the West and Akuntam in the South. This area seems to have undergone some amount of mining operations in the past few decades. See variable **REG_GH**.
2. Selecting the appropriate sensor:
   - For the purposes of this exercise, we will utilize Landsat 7 and Landsat 8 to detect changes between 2000 and 2020. We reuse snippets of code from previous training sessions to select, download, and pre-process Landsat imagery. See dates specified for variables **PRE_ST_DATE** and so forth for formatting to specify dates, and variables **IMG_L7** and **IMG_L8** to select image collections.
3. Selecting the appropriate image indices to monitor:
   - We test two indices: NDVI - to test changes in vegetation vigor, and the Normalized Burn Ratio (NBR), a comparison of NIR and SWIR bands that has been found to be uuseful in tracking surface moisture: 
4. Processing the imagery to calculate image differences:
   - See functions **getNBR** and **getNDV** to extract image indices from Landsat imagery. See variable **DNBR** and **DNDV** for a very simple way for calculating image differences.
5. Assessing the difference image, and determining the threshold of change:
   - See code for generating histograms to allow the inspection of the number of pixels across various values of differences in indices. Use this histogram to assess which level to threshold the difference image to generate a mask of change. Note variable **connections** to obtain an ancillary dataset for estimating 8-connected pixels for cleaning the threshold image.
6. Assessing the magnitude of change observed via an alternative data source:
   - The last part masks MODIS landcover across the thresholded difference map, and generates a histogram to inspect which land cover changed the most.

- Please complete [Exercise 1](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise1.md)
- Please submit your exercises [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=Achidago&labels=Exercise+W4M2&template=w4m2-exercise-submission.md&title=Workshop+4xercise+2+%5Breplace+with+your+name%5D)
### 4.2 Flood damage assessment
Copy the script [here](https://github.com/ecodynlab/GALUP/wiki/Scripts#06_flood_damage_assessment) and paste into GEE.
- Please complete [Exercise 2](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise2.md)
- Please submit your exercises [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=Achidago&labels=Exercise+W4M2&template=w4m2-exercise-submission.md&title=Workshop+4xercise+2+%5Breplace+with+your+name%5D)
### 4.3 Extracting land cover change trajectories
Copy the script [here](https://github.com/ecodynlab/GALUP/wiki/Scripts#07_multiyear_landcover_change) and paste into GEE.
- Please complete [Exercise 3](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise3.md)
- Please submit your exercises [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=Achidago&labels=Exercise+W4M2&template=w4m2-exercise-submission.md&title=Workshop+4xercise+2+%5Breplace+with+your+name%5D)

## 5. Post-training Survey
- Please take this [post-training survey]

## 6. Other Useful Resources
 1. [Cloud-Based Remote Sensing with Google Earth Engine](https://www.eefabook.org/go-to-the-book.html)<br>
 2. [NASA ARSET: Time Series Analysis](https://www.youtube.com/watch?v=RqVselZ5hKM&t=3695s)<br>
