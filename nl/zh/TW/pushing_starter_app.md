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

# 入门教程
{: #pushing_starter_app}

扩展应用程序的边界。利用实时地理空间分析来跟踪设备何时进入、离开所定义的区域或在所定义的区域逗留。在此入门教程中，您将部署入门模板应用程序并快速了解如何使用 {{site.data.keyword.geospatialshort_Geospatial}} 服务：
{:shortdesc}

## 开始之前
{: #prereqs}

部署入门模板应用程序之前，您必须遵循以下步骤：

* 注册 [{{site.data.keyword.Bluemix_notm}} 帐户 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/registration){:new_window}
* 在 {{site.data.keyword.Bluemix_notm}} 组织中创建 {{site.data.keyword.geospatialshort_Geospatial}} 服务的实例。您可以直接通过 [{{site.data.keyword.Bluemix_notm}} 服务目录中的 {{site.data.keyword.geospatialshort_Geospatial}} 页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window} 创建实例。  
* [安装 {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)。

## 步骤 1：创建应用程序并将应用程序连接到服务
{: #create_connect}

1. 在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序：

    a. 在 {{site.data.keyword.Bluemix_notm}} 菜单中，选择 **Cloud Foundry 应用程序**并单击**创建资源**。

    b. 选择应用程序的 {{site.data.keyword.sdk4node}} 运行时。
    **注：**这些指示信息对 Node-RED 入门模板样本同样有效。

      请记住您为应用程序指定的名称，您稍后将需要该名称。

## 步骤 2：设置入门模板应用程序
{: #setup_app}

1. 下载 [{{site.data.keyword.geospatialshort_Geospatial}} 入门模板应用程序 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip)。

1. 重命名目录以匹配在 {{site.data.keyword.Bluemix_notm}} 中为应用程序指定的名称。
1. 将 {{site.data.keyword.geospatialshort_Geospatial}} 服务实例连接到应用程序并重新编译打包应用程序。

## 步骤 3：部署入门模板应用程序
{: #deploy_app}

1. 转至入门模板应用程序目录：
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. 登录到 {{site.data.keyword.Bluemix_notm}}，然后在提示时设置目标组织：
  <pre><code>bx login</code></pre>
  {:pre}

1. 将应用程序推送到 {{site.data.keyword.Bluemix_notm}}：
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## 接下来执行的操作
{: #next}

* 转至可从 {{site.data.keyword.Bluemix_notm}} 仪表板访问的应用程序概述页面，以验证应用程序已成功启动。
* 启动应用程序，以在浏览器中进行查看。可以在应用程序概述页面上找到应用程序的 URL（或“路径”）。样本应用程序的网页显示有关应用程序代码中 REST API 调用的状态和 {{site.data.keyword.geospatialshort_Geospatial}} 检测到的事件的信息。
