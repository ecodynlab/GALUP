# Module4 - Time Series Exercise 2

## Description
In this example, we will fit pixel-wise linear trends to an environmental parameter, and will assess how trends vary spatially across large regions using the script [04_time_series_linear_fit](https://github.com/ecodynlab/GALUP/wiki/Scripts#04_time_series_linear_fit).

## Skills Developed
- Time Series Analysis Concept and Fundamentals,
- Understading how reducers work in GEE.
- Interpretation spatial variations in trends across multiple parameters.

## Instructions
- Copy the script and paste into GEE editor,
- Create a box across a large region of your interest, maybe an entire country.
- Variables **ST_DATE** and **EN_DATE** specify the start and end dates,
- Function **createTimeBand** adds a 'time band' to any image. Think of this as adding the date column to your excel sheet. This will form the X-axis.
- Variables **ERA5_temp** and **ERA5_rain** collect ERA5 reanalysis climatological data, filter dates set above, clip them to the region of interest, and add the time band.
- Variable **linearFitTemp** fits the linear fitting 'reducer' to the stack of images. A 'reducer' is a function that takes information from all bands and computes a certain metric from it. Common reducers include mean, median, min, and max. The **linearFit** reducer fits a linear regression model for every stack of pixels against the time band, and outputs the scale (slope), and the offset (intercept) of the fitting line.
- Inspect the respective histograms to find the best visualization parameters for the map displayed.

## Result
Upon completion of the exercise, submit a screenshot of your document and a two-three sentence explanation of what you see [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=&labels=Exercise_W4M1&template=w4m1-exercise2-submission.md&title=Module+1+exercise+2+%5Breplace+with+your+name%5D)
