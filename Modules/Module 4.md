## Module 4 - Land Cover Classification
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/87503837/141733532-56a05150-6b9d-4ac7-b124-aa1f8d7c5120.gif" alt="animated" />
</p>

**What will you learn from this module?**

- Common methods of land cover classification
- Using indices for classifcation 
- Applications of Random Forests, Support Vector Machines, and Countinous Change Detection and Claffication in Google Earth Engine 

## 1. Supervise and Unsupervised Classification 

**Supervised classification** is based on the idea that a user can select sample pixels in an image that are representative of specific classes and then direct the image processing software to use these training sites as references for the classification of all other pixels in the image. Training sites (also known as testing sets or input classes) are selected based on the knowledge of the user. The user also sets the bounds for how similar other pixels must be to group them together. These bounds are often set based on the spectral characteristics of the training area, plus or minus a certain increment (often based on “brightness” or strength of reflection in specific spectral bands). The user also designates the number of classes that the image is classified into. Many analysts use a combination of supervised and unsupervised classification processes to develop final output analysis and classified maps.

**Unsupervised classification** is where the outcomes (groupings of pixels with common characteristics) are based on the software analysis of an image without the user providing sample classes. The computer uses techniques to determine which pixels are related and groups them into classes. The user can specify which algorism the software will use and the desired number of output classes but otherwise does not aid in the classification process. However, the user must have knowledge of the area being classified when the groupings of pixels with common characteristics produced by the computer have to be related to actual features on the ground (such as wetlands, developed areas, coniferous forests, etc.)([Source](https://mapasyst.extension.org/whats-the-difference-between-a-supervised-and-unsupervised-image-classification/)). 

## 2. Common Classifcation Algorithms
1. The **Minimum-Distance to the Mean Classifier** is used to classify unknown image data to classes which minimize the distance between the image data and the class in multi-feature space. The distance is defined as an index of similarity so that the minimum distance is identical to the maximum similarity ([1](http://sar.kangwon.ac.kr/etc/rs_note/rsnote/cp11/cp11-6.htm)).
    1. Euclidean distance
    2. Normalized Euclidean distance
    3. Mahalanobis distance 
2. The **Parallelepiped Classifier** uses the class limits and stored in each class signature to determine if a given pixel falls within the class or not. The class limits specify the dimensions (in standard deviation units) of each side of a parallelepiped surrounding the mean of the class in feature space  ([2](http://www.sc.chula.ac.th/courseware/2309507/Lecture/remote18.htm)) .
3. The **Gaussian Maximum Likelihood Classifier (GMLC)** quantitatively evaluates both the variance and covariance of the category spectral response patterns when classifying an unknown pixel. It is assumed that the distribution of the cloud of points forming the category training data is Gaussian ([3](http://wgbis.ces.iisc.ernet.in/energy/water/paper/remotesensing/chapter1.htm)) 
4. The **Random Forest Classifier** is an ensemble learning method that creates a multitude of decision trees and takes the average of the trees for classifcaiton. The RF algorithm can also classify variable importance. 
5. **Support Vector Machine (SVM) Classifiers** are a collection of non-parametric learning algorithms which finds the optimal separating hyperplane between classes by focusing on the training data. 
6. **Continuous Change Detection and Classification (CCDC)** is a general-purpose algorithm that evaluates changes in pixel values over time. 

## 3. Applications in Google Earth Engine 
GEE 
flow diagram of the classification process.
sample data/region
creating training data - neeed a video tutorial  - generating boxes in qgis/exporting in excel and in kml; 
used GEE for RF/SVM/CCDC

[GEE CCDC Tools](https://gee-ccdc-tools.readthedocs.io/en/latest/)

[GEE Supervised Classification](https://developers.google.com/earth-engine/guides/classification)

![LCC Flowchart](https://user-images.githubusercontent.com/87503837/141534676-40798bfd-7a25-48a1-9676-c427c99046e0.png)

([Source](https://www.sciencedirect.com/science/article/pii/S2351989420300202))

Exercise
using excel sheet - add training data using google map; google earth pro
submit this after some time...
we will have to turn it into shp file and give it back to them.
perform classification
qs: report on accuracies/metric; differences in classification;

## 
Using indices – simple classification; accuracy & metrics



##
**Next Section:**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; **Previous Section:**

<a href="Module 3.md" title="Module 3">Module 3</a> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; <a href="Module 1.md" title="Module 1">Module 1</a>
