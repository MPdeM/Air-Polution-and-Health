# Determinats of Health: Air Quality and its association with pulmonary morbility and mortality.

Air pollution is a major healh concern and is associated with pulmonary morbidity and mortality. 

With this project we wanted to check if the air pollution had an effect on the population’s respiratory diseases by increasing the incidence in locations where the pollution was higher. We also wanted to see if it was any correlation of disease prevalence and complications with socio-economic status. 

The correlation between respiratory diseases like asthma and COPD and air pollution (particulates) is well documented. Our initial scope was to find:
1) EPA data for recent years for air quality and concentration of 6 main pollutants: particulates PM2.5 and PM10, SO2 Sulfur Dioxide, NO2 Nitrogen Dioxide, CO Carbon Monoxide, and O3 ozone. 
2) CDC data of prevalence of asthma, COPD and lung cancer.
3) census data forthe same recent years.
With this data we wanted to create heat maps and do colocatization of reported pollutant concentrations and prevalence in US. We also wanted to check if the there was more prevalence of cases where people has lower income becouse US health system is not public like in other countries in EU. 

Methodology: We used  Matplotlib, APIs (census API, geolocation), basic statistical analysis using Scipy, and gmaps. 

The data was extracted from the following sources: 

Air Pollution: https://aqs.epa.gov/aqsweb/airdata/download_files.html

USA Income and Population: https://www.countyhealthrankings.org/explore-health-rankings/rankings-data-documentation/national-data-documentation-2010-2017

Lung Cancer: https://gis.cdc.gov/Cancer/USCS/DataViz.html

Asthma:: https://www.cdc.gov/asthma/brfss/2015/tableL1.html

COPD: https://www.cdc.gov/mmwr/volumes/67/wr/mm6707a1.htm 

Google Places API: https://developers.google.com/maps/documentation/geocoding/start

The main challenge within the time constrains was to find the health data. To map prevalence and location, we needed health data at the county -or city- level. However the data from CDC that we found was at the state level. We were able to find more granular data for Lung Cancer.  In addition, the data available was not complete for recent years and the most recent data set we found for health data was 2016. 
We changed the scope and focused our data analysis on building two data sets, first one at the state level with polution data, income/uninsured data, and health data (copd/asthma/lung cancer) and a second one at the county level with polution data, income/uninsured data, and health data from lung cancer. 
Once we build the two data sets the geographical coordinates where added. This two data sets were  used to do statistics and to visualize the  data using Jupyter Gmaps.

Lastly, for fun, we ploted Massachusetts (where health insurance is mandatory since 2007), California and Texas.

#Files

The original csv files from our various sources, the Jupyter notebook used to clean the data, and the final cleaned data sets as csv files are in the data_cleanup folder.

The cleaned files are in the Resources folder

County_Analysis.ipynb has the statistical analysis and the heat maps at the countly level

US_Analysis.ipynb has the statistical analysis and the heat maps at the state level

The analysis for the three states is in the ForFun folder. The three files are basicaly the same except that each one uses subset of data using the loc command. MA_Analysis.ipynb has the statistical analysis for MA, CA_Analysis.ipynb for CA, and TX_Analysis.ipynb for TX.

Stater plots and heat maps are in output_plots folder

#Results

Data showed that Asthma prevalence in 2016 had no correlation with any of the parameters associated with air polition. Lung Cancer prevalence showed a weak correlation with AQI (with unhealthy days) and COPD prevalence had no correlation with any of the air pollution parameters and had a moderate correlation with the percentage of smokers. 
Asthma prevalence is independent of socio-economic status but Lung Cancer and COPD have a moderate correlation.


