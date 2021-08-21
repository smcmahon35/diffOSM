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
In this file we can select what place/city we want to search `osmnx` data from by changing the `city` variable.
```
city = "Chicago"
```
The city variable currently holds the string `"Chicago"` but it can be changed to search any city.

Once we select the area we want to search through we have to select the points of interest that we want to find within that area.
To do this we have to change the `tags` variable.
```
tags = {'amenity': "school"}
```
The tags variable currrently is used to find all schools within the given `city`. Some other options for what tags can be used are found [here](https://wiki.openstreetmap.org/wiki/Map_features)
 
