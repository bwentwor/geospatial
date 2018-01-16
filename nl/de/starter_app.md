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

#{{site.data.keyword.geospatialshort_Geospatial}}-Starteranwendung verwenden
{: #starter_app}


{{site.data.keyword.geospatialshort_Geospatial}} enthält eine [Starteranwendung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip), die Sie als Vorlage zum Experimentieren sowie zum Durchführen von Änderungen und zum Übertragen von Änderungen an die {{site.data.keyword.Bluemix_short}}-Umgebung per Push-Operation verwenden können.
{:shortdesc}

Von der Starteranwendung werden Nachrichten eines MQTT-Demonstrationsbrokers für eine simulierte Anzahl an Geräten in der Umgebung von Las Vegas verwendet. Von der Anwendung werden Informationen zum Status der Operationen und zu den erkannten Ereignissen auf einer einfachen Webseite ausgegeben.


Mithilfe einer Visualisierungskomponente, die mit dieser Webseite verbunden ist, werden Geräte und ihre Bewegungen von Standort zu Standort auf der Karte überwacht. Da die Visualisierungskomponente nicht mit der Starteranwendung verbunden ist, wirken sich die von Ihnen an der Kopie der Starteranwendung vorgenommenen Änderungen nicht auf die Visualisierungskomponente aus. Anhand des Codes der Starteranwendung, die in Node.js geschrieben ist, können Sie erkennen, wie der {{site.data.keyword.geospatialshort_Geospatial}}-Service über die REST-API konfiguriert und gesteuert wird.


Sie können die Starteranwendung ohne Änderungen ausführen. Wenn Sie mit dem Service noch weitere Experimente ausführen möchten, können Sie auch [den Code ändern](/docs/services/geospatial/modifying_starter_app.html) und die Änderungen mit einer Push-Operation wieder in die {{site.data.keyword.Bluemix_short}}-Umgebung übertragen. [Mobile Geräte mit dem {{site.data.keyword.geospatialshort_Geospatial}}-Service überwachen ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/developerworks/library/mo-monitordevices-app/index.html) enthält Details zur Ausführung und Erweiterung der {{site.data.keyword.geospatialshort_Geospatial}}-Starteranwendung.
