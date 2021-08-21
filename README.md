# diffOSM
This project focuses on using open street map data to locate points of interest using a tag at any location. For example in this code I use open street map to find data of chicago and I use the tag = "school" to find all K-12 schools in the chicagoland area. I then use this data to create a grid/map of chicago highlighting the areas with the least/most schools. In this project I also compare data given from other shp files to the open street map data and compare the differences between the datasets.


<h1> Required Libraries</h1>

```
pip -r requirements.txt
```
<h1> Data Files </h1>

[The Chicago Landuse data](https://datahub.cmap.illinois.gov/dataset/land-use-inventory-for-northeast-illinois-2015) used in `cmap_vs_osm.ipynb`as a `.shp` file

<h1> Locating POI's </h1>

The `locating_pois.ipynb` file is used to locate points of interest within a given city/town using open street map data
In this file the `city` variable holds a string that selects what place/city is searched using `osmnx` data.
```
city = "Chicago"
```
The city variable currently holds the string `"Chicago"` but it can be changed to search any city.

Once the `city` variable is set the next step is to change the `tags` variable to the desired point of interest that is going to be searched from the `city`
```
tags = {'amenity': "school"}
```
The tags variable currrently is used to find all schools within the given `city`. Some other options for what tags can be used are found [here](https://wiki.openstreetmap.org/wiki/Map_features)
Once the `city` variable and the `tags` variable is given the program then generates a grid of the `city` showing all the points of interest within that area.

<h3> Examples </h3>

Using `osmnx` to collect data and create a grid on where K-12 schools are located inside of Chicago
```
city = "Chicago"
tags = {'amenity': "school"}
```
![image](https://user-images.githubusercontent.com/73620346/130305383-62917667-589d-4004-9508-766f4f323680.png)

Using `osmnx` to collect data and create a grid on where restaurants are located inside of Los Angeles
```
city = "Los Angeles"
tags = {'amenity': "restaurant"}
```
![image](https://user-images.githubusercontent.com/73620346/130305837-18395b6b-2569-41e7-8883-d5a93c9751f6.png)

<h1> Comparing CMAP data to OSM data </h1>




 
