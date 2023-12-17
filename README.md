![Illustration of worldwide weather](https://img.freepik.com/free-vector/hand-drawn-water-cycle-illustration_23-2149107732.jpg?w=1800&t=st=1698824765~exp=1698825365~hmac=e03c73de147c19b92f341c6c281f3765e955d5fc589663a109d418b52a64d2b5)
# Weather-Exploration-and-Vacation-Planning
## Description
In this project, I'm tasked with answering the question: "What is the weather like as we approach the equator?". In the first part (part 1) of the project, I've created a Python script to visualise the weather of over 500 cities of varying distances from the equator. Using citipy Python library and OpenWeatherMap API, I've created a representative model of weather across cities. In the second part of the project, I use the weather data from part 1 to plan future vacations.
## Usage
Please navigate to the WeatherPy folder for the code for WeatherPy (part 1) and VacationPy (part  2). 
Please navigate to the output folder for a cities data csv file and 4 other png files of scatterplots generated in part 1 of the project.
## Installations
The following dependencies are needed to run the code. Please copy the exact code below to your code editor to import these dependencies:
-Pandas: (1) pip install pandas, (2) import pandas as pd
-hvPlot: (1) pip install holoviews hvplot, (2) import hvplot.pandas
-requests: (1) pip install requests, (2) import requests
-Path: from pathlib import Path

## Weather exploration
### Step 1: Create a map that displays a point for every city in the city_data_df DataFrame. The size of the point should be the humidity in each city.
![Alt text](<Screenshot 2023-12-17 at 10.25.31 pm.png>)

The purpose of the map is to visualise the locations of the cities in our current dataset and their correspondent humidity. The map has the following features:
1. geo: `True`
2. size: `Humidity`
3. scale: 1
4. color: `city`
5. alpha: 0.5
6. tiles: `OSM`
7. frame_width: 800
8. frame_height: 500

### Step 2: Narrow down the `city_data_df` DataFrame to find the ideal weather condition
The purpose of this step is to narrow down cities that fit our pre-defined weather criteria and drop any results with null values.
![Alt text](<Screenshot 2023-12-17 at 10.38.31 pm.png>)

### Step 3: For each city, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates.
In this section, I used Geoapify API to search for the nearest hotel in each city found in step 2. 
![Alt text](<Screenshot 2023-12-17 at 10.44.43 pm.png>)

### Step 5: Add the hotel name and the country as additional information in the hover message for each city in the map.
In this section, I generated an interactive map to display all the hotels in step 3 with the hotel name and the country as additional information for each hotel. 

The following parameters were used for the map:
1. geo: `True`
2. scale: 1
3. color: `Hotel Name`
4. tiles: `OSM`
5. frame_width: `800`
6. frame_height: `500`
7. hover_cols: `Country` and `Hotel Name`

## Credits
Special thanks to these individuals for their contributions to the project:
1. BCS tutors
2. ASK BCS learning assistants
