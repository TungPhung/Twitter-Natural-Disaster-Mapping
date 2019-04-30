# Twitter Mapping of Natural Disasters
A Project by: Tung Phung, Josh Robin, Roohullah Mansoor

![Twitter](https://www.saydaily.com/.image/t_share/MTM0ODg3OTkwOTMyNTc1NTA2/screen-shot-2015-12-03-at-22820-pmpng.png)

## Goals:
During natural disasters, emergency response service efforts are often severely hampered by available resources. Allocation of resources in a more efficient way can result in more lives and property saved. In a disaster event, communication systems are often the first systems affected. This can be due in part to congestion of phone lines by emergency calls, or the inavailability of phone lines being downed due to the natural disaster themselves. By accessing social media, we have another avenue to understand the pathing of natural disasters and which areas are affected given cell phone data towers stay active longer than phone lines. This project seeks to use Twitter, a large social media platform to see if its users behaviors can aptly inform emergency responders of trouble areas during a true emergency situation to properly assess areas of most need.

## Methods:
Using python, we utilized twitterscaper (https://github.com/taspinar/twitterscraper), a twitter scraper developed by github user taspinar for our project. This allowed us to scrape large amounts of data fairly quickly and not be rate-limited by Twitter's normal API. We did encounter some slight bugs with the software, but for the most part, it provided the necessary functionality. A scaled solution would require another type of scraping/API servie. Along with twitterscraper, we utilized Pandas, Natural Language Processing (NLP) techniques, Bokeh, and the Google Maps API to generate the disaster map.

## Executive Summary:
Initially, our approached stemmed around the assumption Twitter stores geo-location data on its users tweets. However, Twitter requires users to opt into this geo-location system. This leads to the vast majority of tweets having no geo-location tag. However, users still may have home location data that they specify in their profile, which is more apt associated with their hometown or their home location, but not the location where they are currently "tweeting" from. This gave us a path to possibly follow. Most other mainstream social media systems such as Facebook, Instagram are not easily scrappable or have API's that are conducive to the data required in this project.

In finding TwitterScraper by taspinar, which is a rudimentary web-scraping system, we were able to input a search query with our own defined GPS coordinates and a specified radius. This was a main part of our approach. Knowing this, we could take any GPS coordinate as a centroid and create a rudimentary grid search around this point in a patterned manner. By using this approach, we could take the GPS coordinates and define a basic radius (we used 7.5km) to search around.

However, in order to understand and label high areas of higher tweet distress, we needed an NLP algorithm to identify and label so we could have a quantized value. From our experiments, we found a Density-Based clustering algorithm and a Counter-Vectorizer with stop-words and 1,2 ngrams along with our own non-NLP determined "danger" words set was adequate to highlight the areas where tweets were more focused on danger and requiring assistance. Due to time-constraints, we were able to only account and train off hurricanes, with further time, we would increase the available range of disasters the model could account for. 

As such, the workflow for an emergency response person would be such. They would input a word such as "hurricane" into our engine, which would scrape for the most current tweets in a user-defined time-frame (probably within the last couple days). They would also input a series of GPS coordinates related to the area of interest. The system creates a grid system around this centroid GPS point and would then scrape twitter for the time-frame and assess each of the points of intersection on the grid for danger. It would then output a map which labels this danger in a user interpretable manner (See examples 1-3)

## Conclusions and Recommendations:
While our results make intuitive sense, we were not able with the time constrictions able to correlate the actual twitter data with actual on-the-ground response to correlate it to real life. Since our model was unsupervised, it was appropriate, but grounding it in real-ground response with buy-in from emergency workers and stakeholders would allow us to improve our model and see where there were positive or negative respones. This would be a huge stepping stone in the model's legitimacy. We would also seek to not only improve it for a wider range of disasters, but also generate Word2Vec models to allow for users to put in a basic word such as "hurricane" and the system would generate a series of related words that it would also search for to increase coverage of teh search terms. We would also use Word2Vec to generate the danger words based on the danger-positive tweets. Hopefully, we would be able to train the system beyond needing to use our own creator-generated values.

### Example 1:
![Screenshot](https://github.com/TungPhung/Twitter-Natural-Disaster-Mapping/blob/master/images/Screen%20Shot%202019-04-26%20at%207.39.42%20AM.png)

### Example 2:
![Screenshot](https://github.com/TungPhung/Twitter-Natural-Disaster-Mapping/blob/master/images/Screen%20Shot%202019-04-26%20at%207.39.57%20AM.png)

### Example 3:
![Screenshot](https://github.com/TungPhung/Twitter-Natural-Disaster-Mapping/blob/master/images/Screen%20Shot%202019-04-26%20at%207.40.29%20AM.png)





