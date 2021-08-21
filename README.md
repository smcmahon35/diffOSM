# diffOSM
This project focuses on using open street map data to locate points of interest using a tag at any location. For example in this code I use open street map to find data of chicago and I use the tag = "school" to find all K-12 schools in the chicagoland area. I then use this data to create a grid/map of chicago highlighting the areas with the least/most schools. In this project I also compare data given from other shp files to the open street map data and compare the differences between the datasets.


<h1> Required Libraries</h1>

```
pip -r requirements.txt
```
<h1> Data Files </h1>

[The Chicago Landuse data](https://datahub.cmap.illinois.gov/dataset/land-use-inventory-for-northeast-illinois-2015) used in `cmap_vs_osm.ipynb`as a `.shp` file

