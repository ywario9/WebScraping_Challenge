# Web Scraping Challenge


The mission_to_mars.ipynb Jupyter notebook file contains all of the scraping code for this application. Specifically, I used BeautifulSoup, Pandas, and Requests/Splinter to scrape the following information about Mars from the following websites:

* NASA Mars News
Scraped the latest news title and paragraph text.
* JPL Mars Space Images - Featured Image
Scraped the full size image url for the current featured Mars image.
* Mars Weather Twitter Account
Scraped the latest Mars weather tweet from the page.
Mars Facts Website
* Scraped the table containing facts about the planet. Then, used Pandas to convert the data to a HTML table string.
USGS Astrogeology Website
* Scraped the name and image url for each of Mar's hemispheres and used a Python dictionary to store the data using the keys img_url and title. Then, appended the dictionary with the image url string and the hemisphere title to a list. This list contains one dictionary for each hemisphere.
* MongDB and Flask Application
After scraping the various sites for the information needed for the application, I used MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above.

To do this, I did the following:

* Converted the Jupyter notebook into a Python script called scrape_mars.py with a function called scrape, which executes all of the scraping code from above and returns one Python dictionary containing all of the scraped data.
* Created a route called /scrape, which imports the scrape_mars.py script and calls the scrape function.
* Created a root route /, which queries the Mongo database and passes the mars data into an HTML template to display the data.
* Created a template HTML file called index.html that takes the mars data dictionary and displays all of the data in the appropriate HTML elements.
