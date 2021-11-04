# Module 2 Exercise 1 
## Description
In this exercise, we will cover satellite dataset visualization using GEE.

## Skills Practices
* Understand how to import and filter a dataset in GEE
* Create a visual map using specific bands
* Identify satellite differences over various years and regions


## Instruction
1. In the GEE [code editor](https://code.earthengine.google.com/), copy and paste the script for this exercise, ["01_search_and_display"](https://github.com/ecodynlab/GALUP/wiki/Scripts).

Here is a video that may be useful for following along with this exercise.
<p align="center">
  <a href="https://mediasite.video.ufl.edu/Mediasite/Play/9d0bd66164844d478357dbb876e9a8b91d" target="_blank" rel="noopener">
    <img src="https://user-images.githubusercontent.com/84922404/137360913-c5aa881a-b338-4829-bbf7-40a355f69ea7.png" alt= "GEE Tutorial" width="800">
  </a>
</p>

2. Using the geometry tools (14.), identify a region of interest (smaller than the size of a country) and draw a polygon around it following the procedure given in the video. This will be automatically imported into the code editor, modifying the existing script.
3. Choose dates over which satellite data will be collected in the format 'YYYY-MM-DD':

    a. Enter a set of dates during the summer months (May through August), and set the start and end dates about 3 months apart.
  
    b. Using the script as a guide, map the satellite images using your chosen region and dates of interest.
  
    c. Take screenshots of the images displayed in the GEE map. 
    
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. Tip: if no images appear, this is likely due to cloud cover. Try changing the region of interest or the cloud cover percentage (e.g. filterMetadata('CLOUD_COVER','less_than',70) to filterMetadata('CLOUD_COVER','less_than',90).
  
4. Repeat the process of 3(a-c) with a set of dates during the winter months (December to March). 
5. Questions: 

    a. What differences do you notice between the data taken during the summer and winter? 
    
    b. Change the cloud cover fraction filtered in GEE: what changes do you notice in the output? 
    
    c. Change the band combinations in the visualization parameters (e.g. for Landsat 8 edit "bands: ['B5', 'B4', 'B3']" to "bands: ['B4','B3','B2']". What do you notice     about the map output after this change? 
    
6.  Submit screenshots of your mapped images as well as the answers to questions 5a through 5c <a href="https://github.com/ecodynlab/GALUP/issues/new?assignees=&labels=Exercises&template=assignment-submission.md&title=Add+your+name+and+the+module+number+for+submission" title="here">here</a>\.


## Result
* Upon completion of the exercise, your submission should look similar to the file [here](https://github.com/ecodynlab/GALUP/blob/main/Exercises/M2_E1.md).

</p>
