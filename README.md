=======

# How to read my files

Part 1: Part1_Choose_top5_cities.ipynb

Part 2: Part2_Scrap_hotels.ipynb

Additionnal files (pictures, scrapping results) to be found in other folders

=======

# Plan your trip with Kayak

## Company's description 📇

[Kayak](https://www.kayak.com) is a travel search engine that helps users plan their next trip at the best price.

The company was founded in 2004 by Steve Hafner & Paul M. English. After a few rounds of fundraising, Kayak was acquired by [Booking Holdings](https://www.bookingholdings.com/) which now holds:

* [Booking.com](https://booking.com)
* [Kayak](https://kayak.com)
* [Priceline](https://www.priceline.com/)
* [Agoda](https://www.agoda.com/)
* [RentalCars](https://Rentalcars.com/)
* [OpenTable](https://www.opentable.com/)

With over $300 million revenue a year, Kayak operates in almost all countries and all languages to help its users book travels across the globe.

## Project 🚧

The marketing team needs help on a new project. After doing some user research, the team discovered that **70% of their users who are planning a trip would like to have more information about the destination they are going to**.

In addition, user research shows that **people tend to be defiant about the information they are reading if they don't know the brand** which produced the content.

Therefore, the Kayak Marketing Team would like to create an application that will recommend where people should plan their next holidays. The application should be based on real data about:

* Weather
* Hotels in the area

The application should then be able to recommend the best destinations and hotels based on the above variables at any given time.

## Goals 🎯

As the project has just started, your team doesn't have any data that can be used to create this application. Therefore, your job will be to:

* Scrape data from destinations
* Get weather data from each destination
* Get hotels' info about each destination
* Store all the information above in a data lake
* Extract, transform and load cleaned data from your data lake to a data warehouse

## Scope of this project 🖼️

The marketing team wants to focus first on the best cities to travel to in France. According to [One Week In.com](https://one-week-in.com/35-cities-to-visit-in-france/), here are the top 35 cities to visit in France:

[
    "Mont Saint Michel",
    "St Malo",
    "Bayeux",
    "Le Havre",
    "Rouen",
    "Paris",
    "Amiens",
    "Lille",
    "Strasbourg",
    "Chateau du Haut Koenigsbourg",
    "Colmar",
    "Eguisheim",
    "Besancon",
    "Dijon",
    "Annecy",
    "Grenoble",
    "Lyon",
    "Gorges du Verdon",
    "Bormes les Mimosas",
    "Cassis",
    "Marseille",
    "Aix en Provence",
    "Avignon",
    "Uzes",
    "Nimes",
    "Aigues Mortes",
    "Saintes Maries de la mer",
    "Collioure",
    "Carcassonne",
    "Ariege",
    "Toulouse",
    "Montauban",
    "Biarritz",
    "Bayonne",
    "La Rochelle"
]

# Project Description

Your team should focus **only on the above cities for your project**.

## Helpers 🦮

To help you achieve this project, here are a few tips that should help you.

### Get weather data with an API

Use [Nominatim](https://nominatim.org/release-docs/develop/api/Search/) to get the GPS coordinates of all the cities (no subscription required).

Use [OpenWeatherMap](https://openweathermap.org/appid) and [One Call API](https://openweathermap.org/api/one-call-api) to get weather information for the 35 cities and put it in a DataFrame.

Determine the list of cities where the weather will be the nicest within the next 7 days. For example, you can use the values of `daily.pop` and `daily.rain` to compute the expected volume of rain within the next 7 days. But it's only an example, and you can have different opinions on what a nice weather would be like. Maybe the most important criterion for you is the temperature or humidity, so feel free to change the rules!

Save all the results in a `.csv` file, including the name of the cities and a unique identifier for each city.

Use Plotly to display the best destinations on a map.

### Scrape Booking.com

Scrape data directly from [Booking.com](https://www.booking.com/) to get hotel information such as name, URL, coordinates, user scores, and hotel descriptions.

### Create your data lake using S3

Once you've built your dataset, store it as a CSV file in an S3 bucket.

### ETL

Extract the data from S3 and create a SQL Database using AWS RDS. Store the data in the database for further analysis.

## Deliverable 📬

To complete this project, your team should deliver:

- A `.csv` file in an S3 bucket containing enriched information about weather and hotels for each French city.
- A SQL Database where the cleaned data can be accessed from S3.
- Two maps showcasing the top 5 destinations and top 20 hotels in the area. You can use Plotly or any other library to create the maps.

![Map](https://full-stack-assets.s3.eu-west-3.amazonaws.com/images/Kayak_best_destination_project.png)
