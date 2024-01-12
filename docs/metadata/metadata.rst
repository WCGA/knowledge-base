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

If the metadata meets the requirements of the Federal Geographic Data Committee (FGDC) endorsed standards, (https://www.fgdc.gov/metadata/geospatial-metadata-standards), it will definitely meet the requirements of the West Coast Ocean Data Portal.


Metadata Standards and Formats
==============================

Use of standard metadata formats is critical for interoperability and access by other automated systems and web catalogs for geospatial data discovery and sharing. There are a large number of metadata standards which address the needs of particular user communities. NOAA and FGDC have a broad catalog of resources about metadata standards. 

* http://www.fgdc.gov/metadata/geospatial-metadata-standards
* http://www.ncddc.noaa.gov/metadata-standards/

.. seealso::
	* http://www.dcc.ac.uk/resources/briefing-papers/standards-watch-papers/what-are-metadata-standards

The following standards can be used for data discovery via the West Coast Ocean Data Portal:

ISO 19115:2003
--------------

ISO 19115:2003(E) - Geographic Information: Metadata

ISO 19115 was developed by the geospatial community to address specific issues relating to both the description and the curation of spatial data. This standard can be used for describing digital or physical objects or datasets which have a spatial dimension. The standard also includes methodologies for creating application profiles, metadata extensions, and hierarchical metadata and provides implementation examples. Geospatial professionals have developed a number of profiles of this standard to fit particular uses: for example, the Australia New Zealand Land Information Council (ANZLIC) Metadata Profile, the North American Profile (NAP), and the UK GEMINI profile. The standard’s accompanying XML schema, ISO/CD TS 19139 Geographic information — Metadata — enables interoperable XML expression of ISO 19115 compliant metadata.

.. seealso::
	* For more information and to acquire the ISO 19115 documentation, see http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020.
	* NOAA, NCDDC workbook for implementing ISO 19115: http://service.ncddc.noaa.gov/rdn/www/metadata-standards/documents/MD-Metadata.pdf	


ISO 19115-2
-----------

ISO 19115 Part 2: 2009 - Geographic Information - Metadata - Part 2: Extensions

ISO 19115-2:2009 extends ISO 19115:2003 by defining the schema required for describing imagery and gridded data. In practice, this schema is used to document other types of instrumentation beyond imagery as well. It provides information about the properties of the measuring equipment used to acquire the data, the geometry of the measuring process employed by the equipment, and the production process used to digitize the raw data.

.. seealso::
	* For more information and to acquire the ISO 19115-2 documentation, see http://www.iso.org/iso/catalogue_detail.htm?csnumber=39229.
	* NOAA, NCDDC workbook for implementing ISO 19115-2: http://service.ncddc.noaa.gov/rdn/www/metadata-standards/documents/MI-Metadata.pdf

FGDC CSDGM
----------

Federal Geographic Data Committee Content Standard for Digital Geospatial Metadata (FDGC CSDGM)

The standard commonly referred to as FGDC (although FGDC is the maintenance agency, and “CSDGM” is the actual element set) is a large and early metadata standard for geospatial information created by agencies of the US federal government. The FGDC web site describes the scope of this standard as to allow users to “determine the availability of a set of geospatial data, to determine the fitness [of] the set of geospatial data for an intended use, to determine the means of accessing the set of geospatial data, and to successfully transfer the set of geospatial data.”
The current production version of FGDC is 2.0, from 1998. Since this time, an international standard for geospatial information (ISO 19115) has emerged. Plans have been announced to create a US national geospatial metadata standard as a profile of ISO 19115, and to create version 3.0 of CSDGM as an implementation of that. This work has not yet been finalized.

.. seealso::
	* For more information on the FGDC standards, see http://www.fgdc.gov/metadata/geospatial-metadata-standards.

Dublin Core
-----------

Dublin Core Metadata Element Set

The Dublin Core Metadata Element Set (ISO Standard 15836) is a basic standard which can be easily understood and implemented and as such is one of the best known metadata standards. It consists of 15 elements which address the most basic descriptive, administrative and technical elements required to uniquely identify a digital resource. Most resource discovery metadata standards can be mapped to the Dublin Core Metadata Element Set, enabling basic federated searching across metadata created using a number of different standards, without detracting from richer metadata held elsewhere.

.. seealso::
	* See http://dublincore.org/ for more information on the Dublin Core Metadata Initiative.

EML
---

Ecological Markup Language

EML is a specification intended to support the description of any type of ecological information, including raw data, published research papers, rights information, and research protocols. At the highest level, EML models four primary entities: datasets, literature, software, and protocols. The WCODP technical community is working on developing a process for harvesting this format of metadata. 

.. seealso::
	* For more information about EML, see http://knb.ecoinformatics.org/software/eml/.

How to Create Metadata
======================

There are many different tools available to create geospatial metadata.  This knowledge base does not intend to cover all the tools available, but to provide information about some tools that can be used to create valid geospatial metadata that can be successfully harvested and displayed by the WCODP.

Following are some geospatial metadata tools that have been used successfully to author standards-compliant metadata for harvest by the WCODP:

====================================  =======  =====================================  =====================  =========
Tool                                  Type     Standards                              Requires               Optional
====================================  =======  =====================================  =====================  =========
`Esri ArcCatalog`_                    Desktop  FGDC CSDGM                             ArcGIS 10
`EPA Metadata Editor (EME) v.3.2`_    Desktop  FGDC CSDGM                             Windows OS             ArcGIS 10
`EPA Metadata Editor (EME) v.4.0`_    Desktop  ISO 19115, 19115-2                     Windows OS, MS Access  ArcGIS 10
`USGS Metadata Wizard`_               Desktop  FGDC CSDGM                             ArcGIS 10
`MERMAID`_                            Web      FGDC CSDGM, ISO 19115-2 (export only)  web browser, login
`ATRAC`_                              Web      ISO 19115-2                            web browser, login
`USGS Online Metadata Editor (OME)`_  Web      FGDC CSDGM                             web browser, login
====================================  =======  =====================================  =====================  =========

.. _Esri ArcCatalog: http://resources.arcgis.com/EN/HELP/MAIN/10.2/index.html#/A_quick_tour_of_creating_and_editing_metadata/003t00000007000000/
.. _EPA Metadata Editor (EME) v.3.2: https://edg.epa.gov/EME/download.html
.. _EPA Metadata Editor (EME) v.4.0: https://edg.epa.gov/EME/download.html
.. _USGS Metadata Wizard: http://www.sciencebase.gov/metadatawizard 
.. _MERMAID: http://www.ncddc.noaa.gov/metadata-standards/mermaid/
.. _ATRAC: https://www.ncdc.noaa.gov/atrac/index.html
.. _USGS Online Metadata Editor (OME): https://www1.usgs.gov/csas/ome/

Allison Bailey presented a Technical Training Webinar to West Coast Ocean Data Network members highlighting some of these metadata tools, tool capabilities, and tips and tricks for creating metadata that can be easily consumed by the WCODP.

Metadata Creation Tools Webinar Videos (July 2015):
	1. `Knowledge Base (3:27) <https://www.youtube.com/watch?v=ePqZnL7CtlQ>`_
	2. `EPA Metadata Editor (EME) v.4.0 - ISO 19115 (10:24) <https://www.youtube.com/watch?v=klhhIRJTiSk>`_
	3. `EPA Metadata Editor (EME) v.3.2 - FGDC CSDGM (6:41) <https://www.youtube.com/watch?v=LjqtCM2tBQk>`_
	4. `ATRAC Editor - ISO 19115-2 (8:51) <https://www.youtube.com/watch?v=T8bUR3EveB0>`_
	5. `Metadata Validation (3:02) <https://www.youtube.com/watch?v=7kGj3OdVUOA>`_
	6. `Questions and Wrap-up (11:21) <https://www.youtube.com/watch?v=qc5YImj9oVQ>`_

For ArcGIS users, the FGDC CSDGM Metadata Style (set in ArcCatalog options) can be used to create, edit, and export FGDC-compliant metadata.  However, the other ArcCatalog styles for producing ISO metadata (ISO 19139 and North American Profile of ISO 19115 2003) have not been extensively tested with the WCODP but have so far had mixed results.  

If the metadata are simple enough, some metadata creators prefer to use a text editor to edit the XML file directly.   This requires a bit of knowledge of both the metadata standard, tags, and XML.  The WCODP has an `ISO 19115 metadata template <http://network.westcoastoceans.org/wp-content/uploads/2015/09/template_xml_iso19115_new.zip>`_ that contributors can use.  

.. seealso::
	* https://www.fgdc.gov/metadata/geospatial-metadata-tools
	* http://service.ncddc.noaa.gov/cdn/metadata-training-materials/Intro-to-ISO/5_ToolsforISOMetadata.pdf
	* http://www.fgdc.gov/metadata/iso-metadata-editor-review
	* http://www.usgs.gov/datamanagement/describe/metadata.php#advanced-users


Validating Your Metadata
========================

Validating metadata content and format is an essential step to assure that your metadata will be useful to others as well as accessible to various portals and metadata catalogs such as the WCODP

In general, any FGDC CSDGM metadata that can be validated as FGDC-compliant, will successfully validate and display in the WCODP.  Because the ISO standards are more comprehensive, more flexible, and more recently adopted, successful validation of an ISO 19115 or ISO 19115-2 record via an external tool, does not always guarantee successful validation and display in the WCODP.  In these cases, some testing and iterations with the WCODP coordinator may be needed.

* USGS FGDC CSDGM Validator: http://geo-nsdi.er.usgs.gov/validation/
* NOAA/NGDC ISO 19115-2 validator: http://www.ngdc.noaa.gov/docucomp/recordServices 

How Is the Metadata Displayed?
==============================

The table below shows the translation between the metadata tags or Xpaths and where the content is displayed in the WCODP.

=============== ====================== ====================== ==================== ======================= ====================== ====================== ==========================                
Metadata Format Date Published         Creator                Publisher            Contact Name            Contact Email          Constraints            URL               
=============== ====================== ====================== ==================== ======================= ====================== ====================== ==========================                
`Dublin Core`_  DC:Date                DC:Creator             DC:Publisher         DC:Creator	                                  DC:Rights              NA		 
`FGDC CSDGM`_   idinfo>                idinfo>                distinfo>            idinfo>                 idinfo>                idinfo>                idinfo>
                citation>              citation>              distrib>             ptcontac>               ptcontac>              useconst               citation>
                citeinfo>              citeinfo>              cntinfo>             cntinfo>                cntinfo>                                      citeinfo>
                pubdate                origin                 cntorgp>             cntorgp>                cntemail                                      onlink																  
                                                              cntorg               cntper
  
`ISO 19115`_    identificationInfo>    identificationInfo>    contact>             identificationInfo>     contactInfo>           identificationInfo>
                MD_DataIdentification> MD_DataIdentification> CI_ResponsibleParty> MD_DataIdentification>  CI_Contact>            MD_DataIdentification> transferOptions>  
                citation>              pointOfContact>        organisationName>    pointOfContact>         address>               resourceConstraints>   MD_DigitalTransferOptions>
                CI_Citation>           CI_ResponsibleParty>   CharacterString      CI_ResponsibleParty>    CI_Address>            MD_LegalConstraints>   onLine>
                date>                  organisationName>                           individualName>         electronicMailAddress> otherConstraints>      CI_OnlineResource>
                CI_Date>               CharacterString                             CharacterString         CharacterString        CharacterString        linkage>
                date>                                                                                                                                    url
                DateTime
`ISO 19115-2`_  identificationInfo>    identificationInfo>    contact>             identificationInfo>     identificationInfo>    identificationInfo>
                MD_DataIdentification> MD_DataIdentification> CI_ResponsibleParty> MD_DataIdentification>  MD_DataIdentification> MD_DataIdentification> transferOptions>  
                citation>              gcitation>             organisationName>    citation>               citation>              resourceConstraints>   MD_DigitalTransferOptions>
                CI_Citation>           CI_Citation>           CharacterString      CI_Citation>            CI_Citation>           MD_LegalConstraints>   onLine>
                date>                  citedResponsibleParty>                      citedResponsibleParty>  citedResponsibleParty> useLimitation>         CI_OnlineResource>
                CI_Date>               CI_ResponsibleParty>                        CI_ResponsibleParty>    CI_ResponsibleParty>   CharacterString        linkage>
                gdate>                 organisationName>                           individualName          contactInfo>                                  url
                Date                   CharacterString                                                     CI_Contact>
                                                                                                           address>
                                                                                                           CI_Address>
                                                                                                           electronicMailAddress>
                                                                                                           CharacterString
=============== ====================== ====================== ==================== ======================= ====================== ====================== ==========================

For further detail, the JavaScript code used to extract the metadata content can be viewed here: https://github.com/Ecotrust/wc-data-registry/blob/master/site_raw/_includes/js/services/Metadata.js 

.. _Dublin Core: http://dublincore.org/
.. _FGDC CSDGM:  http://www.fgdc.gov/metadata/geospatial-metadata-standards
.. _ISO 19115: http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020	
.. _ISO 19115-2: http://www.iso.org/iso/catalogue_detail.htm?csnumber=39229																											  


Best Practices for Metadata
===========================

Content 
-------

It is very important to provide good information within your metadata to assist people in understanding what the data are about, how it was created, how they can use it, who to contact with questions, and how to access the data.  It may even be helpful to you in the future as the data author to remember key details about creation the data set.  It has been said, that "Metadata is a love note to the future."  

USGS has a very good resource clearly describing what type of information needs to go into the various elements of FGDC CSDGM standard.  

* Metadata in Plain Language: http://geology.usgs.gov/tools/metadata/tools/doc/ctc/

Most advice on content is applicable regardless of the metadata standard you use, but the location of the appropriate content may vary.  Focus on what you would like to know if you were interested in discovering and using someone else's data set.


Publishing Great Metadata 
-------------------------

Tanya Haddad gave an excellent presentation about publishing great metadata at the 2014 West Coast Ocean Data Network Meeting:  

`Publishing Great Metadata Presentation Slides <http://network.westcoastoceans.org/wp-content/uploads/2014/12/Haddad_WCGA_Successful_Data_Sharing-1.pdf>`_ 

Publishing Great Metadata Presentation Videos:
	1. `Introduction to Sharing (3:15) <https://www.youtube.com/watch?v=eXHrVy5Xhj4>`_
	2. `Metadata Overview (7:29) <https://www.youtube.com/watch?v=Id3nawOxXio>`_
	3. `Metadata Standards (10:43) <https://www.youtube.com/watch?v=DqyUopruWlU>`_
	4. `Metadata Tools (7:27) <https://www.youtube.com/watch?v=jS9yaZzmnME>`_
	5. `Best Practices (7:43) <https://www.youtube.com/watch?v=EHQqC2AexxM>`_
	6. `Sharing and Publishing (8:51) <https://www.youtube.com/watch?v=XKHeOlF1HUs>`_
	7. `Metadata Catalogs (5:16) <https://www.youtube.com/watch?v=5LgncgpFvXM>`_


Additional Resources
--------------------

Although both FGDC CSDGM and ISO-191xx standards are currently endorsed by the FGDC, federal agencies are being encouraged to transition from the older, CSDGM standard to ISO metadata as soon as they are able.   To share the most current information about experiences, strategies, and resources for implementing ISO metadata, FGDC hosts a monthly webinar and has a library of resources from past webinars.  

	* https://www.fgdc.gov/metadata/events/iso-geospatial-metadata-implementation-forum

NOAA, National Center for Environmental Information (NCEI), formerly National Coastal Data Development Center (NCDDC), conducts a variety of metadata trainings and has an excellent set of material from these courses:

	* http://www.ncddc.noaa.gov/metadata-standards/metadata-training/
	* ftp://ftp.ncddc.noaa.gov/pub/Metadata/Online_ISO_Training/

EPA has provides detailed and clear guidance for developing metadata.  Some of the information is focused on EPA-specific content, but the general concepts and best practices can be applied to any metadata effort.

	* https://edg.epa.gov/EME/pdfs/GenericMetadataGuide.pdf
	* https://edg.epa.gov/EME/resources.html
