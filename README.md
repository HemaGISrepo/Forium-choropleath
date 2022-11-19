Forium-choropleath


Using the folium.Choropleth() class, we can create a choropleth map. If the map below does not render for you, try viewing the page in a different web browser.

![image](https://user-images.githubusercontent.com/118595650/202857453-61d92d66-26cc-4b81-8b2a-439cf30d4f7c.png)


Note that folium.Choropleth() takes several arguments:

geo_data is a GeoJSON FeatureCollection containing the boundaries of each geographical area.
In the code above, we convert the districts GeoDataFrame to a GeoJSON FeatureCollection with the __geo_interface__ attribute.
data is a Pandas Series containing the values that will be used to color-code each geographical area.
key_on will always be set to feature.id.
This refers to the fact that the GeoDataFrame used for geo_data and the Pandas Series provided in data have the same index. To understand the details, we'd have to look more closely at the structure of a GeoJSON Feature Collection (where the value corresponding to the "features" key is a list, wherein each entry is a dictionary containing an "id" key).
fill_color sets the color scale.
legend_name labels the legend in the top right corner of the map.
