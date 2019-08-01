![chicagocity](https://user-images.githubusercontent.com/19572673/62321668-2a919980-b471-11e9-8efd-96efc99e22c7.jpg)
# Chicago Crime Analysis Data Exploration
![Chicago_Zip_Code_Crime_Analysis](https://user-images.githubusercontent.com/19572673/57345072-8f11b680-7117-11e9-90d0-8a55e88f4544.PNG)
## Abstract:
Every day, there are a numerous amount of crimes that occur across the country and the world. This can include major metropolitan areas with high populations and business activity. In this analysis, we look at the city of Chicago. What makes a Chicago dangerous? What types of crimes occur in within Chicago, primarily at the zip level? Which zips/areas have the highest concentration of crimes? What is the level of 'seriousness' for these crimes? Which zips/areas have the highest concentration of serious crimes? And after find that out, what days/times do they occur?  All of these questions are looked at in the analysis below.

## Use Case:
### Figuring out specific Chicago Zips with the highest number of crimes given a period of time

## Initial Dataset:
### Chicago Crimes Dataset - Small subsample Chicago Crimes Dataset from https://www.kaggle.com/currie32/crimes-in-chicago

## Software:
### PowerBI

## Basic Steps:
#### Downloaded the dataset. 

## Summary:
The bottom-line goal is to figure out specific Chicago Zips with the highest number of crimes reported within a period of time. Up on the User Interface, there is a 'date range' slicer to which the user can select the appropriate time frame. To drill down, there is a 'Primary Type' slicer which defines the type of crime. To test the severity of the crime, there are the 'Arrest?' and Domestic? slicers. To figure out what type of location crime happened, there is the 'Location' slicer.
When the end-user clicks on one of the options, the entire dashboard/UI drills down further to get into the point of interest, including the 'Word Cloud' and 'Heat Map'. The word cloud provides a more detailed description of the crime. The Heat Map provides the latitude and longitude coordinates of the zip as well as a special color scheme. The higher the number of crimes in the zip, the bigger and darker the circle. So from a simple 'business' perspective, the problem solving process to decrease the rate of a particular type of crime within a Zip/Area would start at the aforementioned.

#### Categorical slicers include Primary Type, ID, Case Number, Arrest?, Domestic?, Location, Numerical slicer includes the 'date range' (where you can slide accordingly)
##### Primary Type:
![Chicago_Crimes_PrimaryTypeLevels](https://user-images.githubusercontent.com/19572673/60402834-ddb15f00-9b62-11e9-9e13-c355a228ea22.PNG)
##### ID: Unique ID Assigned to Event 
##### Case Number: Unique Case Number Assigned to Event
##### Arrest?: True / False 
##### Domestic?: True / False
##### Location:
![Chicago_Crimes_LocationsLevels](https://user-images.githubusercontent.com/19572673/60402833-ddb15f00-9b62-11e9-8dd6-44b0818fe594.PNG)
##### Date Range:
![Chicago_Crimes_Slicers](https://user-images.githubusercontent.com/19572673/60401626-8dca9c00-9b52-11e9-9918-5ee940b8040d.PNG)
#### Word Cloud
![Chicago_Crimes_WordCloud](https://user-images.githubusercontent.com/19572673/60401686-3b3daf80-9b53-11e9-8f85-a523b2b5976a.PNG)
#### Zip Heat Map
![Chicago_Crimes_HeatMap](https://user-images.githubusercontent.com/19572673/60401685-3b3daf80-9b53-11e9-9fc2-81c5e6cfe324.PNG)
