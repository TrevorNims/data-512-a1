# data-512-a1
This exploration will construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2021. Initilly we will use two different Wikimedia REST API endpoints to acess the data:

   - Legacy Pagecounts API 
      * documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts
      * endpoint: https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end
   - Pageviews API
      * documentation: https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews
      * endpoint: https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end
 
The terms of use for this API can be found here:
 
   https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions
    
There will exist six files in the 'data' folder: 
 
   - Five .json files containing the raw monthly view data from the API calls
   - A single .csv file, containing the cleaned and aggregated .json files with the following column headers
      * year (str)
      * month (str)
      * pagecount_all_views (int)
      * pagecount_desktop_views (int)
      * pagecount_mobile_views (int)
      * pageview_all_views (int)
      * pageview_desktop_views (int)
      * pageview_mobile_views (int)

In the 'visualizations' folder, there will be a single plot showing the traffic over time via mobile and desktop access sites, as well as their sum. It is important to note that all data collected from the Pageviews API omits web crawlers, whereas the data from the Legacy Pagecounts API does not (as it did not possess this filtration feature).

