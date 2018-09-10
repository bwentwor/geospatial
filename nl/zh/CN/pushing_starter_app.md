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

# 入门教程
{: #pushing_starter_app}

扩展应用程序的边界。利用实时地理空间分析来跟踪设备何时进入、离开所定义的区域或在所定义的区域逗留。在此入门教程中，您将部署[入门模板应用程序](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/)并快速了解如何使用 {{site.data.keyword.geospatialshort_Geospatial}} 服务。
{:shortdesc}

## 开始之前
{: #prereqs}

部署入门模板应用程序之前，您必须遵循以下步骤：

* 注册 [{{site.data.keyword.Bluemix_notm}} 帐户 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/registration){:new_window}
* 在 {{site.data.keyword.Bluemix_notm}} 组织中创建 {{site.data.keyword.geospatialshort_Geospatial}} 服务的实例。您可以直接通过 [{{site.data.keyword.Bluemix_notm}} 服务目录中的 {{site.data.keyword.geospatialshort_Geospatial}} 页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window} 创建实例。  
* [安装 {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)。

## 过程
{: #procedure}

要在 {{site.data.keyword.Bluemix_notm}} 中部署入门模板应用程序：

1. 在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序：

    a. 在 {{site.data.keyword.Bluemix_notm}} 菜单中，选择 **Cloud Foundry 应用程序**并单击**创建资源**。

    b. 选择应用程序的 {{site.data.keyword.sdk4node}} 运行时。
    
1. 从 {{site.data.keyword.Bluemix_notm}} 仪表板转至应用程序**概述**页面，将 {{site.data.keyword.geospatialshort_Geospatial}} 服务实例连接到应用程序，然后重新编译打包应用程序。
1. 下载 [{{site.data.keyword.geospatialshort_Geospatial}} 入门模板应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip)，然后解压缩文件。

1. 转至应用程序的**入门**页面，按照该页面上的指示信息将应用程序推送到 {{site.data.keyword.Bluemix_notm}}。

 **注：**如果步骤中提到了代码更改，您可以跳过整个步骤。您可以直接运行所下载的入门模板应用程序，而不进行更改。

## 接下来执行的操作
{: #next}

* 转至应用程序**概述**页面，以验证应用程序是否已成功启动。
* 启动应用程序，以在浏览器中进行查看。在应用程序**概述**页面上，可以找到应用程序的 URL（或“路径”）。样本应用程序的网页显示有关应用程序代码中 REST API 调用的状态和 {{site.data.keyword.geospatialshort_Geospatial}} 检测到的事件的信息。
