# Module4 - Time Series Exercise 1

## Description
In this exercise, we will use GEE to generate a time series image collection and will export the average of a small region as a single time series. We will export this time series in an excel-compatible format, and we will manually fit a linear trendline to it. The slope of the trendline describes the change in the phenomena at that small region across the time period of interest. The next exercise will plot these slopes across the entire region.

## Skills Developed
- Practice extracting and analyzing different kinds of time series imagery,
- Understanding what goes on 'under-the-hood' of the GEE linear fit reducer,
- Understanding what the slope may mean in different locations for different datasets.

## Instructions
- Copy the script Time Series Analysis Example and paste into GEE editor,
- variables **ST_DATE** and **EN_DATE** specify the start and end dates,
- variable **MOD13Q1** is the MODIS 16-day 500m Global NDVI/EVI product,
- variable **imgNDV** filters all MODIS Data to get NDVI images and clip them to the region of interest.
- variable **imgPET** similarly filters all MOD16A2 Data to get PET images and clip them to the region of interest.
- the print statements let you inspect the contents of these image collecetions in the console.
- On the charts generated in the console, click on the upper right corner to open the chart in a new window.
- Download the chart as an CSV sheet by clicking on the button in the upper right corner.
- Open this CSV in Microsoft Excel and fit a trendline to it.
- Take a screenshot of this chart, submit it to the page below, with a short explanation on why you think you see this trend.

## Result
Upon completion of the exercise, submit your screenshot [here](https://github.com/SERVIR-WA/GALUP/issues/new?assignees=Achidago&labels=Exercise+W4M1&template=w4m1-exercise1-submission.md&title=Workshop+4+exercise+1+%5Breplace+with+your+name%5D)
