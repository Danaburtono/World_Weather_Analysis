# World_Weather_Analysis

## Overview of the Analysis
We have been asked to optimize the PlanMyTripp app by adding more functionality to the original test model. We have added weather descriptions to the weather data provided by OpenWeatherMap API, input statements to filter the data for customer weather preferences, and allow the beta testers to choose four cities and create an automated travel itinerary on there behalf. Finally, using the Google Maps Directions API, we mapped out the travel route between the four cities as well as a marker layer map.

# Results
This functionality request is parsed into 3 sections:
1) Retrieve Weather Data
2) Create a Customer Travel Destinations Map
3) Create a Travel Itinerary Map

## Section 1: Weather Database
Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap and refactored code to include "Current Weather Description".

<img width="616" alt="Screen Shot 2022-07-31 at 6 15 01 PM" src="https://user-images.githubusercontent.com/107026442/182056146-b095ee91-a462-4b63-aeb6-6369ba4d82b4.png">


## Section 2: Customer Travel Destinations Map
Based on the customer weather preferences, potential locations are populated for the user with a local Hotel Names in the area. Then we add a marker map for all the potential visit sites. Each pop-up marker contains Hotel Name, City, Country, Weather Description, and Max Temperature.

<img width="616" alt="Screen Shot 2022-07-31 at 6 16 05 PM" src="https://user-images.githubusercontent.com/107026442/182056184-7ef16ef5-7780-46ed-bf48-d67a0f41ee46.png">

<img width="616" alt="Screen Shot 2022-07-31 at 6 17 17 PM" src="https://user-images.githubusercontent.com/107026442/182056213-d3dd7ba8-ae23-417f-9961-2edd39f793f0.png">


## Section 3: Travel Itinerary Map
We allow user to pick four cities and create a vacation itinerary route to travel between the four cities. Then providing a map with markers only for their trip.

<img width="616" alt="Screen Shot 2022-07-31 at 6 30 11 PM" src="https://user-images.githubusercontent.com/107026442/182056239-55109c95-46a8-45a4-acc6-cc7b7b21fb70.png">

<img width="616" alt="Screen Shot 2022-07-31 at 6 30 24 PM" src="https://user-images.githubusercontent.com/107026442/182056257-ccb4705a-8c21-4287-aefa-6770c14f18c4.png">
