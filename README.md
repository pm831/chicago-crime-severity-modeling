# Chicago Crime Analysis Data Exploration
### Pujan Malavia

![chicagocity](https://user-images.githubusercontent.com/19572673/62322030-1b5f1b80-b472-11e9-8b62-a8f5b56383f7.jpg)

### Abstract:

Every day, there are a numerous amount of crimes that occur across the country and the world. This can include major metropolitan areas with high populations and business activity. In this analysis, we look at the city of Chicago. What makes a Chicago dangerous? What types of crimes occur in within Chicago, primarily at the zip level? Which zips/areas have the highest concentration of crimes? What is the level of 'seriousness' for these crimes? Which zips/areas have the highest concentration of serious crimes? And after find that out, what days/times do they occur?  All of these questions are looked at in the analysis below.

### Industry:

Government Administration

### Overview:

Crime in Chicago has been tracked by the Chicago Police Department's Bureau of Records since the beginning of the 20th century. The city's overall crime rate, especially the violent crime rate, is higher than the US average. Chicago was responsible for nearly half of 2016's increase in homicides in the US, though the nation's crime rates remain near historic lows. The reasons for the higher numbers in Chicago remain unclear. An article in The Atlantic detailed how researchers and analysts had come to no real consensus on the cause for the violence.

https://en.wikipedia.org/wiki/Crime_in_Chicago

https://www.chicago.gov/city/en.html

Approximately 10 people are shot on an average day in Chicago.

http://www.chicagotribune.com/news/data/ct-shooting-victims-map-charts-htmlstory.html 

http://www.chicagotribune.com/news/local/breaking/ct-chicago-homicides-data-tracker-htmlstory.html 

http://www.chicagotribune.com/news/local/breaking/ct-homicide-victims-2017-htmlstory.html

### Use Case:
Figuring out specific Chicago Zips with the highest number of crimes given a period of time

### Initial Dataset(s):
Chicago Crimes Dataset 

### Software:
PowerBI

### Data Context:

This dataset reflects reported incidents of crime (with the exception of murders where data exists for each victim) that occurred in the City of Chicago from 2001 to present, minus the most recent seven days. Data is extracted from the Chicago Police Department's CLEAR (Citizen Law Enforcement Analysis and Reporting) system. In order to protect the privacy of crime victims, addresses are shown at the block level only and specific locations are not identified. This data includes unverified reports supplied to the Police Department. The preliminary crime classifications may be changed at a later date based upon additional investigation and there is always the possibility of mechanical or human error. Therefore, the Chicago Police Department does not guarantee (either expressed or implied) the accuracy, completeness, timeliness, or correct sequencing of the information and the information should not be used for comparison purposes over time.

https://www.kaggle.com/chicago/chicago-crime

Update Frequency: Daily

Fork this kernel to get started.

Acknowledgements

https://bigquery.cloud.google.com/dataset/bigquery-public-data:chicago_crime

https://cloud.google.com/bigquery/public-data/chicago-crime-data

Dataset Source: City of Chicago

This dataset is publicly available for anyone to use under the following terms provided by the Dataset Source —https://data.cityofchicago.org — and is provided "AS IS" without any warranty, express or implied, from Google. Google disclaims all liability for any damages, direct or indirect, resulting from the use of the dataset.

Banner Photo by Ferdinand Stohr from Unplash. 

### Data Fields:

unique_key: Unique identifier for the record.

case_number: The Chicago Police Department RD Number (Records Division Number), which is unique to the incident.

Date Date: when the incident occurred. this is sometimes a best estimate.

Block: The partially redacted address where the incident occurred, placing it on the same block as the actual address.

Iucr: The Illinois Unifrom Crime Reporting code. This is directly linked to the Primary Type and Description. See the list of IUCR codes at https://data.cityofchicago.org/d/c7ck-438e.

primary_type: The primary description of the IUCR code.

Description: The secondary description of the IUCR code, a subcategory of the primary description.

location_description: Description of the location where the incident occurred.

Arrest: Indicates whether an arrest was made.

Domestic: Indicates whether the incident was domestic-related as defined by the Illinois Domestic Violence Act.

Beat: Indicates the beat where the incident occurred. A beat is the smallest police geographic area – each beat has a dedicated police beat car. Three to five beats make up a police sector, and three sectors make up a police district. The Chicago Police Department has 22 police districts. See the beats at https://data.cityofchicago.org/d/aerh-rz74.

District: Indicates the police district where the incident occurred. See the districts at https://data.cityofchicago.org/d/fthy-xz3r.
Ward: The ward (City Council district) where the incident occurred. See the wards at https://data.cityofchicago.org/d/sp34-6z76.
community_area: Indicates the community area where the incident occurred. Chicago has 77 community areas. See the community areas at https://data.cityofchicago.org/d/cauq-8yn6.

fbi_code: Indicates the crime classification as outlined in the FBI's National Incident-Based Reporting System (NIBRS). See the Chicago Police Department listing of these classifications at http://gis.chicagopolice.org/clearmap_crime_sums/crime_types.html.

x_coordinate: The x coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.

y_coordinate: The y coordinate of the location where the incident occurred in State Plane Illinois East NAD 1983 projection. This location is shifted from the actual location for partial redaction but falls on the same block.

Year: Year the incident occurred.

updated_on: Date and time the record was last updated.

Latitude: The latitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.

Longitude: The longitude of the location where the incident occurred. This location is shifted from the actual location for partial redaction but falls on the same block.

Location: The location where the incident occurred in a format that allows for creation of maps and other geographic operations on this data portal. This location is shifted from the actual location for partial redaction but falls on the same block.

### Summary:
The bottom-line goal is to figure out specific Chicago Zips with the highest number of crimes reported within a period of time. Up on the User Interface, there is a 'date range' slicer to which the user can select the appropriate time frame. To drill down, there is a 'Primary Type' slicer which defines the type of crime. To test the severity of the crime, there are the 'Arrest?' and Domestic? slicers. To figure out what type of location crime happened, there is the 'Location' slicer.
When the end-user clicks on one of the options, the entire dashboard/UI drills down further to get into the point of interest, including the 'Word Cloud' and 'Heat Map'. The word cloud provides a more detailed description of the crime. The Heat Map provides the latitude and longitude coordinates of the zip as well as a special color scheme. The higher the number of crimes in the zip, the bigger and darker the circle. So from a simple 'business' perspective, the problem solving process to decrease the rate of a particular type of crime within a Zip/Area would start at the aforementioned.

Categorical slicers include Primary Type, ID, Case Number, Arrest?, Domestic?, Location, Numerical slicer includes the 'date range' (where you can slide accordingly)
Primary Type:

![Chicago_Crimes_PrimaryTypeLevels](https://user-images.githubusercontent.com/19572673/60402834-ddb15f00-9b62-11e9-9e13-c355a228ea22.PNG)

ID: Unique ID Assigned to Event 

Case Number: Unique Case Number Assigned to Event

Arrest?: True / False 

Domestic?: True / False

### Data Visualization

Old PowerBI Data Visualization (by Zip Code):
https://github.com/pm831/City_Of_Chicago_Crime_Analysis/blob/master/Chicago_Crimes_Visualization.pbix

![Chicago_Zip_Code_Crime_Analysis](https://user-images.githubusercontent.com/19572673/57345072-8f11b680-7117-11e9-90d0-8a55e88f4544.PNG)

Location:

![Chicago_Crimes_LocationsLevels](https://user-images.githubusercontent.com/19572673/60402833-ddb15f00-9b62-11e9-8dd6-44b0818fe594.PNG)

Date Range:

![Chicago_Crimes_Slicers](https://user-images.githubusercontent.com/19572673/60401626-8dca9c00-9b52-11e9-9918-5ee940b8040d.PNG)

Word Cloud:

![Chicago_Crimes_WordCloud](https://user-images.githubusercontent.com/19572673/60401686-3b3daf80-9b53-11e9-8f85-a523b2b5976a.PNG)

Zip Heat Map:

![Chicago_Crimes_HeatMap](https://user-images.githubusercontent.com/19572673/60401685-3b3daf80-9b53-11e9-9fc2-81c5e6cfe324.PNG)

PowerBI Data Visualization (new and modified):

![Map Viz](https://user-images.githubusercontent.com/19572673/85783658-84d4c200-b6f5-11ea-8caf-9a5a2c09ebc9.PNG)

Tableau Data Visualization (new and modified):
https://public.tableau.com/profile/pujan.malavia#!/

![Crimes vs  Poverty Viz](https://user-images.githubusercontent.com/19572673/85777591-c2cee780-b6ef-11ea-98c3-439e6d88437e.PNG)

Python (Jupyter Notebook) Visualization:
https://github.com/pm831/City_Of_Chicago_Crime_Analysis/blob/master/Chicago%20Crime%20Analysis.ipynb

Number of Crimes by Type:
![output_43_0](https://user-images.githubusercontent.com/19572673/85777642-cbbfb900-b6ef-11ea-9d1a-617670106ada.png)

Occurence Rate: Types of Crimes:
![output_45_1](https://user-images.githubusercontent.com/19572673/85777645-cbbfb900-b6ef-11ea-9edb-d66986a5594d.png)

Occurence Rate: Scene of Crimes:
![output_48_1](https://user-images.githubusercontent.com/19572673/85777646-cbbfb900-b6ef-11ea-9d98-5b03e14118e9.png)

Occurence Rate: Hour Crime Occured:

Occurence Rate: Day Crime Occured:

Occurence Rate: Month Crime Occured:

Normalized Crime Types by Location:

Normalized Crime Types by Time:

Normalized Crime Types by Day:

Normalized Crime Types by Month:

Crime Rates: Forecast

![output_68_0](https://user-images.githubusercontent.com/19572673/85777648-cc584f80-b6ef-11ea-9813-a553ce41edd0.png)

![output_69_1](https://user-images.githubusercontent.com/19572673/85777649-cc584f80-b6ef-11ea-978e-d4b8ced1c64c.png)

![output_73_1](https://user-images.githubusercontent.com/19572673/85777650-ccf0e600-b6ef-11ea-8fcd-dd940d4158b1.png)

![output_74_1](https://user-images.githubusercontent.com/19572673/85777651-ccf0e600-b6ef-11ea-899b-7648f8649161.png)

![output_75_1](https://user-images.githubusercontent.com/19572673/85777652-ccf0e600-b6ef-11ea-9bb5-02339b2a39f9.png)

![output_76_1](https://user-images.githubusercontent.com/19572673/85777654-ccf0e600-b6ef-11ea-851f-a620f41cc7af.png)

![output_77_1](https://user-images.githubusercontent.com/19572673/85777655-ccf0e600-b6ef-11ea-9a6d-c79b245a2c98.png)

![output_78_0](https://user-images.githubusercontent.com/19572673/85777656-cd897c80-b6ef-11ea-9858-ec3454df0f75.png)


![output_95_0](https://user-images.githubusercontent.com/19572673/85777657-cd897c80-b6ef-11ea-9e80-d5d85b7e7218.png)


![output_96_0](https://user-images.githubusercontent.com/19572673/85777659-cd897c80-b6ef-11ea-8205-9d75a79045ba.png)


![output_97_0](https://user-images.githubusercontent.com/19572673/85777660-ce221300-b6ef-11ea-9c06-025c3fe39a2f.png)


![output_104_1](https://user-images.githubusercontent.com/19572673/85777661-ce221300-b6ef-11ea-847d-1a35592ef12c.png)


![output_105_1](https://user-images.githubusercontent.com/19572673/85777662-ce221300-b6ef-11ea-95bc-aeabb4eeb4e0.png)

