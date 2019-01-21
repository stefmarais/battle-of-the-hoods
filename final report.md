## Problem Statement
### Background
#### Introduction
I am currently considering where to move in Beijing, China. Not knowing much about the city and its various residential districts make it difficult and overwhelming to make a decision on where to live. Therefore I decided to employ my newfound data science skills to assist in the decision making.

The decision on where to live will be made based on variety and type of venues in the district. As an expat, a slight bias will be given to districts that can be perceived as being more foreigner friendly and provide some sort of familiarity.

Instead of assessing each district on an individual basis, it should be possible to group districts in terms of similarity and then assess the group based on the grouping criteria. By assessing grouped districts, the decision making process will be simplified since it will not be necessary to consider all districts but only those in a selected grouping.

Although the problem stated is specific to my personal and immediate needs, it is a general problem and can be applied to any person looking to relocate within any city.

### Data
Two sources of data will be used: Popular residential districts provided by a rental agent with their respective geographic centroids; Foursquare venue data as retrieved through the Foursquare API.

Based on a list of 20 residential districts provided by a rental agent, their corresponding geographical centroids were collected and stored locally. These were read into a Pandas Dataframe for use in retrieving venue data from Foursquare.

The Foursquare API was used to retrieve the first 100 venues within a 1000m radius of each district centroid. The Foursquare API returns the venues within the stated limits and provides a corresponding venue category. The APIwas accessed to retrieve the following values for 100 venues in a given district: District;	District Latitude;	District Longitude; Venue;	Venue Latitude;	Venue Longitude;	Venue Category.

Since we are only interested in the venue category and not its name or geographical location information, the resultset can be transformed such that the districts are listed along with only the venue category. By performing further transofrmations on the data we can calculated the normalized frequency of the categories and sort the frequencies in descending order to obtain the most common venue types. Based on this transofrmation of the data, it is possible to perform k-means clustering. This will simplify the task of choosing a district to live in by only considering clusters that are similar to the criteria discussed previously and disregarding districts in clusters that are not of interest.

### Methodology


### Results

### Discussion
