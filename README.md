# mod11-challenge

##Background
You’re now ready to take on a full web-scraping and data analysis project. You’ve learned to identify HTML elements on a page, identify their id and class attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organizing and storing data, analyzing data, and then visually communicating your insights.

##What You're Creating
I created two technical products for this new assignment. I had to submit the following deliverables:
- Deliverable 1: I scraped titles and preview text from Mars news articles.
- Deliverable 2: I scraped and analyzed Mars weather data, which existed in a table.

##Instructions
###Part 1: Scrape Titles and Preview Text from Mars News
I started with Part 1, where I had to scrape Titles and Preview Text from Mars News. I opened the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. I worked in this code as I followed the steps below to scrape the Mars News website:
1. I used automated browsing to visit the Mars news site and inspected the page to identify which elements to scrape.
2. I created a Beautiful Soup object and used it to extract text elements from the website.
3. I extracted the titles and preview text of the news articles that I scraped and stored the scraping results in Python data structures as follows:
   - I stored each title-and-preview pair in a Python dictionary and gave each dictionary two keys: title and preview. An example is the following:
     - {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
       'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}
    - I stored all the dictionaries in a Python list and printed the list in my notebook.

###Part 2: Scrape and Analyze Mars Weather Data
I opened the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. I worked in this code as I followed the steps below to scrape and analyze Mars weather data.
1. I used automated browsing to visit the Mars Temperature Data Site and inspected the page to identify which elements to scrape. The URL I used for this was https://static.bc-edx.com/data/web/mars_facts/temperature.html.
2. I created a Beautiful Soup object and used it to scrape the data in the HTML table. It's worth noting that I could have achieved this using the Pandas read_html function, but I chose to use Beautiful Soup to further sharpen my web scraping skills.
3. After scraping the data, I assembled it into a Pandas DataFrame. The columns in the DataFrame had the same headings as the table on the website, which were as follows:
  - id: The identification number of a single transmission from the Curiosity rover.
  - terrestrial_date: The date on Earth.
  - sol: The number of elapsed sols (Martian days) since Curiosity landed on Mars.
  - ls: The solar longitude.
  - month: The Martian month.
  - min_temp: The minimum temperature, in Celsius, of a single Martian day (sol).
  - pressure: The atmospheric pressure at Curiosity's location.
4. I examined the data types that were associated with each column. When necessary, I cast (or converted) the data to the appropriate datetime, int, or float data types.
**I used the Pandas astype and to_datetime methods to accomplish this task.
5. I analyzed my dataset using Pandas functions to answer the following questions:
- How many months exist on Mars?
- How many Martian (and not Earth) days worth of data exist in the scraped dataset?
- What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
  - Find the average minimum daily temperature for all of the months.
  - Plot the results as a bar chart.
- Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
  - Find the average daily atmospheric pressure of all the months.
  - Plot the results as a bar chart.
- About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
  - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
  - Visually estimate the result by plotting the daily minimum temperature.
6. Then, I exported the DataFrame to a CSV file.
