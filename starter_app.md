---

copyright:
  years: 2015, 2018
lastupdated: "2018-06-11"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

#Using the {{site.data.keyword.geospatialshort_Geospatial}} starter application
{: #starter_app}


{{site.data.keyword.geospatialshort_Geospatial}} includes a [starter application ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) for you to use as a template to experiment with, and make and push changes to the {{site.data.keyword.Bluemix_short}} environment.
{:shortdesc}

The starter application uses messages from a demonstration MQTT broker for a simulated set of devices on the move near Las Vegas. The application outputs information about the status of its operations and the events it detects to a simple web page.


A visualizer that is linked from that web page monitors devices as they move from location to location on a map. The visualizer is not linked to the starter application, so it is not affected by changes you make to your copy of the starter application. The starter application code, which is written in Node.js, shows you how to configure and control the {{site.data.keyword.geospatialshort_Geospatial}} service through its REST API.


You can run the starter application without modification. If you want to experiment further with the service, you can also modify the code and push your changes back to the {{site.data.keyword.Bluemix_short}} environment. Check out [Build a real-time location-monitoring application on {{site.data.keyword.Bluemix_short}} with {{site.data.keyword.geospatialshort_Geospatial}} and Node.js ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) to learn how to run and extend the starter application.
