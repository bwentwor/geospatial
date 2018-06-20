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

# Getting started tutorial
{: #pushing_starter_app}

Expand the boundaries of your application. Leverage real-time geospatial analytics to track when devices enter, leave or hang out in defined regions. In this getting started tutorial you will deploy the [starter application](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) and quickly learn how to use the {{site.data.keyword.geospatialshort_Geospatial}} service.
{:shortdesc}

## Before you begin
{: #prereqs}

Before deploying the starter apps, you must follow these steps:

* Register for an [{{site.data.keyword.Bluemix_notm}} account ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/registration){:new_window}
* Create an instance of the {{site.data.keyword.geospatialshort_Geospatial}} service in your {{site.data.keyword.Bluemix_notm}} organization. You can create the instance directly from the [{{site.data.keyword.geospatialshort_Geospatial}} page in the {{site.data.keyword.Bluemix_notm}} Services Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Install the {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Procedure
{: #procedure}

To deploy the starter application in {{site.data.keyword.Bluemix_notm}}:

1. Create an application in {{site.data.keyword.Bluemix_notm}}:

    a. In the {{site.data.keyword.Bluemix_notm}} menu, select **Cloud Foundry Apps** and click **Create resource**.

    b. Select the {{site.data.keyword.sdk4node}} runtime for your application.
1. Go to your application **Overview** page, accessible from the {{site.data.keyword.Bluemix_notm}} dashboard, connect the {{site.data.keyword.geospatialshort_Geospatial}} service instance to your application, and restage the application.
1. Download the [{{site.data.keyword.geospatialshort_Geospatial}}  starter application ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) and extract the files.

1. Go to the **Getting started** page of the application and follow the instructions on that page to push your application to {{site.data.keyword.Bluemix_notm}}.

 **Note:** You can skip the entire step that mentions making changes to your code.  You can run the starter application that you downloaded without any changes.

## What to do next
{: #next}

* Go to your application **Overview** page to verify that your application started successfully.
* Launch your application to see it in your browser. You can find your application's URL (or "route") on the application **Overview** page. The web page for the sample application displays information about the status of the REST API calls in the application code and the events {{site.data.keyword.geospatialshort_Geospatial}} detects.
