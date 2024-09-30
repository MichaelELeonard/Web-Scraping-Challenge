<img src="Pics/Header.png" width="796" height="383">

# Web Scraping with Beautiful Soup Challenge

[Scrape Mars News Code Link]( https://github.com/MichaelELeonard/Web-Scraping-Challenge/blob/main/part_1_mars_news_working.ipynb)

[Scrape and Analyze Mars Weather Data Code Link]( https://github.com/MichaelELeonard/Web-Scraping-Challenge/blob/main/part_2_mars_weather_working.ipynb)


## Goals
* Scrape Titles and Preview Text from Mars News
* Scrape and Analyze Mars Weather Data

## SCRAPE TITLES AND PREVIEW TEXT FROM MARS NEWS

* Automated browsing (with Splinter) was used to visit the Mars news site, and the HTML code was extracted (with Beautiful Soup).
* The titles and preview text of the news articles were scraped and extracted.
* The scraped information was stored in the specified Python data structure—specifically, a list of dictionaries.
<img src="Pics/Results list A.png" width="1395" height="505">




## SCRAPE AND ANALYZE THE MARTIAN WEATHER DATA
The HTML table was extracted into a Pandas DataFrame and Splinter and Beautiful Soup were used to scrape the data. The data was analyzed to answer the following questions:

  * How many months exist on Mars? 

<img src="Pics/Months.png" width="192" height="270">


  * How many Martian days' worth of data is in the dataset? 

<img src="Pics/Days of data.png" width="61" height="39">

 
  * Display the average Martian low temperature by month

<img src="Pics/Avg Low Temp by Month.png" width="249" height="277">


  * Plot the average Martian low temperature by month 

<img src="Pics/Avg Low Bar.png" width="477" height="366">


  * Plot the average Martian low temperature by month in ascending order

<img src="Pics/Avg Low Temp Bar Ordered.png" width="475" height="367">



* Display the average Martian atmospheric pressure by month

<img src="Pics/Average Pressure by Month.png" width="256" height="269">


* Identify which months with the lowest and highest atmospheric pressure 

<img src="Pics/Average Pressure by Month Bar Ordered.png" width="474" height="361">


 * Plot how many terrestrial (earth) days exist in a Martian year

<img src="Pics/Terrestrial Earth days in a Martian year.png" width="476" height="359">

