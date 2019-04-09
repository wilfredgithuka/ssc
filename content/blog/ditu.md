---
title: "Mapping Welding Training Schools in Kenya With Python Basemap"
date: 2019-04-09T06:25:13Z
draft: false
---

A few weeks ago at work I was asked to create a map of all the technical training institutions
which had equipment for Mechatronics engineering. This process involved getting a map from Google
and using Ms Word to place small triangles where the schools are located.

This map is to help my colleagues who were planning to go for site inspection to plan their
journey well, in the most cost effective manner.

This was the result.

After doing another map for electrical institutions I relalised there was a challenge. The map
I was using was not clear and the locations were a mere estimation of where the school was.

Further more, the process was dauntingly slow and too many clicks. I thought of how I can automate
this process and make it more creative. Python was the solution.

Python's toolkit for generating maps is called Basemap. Using jupyter notebook I created a small
example to learn how to work with Basemap.

With only a weeked to the submission of the map, I managed to get all the GPS co-ordinates of the
institions using Google maps and fed them into Basemap which produced a eat map of all the 10 schools
that needed to be mapped.

### Institutions' GPS Locations

The first step is go get the location of all the schools. I have 10 schools which I need to map.

This I did by looking them up on Google Maps.

### Feed the location to basemap

This is the core part of the solution. For this first part I wrote code that picked each schools location
and plotted it on a map. But I think I can make my code much more lean.

This was after long hours of tweaking and this was the result.

![welding](/img/welding.png)

The generated map was clean and crisp. However eventhough I submitted it, it was lacking in:

* Landmarks
* Roads and Highways
* Cities and County boundaries

These I later realised were important when it comes to localisation.

The map however served its purpose and my boss was happy.

The [GithubRepo](https://www.github.com/wilfredgithuka/ditu) for this project is available.

## So What Have You Learnt?
This is the key question.

I have learnt alot when it comes to mapping and how maps can be able to make us understand data more accurately.
For this project really, this is just the starting. I want to leverage on maps and how I can get more data say
for each school and maybe predict which school is likely to benefit more from the equipment depending on usage.

## Valuable Resources

* [Basemap-Readthedocs](https://basemaptutorial.readthedocs.io/en/latest/plotting_data.html)
* [Matplotlib-Basemap](https://matplotlib.org/basemap/users/examples.html)
* [Sensitive Cities](https://sensitivecities.com/so-youd-like-to-make-a-map-using-python-EN.html)
* [Towards Data Science](https://towardsdatascience.com/lets-make-a-map-using-geopandas-pandas-and-matplotlib-to-make-a-chloropleth-map-dddc31c1983d)
* [Geodesygina](http://geodesygina.com/matplotlib.html#prepare-the-data)
* [Datadependence](https://www.datadependence.com/2016/06/creating-map-visualisations-in-python/)
* [BoundingBox Tool](http://boundingbox.klokantech.com/)
* [Kenya Roads Base Map](https://www.arcgis.com/home/item.html?id=68a8839295c24c7fb17fbc1d47c189f7)
