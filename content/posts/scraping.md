title: Web scraping with Python
date: 2022-06-09
description: Discussing Scraping Dynamic Pages
tag: python
project: Advanced Python Course
platform: Python Workshop
link: http://example.com

Imagine we want to perform web scraping on a platform that contains publicly available real estate listings. We aim to extract the property price, address, distance, station name, and the nearest type of transportation. This information will help us understand how property prices are distributed based on public transportation accessibility in a specific city.

Assuming the query leads to a search results page that looks like this:
Search Results for Python Web Scraping

Once we identify which elements of the website store the necessary data, we need to devise a scraping logic that allows us to retrieve all the required information from each listing.

We will need to address the following questions:

* How to obtain a single data point for one property (e.g., data from the "price" tag in the first listing)?
* How to retrieve all data points for one property from an entire page (e.g., all "price" tags on a single page)?
* How to collect all data points for one property from all result pages (e.g., all "price" tags from all result pages)?
* How to handle discrepancies when data can be of different types (e.g., some listings have prices listed as "price upon request."Ultimately, we'll have a column consisting of numeric and       string values, which doesn't allow for straightforward analysis)?
* How to best extract complex information (e.g., assuming each listing contains information about public transportation, such as "0.5 miles to metro station XY")?

