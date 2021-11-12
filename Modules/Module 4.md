## Module 4 - Land Cover Classification

**What will you learn from this module?**

**In this module, we will discuss supervised classification. DEFINITION....**

Supervised classification is based on the idea that a user can select sample pixels in an image that are representative of specific classes and then direct the image processing software to use these training sites as references for the classification of all other pixels in the image. Training sites (also known as testing sets or input classes) are selected based on the knowledge of the user. The user also sets the bounds for how similar other pixels must be to group them together. These bounds are often set based on the spectral characteristics of the training area, plus or minus a certain increment (often based on “brightness” or strength of reflection in specific spectral bands). The user also designates the number of classes that the image is classified into. Many analysts use a combination of supervised and unsupervised classification processes to develop final output analysis and classified maps.

Unsupervised classification is where the outcomes (groupings of pixels with common characteristics) are based on the software analysis of an image without the user providing sample classes. The computer uses techniques to determine which pixels are related and groups them into classes. The user can specify which algorism the software will use and the desired number of output classes but otherwise does not aid in the classification process. However, the user must have knowledge of the area being classified when the groupings of pixels with common characteristics produced by the computer have to be related to actual features on the ground (such as wetlands, developed areas, coniferous forests, etc.). (https://mapasyst.extension.org/whats-the-difference-between-a-supervised-and-unsupervised-image-classification/) 

**Several methods are used .... refs here review/table**

Here we will use
random forest - defs/explanation
SVM - defs/explanation
CCDC - ccdc bu; standard w/ NASA


GEE 
flow diagram of the classification process.
sample data/region
creating training data - neeed a video tutorial  - generating boxes in qgis/exporting in excel and in kml; 
used GEE for RF/SVM/CCDC

[GEE CCDC Tools](https://gee-ccdc-tools.readthedocs.io/en/latest/)


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
