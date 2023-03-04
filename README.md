# Data Collection Challenge
----
## Table of Contents

- Deliverable 1: Scrape titles and preview text from Mars news articles.
- Deliverable 2: Scrape and analyse Mars weather data, which exists in a table.

## Deliverable 1: Scrape titles and preview text from Mars news articles.
--------------------------------------------------------------------------------------------
The work is stored in Jupyter Notebook file part_1_mars_news.ipynb. Following are the steps below to scrape the Mars News website.
1. Use automated browsing to visit the Mars news siteLinks to an external site. Inspected the page to identify which elements to scrape.
1. Extracted the titles and preview text of the news articles from <th> and <tr> tags inside the <table> tag scraped. 
1. Stored the scraping results by looping through all the rows in the table in Python data structures as follows:
- Stored each title-and-preview pair in a Python dictionary with two keys: title and preview. 
- Stored all the dictionaries in a Python list.
1. Printed the list in part_1_mars_news.ipynb.
1. Stored the scraped list of dictionary in a file using JSON dumps.

## Deliverable 2: Scrape and Analyse Mars Weather Data
--------------------------------------------------------------------------------------------
All the coding was done in  Jupyter Notebook part_2_mars_weather.ipynb. Following are the steps below to scrape and analyse Mars weather data:
1. Use automated browsing to visit the Mars Temperature Data SiteLinks to an external - https://static.bc-edx.com/data/web/mars_facts/temperature.html. Inspected the page to identify which elements to scrape. 
1. Created a Beautiful Soup object and used it to scrape the data in the HTML table. 
1. Assembled the scraped data inside the table tag into a Pandas DataFrame. The column headings for the table are as follows:
 - id: the identification number of a single transmission from the Curiosity rover
 - terrestrial_date: the date on Earth
 - sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
 - ls: the solar longitude
 - month: the Martian month
 - min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
 - pressure: The atmospheric pressure at Curiosity's location

1. Converted the column values to the most relevant data type by cast (or convert) the data to the appropriate datetime, int, or float data types.
      
 - id : int32 data type         
 - terrestrial_date : datetime64[ns]
 - sol : int32 data type          
 - ls : int32  data type         
 - month : int32   data type        
 - min_temp : float64  data type       
 - pressure : float64  data type       
1. Answered the following questions based on the groupby in the dataframes and plotting the relevant graphs to get the answers:
 - How many months exist on Mars? Used unique() method to get the answer that 12 months are in Mars 
 - How many Martian (and not Earth) days worth of data exist in the scraped dataset? counted the number of rows of Sol column 
 - What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
 - Find the average minimum daily temperature for all of the months. Plotted the results as a bar chart.
 - Answer : Hotest Month : 8 , Coldest Month : 
 - Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
 - Found the average daily atmospheric pressure of all the months.
 - Plotted the results as a bar chart.
 - Answer : Highest pressure is there for the martian month : 9 Lowest pressure is there for the martian month : 6
 - About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
 - Considered how many days elapse on Earth in the time that Mars circles the Sun once.
 - Visually estimated the result by plotting the daily minimum temperature.
 - Answer :  As we can see two peaks roughly happened at roughly at 750 and 1425. Thus, making an year in Mars approximately 675 days.
 - Exported the DataFrame to a CSV file.
