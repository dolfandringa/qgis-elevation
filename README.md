Quantum GIS Elevation Plugin
============================

The QGIS Elevation Plugin is available from http://polylinie.de/elevation

Quantum GIS is available from http://www.qgis.org

Functionality: The plugin will obtain and display point elevation data using 
the Google Maps API.

Use of the extension requires acceptance of the Google Maps Terms of Service:
http://code.google.com/intl/en/apis/maps/terms.html

Installation
============

The installation can be installed by selecting Plugins->Manage and Install Plugins... from the menu
followed by a click on "Get more".

Installation from the source tarball is also possible.

Usage in python scripts
=======================

You can also get the elevation from python scripts. 

```
from elevation.Elevation import Elevation #import the plugin
elev = Elevation(iface) #initialise the plugin
ext = iface.mapCanvas().extent() #get the current map canvas extent
point = QgsPoint(ext.xMinimum(),ext.yMinimum()) #make a point for the bottom left corner
elev.get_elevation(point) #get the elevation for the point
```
