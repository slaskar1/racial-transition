
# Table of Contents
- [Racial Transition from 1970 to 2020](#racial-transition-from-1970-to-2020)
- [Data Source](#data-source) 
- [Background and Purpose](#background-and-purpose)
- [Creating the Maps](#creating-the-maps)
- [The Final Map](#the-final-map)
- [Map Summary](#map-summary)
- [Final Project Website](#final-project-website)

# Racial Transition from 1970 to 2020

# Data Source

US County Shapefile: US Census Bureau [Cartographic Boundary Files](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html)

US Race Data: US Census Bureau Race Data: [Race Data](https://www.census.gov/topics/population/race/data.html)


# Background and Purpose:

Over the years, racial demographics have changed in the US. As I work with racial data, I found it useful to create a map and see how much the percentage of Black Population have changed from 1970-2020. The Census has data from 1970 and that is as far as I could go. I created 3 maps. The first one shows the percentage of the Black Population in 1970 in US counties, the second one shows the Percentage Black Population in 2020 and the third one shows which US counties experienced racial transition. I will explain how I defined Racial Transition in the mapmaking process. My supervisor, I and her previous RA have collected race data from census for different years, recoded them and appended them. We also merged them with public finance data from [The Government Finance Database](https://willamette.edu/mba/research-impact/public-datasets/index.html). However, we don’t need public finance data for this project. I am using the final merged dataset from my supervisor for the race data.

I have created 3 maps and the purpose of them is to show the change in the Percentage Black Population in 2020 compared to 1970. I work with racial data and currently I am working on a project with my supervisor that looks into the changes in public finance (especially the revenue side) in relation to the changes in racial demographics.  So, I thought it would be really useful to visually map the changes in racial demographics (Change in percentage Black Population for this Mapping project).

# Creating the Maps

First, I downloaded the shape files from census.gov. I downloaded the 2018 county shapefile for 2020 data and 1990 shapefile(census.gov didn’t have shapefile for the years before 1990) for 1970 data.

![Shape file](<Repository Images/Shapefile website.png>)

Then I got my Census Race dataset. All race has been taken from the Census Bureau.

![Race data](<Repository Images/Race date website.png>)

I had to create an id that identifies both the datasets to join. The County FIPS code in my merged race dataset was 5 digits(combined state and county FIPS). So, that didn’t work. So, instead I exported the shape files in excel format first and merged race data in Stata with an id(that identifies the counties) that was already in the shapefiles. I chose COUNTYNS for 2020 data and C099_D90_ for 1970 data.

|||
|-|-|
|![alt text](<Repository Images/Export as csv.png>)|![alt text](<Repository Images/Export as csv 2.png>)|

I then add the new csv layer that has race data and join the two files.

![Join](<Repository Images/Join.png>)

Checking the Attribute table,

![alt text](<Repository Images/Checking the Attribute table.png>)

The data race data joined perfectly! Now that the data is prepared, we are going to start creating the Maps. First, I will map the percentage Black Population in US counties in 1970 and then do the same for 2020.

![alt text](<Repository Images/Symbology.png>)

Changing the numbers in the legend according to my preference,

![alt text](<Repository Images/Legend.png>)

![alt text](<Repository Images/Creating the Map.png>)

After these two maps, I also created a third map to determine Racial Transition. Racial transition was calculated in Stata. 

![alt text](<Repository Images/Racial Transition Calculation.png>)

Those counties were flagged as “went through a Racial transition” who had percentage Black population below state median in 1970 but their change percentage Black population from 1970 to 2020 is greater that the state median change from 1970-2020. 

![alt text](<Repository Images/Racial Trnaisiton Map.png>)

# The Final Map

The final Map consisted of two pages. The first page consists of the maps of Percentage Black population 1970 and Percentage Black Population in 2020. The second page consists of the Racial Transition. If the county went through a racial transition, then it is blue, if not then its green.

![alt text](<Images/Racial Transition-600dpi.png>)

![alt text](<Images/Racial Transition-600dpi_2.png>)

# Map Summary

The first Map shows the Percentage Black Population in 1970 in the US counties. The second Map shows the Percentage Black Population in 2020 in the US counties. The third Map shows the racial transition in the US counties. Racial Transition is defined as having percentage Black population below state median in 1970 but the change in percentage Black population from 1970 to 2020 for the same county is greater that the state median change from 1970-2020. The counties that went through a racial transition were symbolized as blue, if not then its green. 
We can see in both 1970 and 2020, the most percentage Black population is around the border of Atlantic Ocean and the Gulf of Mexico. Among others, we can see that some counties in Minnesota, some counties in North Dakota, some counties in Texas and some counties in Nevada went through a racial transition.

# Final Project Website

Please click here [Final Project](http.google.com)