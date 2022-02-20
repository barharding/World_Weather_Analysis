# World Weather Analysis

## Weather Data

The Weather_Database jupyter notebook starts by generating 2000 random latitudes and longitudes.  The code then finds the nearest city by leveraging the citipy python library.  This is primarily done to weed out any lat/long combinations which are not on land.

Using the OpenWeatherMap API, information about the cities are returned which includes:
-  Latitude and longitude
-  Maximum temperature
-  Percent humidity
-  Percent cloudiness
-  Wind speed
-  Weather description (for example, clouds, fog, light rain, clear sky)

This data is then exported to a CSV for use in the Travel Destination Map.

## Travel Destination Map

The Vacation_Search jupyter notebook ingests the city weather data from the weather_database.  It asks the end user to specify what is the maximum and minimum temperature preferences for their vacation.  With these inputs a filtered list of cities is generated and using googles Nearby Search Api a list of hotels is retreived.  These hotels are then mapped and the marker updated to include a weather description for the city the hotel is in.

## Travel Itinerary Map

The final deliverable, found in the Vacation_Itinerary juypter notebook leverages the Directions API by Google to display on a map a route which starts and ends with the same city and loops through the other three, effectively creating a milk run.
