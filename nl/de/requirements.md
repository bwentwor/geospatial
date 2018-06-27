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

#Servicevoraussetzungen
{: #requirements}


##Voraussetzungen für Nachrichten von MQTT-Geräten

* Von einem MQTT-Nachrichtenbroker müssen Gerätenachrichten im JSON-Format zu mindestens einem MQTT-Abschnitt bereitgestellt werden.
* Die Gerätenachrichten können eine beliebige Anzahl an Attributen enthalten, die folgenden drei Attribute müssen jedoch immer enthalten sein:
	* Ein Attribut, das das Gerät eindeutig kennzeichnet.
	* Ein Attribut, das den Breitengrad der aktuellen Position des Geräts angibt.
	* Ein Attribut, das den Längengrad der aktuellen Position des Geräts angibt.
* Zwei Nachrichtenmodi werden unterstützt:
	* Eine MQTT-Nachricht kann ein JSON-Objekt mit Informationen zu einem einzigen Gerät enthalten.
	* Eine MQTT-Nachricht kann ein JSON-Array mit Informationen zu mehreren Geräten enthalten.

##MQTT-Ereignisse und Konfiguration des Service

Die Anwendung abonniert MQTT-Nachrichten und steuert {{site.data.keyword.geospatialshort_Geospatial}} über die zugehörige [REST-API ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.ng.bluemix.net/apidocs/246). Über REST-API-Aufrufe stehen folgende Aktionen zur Verfügung:

* Konfigurieren und Starten des Service.
* Hinzufügen geografischer Regionen zur Überwachung und Entfernen geografischer Regionen aus der Überwachung.
* Abrufen von Informationen zum Servicestatus und zu den derzeit definierten Regionen.
* Stoppen Sie den Service.
* Erneutes Starten eines bereits konfigurierten Service.
