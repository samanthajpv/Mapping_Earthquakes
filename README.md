# Mapping_Earthquakes
An interactive earthquake map using D3, Leaflet, and Mapbox API

## Project Overview
The purpose of this project was to create an interactive map that plots GeoJSON USGS earthquake data and tectonic plates data through Mapbox API. The user has the option to change the type of map and choose layers to apply such as major earthquakes, all earthquakes, and tectonic plate boundaries. 

### Resources
- Data Source: 
    - [All Earthquakes - past 7 days](https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_week.geojson)
    - [Major Earthquakes - past 7 days](https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/4.5_week.geojson)
    - [Tectonic Plates](https://raw.githubusercontent.com/fraxen/tectonicplates/master/GeoJSON/PB2002_boundaries.json)
- Languages: JavaScript, HTML, CSS
    - Libraries: Leaflet, D3.js
- Mapbox API
- Software: VSCode
- Code:
    - [challenge_logic.js](https://github.com/samanthajpv/Mapping_Earthquakes/blob/e16e4c0ce0186f3a4935c60ba6ca472bbeb7ee06/Earthquake_Challenge/static/js/challenge_logic.js)
    - [index.html](https://github.com/samanthajpv/Mapping_Earthquakes/blob/e16e4c0ce0186f3a4935c60ba6ca472bbeb7ee06/Earthquake_Challenge/index.html)
    - [style.css](https://github.com/samanthajpv/Mapping_Earthquakes/blob/e16e4c0ce0186f3a4935c60ba6ca472bbeb7ee06/Earthquake_Challenge/static/css/style.css)

## Method

<p align="middle">
    <img src="" width="700" height="400"/>
    <h5 align="center">Interactive Earthquake Map</h5>
</p>

1. **Create tile layers** - This displays the tile layer or background of the map. In this project, there are three tile layers; streets, satellite streets, and dark. The type of map can be switched using the Layers Control found on the top right-hand corner of the map.
2. **Create map object** - This creates the map referencing the id of the div that holds the map in the index.html file, its center coordinates, zoom level, and default layer.
3. **Create base layer** - This hold all three maps.
4. **Create layer groups** - There are three overlays; 'Earthquakes', 'Tectonic Plates', and 'Major Earthquakes'. 
5. **Add control layer** - This enables the user to toggle between maps and layers. 
6. **Retrieve GeoJSON data** 
    - Data was retrieved using D3. 
    - Radius of circle markers are relative to the earthquakes' magnitude.
    - Color of the circle markers are relative to the earthquakes' magnitude.
    - A pop up was added for every marker to show the magnitude and location.
    - For the tectonic plates, boundaries were plotted.
    - Data retrieved from each D3 function was added to its respective layer and then added to the map.
7. **Create legend** - The legend found on the bottom right-hand corner of the map was created to show that the color of the markers get darker as the magnitude increases.

## Reference
(1) Trilogy Education Services. (2021, September). *Module 13 Challenge*. https://courses.bootcampspot.com/courses/626/assignments/13333?module_item_id=213329