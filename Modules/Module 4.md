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
### 1.1 Supervised and Unsupervised Classification 
- **Unsupervised classification** is where the outcomes  are based on the software analysis of an image without the user providing sample classes. The computer uses techniques to determine which pixels are related and groups them into classes. 

- **Supervised classification** is based on the idea that a user can select sample pixels in an image that are representative of specific classes and then direct the image processing software to use these training sites as references for the classification of all other pixels in the image. 


### 1.2 Common Classification Algorithms
- The **Minimum-Distance to the Mean Classifier** is a remote sensing technique used to classify unknown image data to known classes by calculating the mean point in digital parameter space. This classifier includes the 
    - Euclidean distance,
    - Normalized Euclidean distance, and
    - Mahalanobis distance. 
- The **Parallelepiped Classifier** uses a decision rule to classify multispectral data by forming a n-dimensional parallelepiped classification in image data space by assigning given pixels to classes based on threshold values. 

- The **Gaussian Maximum Likelihood Classifier (GMLC)** quantitatively evaluates both the variance and covariance of the category spectral response patterns when classifying an unknown pixel. It is assumed that the distribution of the cloud of points forming the category training data is Gaussian ([3](http://wgbis.ces.iisc.ernet.in/energy/water/paper/remotesensing/chapter1.htm)) 
- The **Random Forest Classifier** is an ensemble learning method that creates a multitude of decision trees and takes the average of the trees for classifcaiton. The RF algorithm can also classify variable importance. 
- **Support Vector Machine (SVM) Classifiers** are a collection of non-parametric learning algorithms which finds the optimal separating hyperplane between classes by focusing on the training data. 
- **Continuous Change Detection and Classification (CCDC)** is a general-purpose algorithm that evaluates changes in land cover, land use, or condition over time. The algorithm includes a two-step masking algorithm to eliminate any noisy data caused by snow, clouds, or cloud shadows. Classification occurs after change is detected in a pixel value. 

### 1.3 Land Cover Classification Systems 


## 2 Applications in Google Earth Engine  
We will be focusing only on supervised classification methods,particularly random forests, SVM, and CCDC in GEE. 

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
