## Module 2 - Remote Sensing Applications using Google Earth Engine (GEE)
### 2.1 Setting up GEE
First, you must request to set up an account with Google Earth Engine (GEE):
* Start [here](https://earthengine.google.com/)
* click “Sign Up” at the top right of the page and input institution and intention for use (e.g. using remote sensing datasets for land use suitability modeling).



### 2.2 Exploring GEE interface using RS concepts from Module 1
The GEE [code editor](code.earthengine.google.com) uses the JavaScript language for programming. There are extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) available from Google to introduce the JavaScript API.

The general interface functions for GEE can be seen below:

<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/55447fcbfc2f487ebaae8d1258e829ca1d">
    <img src="https://user-images.githubusercontent.com/84922404/135470199-719878b5-7cb6-4a7a-aacd-e40881cda2e3.JPG" alt= "GEE Tutorial" width="800">
  </a>
</p>
  
![GEEinterface](https://user-images.githubusercontent.com/84922404/132246323-4b2d7dee-6cdc-4828-aa9a-b3ab4193ffa5.png)

Further description of the components of the figure above:

**1. Scripts** 

• This tab contains the code files for past saved projects. To begin a new file, click the "NEW" button and choose the intended format supply a descriptive name.  You can also create a folder or repository if desired to organize projects. For the purposes of this workshop, we will create a folder titled “RS Workshop.” All files created and used during the workshop should be placed in this folder. 

**2. Docs**  

• Under the “Docs” tab, there is a comprehensive list of the various functions and algorithms available in GEE, along with explanations of their inputs and outputs. 

  • Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection. 
  
• GEE has further explanation and examples of how to use the "Docs" at this [link](https://developers.google.com/earth-engine/guides/getstarted#earth-engine-algorithms).

**3. Assets** 

• The “Assets” tab allows for user to load in their own images (GeoTIFF or TFRecord) or tables (shapefiles or CSVs). These will show up under the "Tasks" (10.) tab when uploading to show progress. The “Tasks” tab is also where any exports from GEE will run.

**4. Search Bar** 

• The search bar allows the user to find publicly available datasets to utilize for their own analysis. Use keywords such as satellite name or desired parameter to find a relevant dataset.

• Imports from the search bar or assets show up in an “imports” tab at the top of the code editor. You can change the automatically supplied name of the object (e.g. "imageCollection") to improve comprehensibility in your code (e.g. Landsat8Collection).

**5. Get Link**

• GEE contains a "get link" option in order to copy the code to share it with other users for collaboration.

**6. Save**

• To ensure that the code does not accidentally get deleted, there is a "save" option, which should be used when important changes have been made to the code.

**7. Run** 

• Once the script has been written and completed by the user, the "run" button is pressed to execute the code.

**8. Help** 

• For any issues or questions that may need to be resolved within GEE, there is a Help button.

**9. Feedback** 

• A feedback option is supplied to reach out directly to Google.

**10. Tasks**  

• Assets and exports from GEE will show up under the "Tasks" (10.) tab when uploading to show progress. 

**11. Console** 

• The “Console” contains anything that has been printed or any errors existing in the c

**12. Inspector** 

• The “Inspector” tab gives information about the map, such as coordinates or scale. Once images or image collections have been added to the map, these will also have details that show up under this tab.

**13. Layer manager**  

• Any layers that have been added to the map will appear listed under the "Layer Manager" (13.), where the user can turn layers on and off and adjust visualization parameters.

• Parameters can be established, typically as color palettes, by the user to visualize the data on the map. 

**14. Geometry tools** 

• Geometry tools allow the user to draw directly on the map to specify a region of interest to which analysis will be applied, which will also appear in the "imports" tab.

**15. Zoom**

• The user can zoom in and out on the map using the "zoom" feature.

### 2.3 Exercises in GEE to play with RS data 
#### Module 2 Exercise 1 ####
##### Description #####
In this exercise, we will cover satellite dataset visualization using Google Earth Engine.

##### Skills and Goals #####
* Understand how to import and filter a dataset in GEE

* Create a visual map using specific bands

* Identify satellite differences over various years and regions

##### Instructions #####
1. In Google Earth Engine, open the script "01_search_and_display."
2. Using the geometry tools, identify a region of interest (smaller than the size of a country) and draw a polygon around it. This will be imported into the code editor.
3. Choose two sets of dates over which satellite data will be collected: one set in the summer months (May through August) and one set in the winter months (December to March). Set the initial and end dates for each set to be about 3 months apart. 
5. Using the script as a guide, map the satellite images using your chosen region and dates of interest.
6. Questions: What differences do you notice between the data taken during the summer and winter? Change the cloud cover fraction filtered in GEE: what changes do you notice in the output? Change the band combinations in the visualization parameters (e.g. for Landsat 8 edit "bands: ['B5', 'B4', 'B3']" to "bands: ['B4','B3','B2']". What do you notice about the map output after this change?
7. Submit images/screenshots of your map https://github.com/ecodynlab/GALUP/issues/new.

##### Result #####
* Upon completion of the exercise, your submission should look similar to the file **here**.

</p>

##
Next Section: 

<a href="Module 3.md" title="Module 3">Module 3</a>

Previous Section:

<a href="Module 1.md" title="Module 1">Module 1</a>


