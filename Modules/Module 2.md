## Module 2 - Remote Sensing Applications using Google Earth Engine (GEE)

What will you learn from this module?

• How to set up the Google Earth Engine 

• Using GEE for remote sensing applications 

## 

### 2.1 Setting up GEE 
First, you must request to set up an account with Google Earth Engine (GEE):
* Start [here](https://earthengine.google.com/)
* click “Sign Up” at the top right of the page and input institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).
* Approval may not happen immediately; be sure to sign up in advance to provide a few days for completion.

(Do this as soon as possible since it make take a few days for the account to be registered.)

### 2.2 Exploring GEE interface using RS concepts from Module 1
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:

<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/55447fcbfc2f487ebaae8d1258e829ca1d">
    <img src="https://user-images.githubusercontent.com/84922404/135470199-719878b5-7cb6-4a7a-aacd-e40881cda2e3.JPG" alt= "GEE Tutorial" width="800">
  </a>
</p>
  
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

Further description of the components of the figure are found [here](https://github.com/ecodynlab/GALUP/wiki/GEE-Interface).

### 2.3 Exercises in GEE to play with RS data 
#### Module 2 Exercise 1 ####
##### Description #####
In this exercise, we will cover satellite dataset visualization using GEE.

##### Skills and Goals #####
* Understand how to import and filter a dataset in GEE

* Create a visual map using specific bands

* Identify satellite differences over various years and regions

##### Instructions #####
1. In the GEE [code editor](https://code.earthengine.google.com/), copy and past the script for this exercise, ["01_search_and_display"](https://github.com/ecodynlab/GALUP/wiki/Scripts).
2. Using the geometry tools (14.), identify a region of interest (smaller than the size of a country) and draw a polygon around it following the procedure given in the video. This will be automatically imported into the code editor, modifying the existing script.
3. Choose dates over which satellite data will be collected in the format 'YYYY-MM-DD':

    a. Enter a set of dates during the summer months (May through August), and set the start and end dates about 3 months apart.
  
    b. Using the script as a guide, map the satellite images using your chosen region and dates of interest.
  
    c. Submit screenshots of your mapped images <a href="https://github.com/ecodynlab/GALUP/issues/new" title="here">here</a>\.
  
4. Repeat the process of 3(a-c) with a set of dates during the winter months (December to March). 
5. Questions: What differences do you notice between the data taken during the summer and winter? Change the cloud cover fraction filtered in GEE: what changes do you notice in the output? Change the band combinations in the visualization parameters (e.g. for Landsat 8 edit "bands: ['B5', 'B4', 'B3']" to "bands: ['B4','B3','B2']". What do you notice about the map output after this change? Submit your answers to these questions on this [form](https://docs.google.com/forms/d/e/1FAIpQLSexZ7T8WgL7gh1BDYaJ0_BCe4ndr03Q81Z0T5-gC-nG6SZa_A/viewform?usp=sf_link).


##### Result #####
* Upon completion of the exercise, your submission should look similar to the file **here**.

</p>

##
Next Section: 

<a href="Module 3.md" title="Module 3">Module 3</a>

Previous Section:

<a href="Module 1.md" title="Module 1">Module 1</a>


