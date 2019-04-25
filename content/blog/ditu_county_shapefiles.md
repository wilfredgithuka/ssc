---
title: "Working With Kenya County Shapefiles"
date: 2019-04-19T16:55:28Z
draft: false
---

This is an update to the previous mapping project of Technical Training Institutes
with welding equipment supplied by AVIC. You can read more about it here.

In the previous map I managed to produce a map but it lacked the following crucial
features which are very important.

* Landmarks
* Roads & Highways
* County Boundaries

Today I have solved the last 2 issues on the above list.

## County Boundaries

By working with something called Shapefiles, I have managed to add this to my map
plot to produce the county boundaries, now the map looks more navigateable. Have a look.

![map+county](/img/welding_county.png)

To plot the [shapeflies](https://basemaptutorial.readthedocs.io/en/latest/shapefile.html), extract the .zip into a folder. On the code link it as follows:

`map.readshapefile('data/County', 'County')`

The folder where the shapefiles were extracted is called data. All the files in the folder
shall have a common name, this is what you use before and after the comma.

#### Basic Usage of Shapefiles in basemap

```from mpl_toolkits.basemap import Basemap
import matplotlib.pyplot as plt

map = Basemap(llcrnrlon=-0.5,llcrnrlat=39.8,urcrnrlon=4.,urcrnrlat=43.,
             resolution='i', projection='tmerc', lat_0 = 39.5, lon_0 = 1)

map.drawmapboundary(fill_color='aqua')
map.fillcontinents(color='#ddaa66',lake_color='aqua')
map.drawcoastlines()

map.readshapefile('../sample_files/comarques', 'comarques')

plt.show()
```
Using above examples I implemented the shapefile into my code as follows:

### My Shapefile Implementation

```
from mpl_toolkits.basemap import Basemap
import matplotlib.pyplot as plt
import numpy as np

plt.figure(figsize=(40,20))
plt.title('Welding Technology Training Institutions')
map = Basemap(projection='cyl', llcrnrlat=-4.9, llcrnrlon=33.75, urcrnrlat=5.19, urcrnrlon=42.03, resolution='h', suppress_ticks=True)

map.drawcoastlines()
map.drawparallels(np.arange(0,4,10), labels=[1,1,1,1])
map.drawmeridians(np.arange(-180, 180,30), labels=[1,1,1,1])
#map.drawstates()
#map.drawcountries()
map.readshapefile('data/County', 'County')
#map.drawcounties()
#map.shadedrelief()

#map.drawrivers(color='#0000ff')
#map.drawstates(color='0.5')


lons = [34.77, 36.61, 36.59, 37.09, 35.55, 34.97, 37.80, 37.06, 34.75, 38.35]
lats = [-0.7, -1.41, -1.26, -0.47, -0.21, -0.77, 1.59, -1.29, -0.05, -3.48]

map.plot(lons, lats,'ro')
plt.text(34.77,-0.7,'Kisii NP',fontsize=15, ha='center', va='bottom', color='k')
plt.text(36.61,-1.41,'Kajiado West TTI', fontsize=15, ha='center', va='top',color='k')
plt.text(36.59,-1.26,'Nachu TTI',fontsize=15, ha='center', va='bottom',color='k')
plt.text(37.09,-0.47,'Mathira TVC',fontsize=15, ha='center', va='bottom',color='k')
plt.text(35.55,-0.21,'Kimasian TTI',fontsize=15, ha='center', va='bottom',color='k')
plt.text(34.97,-0.77,'Riragi TTI', fontsize=15, ha='center', va='top',color='k')
plt.text(37.80,1.59,'Leisamis TTI',fontsize=15, ha='center', va='bottom',color='k')
plt.text(37.06,-1.29,'Kasarani TVC',fontsize=15, ha='left', va='center',color='k')
plt.text(34.75,-0.05,'Riat TVC',fontsize=15, ha='center', va='bottom',color='k')
plt.text(38.35,-3.48,'Mwatate TVC',fontsize=15, ha='center', va='top',color='k')
plt.text(36.82,-1.29,'NAIROBI',fontsize=7, ha='center', va='top',color='k', bbox=dict(facecolor='b', alpha=0.2))
plt.text(39.66,-4.04,'MOMBASA',fontsize=15, ha='center', va='top',color='k', bbox=dict(facecolor='b', alpha=0.2))
plt.text(34.76,-0.09,'KISUMU',fontsize=7, ha='center', va='top',color='k', bbox=dict(facecolor='b', alpha=0.2))

x, y = map(lons, lats)
map.scatter(x, y, marker='s',color='m')

#x, y = map(lons, lats)

#map.scatter(x, y, marker='D',color='m')

plt.show()
plt.savefig('Final_2.png')
```

### So where did I get the shapefiles?

The shapefiles are from [AfricaOpenData](https://africaopendata.org/dataset/kenya-counties-shapefile) and its available for free download. The shapefiles are
authored by David Muthami and were last updated in December 2015. A huge thanks to David for
the wonderful work.

## Roads and Highways

For showing roads it was straight forward, thats what I thought.

I got a shapefile for all roads from [OCHA](https://data.humdata.org/dataset/hotosm_ken_roads) and when I ran the code, the laptop quickly ran out of RAM and
froze. The dataset was over 100MB big and given that I had 7 workspaces running, that was the problem.

I rebooted and ran the notebook again and this is what I got:

![map_roads](/img/roads_all.png)

The map was super detailed, infact too detailed for my use.

I think thats enough for today.
