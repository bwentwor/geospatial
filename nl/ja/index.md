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


#{{site.data.keyword.geospatialshort_Geospatial}} 概説
{: #gettingstarted}

{{site.data.keyword.geospatialfull}} を使用すると、{{site.data.keyword.Bluemix_notm}} のアプリケーションから移動中のデバイスをモニターできます。

{{site.data.keyword.geospatialshort_Geospatial}} サービスを開始する前に、デバイスの地理情報データを供給し、デバイスに関するイベント通知を受信するための、[MQTT ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://mqtt.org/){:new_window} メッセージ・ブローカーがあることを確認します。

スターター・アプリケーションは、シミュレートされたデバイスの情報を生成するメッセージ・ブローカーをポイントします。 {{site.data.keyword.geospatialshort_Geospatial}} スターター・アプリケーションについて詳しくは、[Build a real-time location-monitoring application on {{site.data.keyword.Bluemix_notm}} with {{site.data.keyword.geospatialshort_Geospatial}} and Node.js ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/)を参照してください。 MQTT デバイス・メッセージの要件および構成については、[サービス要件](/docs/services/geospatial/requirements.html){:new_window}を参照してください。

{{site.data.keyword.geospatialshort_Geospatial}} の GUI をビルドするための {{site.data.keyword.iot_short}} レシピの使用方法は、[Whip up a GUI for {{site.data.keyword.geospatialshort_Geospatial}} with this Watson IoT Recipe](https://www.ibm.com/blogs/bluemix/2017/03/whip-gui-geospatial-analytics-watson-iot-recipe/)に説明されています。

{{site.data.keyword.Bluemix_notm}} の
[Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform/){:new_window} サービス
は、MQTT メッセージ・ブローカーのニーズを満たすソリューションです。 {{site.data.keyword.geospatialshort_Geospatial}} を Internet of Things Platform サービスと共に使用する方法については、[Build a connected-car IoT app with {{site.data.keyword.geospatialshort_Geospatial}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://www.ibm.com/developerworks/mobile/library/mo-connectedcar-app/index.html){:new_window} を参照してください。
