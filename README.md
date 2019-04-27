# Chicago-Traffic-Violations

### Project Overview
The goal was to create a set of visualizations about the traffic cameras in Chicago intended for the Mayor of Chicago. The project included downloading the data from the City of Chicago's Website and understanding the information from the data: https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4/data. 

Then the first round of data visualizations were intended to explore the data set using Tableau and then to further develope a deeper analysis based on that exploration. 

### Data Set Information

The Chicago Speed Camera Violations set is of the number of traffic violations that occur over time from July 1, 2014, through April 10, 2019. The violations in the dataset reflect all instances collected by the camera's radar system that has been viewed by two individual city contractors, including instances not resulting in a citation.

In an effort to increase the safety for children in the City of Chicato, speed cameras were installed in key childrens safety zones around schools and parks. School zones have active cameras Monday through Friday from  7 am to 4 pm when children are present, whereas cameras near parks are active 365 days per year, generally from 6 am until 11 pm. Fines for violations 10 miles per hour (MPH) or less is $35.00, and violations 11 MPH and over is $100.
https://www.chicago.gov/city/en/depts/cdot/supp_info/children_s_safetyzoneporgramautomaticspeedenforcement.html

Data about alleged crimes in Chicago was also examined to look at the relationship between the number of speeding violations and the amount of criminal activity in Chicago. The data was extracted from the Police Department's Citizen Law Enforcement Analysis and Reporting (CLEAR) system and spanned from May 7, 2015 through April 14, 2019. In order to protect the privacy of the victims, locations are only given at the block level. 
https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2

In order to examine the relationship between crimes and speed violations, the data sets were cleaned and merged on a truncated longitude and latitude. In the exported csv files the null vlaues were discarded, then longitudes and latitudes were truncated to the 100's place after the decimal for less precision. In the python notebook attached, the average number of violations were grouped by the unique set of truncated coordinates and the number of crimes were summed at an aggregated level for each unique truncated coordinates. The data was merged to show all of the overlapping coordinates between the two data sets.   

### Data Exploration and Final Analysis
The first stage of data exploration lead to the discovery that the number of violations were decreasing overtime. 

![Data Exploration](Daily_Speed_Trap_Violations.png)
https://public.tableau.com/profile/laura.klipp#!/vizhome/Speed_Violations/TrafficCameraDataExploration

Since the daily violations over time show a lot of noise. My next visualization shows the same number of violations, but at a weekly level for a smoother graph. While it is clear to see the downward trend over time, there is still a lot of  seasonality to this data and therefore adding a trendline shows the decrease more clearly.  

![Violations Over Time](weekly_time_trend.png)
https://public.tableau.com/profile/laura.klipp#!/vizhome/Data_for_Mayor/DecreasingViolations

While many factors could effect the declining number of violations over time, the intended outcome was for people to stope speeding through children's safety zones. One way to see that is to see how the number of violations per camera changes over time, to ensure that it wasn't a decreased number of cameras causing a decrease in violations. Making a calculation of the average number of violations per unique camera ID we see that there is also a decline in the average violations for each camera over time. 

![Violations Per Camera ID](per_cam_violations.png)
https://public.tableau.com/profile/laura.klipp#!/vizhome/Data_for_Mayor/DecreasingViolations


![Crime and Violation Correlation](correlation.png)
https://public.tableau.com/profile/laura.klipp#!/vizhome/Data_for_Mayor/DecreasingViolations

![Chicago_police](Police_Expediture.png)
https://www.forbes.com/sites/niallmccarthy/2017/08/07/how-much-do-u-s-cities-spend-every-year-on-policing-infographic/#17321124e7b7
