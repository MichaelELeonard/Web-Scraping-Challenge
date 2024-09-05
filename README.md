<img src="Pics/Header.png" width="796" height="383">

# Web Scraping with Beautiful Soup Challenge
Scrape Mars News Code - https://github.com/MichaelELeonard/Web-Scraping-Challenge/blob/main/part_1_mars_news_working.ipynb

Scrape and Analyze Mars Weather Data Code - https://github.com/MichaelELeonard/Web-Scraping-Challenge/blob/main/part_2_mars_weather_working.ipynb

## Goals
* Scrape Titles and Preview Text from Mars News
* Scrape and Analyze Mars Weather Data

## SCRAPE TITLES AND PREVIEW TEXT FROM MARS NEWS

* Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup).
* The titles and preview text of the news articles were scraped and extracted.
* The scraped information was stored in the specified Python data structure—specifically, a list of dictionaries.
<img src="Pics/Results list A.png" width="1565" height="574">




## SCRAPE AND ANALYZE MARS WEATHER DATA
* The HTML table was extracted into a Pandas DataFrame. Either Pandas or Splinter and Beautiful Soup were used to scrape the data. The columns have the correct headings and data types. (15 points)
* The data was analyzed to answer the following questions: (10 points)
  * How many months exist on Mars? (5 points)
  * How many Martian days' worth of data are there? (5 points)

 
* The data was analyzed to answer the following questions, and a data visualization was created to support each answer: (30 points)
  * Which month, on average, has the lowest temperature? The highest? (10 points)
  * Which month, on average, has the lowest atmospheric pressure? The highest? (10 points)
  * How many terrestrial days exist in a Martian year? A visual estimate within 25% was made. (10 points)
* The DataFrame was exported into a CSV file. (5 points)

