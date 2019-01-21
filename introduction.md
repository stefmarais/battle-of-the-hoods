## Problem Statement
### Background
I am currently considering where to move in Beijing, China. Not knowing much about the city and its various residential districts make it difficult and overwhelming to make a decision on where to live. Therefore I decided to employ my newfound data science skills to assist in the decision making.

The decision on where to live will be made based on variety and type of venues in the district. As an expat, a slight bias will be given to districts that can be perceived as being more foreigner friendly and provide some sort of familiarity. 

Two sources of data will be used: **Popular residential districts** provided by a rental agent with their respective geographic centroids; **Foursquare venue data** as retrieved through the Foursquare API.

Based on a list of 20 residential districts provided by a rental agent, their corresponding geographical centroids were collected and stored locally. These were read into a Pandas Dataframe for use in retrieving venue data from Foursquare.

The Foursquare API was used to retrieve the first 100 venues within a 1000m radius of each district centroid. The Foursquare API returns the venues within the stated limits and provides a corresponding venue category. By transforming the retrieved data such that the districts are listed along with category frequency, it is possible to perform k-means clustering. This will simplify the task of choosing a district to live in by only considering clusters that are similar to the criteria discussed previously and disregarding districts in clusters that are not of interest.

