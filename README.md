# Twitter Mapping of Natural Disasters
A Project by: Tung Phung, Josh Robin, Roohullah Mansoor

## Goals:
During natural disasters, emergency response service efforts are often severely hampered by available resources. Allocation of resources in a more efficient way can result in more lives and property saved. During a disaster, communication systems are often the first systems affected. This can be due in part to congestion of phone lines by emergency calls, or the inavailability of phone lines being downed due to the natural disaster themselves. By accessing social media, we have another avenue to understand the pathing of natural disasters and which areas, are affected, given cell phone data towers stay active longer than phone lines. This project seeks to use Twitter, a large social media platform to see if its users behaviors can aptly inform emergency responders of trouble areas during a true emergency situation to properly assess areas of most need.


## Methods:
Using python, we utilized twitterscaper (https://github.com/taspinar/twitterscraper), a twitter scraper developed by github user taspinar for our project. This allowed us to scrape large amounts of data fairly quickly and not be rate-limited by Twitter's normal API. We did encounter some slight bugs with the software, but for the most part, it provided the necessary functionality. A scaled solution would require another type of scraping/API servie. Along with twitterscraper, we utilized Pandas, Bokeh, and the Google Maps API to generate the disaster map.


## Executive Summary:



## Conclusions and Recommendations:
While our results make intuitive sense, we were not able with the time constrictions able to correlate the actual twitter data with actual on-the-ground response to correlate it to real life. Since our model was unsupervised, it was appropriate, but grounding it in real-ground response with buy-in from emergency workers and stakeholders would allow us to improve our model and see where it actually missed responses where it should have been. 


### Example 1:
[Screenshot](https://github.com/TungPhung/Twitter-Natural-Disaster-Mapping/blob/master/images/Screen%20Shot%202019-04-26%20at%207.39.42%20AM.png)






