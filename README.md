# Bike Sharing Demand
For my Metis Intro to Data Science project, I'm working on the **Bike Sharing Demand** Kaggle competition at https://www.kaggle.com/c/bike-sharing-demand

## Objective
My goal is to build a model to predict bike rental demand for the Capital Bikeshare program in Washington, D.C. using the provided historical usage and weather data.

I'll be using hourly rental data spanning two years (January 2011 - December 2012), with the 1st-19th day of each month for training. The required output is total count of bikes rented per hour for the 20th to end of month.

## Data Fields
* datetime: hourly date + timestamp  
* season
  - 1 = spring
  - 2 = summer
  - 3 = fall
  - 4 = winter
* holiday: whether the day is considered a holiday
* workingday: whether the day is neither a weekend nor holiday
* weather
  - 1 = Clear, Few clouds, Partly cloudy
  - 2 = Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  - 3 = Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  - 4 = Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
* temp: temperature in Celsius
* atemp: "feels like" temperature in Celsius
* humidity: relative humidity
* windspeed: wind speed
* casual: number of non-registered user rentals initiated
* registered: number of registered user rentals initiated
* count: number of total rentals

## Background
I chose this Kaggle competition since I've been following the rollout of various bikeshare programs around the country and the Ford GoBike system recently launched in the Bay Area. A bike station is located on my block and I'm curious how much demand there currently is and will be for this new mode of local transportation. Ford GoBike will be making their trip data public soon (https://www.fordgobike.com/system-data), so in the meantime this is a very similar dataset on which I'll be able to test out different approaches.

## Results
All of my code and findings are in the "Bikeshare Demand - EDA and Modeling" Jupyter notebook. After three late submissions (competition ended in 2015), I achieved a RMSLE of 0.45434 using a slightly tuned Random Forest and a handful other tweaks to the training data, but I was not placed on the public leaderboard. However, this score corresponds to 883 out of 3252 total competitors, i.e. within the top 28 percent. The mean value RMSLE benchmark was 1.58455, so I'm quite happy with my result given the short duration of this project. I will continue to explore further ways to improve my score as outlined in the final section of the notebook.
