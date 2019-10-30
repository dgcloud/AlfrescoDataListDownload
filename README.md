AlfrescoDataListDownload
========================

Download as Spreadsheet support for Alfresco DataLists

This comes as two JARs:
 * datalist-download-share-1.0-SNAPSHOT.jar.amp - Share Module
 * datalist-download-repo-1.0-SNAPSHOT.jar - Repository (Alfresco) Module

The Share JAR provides a Dashlet which allows you to browse the DataLists
defined in your site, then trigger an export of the selected DataList
as one of:
 * Excel (xls)
 * Excel (xlsx)
 * CSV (csv)

The Repository JAR provides the support for exporting DataLists as
Spreadsheets. It builds upon the code in Alfresco, fixing various bugs
present in the webscripts there, and extending them to add additional
features and formats. (Attempts to get the fixes upstream into Alfresco
have sadly not worked so far...)

Dashlet
=======
The dashlet will show all datalists in the site, and give options to
download or view, along with changing the default. It looks something like:
![Screenshot](/screenshots/dashlet.png?raw=true)

Building
========
The current version works Alfresco Community 5.2.x. It ought to be fine for 6.0 and newer too, but
that hasn't been tested. 

To build, simply run "mvn clean install", and the two JARs will be produced in
the target directories. Install them to Share and the Alfresco Repository
wars as normal.

Installation
============
Once you have built both the JARs, install them to the simply copying them into the /modules/plataform and /modules/share folders.

The export is handled by a site dashlet. On the site where you would like
to export Data Lists, Customise the Dashboard and add the **DataList Export**
Dashlet to your site. No configuration is required, just pick the 
DataList you'd like to export and the format to export in!

License
=======
The code is available under the LGPL v3 License, which is the same license
that Alfresco itself is made available under.