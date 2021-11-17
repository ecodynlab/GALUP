# Module-3 Exercise 1
## Description
In this exercise, we will analyze temporal trends and visual representations of indices and environmental variables.

## Skills Developed
- Use graphing techniques available in GEE
- Perform spatial and temporal analysis of indices 
- Understand calculations of indices

## Instructions
1. Using the script ["02_image_indices_environmental_data"](https://github.com/SERVIR-WA/GALUP/wiki/Scripts#02_image_indices_environmental_data), alter the variables "YEAR1", "YEAR2","ST_DATE", and "END_DATE" to indicate a period of interest.
2. Choose a region of interest by either drawing a polygon to automatically import a geometry or by manually specifying the Longitue_Min,Latitude_Min,LongitudeMax, and LatitudeMax as coordinates of a rectangle.
3. Alter the given function: <br> ```var getNDVI = function(image){``` <br>
  ```var ind = image.expression('(nir-red)/(nir+red)',{'nir':image.select('nir'),'red':image.select('red')}``` <br>
  ```var ret = ind.copyProperties({source: image,properties: ['system:time_start']});``` <br>
  ```return ret;``` <br>
  ```};``` <br> 
  to represent another chosen variable <br>
 :pushpin: Some common indices are given at the bottom of the script. <br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. If you change the variable name "getNDVI" (e.g. to "getSAVI") (this is good coding practice), ensure that the rest of the code that utilizes the "getNDVI" function is also changed.
3. Run the script over the chosen region and time period, and take screenshots of: <br>
    a. The raw Landsat image <br>
    b. The image of the chosen index <br>
    c. The SRTM elevation image <br>
    d. The LST image <br>
    e. The time series chart for the chosen index <br>
    f. The time series chart for LST <br>
  :pushpin: Check and Uncheck the layers in the GEE map to be able to see each image individually. 
5. Download this document [template](https://github.com/ecodynlab/GALUP/files/7516603/WS2_M3E1_Template.docx) and add the 6 screenshots stated above, as well as the answers to the follwing questions:<br>
    a. What does your chosen index represent? Do you notice any distinct patterns in values of the chosen index over the course of the chosen time period? <br>
    b. What do you notice about the images that represent each different layer (Landsat, index, SRTM elevation, and LST)? Can you infer any information about the chosen region through these images? <br>
5. Once completed, submit the document <a href="https://github.com/ecodyn/GALUP/issues/new?assignees=&labels=exercise+w2m2&template=w2m2-exercise-submission.md&title=Module+2+exercises+%5Breplace+with+your+name%5D" title="here">here</a>\. Please submit the Post-Module-3 survey [here](https://ufl.qualtrics.com/jfe/form/SV_bpjF7THHLlhtWCO).
