
## Challenge 11 Mars News

# Mars_News_Scraping
![HQ graphic](https://github.com/Lanceowesalot/Pewlett_Hackard_Challenge/blob/main/Images/Pewlette%20Hackard%20HQ%20image.png)
Web-scrape and data analyse using both automated browsing with Splinter and HTML parsing with Beautiful Soup.

- [Getting Started](#getting-started)
- [Prerequisites](#Prerequisites)
- [Coding Instruction](#Coding-Instruction)
- [References](#references)

## Getting Started

This assignment consists of two technical products. You will submit the following deliverables:

- Deliverable 1: Scrape titles and preview text from Mars news articles.
       
- Deliverable 2: Scrape and analyze Mars weather data, which exists in a table.

### Prerequisites
Before you begin, ensure you have the following installed:

- [Jupyter Notebook](https://jupyter.org/)
- [Splinter](https://pypi.org/project/splinter/)
- [BeautifulSoup](https://pypi.org/project/BeautifulSoup/)
- [matplotlib](https://pypi.org/project/matplotlib/)
- [pandas](https://pypi.org/project/pandas/)


## Coding Instruction

#### The instructions for this module are divided into the following parts:

* Part 1: Scrape Titles and Preview Text from Mars News
  
* Part 2: Scrape and Analyze Mars Weather Data
  
#### Part 1: Scrape Titles and Preview Text from Mars News

Open the Jupyter Notebook in the starter code folder named part_1_mars_news.ipynb. You will work in this code as you follow the steps below to scrape the Mars News website.

1. Use automated browsing to visit the [Mars news](https://static.bc-edx.com/data/web/mars_news/index.html) . Inspect the page to identify which elements to scrape.
    
   - Hint: To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools.
    
2. Create a Beautiful Soup object and use it to extract text elements from the website.
    
3. Extract the titles and preview text of the news articles that you scraped. Store the scraping results in Python data structures as follows:
    
   1. Store each title-and-preview pair in a Python dictionary and, give each dictionary two keys: title and preview.
   2. Store all the dictionaries in a Python list.
   3. Print the list in your notebook.
    
4. Optionally, store the scraped data in a file (to ease sharing the data with others). To do so, export the scraped data to a JSON file. (Note: there will be no extra points for completing this.)

#### Part 2: Scrape and Analyze Mars Weather Data

Open the Jupyter Notebook in the starter code folder named part_2_mars_weather.ipynb. You will work in this code as you follow the steps below to scrape and analyze Mars weather data.

1. Use automated browsing to visit the [Mars Temperature Data](https://static.bc-edx.com/data/web/mars_facts/temperature.html). Inspect the page to identify which elements to scrape. Note that the URL is https://static.bc-edx.com/data/web/mars_facts/temperature.html.
    
   - Hint: To identify which elements to scrape, you might want to inspect the page by using Chrome DevTools to discover whether the table contains usable classes.
    
2. Create a Beautiful Soup object and use it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas read_html function. However, use Beautiful Soup here to continue sharpening your web scraping skills.
    
3. Assemble the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here’s an explanation of the column headings:
    
   - id: the identification number of a single transmission from the Curiosity rover
       
   - terrestrial_date: the date on Earth
       
   - sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
       
   - ls: the solar longitude
       
   - month: the Martian month
       
   - min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
       
   - pressure: The atmospheric pressure at Curiosity's location
    
5. Examine the data types that are currently associated with each column. If necessary, cast (or convert) the data to the appropriate datetime, int, or float data types.
    
   - Hint: You can use the Pandas astype and to_datetime methods to accomplish this task.
    
6. Analyze your dataset by using Pandas functions to answer the following questions:
    
   - How many months exist on Mars?

      * There are 12 months on Mars.
           
   - How many Martian (and not Earth) days worth of data exist in the scraped dataset?

      * Approximately 675 Martian days' worth of data exist in the dataset.

           
   - What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
     
       - Find the average minimum daily temperature for all of the months.

         * On average, the third month has the coldest minimum temperature on Mars, while the eighth month is the warmest.

        

       - Plot the results as a bar chart.

       ![entity_relationship_diagram](https://github.com/Lanceowesalot/Pewlett_Hackard_Challenge/blob/main/ERD_Final.png).
                
    - Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
           
       - Find the average daily atmospheric pressure of all the months.
         * On average, atmospheric pressure is lowest in the sixth month and highest in the ninth.
       - Plot the results as a bar chart.
      
      ![entity_relationship_diagram](https://github.com/Lanceowesalot/Pewlett_Hackard_Challenge/blob/main/ERD_Final.png).

    - About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
           
       - Consider how many days elapse on Earth in the time that Mars circles the Sun once.

         * The plot indicates that a year on Mars is roughly 675 Earth days long, confirmed by an internet search which states that a Mars year is equivalent to 687 Earth days.

![entity_relationship_diagram](https://github.com/Lanceowesalot/Pewlett_Hackard_Challenge/blob/main/ERD_Final.png).

Overall, the analysis provides insights into the temperature and atmospheric pressure variations across different months on Mars, as well as the length of a Martian year compared to Earth years. 