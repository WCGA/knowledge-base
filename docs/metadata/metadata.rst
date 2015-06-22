========
Metadata
========

Why Create Metadata?
====================

Metadata helps potential users of your geospatial data to answer the questions:

* What 
* Why
* When  
* Who 
* Where
* How 

.. sidebar:: Metadata in the WCODP

	The primary use of metadata in the `West Coast Ocean Data Portal <http://portal.westcoastoceans.org/>`_ is data discovery and access.

There are a variety of purposes for creating metadata, including

* Discovery
* Exploration and Documentation
* Archive
* Access and Retrieval


Most metadata serves multiple purposes, but it is helpful to understand what level and type of information is needed to meet your primary purpose(s).  Much of the metadata created for geospatial data, especially in the natural resources and scientific domains, has focused on documenting the details of data sets: what is the purpose of the data, how it was created, what do the attributes mean, etc. 

We are now experiencing a transition that emphasizes metadata's role in data discovery and retrieval by other systems and people. This function of metadata is becoming critical as web services and data download linkages are increasingly packaged with the metadata.

.. seealso::
	
	The business case for metadata
		https://www.fgdc.gov/metadata/metadata-business-case

What Information Is Required?
=============================

For the purposes of data discovery and access, the West Coast Ocean Data Portal requires only a minimal set of information from the metadata. The following information is displayed in the portal, some of which is accessed when users filter or search for data of interest: 

* Title
* Abstract / Description
* Use Limitations / Constraints
* Bounding Box Coordinates in Latitude/Longitude (decimal degrees)
* Keywords
* Date Published
* Contacts
	* Originator
	* Publisher
	* Distributor
* URLs for data download, web services, kml, web application, documentation

If the metadata meets the requirements of the Federal Geographic Data Committee endorsed standards, (https://www.fgdc.gov/metadata/geospatial-metadata-standards), it will definitely meet the requirements of the West Coast Ocean Data Portal.


Metadata Standards and Formats
==============================

Use of standard metadata formats is critical for interoperability and access by other automated systems and web catalogs for geospatial data discovery and sharing. There are a large number of metadata standards which address the needs of particular user communities. The following standards can be used for data discovery via the West Coast Ocean Data Portal.

ISO 19115:2003
--------------

ISO 19115:2003(E) - Geographic Information: Metadata

ISO 19115 was developed by the geospatial community to address specific issues relating to both the description and the curation of spatial data. This standard can be used for describing digital or physical objects or datasets which have a spatial dimension. The standard also includes methodologies for creating application profiles, metadata extensions and hierarchical metadata and provides implementation examples. Geospatial professionals have developed a number of profiles of this standard to fit particular uses: for example, the Australia New Zealand Land Information Council (ANZLIC) Metadata Profile, the North American Profile (NAP), and the UK GEMINI profile. The standard’s accompanying XML schema, ISO/CD TS 19139 Geographic information — Metadata — enables interoperable XML expression of ISO 19115 compliant metadata.

.. seealso::
	* For more information and to acquire the ISO 19115 documentation, see http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020.


ISO 19115-2
-----------

ISO 19115 Part 2: 2009 - Geographic Information - Metadata - Part 2: Extensions

ISO 19115-2:2009 extends ISO 19115:2003 by defining the schema required for describing imagery and gridded data. In practice, this schema is used to document other types of instrumentation beyond imagery as well. It provides information about the properties of the measuring equipment used to acquire the data, the geometry of the measuring process employed by the equipment, and the production process used to digitize the raw data.

.. seealso::
	* For more information and to acquire the ISO 19115-2 documentation, see http://www.iso.org/iso/catalogue_detail.htm?csnumber=39229.

FGDC CSDGM
----------

Federal Geographic Data Committee Content Standard for Digital Geospatial Metadata (FDGC CSDGM)

The standard commonly referred to as FGDC (although FGDC is the maintenance agency, and “CSDGM” is the actual element set) is a large and early metadata standard for geospatial information created by agencies of the US federal government. The FGDC web site describes the scope of this standard as to allow users to “determine the availability of a set of geospatial data, to determine the fitness [of] the set of geospatial data for an intended use, to determine the means of accessing the set of geospatial data, and to successfully transfer the set of geospatial data.”
The current production version of FGDC is 2.0, from 1998. Since this time, an international standard for geospatial information (ISO 19115) has emerged. Plans have been announced to create a US national geospatial metadata standard as a profile of ISO 19115, and to create version 3.0 of CSDGM as an implementation of that. This work has not yet been finalized.

.. seealso::
	* For more information on the FGDC standards, see http://www.fgdc.gov/standards/projects/FGDC-standards-projects/metadata/base-metadata/index_html.

Dublin Core
-----------

Dublin Core Metadata Element Set

The Dublin Core Metadata Element Set (ISO Standard 15836) is a basic standard which can be easily understood and implemented and as such is one of the best known metadata standards. It consists of 15 elements which address the most basic descriptive, administrative and technical elements required to uniquely identify a digital resource. Most resource discovery metadata standards can be mapped to the Dublin Core Metadata Element Set, enabling basic federated searching across metadata created using a number of different standards, without detracting from richer metadata held elsewhere.

.. seealso::
	* See http://dublincore.org/ for more information on the Dublin Core Metadata Initiative.

EML
---

Ecological Markup Language

* EML is a specification intended to support the description of any type of ecological information, including raw data, published research papers, rights information, and research protocols. At the highest level, EML models four primary entities: datasets, literature, software, and protocols.
* For more information about EML, see http://knb.ecoinformatics.org/software/eml/.

How to Create Metadata
======================

Describe and compare Tools here.   Will not be exhaustive list, but some tips for using tools as it relates to WCODP and recommendations based on our experiences.   

Will include lots of links to other sites here.

https://www.fgdc.gov/metadata/geospatial-metadata-tools

WCODP metadata template can be linked here too.

Validating Your Metadata
========================


How Is the Metadata Displayed?
==============================

This part will explicitly show the translation between the metadata content or Xpaths and where it shows up on the WCODP.  (Because that isn't necessarily intuitive)

Best Practices for Metadata
===========================

Content 
-------
Guidance on what makes a good title, abstract, etc.

Publishing Great Metadata 
-------------------------

Tanya Haddad gave the following presentation at the 2014 West Coast Ocean Data Network Meeting:  

`Presentation Slides <http://network.westcoastoceans.org/wp-content/uploads/2014/12/Haddad_WCGA_Successful_Data_Sharing-1.pdf>`_ 

Presentation Video Links will go here too.

