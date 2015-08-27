========
Catalogs
========

Importance of Catalogs
======================

Catalog services are a type of web service used to discover, browse, and query standardized geospatial metadata records. A key component of the technology underlying the West Coast Ocean Data Portal (WCODP) is ESRI's Geoportal Server, an open source catalog server.  

Because of standardized interface specifications, clients of different origins and with potentially different focuses can access this technology and the geospatial metadata to which it provides potential access.  Since these interfaces are standardized, a major role in the development of catalog services is left to develpers, defining information models which can be utilized by these interfaces and yet remain independent of the underlying metadata. 

Types of Catalogs
=================

Web Accessible Folder
---------------------

A Web Accessible Folder (WAF) is an HTTP accessible directory of files, typically metadata files in XML format, in which all files and their time-stamps are visible to a web browser or client.  They represent and easy and lightweight way to share metadata, although they are limited in their ability to support higher level search and harvesting of records.

If your organization has a website, it should be fairly easy to set up a folder (WAF) to store the metadata XML files you would like to make available to the West Coast Ocean Data Portal or other catalogs and portals, such as Data.gov or your state's geospatial portal.   

Below are some example metadata WAFs harvested by the WCODP:
	* Bureau of Ocean Energy Management (BOEM), `Pacific Region WAF`_
	* `Marine Cadastre WAF`_
	* United States Geologic Services (USGS) `West Coast WAF`_

.. _Pacific Region WAF: http://metadata.boem.gov/geospatial/
.. _Marine Cadastre WAF: http://coast.noaa.gov/data/Documents/Metadata/harvest/MarineCadastre/
.. _West Coast WAF: http://coastalmap.marine.usgs.gov/metadata/westcoast/

Catalog Service for the Web
---------------------------

Catalog Service for the Web (`CSW`_) is a standard for exposing a catalog of geospatial records on the internet (over HTTP).  CSW is one part (or profile) of the Open Geospatial Consortium (OGC) Catalog Service, which defintes common interfaces to discover, browse, and query metadata about data, services, and other potential resources

The catalog is made up of metadata records that describe these types of data:
	* geospatial data (e.g. KML, shapefiles)
	* geospatial services (e.g. WMS)
	* other related resources

The format of each metadata record is defined in the standard only as XML, but is typically an encoding of Dublin Core, ISO 19139, or FGDC CSDGM metadata with UTF-8 character encoding.  Whatever format is used, each record must contain a set of core fields, such as Title, Format, Type (e.g. Dataset, Dataset Collection, or Service), Bounding Box (a rectangle of interest, expressed in latitude and longitude), Coordinate Reference System, and Association (a link to another metadata record). These sophisticated metadata sharing approaches support high level search requests of resources within the catalog.

CSW Requests include:

	GetCapabilities
		returns the properties of requests that are accepted by the server

	DescribeRecord
		returns information about the model of records

	GetDomain (optional)
		returns for a given record field, the range of values held by records

	GetRecords
		search for records, returning record IDs

	GetRecordsByID
		returns records, specified by their ID

	Harvest (optional)
		create or updated metadata by asking the surver to 'pull' metadata from somewhere

	Transaction (optional)
		create or edit metadata by 'pushing' the metadata to the server


.. _CSW: http://www.opengeospatial.org/standards/cat


Catalog Server Software
=======================

PyCSW
-----
.. sidebar:: PyCSW Sites
	
	* `Inside Idaho <http://www.insideidaho.org/>`_
	* `OpenDataPhilly <https://www.opendataphilly.org/>`_

The main focus of `PyCSW`_ is providing a very lightweight Python CSW server solution.  Another goal is to allow you to quickly publish your metadata repository and make your resources doscoverable.  A number of data catalog projects, including CKAN, have begun using PyCSW to provide their CSW harvesting and serving capabilities.


GeoNetwork
----------
.. sidebar:: GeoNetwork Site

	* `Oregon Coastal Atlas <http://www.coastalatlas.net/>`_

`GeoNetwork`_ is a mature data catalog product and is one of the flagship projects of OSGeo.   It is populare outside of the United States and has excellent support fo the EU INSPIRE Initiative. GeoNetwork is increasingly developed in lock-step with other open source GIS projects including GeoServer, GeoWebCache, and GeoNode.


ESRI Geoportal Server
---------------------

.. sidebar:: ESRI Geoportal Sites

	* `Oregon Spatial Data Library <http://spatialdata.oregonexplorer.info/geoportal/catalog/main/home.page>`_
	* `National Geophysical Data Center Geoportal <http://www.ngdc.noaa.gov/metadata>`_

`ESRI Geoportal`_ is a mature data catalog product created by ESRI, and is now open source.  It is in widespread use by state and federal agencies that have traditional GIS departments.  It is used on the backend of the West Coast Ocean Data Portal.

.. seealso::

	`ESRI Geoportal Server Wiki <https://github.com/Esri/geoportal-server/wiki>`_

CKAN
----
.. sidebar:: CKAN Site

	* `Data.gov <http://www.data.gov/>`_

`CKAN`_ was created by the Open Knowledge Foundation (`OKFN`_) in the United Kingdom and is the data catalog platform behind data.gov.uk.  CKAN is now beginning to catch on in the United States.  It was chosen to become the data catalog behind data.gov and geo.data.gov.  CKAN now employs PyCSW as its CSW engine.


THREDDS Data Server (TDS)
-------------------------

.. sidebar:: THREDDS Sites

	* `CENCOOS <http://www.cencoos.org/data/access>`_
	* `SCCOOS <http://sccoos-obs0.ucsd.edu/thredds/catalog.html>`_
	* `IOOS <http://catalog.ioos.us/>`_

`THREDDS Data Server (TDS)`_ is a web server that provides metadata and data access for scientific datasets using OPenDAP, OGC, WMS, and WCS, HTTP, and other remote data access protocols.  TDS can be used to create virtual directories of available data and their associated metadata and present a combined file that a user seas and can access as a single file containing data.  It is developed by Unidata and is in widespread use by NOAA offices and the Ocean Observing Community.

.. seealso::

	http://www.unidata.ucar.edu/software/thredds/current/tds/TDS.html


.. _PyCSW: http://pycsw.org
.. _GeoNetwork: http://www.geonetwork-opensource.org
.. _ESRI Geoportal: http://www.esri.com/software/arcgis/geoportal
.. _CKAN: http://ckan.org
.. _OKFN: https://okfn.org/
.. _THREDDS Data Server (TDS): http://www.unidata.ucar.edu/software/thredds/current/tds/


Best Practices for Catalogs
===========================
* Advertise your CSW endpoint so that people can readily access it through an 'API' or 'Developer' tab.
* ESRI Geoportal and CKAN both provide comprehensive open source catalog software options that have been adopeted by a wide user community and are recommended.
* Publish only your original metadata and data.
