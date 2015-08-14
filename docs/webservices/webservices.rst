============
Web Services
============

What are Web Services?
======================

A Web service is a method of communication between two electronic devices over a network. It is a software function provided at a network address over the Web with the service always on as in the concept of utility computing. The W3C defines a Web service generally as, "a software system designed to support interoperable machine-to-machine interaction over a network." (from `Wikipedia <https://en.wikipedia.org/wiki/Web_service>`_) 

For the WCODP and this knowledge base, we are most interested in web mapping services and catalog services.  Web mapping services are web services that allow us to view, query, and manipulate or process geospatial maps and/or data.   Catalog services, which are described in the `next section`_, are for publishing and searching metadata.

.. _Catalog services: ../catalogs/catalogs.html
.. _next section: ../catalogs/catalogs.html

Why Create Web Services?
========================

Web services provide an open interoperable and highly efficient framework for using distributed data resources in common systems.  A web mapping service published by a single data provider, can be used simultaneously by many different users and applications, both web and desktop applications.

Web mapping services give the publisher control over how the data are displayed and the types of capabilities that the end-user can access, such as query, edit, geoprocess, download, etc.  Publishing a web mapping service facilitates end-user access to the most current and authoritative data because the web service address (URL) remains unchanged, while data supporting the service can be modified and updated.   

In the West Coast Ocean Data Portal (WCODP), web mapping services are used to facilitate data discovery by allowing end-users to preview and visualize the data on a map.   

.. image:: images/Visualize_example.png
	:scale: 40 %
	:target: http://portal.westcoastoceans.org/discover/#?text=humpback%20pacific
	:align: center

For example, if you selected the `VISUALIZE`_ link in the example WCODP record above, it would display the associated web mapping service in the WCODP map viewer. 

.. _VISUALIZE: http://maps.westcoastoceans.org/visualize/#humpback-whale-pacific-summer

Types of Web Mapping Services
=============================

Web mapping services comprise a lot of  different kinds of services, including:

	* mapping services - to get a map image
	* data services - to get coordinates of map features or attributes about the features
	* geocoding or address matching services - to get a coordinate for an address
	* geoprocessing services - to get information about feature services or to modify those shapes

.. sidebar:: Web Mapping Service versus Web Map Service (WMS)

	The terminology is a bit confusing because Web Map Service (WMS) refers specifically to the Open Geospatial Consortium (OGC) `WMS interface standard`_.  However, some people or software vendors may use the term as a generic description of  web services for geospatial data.   For this knowledge base, when we are referring to geospatial web services in general, we will use the term *web mapping services*.  

	.. _WMS interface standard: http://www.opengeospatial.org/standards/wms

The Open Geospatial Consortium (OGC) provides a variety of open source standards for web mapping services which have been broadly adopted by the geospatial community.  Some of the commonly used standards are listed below. 

	* A Web Map Service (`WMS`_) defines an interface that allows a client to get maps of geospatial data and gain detailed information on specific features.
	* A Web Feature Service (`WFS`_) allows a client to perform data manipulation operations on one or more geographic features.  WFS offers direct fine-grained access to geographic information at the feature and feature property level.
	* A Web Processing Service (`WPS`_) provides access to calculations or models which operate on spatially referenced data.
	* A Web Map Tile Service (`WMTS`_) provides access to cartographic maps of geo-referenced data.  WMTS is commonly used for base maps.
	* A Web Coverage Service (`WCS`_) defines a standard interface and operations that enable interoperable access to geospatial coverages consisting of intact, raw data.  WCS is commonly used with multidimensional or raster data.

Some additional OGC standards (data formats and services) include: `KML`_, Sensor Observation Service (`SOS`_), `GeoPackage`_, `NetCDF`_, and Catalogue Service (`CSW`_). 

.. _WMS: http://www.opengeospatial.org/standards/wms
.. _WFS: http://www.opengeospatial.org/standards/wfs
.. _WPS: http://www.opengeospatial.org/standards/wps
.. _WMTS: http://www.opengeospatial.org/standards/wmts
.. _WCS: http://www.opengeospatial.org/standards/wcs
.. _KML: http://www.opengeospatial.org/standards/kml
.. _SOS: http://www.opengeospatial.org/standards/sos
.. _GeoPackage: http://www.opengeospatial.org/standards/geopackage
.. _NetCDF: http://www.opengeospatial.org/standards/netcdf
.. _CSW: http://www.opengeospatial.org/standards/cat

ESRI has its own proprietary web mapping services that are usually referred to as ArcGIS REST or ESRI REST services, and can be accessed via the `ArcGIS REST API`_. The ArcGIS REST services have similar capabilities to the OGC services, including, 

	* `Map Service`_
	* `Feature Service`_
	* `Geoprocessing Service`_
	* `Image Service`_

.. _ARCGIS REST API: http://resources.arcgis.com/en/help/arcgis-rest-api/index.html#/The_ArcGIS_REST_API
.. _Map Service: http://server.arcgis.com/en/server/latest/publish-services/windows/what-is-a-map-service.htm
.. _Feature Service: http://server.arcgis.com/en/server/latest/publish-services/windows/what-is-a-feature-service-.htm
.. _Geoprocessing Service: http://server.arcgis.com/en/server/latest/publish-services/windows/what-is-a-geoprocessing-service-.htm
.. _Image Service: http://server.arcgis.com/en/server/latest/publish-services/windows/key-concepts-for-image-services.htm


How to Create Web Mapping Services
==================================

foo

Best Practices for Creating Services
====================================

Put Anna's presentation links here

Projection/Coordinate System
----------------------------

foo

Cartography
-----------

foo
