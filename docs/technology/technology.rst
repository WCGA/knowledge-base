==============
Our Technology
==============
The following sections describe the technology and architecture behind the West Coast Ocean Data Portal (WCODP).  It is not necessary to understand this information in order to contribute to the portal, but may be of interest to developers, technologists, and those who  update, maintain, or troubleshoot the WCODP. 

Architecture
============
The West Coast Ocean Data Portal is comprised of a number of technologies and software components.  The following diagram shows a generalized view of the software architecture.

.. image:: images/WCODP_expanded_system_diagram.png
	:scale: 100 %
	:align: center


**The WCODP relies upon the following technologies:**

`Nginx`_
	HTTP server and reverse proxy

`Apache Tomcat 6`_
	Java web server.  Tomcat is particularly good for Java-based apps like Geoportal, but is flexible enough to handle most of the other apps as well.

`WCGA Data Portal UI`_
	WCODP front-end -- mostly JavaScript and HTML.  The HTML is generated using Jekyll. The JavaScript includes AngularJS, Bootstrap, JQuery, and several other building blocks.  This static site pulls data from Geoportal Server and Solr to display the contents and information stored in the Portal

`ESRI Geoportal Server`_ 
	An open source geo-data catalog.  It allows for the entry or collection (‘harvesting’) of metadata files. Using these metadata files, Geoportal Server can organize, search, and display all if the information in meaningful, human-readable ways. We are also using the “collections” feature of Geoportal Server to define custom categories and issues, and assign those as attributes of the records we have harvested. This way we can organize the data according to categories that we have determined and applied ourselves, categories that are not defined in the metadata.

`Solr`_
	Solr is a tool used to aid in the quick searching of large amounts of data. It takes specific attributes of the data, and keeps track of which records shared that attribute, so that when it is requested, it doesn’t have to search every record: it already knows. Technically, that work is already done by a software called Lucene, and it is installed with Geoportal Server. Solr is built on top of Lucene and allows for faceted searches. The most visible result of which is the numeric indicator of how many records will match your query if you add specific filters (like the categories or issues).

GFC 
	Geoportal Facet Customizations.  This custom tool was built by ESRI for us specifically to handle some of our needs that were not met by the basic Geoportal Server software. Namely, this is the piece that gets our custom-defined categories and issues indexed by Solr for faceted searches, and exposes the harvest source of each record to Solr as well. As of this writing, it does not yet, but may soon also facilitate in searching which records were harvested from a given source.

`PostgreSQL`_/`PostGIS`_
	PostgreSQL is a nice database for moderate to heavy traffic websites. It is fast and powerful. PostGIS is built on top of PostgreSQL to handle geographic queries, which Geoportal Server relies on to search by location, bounding box, etc…

`Munin`_
	Monitoring software. This tool visualizes the status of the server hardware.

.. _Nginx: http://wiki.nginx.org/Main
.. _Apache Tomcat 6: https://tomcat.apache.org/index.html
.. _WCGA Data Portal UI: https://github.com/Ecotrust/wc-data-registry
.. _ESRI Geoportal Server: https://github.com/Esri/geoportal-server
.. _Solr: http://lucene.apache.org/solr/
.. _PostgreSQL: http://www.postgresql.org/
.. _PostGIS: http://postgis.net/
.. _Munin: http://munin-monitoring.org/

.. seealso::

	Background on the selection of technologies for the West Coast Ocean Data Portal
		`WCGA RDF Data Registry Design Assessement <http://www.westcoastoceans.org/media/data_network_act/wcga_rdf_data_registry_design_assessment_2013.pdf>`_

Registration / Harvest Process
==============================

Registration and metadata harvest into the WCODP is done through the Adminstrative interface of ESRI Geoportal Server.  This is generally done by the WCODP Administrator, but can be done by others with administrative access.

If the WAF or Catalog is not yet registered in the WCODP, it must be added via the Register Resource page.  
	1. Log into ESRI Geoportal (http://portal.westcoastoceans.org/geoportal) as an administrator
	2. On the Administration page, click Add, and select Register resource on the network
	3. Add the Host URL for the WAF or Catalog (CSW).  It's good practice to use the Test button to confirm that the URL works
	4. Add a Title -- This is what will show up in the Sources list of the WCODP, so make sure it is clear and user-friendly.
<<<<<<< HEAD
	5. If you are harvesting from a catalog, you need to select the Profile.  There are three custom profiles for WCODP depending on the type of CSW being harvested:
		* ESRI Geoportal (GPT)
		* GeoNetwork APISO
		* PyCSW Custom
=======
	5. If harvesting from a Catalog, select a Profile based on publisher's CSW. WCODP has three custom profiles:   
		* WCGA RDF ESRI Geoportal (GPT)
		* WCGA RDF GeoNetwork APISO
		* pycsw - harvest by dc:identifiers
>>>>>>> 91a9e347ebbc00cfac80ff838c23f85277bdd942
	6. You can leave all the other information as-is.  Create and Close.

After you register the resource for the first time, you must approve and synchronize the resource.
	1. Return to the Manage page of the Administration interface.
	2. Select the checkbox next to the resource you just registered
	3. Select "Set as Approved" in the pull-down menu, and click Execute Action
	4. Click on the blue arrow (Synchronize content) icon next to the resource of interest.  This may take a minute or two and you may need to manually refresh the page

Review the synchronization results.
	1. Click on the clock icon (History) next to the resource of interest.  
		* This will show the date of the most recent synchronization, the number of records obtained, the number of records validated, and the number of records published.
	2. If the number of records validated or published does not match the number of records obtained, 
		1. Click on the empty box icon (View report)
		2. Click the plus sign next to Details to see the validation results which shows the metadata records harvested and the validation errors.

If the harvested resource is a WAF, all valid metadata records in that folder will be harvested.   

If the harvested resource is a CSW, it is possible to selectively harvest relevant records through the use of profiles in Geoportal.  The unique UUID of each metadata record of interest must be added to a specific XSLT file on the server.   The XSLT file corresponding to the profile that you selected when registering the resource is the one to update.

When there are updates or additions to metadata in a WAF or Catalog that is already registered in the WCODP, simply synchronize the resource.  For a CSW, you must also add the relevant UUIDs to the profile file prior to synchronization.

After registration and harvest, the portal admin assigns additional attributes to the records using the `WCGA-specific controlled vocabulary/taxonomy <https://docs.google.com/spreadsheets/d/1u302tn8UEtKlW1o2TpVwuG0xljpqJXUV29eYrx4LQmg/edit?usp=sharing>`_.  This assignment is accomplished either by assigning records to Collections through the Geoportal admin interface, or directly via adding records to the Postgres database.  These attributes are used in the Categories tab in the WCODP.


Additional Resources
====================
* `Source Code for the West Coast Ocean Data Portal <https://github.com/Ecotrust/wc-data-registry>`_
* Management Guide 


