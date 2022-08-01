# World_Weather_Analysis

##Overview of the Analysis
We have been asked to optimize the PlanMyTripp app by adding more functionality to the original test model. We have added weather descriptions to the weather data provided by OpenWeatherMap API, input statements to filter the data for customer weather preferences, and allow the beta testers to choose four cities and create an automated travel itinerary on there behalf. Finally, using the Google Maps Directions API, we mapped out the travel route between the four cities as well as a marker layer map.

#Results
This functionality request is parsed into 3 sections:
1) Retrieve Weather Data
2) Create a Customer Travel Destinations Map
3) Create a Travel Itinerary Map

##Section 1
Attained Weather data from API and refactored code to include "Current Weather Description"

##Section 2
Based on the customer weather preferences, potential locations are populated for the user with a local Hotel Names in the area. Then we add a marker map for all the potential visit sites. Each marker contains Hotel Name, City, Country, Weather Description, and Max Temperature.

##Section 3
We allow user to pick four cities and create a vacation itinerary route to travel between the four cities. Then providing a map with markers only for their trip.

#Summary

#Challenges:
Get the latitude-longitude pairs as tuples from each city DataFrame using the to_numpy function and list indexing.

start = vacation_start['Lat'].to_numpy()[0], vacation_start['Lng'].to_numpy()[0]
end = vacation_end['Lat'].to_numpy()[0], vacation_end['Lng'].to_numpy()[0]
stop1 = vacation_stop1['Lat'].to_numpy()[0], vacation_stop1['Lng'].to_numpy()[0]
stop2 = vacation_stop2['Lat'].to_numpy()[0], vacation_stop2['Lng'].to_numpy()[0]
stop3 = vacation_stop3['Lat'].to_numpy()[0], vacation_stop3['Lng'].to_numpy()[0]

Create a direction layer map using the start and end latitude-longitude pairs,
## and stop1, stop2, and stop3 as the waypoints. The travel_mode should be "DRIVING", "BICYCLING", or "WALKING".
fig = gmaps.figure()
travel_route = gmaps.directions_layer(start, end, waypoints=[stop1,stop2,stop3], travel_mode="DRIVING" or "BICYCLING" or "WALKING")
fig.add_layer(travel_route)
fig
## 8. To create a marker layer map between the four cities.
##  Combine the four city DataFrames into one DataFrame using the concat() function.
itinerary_df = pd.concat([vacation_start, vacation_stop1,
                          vacation_stop2, vacation_stop3]
                         ,ignore_index=True)
itinerary_df
