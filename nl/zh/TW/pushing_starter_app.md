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

# 入門指導教學
{: #pushing_starter_app}

延展您應用程式的界限。利用即時地理空間分析來追蹤裝置何時進入、離開或停留在定義的地區。在此入門指導教學中，您將部署[入門範本應用程式](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/)，並快速瞭解如何使用 {{site.data.keyword.geospatialshort_Geospatial}} 服務。
{:shortdesc}

## 開始之前
{: #prereqs}

部署入門範本應用程式之前，您必須遵循下列步驟：

* 登錄 [{{site.data.keyword.Bluemix_notm}} 帳戶 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}/registration){:new_window}
* 在您的 {{site.data.keyword.Bluemix_notm}} 組織中建立 {{site.data.keyword.geospatialshort_Geospatial}} 服務的實例。您可以直接從 [{{site.data.keyword.Bluemix_notm}} 服務型錄的 {{site.data.keyword.geospatialshort_Geospatial}} 頁面 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window} 建立實例。  
* [安裝 {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)。

## 程序
{: #procedure}

若要在 {{site.data.keyword.Bluemix_notm}} 中部署入門範本應用程式，請執行下列動作：

1. 在 {{site.data.keyword.Bluemix_notm}} 中建立應用程式：

    a. 在 {{site.data.keyword.Bluemix_notm}} 功能表中，選取 **Cloud Foundry 應用程式**，然後按一下**建立資源**。

    b. 選取應用程式的 {{site.data.keyword.sdk4node}} 運行環境。
    
1. 移至您的應用程式**概觀**頁面（可從 {{site.data.keyword.Bluemix_notm}} 儀表板存取），將 {{site.data.keyword.geospatialshort_Geospatial}} 服務實例連接至應用程式，然後重新編譯打包應用程式。
1. 下載 [{{site.data.keyword.geospatialshort_Geospatial}}  入門範本應用程式 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip)，並擷取檔案。

1. 移至應用程式的**開始使用**頁面，並遵循該頁面上的指示，將應用程式推送至 {{site.data.keyword.Bluemix_notm}}。

 **附註：**您可以跳過提及變更程式碼的整個步驟。您可以執行下載的入門範本應用程式，而不需要進行任何變更。

## 下一步
{: #next}

* 移至您的應用程式**概觀**頁面，以驗證您的應用程式已順利啟動。
* 啟動應用程式以在瀏覽器中看到它。您可以在應用程式**概觀**頁面上找到應用程式的 URL（或「路徑」）。範例應用程式的網頁會顯示應用程式碼中 REST API 呼叫狀態的相關資訊，以及 {{site.data.keyword.geospatialshort_Geospatial}} 偵測到的事件。
