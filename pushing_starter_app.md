---

copyright:
  years: 2015, 2017
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Getting started tutorial
{: #pushing_starter_app}

Expand the boundaries of your application. Leverage real-time geospatial analytics to track when devices enter, leave or hang out in defined regions. In this getting started tutorial you will deploy the starter application and quickly learn how to use the {{site.data.keyword.geospatialshort_Geospatial}} service:
{:shortdesc}

## Before you begin
{: #prereqs}

Before deploying the starter apps, you must follow these steps:

* Register for an [{{site.data.keyword.Bluemix_notm}} account ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/registration){:new_window}
* Create an instance of the {{site.data.keyword.geospatialshort_Geospatial}} service in your {{site.data.keyword.Bluemix_notm}} organization. You can create the instance directly from the [{{site.data.keyword.geospatialshort_Geospatial}} page in the {{site.data.keyword.Bluemix_notm}} Services Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Install the {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Step 1: Create app and connect app to your service
{: #create_connect}

1. Create an application in {{site.data.keyword.Bluemix_notm}}:

    a. In the {{site.data.keyword.Bluemix_notm}} menu, select **Cloud Foundry Apps** and click **Create resource**.

    b. Select the {{site.data.keyword.sdk4node}} runtime for your application.
    **Note:** These instructions also work for the Node-RED starter boilerplate.

      Remember the name that you give your application; you will need it later on.

## Step 2: Set up starter app
{: #setup_app}

1. Download the [{{site.data.keyword.geospatialshort_Geospatial}}  starter application ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip).

1. Rename the directory to match the name you gave your application in {{site.data.keyword.Bluemix_notm}}.
1. Connect the {{site.data.keyword.geospatialshort_Geospatial}} service instance to your application and restage the application.

## Step 3: Deploy starter app
{: #deploy_app}

1. Go to the starter application directory:
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Log in to {{site.data.keyword.Bluemix_notm}} and set your target organization when prompted:
  <pre><code>bx login</code></pre>
  {:pre}

1. Push your application to {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## What to do next
{: #next}

* Go to your application overview page, accessible from the {{site.data.keyword.Bluemix_notm}} dashboard, to verify that your application started successfully.
* Launch your application to see it in your browser. You can find your application's URL (or "route") on the application overview page. The web page for the sample application displays information about the status of the REST API calls in the application code and the events {{site.data.keyword.geospatialshort_Geospatial}} detects.
