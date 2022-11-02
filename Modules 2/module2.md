# Module 2 - Change Detection
**What will you learn from this module?**
- Introduction to Change Detection
- Change Detection using Remote Sensing
- Change Detection in GEE

## 1. Introduction to Change Detection
**Change Detection** Is the conversion of a landscape from one dominant feature type to another. Changes could be observed in the shape or size of patches of land cover, timing of the seasonal processes or the pace of conversion to other cover types. Examples include;
- Land degradation as a result of grazing
- Changes in tree cover due to wildfire or deforestation
- Urbanization



**Change Detection answers the questions;**
- How much and what kind of change has occurred?
- Where and when has change taken place?
- What are the trends in the change?

**Forms of Change;**
- Directional change. E.g Urban development/growth direction
- Cyclic change. E.g Seasonal phenology
- Multidirectional change. E.g. Deforestation and forest regeneration
- Between class changes. E.g. forest to agriculture conversion
- Within-class changes. E.g. change in vegetation index values


## 2. Change Detection Using Remote Sensing
Changes in the landscape are detected as changes in the spectral values of pixels. We can use spectral signatures to differentiate between cover types and calculate environmental indices. For example, healthy vegetation has high reflectance in the green and near-infrared but low in the short-wave infrared while burned areas have low reflectance in the green and near-infrared but high in the S short-wave infrared. Note, Change detetcion is only possible if time series data is available  to compare changes to cover types and features.

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

**4.2 Running Time Series Analysis**<br>

   

## 5. Exercises and Post-training Survey

- Please complete the [Exercise 1]
- Please complete the [Exercise 2]

- Please take this [post-module survey]
- Please take this [post-training survey]
  
- Please submit your exercises [here]

## 6. Other Useful Resources

