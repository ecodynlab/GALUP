# Module-4 Exercise 1
## Description
In this exercise, we will use the index extraction covered in the last module to perform land cover classification in GEE.
## Skills Developed
- Understand different methods of image classification,
- Use training points for classifying land cover types, 
- apply RS indices to classification algorithms.

## Instructions
1. Download these **KML files** that contain random points within Ghana.
2. Each institution will be assigned numbered points from the KMLL files in the format of a Google sheet: <br>
    a. AGRHYMET will fill out this sheet: <br>
    b. CERSGIS will fill out this sheet: <br>
    c. ICRISAT will fill out this sheet: <br>
    b. LUSPA wil fill out this sheet: <br>
2. To complete the classifications, upload the given KML files to Google Earth Pro, and zoom in to determine the respective classification of each point. To classify the points, use the dropdown bar in the Google sheet in the row that corresponds to the point's ID.
3. Once the sheet has been filled and the classification of each point completed, send this back to us by submitting it **here**.
4. Once you receive the merged file of the classifications and original random points (this will be in the form of a shapefile), download this file.
5. Upload the shapefile into GEE as an asset (see this [link](https://developers.google.com/earth-engine/guides/asset_manager) for help with managing assets in GEE)
6. Once the asset has been loaded into GEE, run the **script**. This will utilize the training data (the asset) to classify Ghana's land cover using the Random Forest classification method.
7. Repeat step 6 using the SVM classification method.
8. Open up the **CCDC** code in GEE 
    
