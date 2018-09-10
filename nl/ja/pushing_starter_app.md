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

# 入門チュートリアル
{: #pushing_starter_app}

アプリケーションの境界を拡大します。 リアルタイム地理情報分析を活用して、定義された地域でデバイスがいつ開始されているか、終了されているか、または停止されているかを追跡します。 この入門チュートリアルでは、[スターター・アプリケーション](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/)をデプロイし、{{site.data.keyword.geospatialshort_Geospatial}} サービスの使用方法を素早く習得します。
{:shortdesc}

## 始めに
{: #prereqs}

スターター・アプリケーションをデプロイする前に、以下のステップを実行する必要があります。

* [{{site.data.keyword.Bluemix_notm}} アカウント ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}/registration){:new_window} に登録します。
* {{site.data.keyword.Bluemix_notm}} 組織に {{site.data.keyword.geospatialshort_Geospatial}} サービスのインスタンスを作成します。 このインスタンスは、{{site.data.keyword.Bluemix_notm}} サービス・カタログ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン"){:new_window} の [{{site.data.keyword.geospatialshort_Geospatial}} ページから直接作成できます。  
* [{{site.data.keyword.Bluemix_notm}} CLI をインストール](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)(https://console.{DomainName}/catalog/services/geospatial-analytics/)]します。

## 手順
{: #procedure}

{{site.data.keyword.Bluemix_notm}} でスターター・アプリケーションをデプロイするには、次のようにします。

1. 以下のようにして、{{site.data.keyword.Bluemix_notm}} にアプリケーションを作成します。

    a. {{site.data.keyword.Bluemix_notm}} メニューから**「Cloud Foundry アプリ」**を選択し、**「リソースの作成」**をクリックします。

    b. アプリケーション用の {{site.data.keyword.sdk4node}} ランタイムを選択します。
1. {{site.data.keyword.Bluemix_notm}} ダッシュボードからアクセスできる、アプリケーションの**「概要」**ページに移動し、{{site.data.keyword.geospatialshort_Geospatial}} サービス・インスタンスをアプリケーションに接続して、アプリケーションを再ステージします。
1. [{{site.data.keyword.geospatialshort_Geospatial}} スターター・アプリケーション ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) をダウンロードし、ファイルを解凍します。

1. アプリケーションの**「開始」**ページに移動し、そのページの指示に従ってアプリケーションを {{site.data.keyword.Bluemix_notm}} にプッシュします。

 **注:** コードの変更を説明した手順全体をスキップすることができます。ダウンロードしたスターター・アプリケーションは、変更せずに実行できます。

## 次に行うこと
{: #next}

* アプリケーションの**「概要」**ページに移動して、アプリケーションが正常に開始したことを確認します。
* アプリケーションを起動してブラウザーに表示します。 アプリケーションの URL (または「経路」) は、アプリケーションの**「概要」**ページにあります。サンプル・アプリケーションの Web ページには、
アプリケーション・コード中の REST API 呼び出しの状況についての情報、および {{site.data.keyword.geospatialshort_Geospatial}} が検出するイベントについての情報が表示されます。
