# World_Weather_Analysis
## Project Overview
The intent of the project was to investigate ways in which we can enhance the PlanMyTrip App by adding interactive capabilites to it. This project was done in three stages.

## STAGE ONE - Retrieve Weather Data for 500+ random cities
### Step One - Generating various destination possibilities
We started off by generating 2000 latitudes and longitudes. Based on these co-ordinates we then generated a list of cities as locations. We started off with 748 cities in the database.
### Step Two - Gathering weather related information for the locations
We used the Open Weather API to download and parse weather related information for each of the cities in our database. We eliminated the cities that did not have the relevant information we needed and ended up with 693 cities. For each of these cities we hade the following informaiton:<br>
City, Country, Date, Latitude, Longitude, Max Temp, Humidity, Cloudiness, Wind Speed and Weather description.
### Step Three - Creating a final database 
At the end of this stage we now had a database of 693 cities with the 10 cahracteristics for each one of them. We saved this information in a csv file.

## STAGE TWO - Creating a Customer Travel Destinations Map
### Step One - Ask for input
In this step we used the database from Stage One and created the option to capture input from the user relating to the Maximum and Minimum temperatures they would be comfortable with at their preferred locations.
### Step Two - Identify possible destinations
The parameters chosen by the user were then used to narrow down the original database and create a list of preferred locations. We made sure that the list was complete and did not include rows with incomplete information since that would not lend to a good user experience.
### Step Three - Identify the closest Hotel to the destinations & add to the database
It was felt that it would be a great to also provide the name of a Hotel that was closest to the preferred vacation spot as well. In order to accomplish this we took advantage of the Google Maps & Places API and in particular the Nearby Search. Once again we extracted the JSON file for the co-ordinates (Latitude & Longitude) for each city, which was part of the database, and extracted the name of the nearest Hotel. This hotel name was also added to the existing information previously gathered for each city.
### Step Four - Create a Map with location markers
Finally, we decided that it would be great to present a visual representation of the information that we had gathered in the way of markers on a map, and each of these markers, when clicked on would provide relevant information to the user. We felt this would be a wonderful and essential feature that would be useful to the user. Here is what the map would look like, we have activated a couple of markers to show the information displayed:<br>
![Map with markers](https://github.com/lallben/World_Weather_Analysis/blob/main/Vacation_Search/WeatherPy_vacation_map.png)
## STAGE THREE - Creating a Travel Itinerary Map
This was the final piece to this project where we thought - "Wouldn't it be a great idea to provide an itinerary to the user based on their choice of destinations?".
In order to accoomplish this, we simply built on the work done in Stage Two. However here we had to take the help of the Directions API. With the Directions API we were then able to create a travel map and a Itinerary based on four possible choices that a user could make. We made the choice ourselves and created a mp to see what this would look like.<br>
Here is a view of the two maps we got:<br>
![Itinerary Map](https://github.com/lallben/World_Weather_Analysis/blob/main/Vacation_itinerary/WeatherPy_travel_map_markers.png)
![Travel Map](https://github.com/lallben/World_Weather_Analysis/blob/main/Vacation_itinerary/WeatherPy_travel_map.png)
## Summary
The possibilities of what can be done to enhance the PlanMyTrip user experience are endless. Tis project has opened our eyes to what we can do using API's that are available for use. The results of this project will be used to create code that will actually enable the App to be more interactive and useful.
