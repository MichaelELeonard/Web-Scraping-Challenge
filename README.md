<img src="Pics/Header.png" width="796" height="383">

# Web Scraping with Beautiful Soup Challenge
Scrape Mars News Code
Scrape and Analyze Mars Weather Data Code 

For the Web Scraping with Beautiful Soup Challenge, our goal was to:
* Scrape Titles and Preview Text from Mars News
* Scrape and Analyze Mars Weather Data

## SCRAPE TITLES AND PREVIEW TEXT FROM MARS NEWS
For the first activity challenge we needed to go the website Mars Planet Science at https://static.bc-edx.com/data/web/mars_news/index.html and use automated browsing to inspect the site.  This was accomplished by right-clicking on the site and selecting Inspect using DevTools.  With the DevTools window open we were able to inspect the entire HTML code for the website as well as selecting specific items on the site and having DevtTools locate the specific corresponding HTML code.  The goal was to acquire all the article titles and article previews from the webpage.    
To start the Python coding we first imported our dependencies, established a browser connection to Google Chrome, set the browser instance to the Mars website and scraped all the HTML code by setting up a html.parser using Beautiful Soup.  Through our inspection it was determined that we would be looking for a div tag <div> and a class of ‘list_text’.  All the components matching that criteria were identified and stored in a variable called ‘all_text_elem’.  Finally, the stored elements were place in a list of dictionaries using a for-loop where the title of the article as placed in a variable called ‘title’ and the previews were stored in a variable called ‘teaser_preview’.  The titles were identified by finding the div tag <div> and the class ‘content_title’ and the preview information was located using the div tag <div> and the class ‘article_teaser_body’.  Each webpage component was saved in a dictionary ‘article_dict’ and appended to a list of dictionaries called ‘text_list’.  The list was printed to confirm the successful completion of the task and the browser element was closed using browser.quit.    

SCRAPE AND ANALYZE MARS WEATHER DATA
For the second activity in the challenge, we were tasked with scraping data from a table on a webpage, reading it into a Pandas DataFrame and conducting data analysis on the information to identify certain data metrics.  DevTools was utilized to examine the webpage https://static.bc-edx.com/data/web/mars_facts/temperature.html and identify the tags and classes that would be used to acquire the data from the data table.  In VS code, Python was used to gather HTML code by establishing the needed dependencies, establishing a browser connection, and scraping the data using a Beautiful Soup HTML parser. The HTML data was stored in the variable ‘soup’, and the tag <table> and class ‘table’ was used to gather the table data into a variable called “mars_data_table’.  The data was then entered into two lists using for-loops.  The column headings were identified by the tag <th> and read into the variable mars_data_column_headers.  The table row data was identified generally through the <th> tag and the class ‘data-row’, and then specifically through the tag <td>.  The data was stored in the variable ‘mars_row_data’.  Finally, both lists were uploaded into a Pandas DataFrame called mars_weather_df for analysis.                 
DATA ANAYLSIS
The elements in the DataFrame were cast into the specific required data types and the DataFame was checked to ensure the process was successful.  This step was conducted using the following code:
•	mars_weather_df['terrestrial_date'] = pd.to_datetime(mars_weather_df['terrestrial_date'])
•	mars_weather_df['sol'] = mars_weather_df['sol'].astype(int)
•	mars_weather_df['ls'] = mars_weather_df['ls'].astype(int)
•	mars_weather_df['month'] = mars_weather_df['month'].astype(int)
•	mars_weather_df['min_temp'] = mars_weather_df['min_temp'].astype(float)
•	mars_weather_df['pressure'] = mars_weather_df['pressure'].astype(float)

HOW MANY MONTHS EXIST ON MARS?
The number of months on Mars was established:  
•	mars_months = mars_weather_df.groupby('month')['id'].count()
with results showing:
1     174
2     178
3     192
4     194
5     149
6     147
7     142
8     141
9     134
10    112
11    138
12    166

SUMMARY
There are 12 months on Mars.


HOW MANY MARTIAN DAYS' WORTH OF DATA ARE THERE?
The number of Martian data of data was identified using: 
•	mars_months_count = mars_weather_df['sol'].count()

SUMMARY
The number of Marian days’ data was identified as 1,876.



WHICH MONTH, ON AVERAGE, HAS THE LOWEST TEMPERATURE? THE HIGHEST?

The average Martian low temperature by month was found by using: 
•	mars_low_temp_avg_by_months = mars_weather_df.groupby('month')['min_temp'].mean()
With the results of:
1    -77.160920
2    -79.932584
3    -83.307292
4    -82.747423
5    -79.308725
6    -75.299320
7    -72.281690
8    -68.382979
9    -69.171642
10   -71.982143
11   -71.985507
12   -74.451807 	

SUMMARY
Upon examination the third month of the Martin year is the coldest, with the eighth month being the warmest. This chart of the average low temperatures on Mars also outlines the very challenging conditions presented by the Martain environment.    


WHICH MONTH, ON AVERAGE, HAS THE LOWEST ATMOSPHERIC PRESSURE? THE HIGHEST?	

Unsorted and sorted bar graphs were created using matplotlib.pyplot and utilizing the following code:
•	mars_low_temp_avg_by_months.plot.bar()  
•	mars_low_temp_ordered = mars_low_temp_avg_by_months.sort_values()
o	mars_low_temp_ordered.plot.bar()

Both created bar graphs were saved in the submitted Output folder.

The average pressure by Martian month was identified and plotted using:
•	mars_avg_pressure_by_months_ordered = mars_avg_pressure_by_months.sort_values()
•	mars_avg_pressure_by_months_ordered.plot.bar()
With the resulting bar graph saved in the submitted Output folder.
SUMMARY
On average, the nineth month of the Martian year had the highest level of Atmosphere Pressure with the sixth month having the lowest levels.  These atmosphere pressure levels are very low in comparison of the levels that we experience on Earth , resulting in Martan air being extremely thin and unbreathable .

HOW MANY TERRESTRIAL DAYS EXIST IN A MARTIAN YEAR? A VISUAL ESTIMATE WITHIN 25% WAS MADE.
The number of terrestrial (earth) days that are in a Martian year was identified and plotted using:
•	plt.plot(mars_weather_df.terrestrial_date,mars_weather_df.min_temp)
With the resulting graph saved in the submitted Output folder.

SUMMARY
In my graph there is a peak around day 740 and the next peak takes place at approximately day 1425. Therefore, on Martian year is about 685 terrestrial days in the graph.  This data was backed to by an internet search showing a full Martial cycle around the sun taking 687 Earth days. 
















CITATIONS: 

