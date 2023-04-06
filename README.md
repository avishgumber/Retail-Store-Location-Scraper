# Retail-Store-Location-Scraper
Using web scraping methods (such requests and BeautifulSoup) to collect information from a website, such as store names, addresses, opening and closing times, coordinates (latitude and longitude), and phone numbers.

## Introduction
In this assignment, the goal was to scrape the store locations, store
name, address, timings, coordinates, and phone number of my
favourite retail brand in India. I chose a popular retail brand Café
Coffee day and used Python libraries like BeautifulSoup , requests
and json to scrape the website and extract the required information.
The extracted data was saved to a CSV file and uploaded to a GitHub
repository along with the code. This report outlines the approach,
challenges faced, and solutions implemented during the web
scraping process.
![Cafe-Coffee-Day-Logo-Vector](https://user-images.githubusercontent.com/103429014/230310384-24f302f9-f99f-46eb-975f-5395a52cc4d2.png)

## Approach
The first step was to identify the website of the retail brand where
the location data can be found (cafecoffeeday.com/store-locator)
and understand its HTML structure. I inspected the website's source
code and found that the store locator was a dynamic element that
required JavaScript to load. After analysing the website, I found that
the relevant data was present in index 11 of script elements that
contained JSON data.
Firstly, I import the necessary modules, including requests for
sending HTTP requests, JSON for handling JSON data, BeautifulSoup
for parsing the content and converting html content for reading and
interpreting and finally used pandas for converting JSON into
DataFrame that later can help in storing data in csv format and also
help in data pre-processing if needed.
I used Request library in python to send a request to the website's
URL and retrieve the JSON data. I used the built-in Python JSON
module to parse the JSON data and extract the required information
such as store name, address, timings, coordinates, and phone
number.

## Challenges
One of the main challenges faced while working with this code was
to extract the required data from the JSON response. As the JSON
response was a nested structure, it required careful understanding
and analysis to extract the relevant data. We had to identify the keys
and values that corresponded to the information we needed.
Another challenge was to check the reliability of locations
coordinates whether they are working or not and next was to check
if I have the required information or not and also to remove
unnecessary columns which don’t have any use case.

## Solution
To overcome the challenge of extracting the required data from the
JSON response, we carefully analysed the structure of the JSON data
and used the appropriate keys to extract the information we needed.
We also used the built-in Python JSON module to simplify the parsing
process.
To check the reliability of location coordinates if they are working I
used folium library to plot the locations and markers in the map
(FastMarkerCluster in folium)
![Screenshot (379)](https://user-images.githubusercontent.com/103429014/230310117-4e3434b6-aa41-4304-b059-cb5f129fb913.png)

To clean the data, we removed the irrelevant columns from the CSV
file, ensuring that only the required information was present change
the data types for some column like time column and coordinates
and make csv ready for the end use case for further analysing like
Exploratory data analysis, predictive analytics etc. which can help in
taking important business decisions and build strategy.
Use case can be If company wants to open a new store where it
should be , which stores are working great and which are not can be
easily understand with map visualisation because it opens door for
think with a new perspective like it can tell if the location have a
relationship with store performance.

## Conclusion
In conclusion, web scraping is a powerful technique that can be used
to extract valuable information from websites. However, it can also
be challenging, especially when dealing with dynamic elements and
nested JSON structures. By understanding the website's HTML
structure, using appropriate tools and libraries, and ensuring the
extracted data is accurate and reliable, we can successfully extract
the required information from a website. The data is 100% reliable
and extracted from the café coffee day official website and it can be
useful for various business use cases.
