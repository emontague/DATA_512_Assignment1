Created by: Libby Montague
Date: 10/16/2017

Goal: Graph data from the wikipedia API on page views from 8/2008-10/2017. 

Source Data Information:
- From the Wikimedia Foundation
- Accessed on 10/16/2017
- Endpoints and documentation: 
    - Page views: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews, https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end
    - Page counts: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts, https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end
- The data was accessed under the CC0 1.0 license (https://creativecommons.org/publicdomain/zero/1.0/).
- The responses of the API are stored in the following files:
    - pageviews_mobile-app_201507-201709.json
    - pagecounts_desktop-site_200801-201608.json  
    - pageviews_mobile-web_201507-201709.json
    - pagecounts_mobile-site_200801-201608.json   
    - pageviews_desktop_201507-201709.json
- The page views are available 7/2015-Present. The page counts are available for 1/2008-8/2016. The page counts data includes 'spiders' but the page views allows for filtering out the 'spiders.' I filtered out the 'spiders' in the page views. 

Files:
LICENSE 
    - The MIT License for the code (hcds-a1-data-curation.ipynb). 
hcds-a1-data-curation.ipynb
    - Fully documentated jupyter python notebook that uses the Wikimedia API to get the page counts and page views. 
    - The script then stores the responses in .json files. 
    - The data are then processed and graphed. The processed data is stored in .csv file and the graph is written to a .png. 
en-wikipedia_traffic_200801-201709.csv
    - The processed page views data that originated from the Wikimedia API. 
    - Columns: year (YYYY), month (MM), pagecount_all_views (all views from page counts, includes 'spiders'), pagecount_desktop_views (all the views of the desktop, includes 'spiders'), pagecount_mobile_views (all of the mobile site views, includes 'spiders'), pageview_all_views (all of the views, does not include 'spiders'), pageview_desktop_views (all of the desktop views, does not include 'spiders'), pageview_mobile_views (all of the mobile web and app views, does not include 'spiders')
    - Note that there are some fields with 0 views, that is expected from the scope of the data collected by Wikimedia. 
wikipedia_pageviews_en_2008_2017.png
    - This graph displays the page views and counts over time. The data are from the .csv file, from the .json, and originally from the Wikimedia API. 
pageviews_mobile-app_201507-201709.json
    - Response from the Wikimedia API. The page views for the mobile app without 'spiders' from 7/2015 - 9/2017. 
    - Data elements: timestamp (YYYYMMDDHH), granularity (aggregate levels), views (number of views), access (type of site access), project (wikipedia project), agent (the type of user that accesses) 
pagecounts_desktop-site_200801-201608.json  
    - Response from the Wikimedia API. 
    - Data elements: count (number of views, includes spider users), timestamp (YYYYMMDDHH), project (wikipedia project), granularity (aggregate levels), access-site (type of site access) 
pageviews_mobile-web_201507-201709.json
    - Response from the Wikimedia API. The page views for mobile web without 'spiders' from 7/2015 - 9/2017. 
    - Data elements: timestamp (YYYYMMDDHH), granularity (aggregate levels), views (number of views), access (type of site access), project (wikipedia project), agent (the type of user that accesses) 
pagecounts_mobile-site_200801-201608.json  
    - Response from the Wikimedia API. 
    - Data elements: count (number of views, includes spider users), timestamp (YYYYMMDDHH), project (wikipedia project), granularity (aggregate levels), access-site (type of site access) 
pageviews_desktop_201507-201709.json
    - Response from the Wikimedia API. The page views for desktop site without 'spiders' from 7/2015 - 9/2017. 
    - Data elements: timestamp (YYYYMMDDHH), granularity (aggregate levels), views (number of views), access (type of site access), project (wikipedia project), agent (the type of user that accesses) 
