Scraping Health Inspection Data from King County

-Used class lecture notes to complete web scraper:
https://codefellows.github.io/sea-python-401d5/assignments/tutorials/scraper.html

-python scraper.py will fetch results directly from King County.
-python scraper.py test will use your stored results from file.


-BeautifulSoup allows us to use functions as filters. These functions must take an element as their only argument, and return True if the element should pass through the filter, and False if not.


Function List:

Step 1: Fetch Search Results
The first step uses the requests library to fetch a set of search results from the King County government website.


Step 2: Parse Search Results
Next, we use a function parse_source to set up the HTML as DOM nodes for scraping. 


Step 3: Extract Listing Information
The next series of functions will extract useful information from each of the restaurant listings in the parsed HTML search results. 

3a: Find Individual Listings
This finds the container that holds each individual listing.

3b: Extract Metadata

3b1 The first is the rows that contain this information have two cells in them. One that might contain a label for the metadata and a second that contains the value.

3b2 The second is that the two <td> elements it contains are immediate children, not contained within some nested structure.

3c: Store Metadata
This function puts all our data into a data structure that will represent a single restaurant. Our data is paired as labels and values. 

3d: Extract Inspection Data
This extracts the information we need to build our inspection data for each restaurant. 