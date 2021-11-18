## Module 4 - Land Cover Classification
**What will you learn from this module?**

- Common methods of land cover classification
- Using indices for classifcation 
- Applications of Random Forests, Support Vector Machines, and Countinous Change Detection and Claffication in Google Earth Engine 

</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/87503837/141733532-56a05150-6b9d-4ac7-b124-aa1f8d7c5120.gif" alt="animated" />
</p>


## 1. Land Cover Classification Method



### 1.1 Supervised image Classification 
**Supervised image classification** is a method for identifying spectrally similar areas on images by first identifying known classes from training sites and then directing the image processing towards those training sites as reference for unknown targets.  

- **Minimum-Distance to the Mean Classifier**: a remote sensing technique used to classify unknown image data to known classes by calculating the mean point in digital parameter space.
   <blockquote> 
   Note: this classifier includes multiple metrics including Euclidean distance, normalized Euclidean distance, and Mahalanobis distance. 
   </blockquote>
  
-  **Parallelepiped Classifier**: uses a decision rule to classify multispectral data by forming a n-dimensional parallelepiped classification in image data space by assigning given pixels to classes based on threshold values. 
- **Gaussian Maximum Likelihood Classifier (GMLC)**: quantitatively evaluates both the variance and covariance of the category spectral response patterns when classifying an unknown pixel. It is assumed that the distribution of the cloud of points forming the category training data is Gaussian ([3](http://wgbis.ces.iisc.ernet.in/energy/water/paper/remotesensing/chapter1.htm)) 
- **Random Forest Classifier**: an ensemble learning method that creates a multitude of decision trees and takes the average of the trees for classifcaiton. The RF algorithm can also classify variable importance. 
- **Support Vector Machine (SVM) Classifiers**: a collection of non-parametric learning algorithms which finds the optimal separating hyperplane between classes by focusing on the training data. 
- **Continuous Change Detection and Classification (CCDC)**: a general-purpose algorithm that evaluates changes in land cover, land use, or condition over time. The algorithm includes a two-step masking algorithm to eliminate any noisy data caused by snow, clouds, or cloud shadows. Classification occurs after change is detected in a pixel value. 

### 1.2 Land Cover Classification Systems 
The National Land Cover Database (NLCD) is a comprehensive land use and land cover product covering all 50 states and Puerto Rico. The classification scheme developed in this product is primarily based on Landsat satellite data and the product is renewed every 5 years. 

<blockquote>
Additional info: https://www.mrlc.gov/data/legends/national-land-cover-database-2019-nlcd2019-legend
</blockquote>

<br/>

The following outline shows the classification scheme for NLCD:  


<details>
  <summary> <b> NLCD (Class, Value, Description) </b> </summary>
  <details>
  <summary>Water</summary>
  
   - 11	_Open Water_ - areas of open water, generally with less than 25% cover of vegetation or soil.
   
   - 12	_Perennial Ice/Snow_ - areas characterized by a perennial cover of ice and/or snow, generally greater than 25% of total cover.   
  </details>
  
 <details>
 <summary>Developed</summary>
 
  - 21	_Developed, Open Space_ - areas with a mixture of some constructed materials, but mostly vegetation in the form of lawn grasses. Impervious surfaces account for less than 20% of total cover. These areas most commonly include large-lot single-family housing units, parks, golf courses, and vegetation planted in developed settings for recreation, erosion control, or aesthetic purposes.
   
  - 22	_Developed, Low Intensity_ - areas with a mixture of constructed materials and vegetation. Impervious surfaces account for 20% to 49% percent of total cover. These areas most commonly include single-family housing units.
   
  - 23	_Developed, Medium Intensity_ - areas with a mixture of constructed materials and vegetation. Impervious surfaces account for 50% to 79% of the total cover. These areas most commonly include single-family housing units.
   
  - 24	_Developed High Intensity_ - highly developed areas where people reside or work in high numbers. Examples include apartment complexes, row houses and commercial/industrial. Impervious surfaces account for 80% to 100% of the total cover.
 </details>
  
 <details>
 <summary>Barren</summary>
 
   - 31	_Barren Land (Rock/Sand/Clay)_ - areas of bedrock, desert pavement, scarps, talus, slides, volcanic material, glacial debris, sand dunes, strip mines, gravel pits and      other accumulations of earthen material. Generally, vegetation accounts for less than 15% of total cover.
 </details>
  
 <details> 
 <summary>Forest</summary>
   
  - 41	_Deciduous Forest_ - areas dominated by trees generally greater than 5 meters tall, and greater than 20% of total vegetation cover. More than 75% of the tree species shed - foliage simultaneously in response to seasonal change.
   
  - 42	_Evergreen Forest_ - areas dominated by trees generally greater than 5 meters tall, and greater than 20% of total vegetation cover. More than 75% of the tree species maintain their leaves all year. Canopy is never without green foliage.
   
  - 43	_Mixed Forest_ - areas dominated by trees generally greater than 5 meters tall, and greater than 20% of total vegetation cover. Neither deciduous nor evergreen species are greater than 75% of total tree cover.  
 </details>
  
 <details>
 <summary>Shrubland</summary>
   
  - 51 _Dwarf Scrub_ - Alaska only areas dominated by shrubs less than 20 centimeters tall with shrub canopy typically greater than 20% of total vegetation. This type is often co-associated with grasses, sedges, herbs, and non-vascular vegetation.
   
  - 52	_Shrub/Scrub_ - areas dominated by shrubs; less than 5 meters tall with shrub canopy typically greater than 20% of total vegetation. This class includes true shrubs, young trees in an early successional stage or trees stunted from environmental conditions. 
 </details>

 <details>
 <summary>Herbaceous</summary>
   
  - 71	_Grassland/Herbaceous_ - areas dominated by gramanoid or herbaceous vegetation, generally greater than 80% of total vegetation. These areas are not subject to intensive management such as tilling, but can be utilized for grazing.
   
  - 72	_Sedge/Herbaceous_ - Alaska only areas dominated by sedges and forbs, generally greater than 80% of total vegetation. This type can occur with significant other grasses or other grass like plants, and includes sedge tundra, and sedge tussock tundra.
   
  - 73	_Lichens_ - Alaska only areas dominated by fruticose or foliose lichens generally greater than 80% of total vegetation.
   
  - 74	_Moss_ - Alaska only areas dominated by mosses, generally greater than 80% of total vegetation.  
 </details>
  
 <details>
 <summary>Planted/Cultivated</summary>
   
  - 81	_Pasture/Hay_ - areas of grasses, legumes, or grass-legume mixtures planted for livestock grazing or the production of seed or hay crops, typically on a perennial cycle. Pasture/hay vegetation accounts for greater than 20% of total vegetation.
   
  - 82	_Cultivated Crops_ - areas used for the production of annual crops, such as corn, soybeans, vegetables, tobacco, and cotton, and also perennial woody crops such as orchards and vineyards. Crop vegetation accounts for greater than 20% of total vegetation. This class also includes all land being actively tilled.   
 </details>
  
 <details> 
 <summary>Wetlands</summary>
   
  - 90	_Woody Wetlands_ - areas where forest or shrubland vegetation accounts for greater than 20% of vegetative cover and the soil or substrate is periodically saturated with or covered with water.
   
  - 95	_Emergent Herbaceous Wetlands_ - areas where perennial herbaceous vegetation accounts for greater than 80% of vegetative cover and the soil or substrate is periodically saturated with or covered with water.
  </details>
  
</details>

<br/>

International Geosphere–Biosphere Programme (IGBP)
<blockquote>
  Additional info: http://www.igbp.net
</blockquote>

<br/>

The following outline shows the IGBP Ecosystems Surface Classifications classification scheme: 
<details>
<summary> <b> IGBP (Class, Class name, Description) </b> </summary>
 
1. **Evergreen needleleaf forests** - Lands dominated by needleleaf woody vegetation with a percent cover >60% and height exceeding 2m. Almost all trees remain green all year. Canopy is never without green foliage.
2. **Evergreen broadleaf forests** - Lands dominated by broadleaf woody vegetation with a percent cover >60% and height exceeding 2m. Almost all trees and shrubsremain green year round. Canopy is never without green foliage.
3. **Deciduous needleleaf forests** - Lands dominated by woody vegetation with a percent cover >60% and height exceeding 2m. Consists of seasonal needleleaf tree communities with an annual cycle of leaf-on and leaf-off periods.
4. **Deciduous broadleaf forests** - Lands dominated by woody vegetation with a percent cover >60% and height exceeding 2m. Consists of broadleaf tree communities with an annual cycle of leaf-on and leaf-off periods
5. **Mixed forests** - Lands dominated by trees with a percent cover >60% and height exceeding 2m. Consists of tree communities with interspersed mixtures or mosaics of the other four forest types. None of the forest types exceeds 60% of landscape.
6. **Closed shrublands** Lands with woody vegetation less than 2m tall and with shrub canopy cover >60%. The shrub foliage can be either evergreen or deciduous.
7. **Open shrublands** - Lands with woody vegetation less than 2m tall and with shrub canopy cover between 10% and 60%. The shrub foliage can be either evergreen or deciduous.
8. **Woody savannas** - Lands with herbaceous and other understory systems, and with forest canopy cover between 30% and 60%. The forest cover height exceeds 2m.
9. **Savannas** - Lands with herbaceous and other understory systems, and with forest canopy cover between 10% and 30%. The forest cover height exceeds 2m.
10. **Grasslands** - Lands with herbaceous types of cover. Tree and shrub cover is less than 10%.
11. **Permanent wetlands** - Lands with a permanent mixture of water and herbaceous or woody vegetation. The vegetation can be present either in salt, brackish, or fresh water.
12. **Croplands** - Lands covered with temporary crops followed by harvest and a bare soil period (e.g., single and multiple cropping systems). Note that perennial woody crops will be classified as the appropriate forest or shrub land cover type.
13. **Urban and built-up lands** - Land covered by buildings and other man-made structures.
14. **Cropland/natural vegetation mosaics** - Lands with a mosaic of croplands, forests, shrubland, and grasslands in which no one component comprises more than 60% of the landscape.
15. **Snow and ice** - Lands under snow/ice cover throughout the year.
16. **Barren** - Lands with exposed soil, sand, rocks, or snow and never have more
than 10% vegetated cover during any time of the year.
17. **Water bodies** -  Oceans, seas, lakes, reservoirs, and rivers. Can be either fresh or saltwater bodies.


</details>

## 2 Applications in Google Earth Engine  
GEE 
flow diagram of the classification process.
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/84922404/142236533-7e953e69-75a8-4de1-abbe-b60a6a89b6f7.png" />
</p>

sample data/region
creating training data - neeed a video tutorial  - generating boxes in qgis/exporting in excel and in kml; 
used GEE for RF/SVM/CCDC

[GEE CCDC Tools](https://gee-ccdc-tools.readthedocs.io/en/latest/)

[GEE Supervised Classification](https://developers.google.com/earth-engine/guides/classification)


Exercise
using excel sheet - add training data using google map; google earth pro
submit this after some time...
we will have to turn it into shp file and give it back to them.
perform classification
qs: report on accuracies/metric; differences in classification;

## 
Using indices – simple classification; accuracy & metrics

## Exercise and Post-Module Survey (required)

1. Please complete and submit [Exercise 1](https://github.com/ecodynlab/GALUP/blob/main/Exercises/M4_Exercise1.md) for Module 4.
2. Submit the Post-Module survey. 




##
**Previous Section:**

<a href="Module 3.md" title="Module 3">Module 3</a>
