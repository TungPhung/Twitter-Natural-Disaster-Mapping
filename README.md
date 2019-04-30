# Twitter Mapping of Natural Disasters
## A Project by: Tung Phung, Josh Robin, Roohullah Mansoor

## Goals:
During natural disasters, emergency response service efforts are often severely hampered by information on where to allocate their resources. This can be due in part to congestion of phone lines, or simply the inavailability of phone lines being downed due to the natural disaster themselves. By accessing social media, we have another avenue to understand the pathing of natural disasters and which areas, are affected. If successful, a method like this can alert first responders further understand the best allocation of their resources.

## Methods:
Using python, we utilized twitterscaper (https://github.com/taspinar/twitterscraper) for our project. This allowed us to scrape large amounts of data fairly quickly and not be rate-limited by Twitter's normal API. We did encounter some slight bugs with the software, but for the most part, it provided the necessary functionality. Along with twitterscraper, we utilized Pandas, Bokeh, and the Google Maps API to generate the map.

## Executive Summary:


## Conclusions and Recommendations:
While our results make intuitive sense, we were not able with the time constrictions able to correlate the actual twitter data with actual on-the-ground response to correlate it to real life. Since our model was unsupervised, it was appropriate, but grounding it in real-ground response with buy-in from emergency workers and stakeholders would allow us to improve our model and see where it actually missed responses where it should have been. 

![Screenshot](/images/"Screen Shot 2019-04-26 at 7.39.42 AM".png)

