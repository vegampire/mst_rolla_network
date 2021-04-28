# OSM testing data sets
This repository is a demo for several practices with OpenStreetMap data, including transforming osm file to gmns file and finding roundabout links from osm file. To begin with, what you only need to do is exporting your own *.osm file from https://www.openstreetmap.org/export#map=13/37.7758/-122.4155. In this repository, we use the osm file from Rolla Mo as an example.  

## 1 Rolla_Mo.ipynb
Rolla_Mo.ipynb is an example for transforming osm file to gmns. It also illustrates generating traffic demand based POI rates and calculating the shortest path.


## 2 filter_roundabout.ipynb
filter_roundabout.ipynb shows how to find the links representing roundabouts in an osm map. The input is a osm file and output is a csv file. There are four columns in the out file. **id** and **osm_id** are the same, denoting the osm id of the selected link. **geometry** is the coordinate consisting a link. **junction** is a tag retrived from other_tags file of map_lines lay of the osm file, denoting the link is consisting a roundabout. 

It is strongly suggested running filter_roundabout.ipynb in Google Colab not in your local machine. Or you may run into error when importing **ogr**.
To avoid the ImportError, make sure uninstalling ogr package. Then install GDAL package refering to the tutorials(Ubuntu/Windows) below. after that, you can run from osgeo import ogr to call ogr.

https://mothergeo-py.readthedocs.io/en/latest/development/how-to/gdal-ubuntu-pkg.html

https://pythongisandstuff.wordpress.com/2016/04/13/installing-gdal-ogr-for-python-on-windows/