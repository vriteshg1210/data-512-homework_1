This is the Readme file for homework 1 done by Vritesh Gera for the class DATA 512.

## Project Goal 
The main aim is to measure the article traffic of various Wikipedia articles from 2015 to 2023. For doing this we will be using Wikimedia’s REST API. The data coming back after calling the API would include the number of views, the name of the article, the mode through which it was accessed (mobile or desktop) along with a lot of other details. We want to store this data in JSON files and later run some Data Visualization analysis on the data retrieved.

## Data Source
You can view and use the dataset that we have used for this activity here- https://docs.google.com/spreadsheets/d/1A1h_7KAo7KXaVxdScJmIVPTvjb3IuY9oZhNV4ZHxrxw/edit#gid=1229854301.
This project relies on the Wikimedia Foundation REST API to access pageview data for Wikipedia articles. The data spans from July 2015 through the previous complete month.

## API Documentation
In order to measure article traffic from 2015-2023, you will need to collect data from the Pageviews API. The Pageviews API (documentation, endpoint) provides access to the desktop, mobile web, and mobile app traffic data from July 2015 through the previous complete month.
Please find below the terms of use of the Wikimedia Foundation REST API:
 https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions
 
## Environment
In this project, we will use a Google Colab environment to run a Python notebook. We will also be using Google Drive to store the dataset which contains the list of all the Wikipedia articles.

## Data-preprocessing and Analysis

**Data Gathering, Data Transformation, and Dataset Generation are key phases within this project:**

**Data Retrieval:** The project sources pageview statistics for specific Wikipedia articles through the Pageviews API.

**Data Transformation:** After retrieval, the data undergoes processing, where it is organized into time series representations, depicting monthly pageview activities.

**Dataset Creation:** The project generates three distinct datasets:

1. **Monthly Mobile Access:** This dataset combines pageviews from both mobile apps and mobile web.

2. **Monthly Desktop Access:** This dataset focuses on pageviews originating from desktop devices.

3. **Monthly Cumulative:** This dataset aggregates the total pageview traffic for each article, encompassing both desktop and mobile sources using "all-access" access types.

## Documentaion
The project follows the recommended procedures for replication and documentation:

1)Jupyter Notebook(s): Detailed explanations of the steps involved in data collection, processing, and analysis.

2)README File (this file): Gives a general description of the project, outlining its objectives, data sources, data processing procedures, and reproducibility standards.

3)LICENSE File: This file contains the code's MIT LICENSE, which guarantees that it can be used freely.

##License
This project is open-source and follows the MIT License. You are free to use and modify the code following the terms of the MIT License.

## Steps you can Follow to reproduce this work:
1)	Import the needed Python libraries into your notebook.
2)	To successfully hit any API for gathering data, define functions(methods) to take the required parameters and fetch data from the mentioned data source. Hence, define these parameters and functions to successfully do this part of the procedure. Keep in mind that we should make this function reusable so that it can be used for fetching different kinds of data using the API.
3)	Store the fetched data in the form of a list of dictionaries in Python. As the mobile data is split into website and      app, aggregate both types of access to create 1 list.
4)	There will be 3 lists that show views on mobile, desktop, and cumulative(mobile+desktop).
5)	Write these lists of dictionaries into 3 separate JSON files-   
    academy_monthly_desktop_<start201501>-<end202309>.json, academy_monthly_mobile_<start201501>-<end202309>.json, 
    academy_monthly_cummulative_<start201501>-<end202309>.json
6) Create Dataframes from the list of dictionaries created during the previous activity.
7)	Use these DataFrames to plot 3 visualizations:
    Maximum Average and Minimum Average - time series for the articles that have the highest average monthly page requests   
    and the lowest average monthly page requests for desktop access and mobile access. 
    Top 10 Peak Page Views - time series for the top 10 article pages by largest (peak) page views over the entire time by 
    access type. We first find the month for each article that contains the highest (peak) page views, and then order the 
    articles by these peak values. The graph contains the top 10 for desktop and the top 10 for mobile access (20 lines).
    Fewest Months of Data - The third graph shows pages that have the fewest months of available data. These are relatively 
   short time series and contain a set of the most recent Academy Award winners. The graph shows the 10 articles with the 
   fewest months of data for desktop access and the 10 articles with the fewest months of data for mobile access.

## Output Files
The project generates three JSON files:
academy_monthly_mobile_201507-202312.json: Monthly mobile access data.
academy_monthly_desktop_201507-202312.json: Monthly desktop access data.
academy_monthly_cumulative_201507-202312.json: Monthly cumulative data.
Please refer to each file for detailed data on Wikipedia pageviews.

Note: For additional details and code implementation, please refer to the provided Jupyter Notebook(s).



