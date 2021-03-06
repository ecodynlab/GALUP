# Module-4 Exercise 1
## Description
In this exercise, we will use the index extraction covered in the last module to perform land cover classification in GEE.
## Skills Developed
- Understand how to collaboratively collect 'ground truth' data,
- Use ground truth data with different classification methods to generate land cover maps,
- Use GEE scripts to derive simple metrics of classification accuracy, 
- Download classified maps for your area.

## Instructions
📌 This process may be made easier by downloading and installing Google Eath Pro (<a href="https://www.google.com/earth/versions/#earth-pro">link</a>). <br>
This video may help in completing steps 1 through 5:

 <p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/38ea2eb245184e9d8bab2a4c6fc28ed31d" target="_blank" rel="noopener">
    <img src="https://user-images.githubusercontent.com/84922404/142556118-d1429e06-8332-44c5-bc2e-9baa7b4f87af.png" alt= "GEE Tutorial" width="800">
  </a>
</p>


1. Download these **KML files** that contain boxes assigned to your organization: <br>
    a. [AGRHYMET KML](https://github.com/ecodynlab/GALUP/files/7565808/BOXES_AGRHYMET.zip) <br>
    b. [CERSGIS KML](https://github.com/ecodynlab/GALUP/files/7565809/BOXES_CERSGIS.zip) <br>
    c. [ICRISAT KML](https://github.com/ecodynlab/GALUP/files/7565810/BOXES_ICRISAT.zip) <br>
    b. [LUSPA KML](https://github.com/ecodynlab/GALUP/files/7565811/BOXES_LUSPA.zip) <br>
2. Opening these files in Google Earth Pro will zoom to the entire country. Expand the dropdown list to reveal individual boxes. Double-clicking on the boxes should make Google Earth Pro zoom into that location.
3. Access this [Google Spreadsheet](https://docs.google.com/spreadsheets/d/10JV0HxQAPhW3V7qjp5-bVLld8_-E8WhpeJayIAlVW2s/edit#gid=1266282790).
4. Each organization has a tab assigned to it. The ID column corresponds to the ID of the boxes in the KML (do not change the ID). We have asumed each registered participant should be able to classify at least 100 locations by the end of the exercise, 
5. Double-click on any box in the KML to zoom to that location. On the spreadsheet, locate the row corresponding to the KML box ID and click on the "Landcover" cell to reveal several options. Click on an option to select the landcover class. Clicking on this cell will result in several options appearing in the "Subclass cell". These are details of the landcover you selected. Select an option if you are sure the land cover class can be better defined using one of the subclasses. See this [PowerPoint](https://github.com/SERVIR-WA/GALUP/files/7573041/GALUP-GLanCE-Classification.pptx) on classifying land cover in West Africa.

6. Once the sheet has been filled and the classification of each point completed, we will export the collected data and merge it with the coordinates of the random points.

**The classifications on the spreadsheet must be completed by Monday, 11/22 at 1:00 PM GMT**

7. Once you receive the merged file of the classifications and original random points (this will be in the form of a shapefile), download this file.
8. Upload the shapefile into GEE as an asset (see this [link](https://developers.google.com/earth-engine/guides/asset_manager) for help with managing assets in GEE)
9. Once the asset has been loaded into GEE, run the **script**. This will utilize the training data (the asset) to classify Ghana's land cover using the Random Forest classification method.
10. Repeat step 6 using the SVM classification method.
11. Open up the **CCDC** code in GEE. The [GEE CCDC Tools](https://gee-ccdc-tools.readthedocs.io/en/latest/) will be useful for this. 
    
