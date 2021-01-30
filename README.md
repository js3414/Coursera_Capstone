# Coursera_Capstone
Coursera capstone project of Applied Data Science Capstone 

by Jongseob Shin

## 1. Introduction to Capstone Project
This is a capstone project of Coursera "Applied Data Science Capstone". "Applied Data Science Capstone" is a part of IBM Data Science Professional Certificate.

# Coursera Capstone Project

This is a Coursera capstone project of the IBM Data Science Professional Certificate course.

#### Capstone Project Scenario
You live on the west side of the city of Toronto in Canada. Your neighbourhood is all the great amenities and other types of venues that exist in the neighbourhood. You receive a job offer from a great company on the other side of the city with great career prospects. However, the company is a far distance from our current place. You, unfortunately, must move if you decide to accept the offer. You are looking for a place to move to.
The new place must be:
- exactly the same as your current neighbourhood, or
- similar neighbourhoods that are at least closer to your new job.

#### Project Goal: City Segmentation and Clustering
- Segment city into different neighbourhoods using the geographical coordinates of the center of each neighbourhood
- Using a combination of location data and machine learning, roup the neighbourhoods into clusters

## 2. Gathering Neighborhood Information of the city of Toronto, Canada
### 2.1 Postal Code and Neighborhood Information
Gather the postal code and neighbourhood information of the city of Toronto from Wikipedia.
https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M, 

Obtain the postal code table on the above page and transform the data into a pandas dataframe.
- Use BeautifulSoup4 to parse HTML
- The dataframe will consist of three columns: PostalCode, Borough, and Neighborhood
- Drop the rows with a borough that is "Not assigned."
- More than one neighbourhood can exist in one postal code area.
- If a cell has a borough but a "Not assigned" neighbourhood, then the neighbourhood will be the same as the borough.
(See Neighborhood_Toronto.ipynb)

### 2.2 Coordinates of the Neighbourhood
- Find the coordinate using the Geospatial_Coordinates.csv file
- Read Geospatial_Coordinates.csv file
- Merge two dataframes using postal code
(See Neighborhood_Coordinates_Toronto.ipynb)

### 2.3 Segmenting and Clustering of York borough
- Split neighborhood to separate rows
- Create map of Toronto and marking boroughs
- Creat map of York borough and makring neighborhoods
- Get the venue information from Foursquare
- Cluster neighborhood into 5 clusters using k-mean
(See Segment_Cluster_York_Toronto.ipynb)
