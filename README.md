# OpenStreetMap
Open Street Map is an open editable map of the whole world which is being build by the volunteers.
# OSM Tags
- OpenStreetMap (OSM) tags are key-value pairs that are used to describe the different features that are present on the map.
- Tags describe specific features of all elements (node, ways, relations) or changesets.
- Name tag is used to describe the label of the features. The primary name should be the most obvious name of the feature which is contained in `name` tag.
- Then there are names in different languages which are present in `name:<lang_code>`.

This project is used to sort the name tag values on OpenStreetMap so that when a feature is selected on OSM their names appear in their respective name tag.
# Map Area
Pune, Maharashtra, India


![image](https://user-images.githubusercontent.com/108971372/229038357-b33c167b-3b90-410e-8fa3-bd6205f4e21a.png)

# Data Download
The OSM data was downloaded from the Overpass turbo using the overpass query in Geojson format.
# Working With Geojson Data
- Drive to geojson is mounted on Google collab.
- Geojson file is read and converted to geodataframe using geopandas in python.
- Relevant columns in the geodataframe can be searched by slicing.
- OpenStreetMap uses **Unicode characters** to represent tags for geographic features. The Unicode pattern for OSM tags varies depending on the language and script       being used.
- We have used the **Marathi Unicode Pattern **for which Unicode range is `'[\u0900-\u097F]+'`**, to search for the marathi characters from `name` and `name:en` tag and transfer them to `name:mr` tag.
Similary, one can use other language codes and appropriate scripts to tag geographic features in different languages and scripts.
