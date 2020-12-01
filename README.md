# Lab 6: Interactive Maps with Folium
Due: 4th December 2020

This repo contains one script titled `Jess-Strzempko_Folium-Python_IDCE30274Lab6.ipynb`. This script was created as part of Lab 6: Interactive Maps with Folium for IDCE 30274: Computer Programming in GIS taught by Professor Shadrock Roberts at Clark University. 

## Objectives

This lab introduces the Python library [Folium](https://python-visualization.github.io/folium/), which builds on the web mapping JavaScript library [Leaflet](https://leafletjs.com/) to allow the user to build interactive maps into Python notebooks. If this code is run outside of Google Colab, it should be in a Python coding environment with [Pandas](https://pandas.pydata.org/), [Folium](https://python-visualization.github.io/folium/), and [JSON](https://docs.python.org/3/library/json.html) libraries. Pandas dataframes are used in this lab to combine information across the three datasets found in the data folder: LA county (`laMap.geojson`), LA zip codes (`laZips.geojson`), and Starbucks Locations in LA County (`starbucksInLaCounty.csv`). 

## Method

The first map is a chloropleth map of Starbucks per zip code in LA county. First, files are uploaded in Colab using a Browse button to search for the files in the local computer. Next, we import all necessary libraries, then initialize a dataframe to input the data into. From here, we can count the number of stores in each zip code, attaching this to the appropriate geometry for that zip code using the Pandas dataframe we've previously created. The last step is to create the interactive map - many of the parameters for the construction of the maps is found in [the Quickstart Guide for Folium](https://python-visualization.github.io/folium/quickstart.html). Layer control is added to the map before display so users can toggle the available layers. Other options for customization include the attribution (OpenStreetMap, Carto, and Ritvik Kharkar in our case), basemap style, and bin size or number. 

Next, we create a precise map of all Starbucks' locations in LA County from the latitude/longitude pairs in our dataframe . This is created to contrast the previous map in which we've binned our point data for Starbucks by a random administrative unit that does not correlate to store locations or tell a meaningful story with the data. If anything it creates confusion and potential for misinterpretation. This is the "[Modifiable Areal Unit Problem](https://www.e-education.psu.edu/sgam/node/214)" or MAUP, which [Carto has a nice blog post about](https://carto.com/blog/zip-codes-spatial-analysis/). 

The last map created with this tutorial demonstrates unemployment rates in 2012 by US state. This additional map demonstrates the proper use of administrative boundaries as a geography to display by. The code used in this section of the script accesses the data stored in a Github repo through the repo's URL [here](https://github.com/python-visualization/folium/tree/master/examples/data)

# The Code
All data can be accessed and downloaded publicly and script can be re-run using modified file paths and names. If questions arise, users can contact Jess Strzempko at JeStrzempko@clarku.edu for more help and further information.

# Citation
This tutorial is based on [this Medium Tutorial by Ritvik Kharkar](https://towardsdatascience.com/making-3-easy-maps-with-python-fb7dfb1036) and the associated [Github repo for his tutorial](https://github.com/ritvikmath/StarbucksStoreScraping). Professor Roberts updated deprecated Folium code, re-ordered steps in the tutorial to address the conceptual problem of MAUP, and adds the brief follow-up using unemployment rates. 
