# Airline On-Time Performance Data Exploration
## by Corinne Sandor


## Dataset

The dataset I selected for my analysis was through Udacity: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/HG7NV7

There were originally 21 datafiles (with a total of 2.5 millions flights) ranging from 1987 - 2008. Since there were so many files, I merged all the data files together in a seperate Jupyter notebook, Merged_Airline_Data. I was able to successfully merge 19 of the datafiles, 2 of them were corrupt (2001 & 2002).

Upon successful merging, I read the data into the Jupyter notebook, Part_I_exploration, where I performed some data wrangling. I went through the columns that I had interest in using for my analysis:
- Replacing a miscoded Origin airport with "None"
- Converting WeatherDelay and NASDelay to floats
- Keeping only positive DepDelay times in the dataframe
- Dropping rows with data missing from the dataframe
- Dropped an extra column (Unnammed - appeared after merging data)
- Added a delay type column 

After wrangling the data, I was left with about 200K flights.


## Summary of Findings

Throughout my exploration, the main feature of interest has been departure delay time. Here is a short summary of what I found:
 
> Feature with high frequency of departure delays:
- Late Aircraft delays, Carrier Delay, and NAS (National Aviation System) delays
- Southwest Airlines (WN) had the most delayed flights out of all 4 carriers
 
> Features with to short departure delays (less than 40 minutes):
- Carriers: Southwest (WN) and US Airways (US).
- Security Delays & NAS Delays (with the exception of security delays on Saturdays).

> Features with long departure delays (above 40 minutes):
- Weather Delays, Late Aircraft Delays & Carrier Delays
- Carriers: JSX Airlines (XE) & United Airlines (UA).


## Key Insights for Presentation

For my presentation, I focus on the just the influence of delay types and airline carriers on departure delay times. 

I start by introducing the frequency at which certain delay types occur, then looking at the average delay time for each main delay type on a day to day basis. Afterwards, I do the same thing for airline carriers. 

Since there seemed to be some trends with airline carrier delays, we wrap up this presentation by looking at the average departure delays for each airline carrier by delay type. 