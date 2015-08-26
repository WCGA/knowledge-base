========
Catalogs
========

Importance of Catalogs
======================

Catalog services are a special kind of web service used to discover, browse, and query standardized geospatial metadata records. A key component of the technology underlying the West Coast Ocean Data Portal (WCODP) is ESRI's Geoportal Server, an open source catalog server.  

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

	**GetCapabilities**
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


Best Practices for Catalogs
===========================