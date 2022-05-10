
Data Description: 

solarEfficiencyAndWeather2020.xlsx holds the coordinated location of every PV solar power plant in the United States operating every month of the year, along with seven features of every plant's monthly weather data. For every month, every PV power plant has the following weather features: 

PPT (Precipitation) 
Tmin (Minimum Temperature) 
Tmean (Mean Temperature) 
Tmax (Maximum Temperature) 
TDmean (Mean Dewpoint Temp)  
VPDmin (Minimum Vapor Pressure Deficit) 
VPDmax (Maximum Vapor Pressure Deficit)


How the data is retrieved:
 
Solar Workbook.xlsx is a combination of the 2020 EIA-860 and EIA-923. The Generator sheet in EIA-860 is used to match the coordinates to power plants in the Plants sheet in EIA-860. 

Data is refined to only include photo-voltaic power plants. 

The monthly efficiency of every PV power plant is found by dividing the EIA-960 monthly generation data by the number of days in the month and divided by the nameplate capacity of the power plant. These efficiency values are then normalized between -1 and 1. 

Now that the coordinated location of every power plant and its monthly efficiency is found, drop any power plant sample that is missing an efficiency for any particular month. 

Next, interpret weather data.ipynb script is used to match the monthly weather data. 


Proof of Accuracy: 
To prove that EIA data correctly matches the Oregon State PRISM weather data, go to https://www.eia.gov/electricity/data/eia923/, select monthly weather features for the year 2020, and search and compare the power plants by any coordinates in solarEfficiencyAndWeather2020.xlsx. 


Sources: 
EIA-860 https://www.eia.gov/electricity/data/eia860/ 
EIA-923 https://www.eia.gov/electricity/data/eia923/ 
Weather Data: https://prism.oregonstate.edu/explorer/ 
