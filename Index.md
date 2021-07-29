# Introduction to Remote Sensing Concepts
<br>

## Basic Remote Sensing 
### EM Spectrum 
### Satellite Imagery 
### Bands
### Hyperspectral
### Environmental Data  
<br>

## GEE (software and implementing RS intro)
### Setting up GEE
Setting up account

[Sign up](https://earthengine.google.com/) -> “Sign Up” and list institution and intention for use: e.g. using remote sensing datasets for land use suitability modeling

Extra [resources](https://developers.google.com/earth-engine/tutorials/tutorial_api_01) from Google

Coding in JavaScript in the editor: code.earthengine.google.com




### Exploring interface using the theoretical concepts above

The general interface functions for GEE can be seen below:
![GEEtools](https://user-images.githubusercontent.com/84922404/127547280-1f8966eb-b87c-4a4b-8c28-e2169d7ed864.JPG)

Create scripts under the “scripts” tab

Create NEW -> name file and organize into folders if desired

We will create a “RS Workshop” Folder

“Docs” tab explains various tools and algorithms available in GEE (JavaScript documentation)

“Assets” tab allows for user to load in their own images or tables (shapefiles, CSVs)

Search bar allows user to find publicly available datasets to utilize for their own analysis

Imports from the search bar or assets show up in an “imports” tab at the top of the code. You can change the name of these to better represent the object in your code

Can search datasets based on keywords Radiation, NDVI, etc

“Inspector” tab gives information about the map (e.g. coordinates, pixels)

“Console” provides what has been printed by the code or any errors

“Tasks” tab is where any exports or assets will show up as running

Bands in datasets (e.g. Landsat) allow for calculation of these remote sensing variables:

RS in GEE: NDVI = (nir - red)/(nir + red) 

Can use parameters to visualize the data (use colors)

Map.setCenter and Map.addLayer visualize the map in the GEE map tool of an ee.Image or ee.ImageCollection

### Exercises in GEE to play with RS data  
<br>
Look at MODIS vegetation dataset (MOD13A2.006 Terra Vegetation Indices 16-Day Global 1km) to see NDVI and EVI values

Import MODIS classification and add layer on map (MCD12Q1.006 MODIS Land Cover Type Yearly Global 500m)


## Indices
### Formulation, use/purpose, and significance
### Exercises in GEE to play with indices  
<br>

## Classification
### Using indices – simple classification; accuracy & metrics
### Exercises in GEE to play with classification & temporal changes in indices for different classes (Ag/Forest/Urban)
<br>
