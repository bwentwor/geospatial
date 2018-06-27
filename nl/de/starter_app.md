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

#{{site.data.keyword.geospatialshort_Geospatial}}-Starteranwendung verwenden
{: #starter_app}


{{site.data.keyword.geospatialshort_Geospatial}} enthält eine [Starteranwendung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip), die Sie als Vorlage zum Experimentieren sowie zum Durchführen von Änderungen und zum Übertragen von Änderungen an die {{site.data.keyword.Bluemix_short}}-Umgebung per Push-Operation verwenden können.
{:shortdesc}

Von der Starteranwendung werden Nachrichten eines MQTT-Demonstrationsbrokers für eine simulierte Anzahl an Geräten in der Umgebung von Las Vegas verwendet. Von der Anwendung werden Informationen zum Status der Operationen und zu den erkannten Ereignissen auf einer einfachen Webseite ausgegeben.


Mithilfe einer Visualisierungskomponente, die mit dieser Webseite verbunden ist, werden Geräte und ihre Bewegungen von Standort zu Standort auf der Karte überwacht. Da die Visualisierungskomponente nicht mit der Starteranwendung verbunden ist, wirken sich die von Ihnen an der Kopie der Starteranwendung vorgenommenen Änderungen nicht auf die Visualisierungskomponente aus. Anhand des Codes der Starteranwendung, die in Node.js geschrieben ist, können Sie erkennen, wie der {{site.data.keyword.geospatialshort_Geospatial}}-Service über die REST-API konfiguriert und gesteuert wird.


Sie können die Starteranwendung ohne Änderungen ausführen. Wenn Sie mit dem Service weitere Experimente ausführen möchten, können Sie auch den Code ändern und die Änderungen per Push-Operation wieder an die {{site.data.keyword.Bluemix_short}}-Umgebung übertragen. Lesen Sie [Anwendung zur Echtzeitstandortüberwachung in {{site.data.keyword.Bluemix_short}} mit {{site.data.keyword.geospatialshort_Geospatial}} und Node.js erstellen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/), um sich über das Ausführen und Erweitern der Starteranwendung zu informieren.
