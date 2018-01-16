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

# 入門チュートリアル
{: #pushing_starter_app}

アプリケーションの境界を拡大します。リアルタイム地理情報分析を活用して、定義された地域でデバイスがいつ開始されているか、終了されているか、または停止されているかを追跡します。この入門チュートリアルでは、スターター・アプリケーションをデプロイし、{{site.data.keyword.geospatialshort_Geospatial}} サービスの使用方法を素早く習得します。
{:shortdesc}

## 始めに
{: #prereqs}

スターター・アプリケーションをデプロイする前に、以下のステップを実行する必要があります。

* [{{site.data.keyword.Bluemix_notm}} アカウント ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}/registration){:new_window} に登録します。
* {{site.data.keyword.Bluemix_notm}} 組織に {{site.data.keyword.geospatialshort_Geospatial}} サービスのインスタンスを作成します。このインスタンスは、{{site.data.keyword.Bluemix_notm}} サービス・カタログ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン"){:new_window} の [{{site.data.keyword.geospatialshort_Geospatial}} ページから直接作成できます。  
* [{{site.data.keyword.Bluemix_notm}} CLI をインストール](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install)(https://console.{DomainName}/catalog/services/geospatial-analytics/)]します。

## ステップ 1: アプリケーションを作成し、アプリケーションをサービスに接続する
{: #create_connect}

1. 以下のようにして、{{site.data.keyword.Bluemix_notm}} にアプリケーションを作成します。

    a. {{site.data.keyword.Bluemix_notm}} メニューから**「Cloud Foundry アプリ」**を選択し、**「リソースの作成」**をクリックします。

    b. アプリケーション用の {{site.data.keyword.sdk4node}} ランタイムを選択します。
    **注:** これらの指示は、Node-RED スターター・ボイラープレートでも機能します。

      アプリケーションに付ける名前を覚えておいてください。後で必要になります。

## ステップ 2: スターター・アプリケーションをセットアップする
{: #setup_app}

1. [{{site.data.keyword.geospatialshort_Geospatial}} スターター・アプリケーション ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip) をダウンロードします。

1. {{site.data.keyword.Bluemix_notm}}  内のアプリケーションに指定した名前に一致するように、ディレクトリーの名前を変更します。
1. {{site.data.keyword.geospatialshort_Geospatial}} サービス・インスタンスをアプリケーションに接続し、アプリケーションを再ステージします。

## ステップ 3: スターター・アプリケーションをデプロイする
{: #deploy_app}

1. 以下を実行して、スターター・アプリケーションのディレクトリーに移動します。
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. 以下を実行して {{site.data.keyword.Bluemix_notm}} にログインし、プロンプトが出されたらターゲット組織を設定します。
  <pre><code>bx login</code></pre>
  {:pre}

1. 以下を実行して、アプリケーションを {{site.data.keyword.Bluemix_notm}} にプッシュします。
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## 次に行うこと
{: #next}

* アプリケーションが正常に開始したことを検証するため、{{site.data.keyword.Bluemix_notm}} ダッシュボードからアクセス可能なアプリケーション概要ページに移動します。
* アプリケーションを起動してブラウザーに表示します。 アプリケーションの URL (または「経路」) は、アプリケーション概要ページにあります。 サンプル・アプリケーションの Web ページには、
アプリケーション・コード中の REST API 呼び出しの状況についての情報、および {{site.data.keyword.geospatialshort_Geospatial}} が検出するイベントについての情報が表示されます。
