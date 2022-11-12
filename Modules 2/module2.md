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

**Forms of Change** Landscapes can change in different ways; a detailed understanding of the kind of change to be monitored determines the sensor to be used to extract the best performance out of remote sensing techniques.
<p align="center">
<img src="https://user-images.githubusercontent.com/40871781/201491844-a3dd8fa8-2b9f-4ce4-b315-cd339e1d9c45.gif">
</p>
<sub> Continental-scale vegetation phenology tracked by MODIS. Source: [Google Earth Engine](https://developers.google.com/earth-engine/tutorials/community/modis-ndvi-time-series-animation)</sub>

- Directional change. E.g Urban development/growth direction: Needs high spatial resolution imagery, generally involving at least one band that can track vegetation (e.g. NIR)
- Cyclic change, for example crop or grassland phenology: Needs high temporal resolution imagery so changes around critical growth stages can be captured, typically also using a vegetation tracking band (NIR),
- Multidirectional change. E.g. Deforestation and forest regeneration: Needs moderate spatial and temporal resolution depending upon the magnitude of change. Having calendar-date imagery is useful when change needs to be traked across multiple years.
- Between class changes. E.g. forest to agriculture conversion: Typically needs high spatial and temporal resolution to be able to tell different growth stages apart,
- Within-class changes. E.g. change in vegetation index values: Typically needs high spectral resolution to be able to tell different vegetation types apart

**Change Detection answers the questions;**
- How much and what kind of change has occurred?
- Where and when has change taken place?
- What are the trends in the change?

## 2. Change Detection Using Remote Sensing
At the most basic, remote sensing techniques rely on tracking changes in spectral reflectance profiles of individual pixels. Differences in spectral characteristics of different cover types can often be exploited to differentiate between cover types. As an example, healthy vegetation has high reflectance in the near-infrared spectrum but low reflectance in the red spectrum. Moisture in vegetation also strongly absorbs shortwave radiation making these bands very useful for tracking water status in plants. Further, differences in spectral characteristics can be explited by combining different spectral bands into standardized indicies, with the bands determining which phenomenon can be best tracked. Note that change detection almost always requires imagery to be available at at least two different time periods.

<p align="left">
<img src="https://user-images.githubusercontent.com/85199074/194796915-95e941ba-75d1-4c58-aa52-2462e10d18ba.jpg">
</p>
<sub> Healthy vegetation has a large peak in the near infrared, while soil or burned areas are much lower. Healthy vegetation also has low reflectance in the shortwave infrared, while burned areas have high reflectance.</sub>

([Source](https://appliedsciences.nasa.gov/join-mission/training/english/arset-using-google-earth-engine-land-monitoring-applications))<br>

## 3. Change Detection Methods
**a**.  **Visual Analysis** - It is the identification of change through visual comparison, digitization, and/or band combinations. It is suitable for large changes such as patch shape or size but not for subtle changes such as land degradation.. It does not neccesarily utilise spectral reactivity.

**b**.  **Image Differencing** - is computed on a pixel-by-pixel basis and is executed across the full extent of both images.The pixel-based nature of image differencing allows for more precise identification of change. This method is particularly useful for assessing change over continuous indices (such as those used to measure vegetation and soil). 
<p align="center">
<img src="https://user-images.githubusercontent.com/85199074/194987983-817db71d-207d-4624-a9bc-fcaf350750c9.png">
</p>


 
## 4. Change Detection in GEE



**4.1 Video tutorial for the section 3.1** <br>
   

## 5. Exercises and Post-training Survey

- Please complete the [Exercise 1](https://github.com/ecodynlab/GALUP/blob/main/ExercisesM2/Exercise3.md)
  
- Please submit your exercises [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=Achidago&labels=Exercise+W4M2&template=w4m2-exercise-submission.md&title=Workshop+4xercise+2+%5Breplace+with+your+name%5D)

- Please take this [post-training survey]

## 6. Other Useful Resources
 1. [Cloud-Based Remote Sensing with Google Earth Engine](https://www.eefabook.org/go-to-the-book.html)<br>
 2. [NASA ARSET: Time Series Analysis](https://www.youtube.com/watch?v=RqVselZ5hKM&t=3695s)<br>
