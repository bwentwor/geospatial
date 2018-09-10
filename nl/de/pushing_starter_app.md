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

# Lernprogramm zur Einführung
{: #pushing_starter_app}

Erweitern Sie die Grenzen Ihrer Anwendung. Nutzen Sie die Echtzeitanalyse von Geodaten, um zu verfolgen, wann Geräte in definierte Regionen kommen, wann sie sie verlassen und wie lange sie sich darin aufhalten. In diesem Lernprogramm zur Einführung stellen Sie die [Starteranwendung](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) bereit und lernen in kurzer Zeit, wie Sie den {{site.data.keyword.geospatialshort_Geospatial}}-Service einsetzen können.
{:shortdesc}

## Vorbereitung
{: #prereqs}

Führen Sie vor dem Bereitstellen der Starter-Apps diese Schritte aus:

* Nehmen Sie eine Registrierung für ein [{{site.data.keyword.Bluemix_notm}}-Konto ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link") vor. ](https://console.{DomainName}/registration){:new_window}
* Erstellen Sie eine Instanz des {{site.data.keyword.geospatialshort_Geospatial}}-Service in Ihrer {{site.data.keyword.Bluemix_notm}}-Organisation. Sie können die Instanz direkt auf der [{{site.data.keyword.geospatialshort_Geospatial}}-Seite im {{site.data.keyword.Bluemix_notm}}-Servicekatgalog ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window} erstellen.  
* [Installieren Sie die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Vorgehensweise
{: #procedure}

Gehen Sie wie folgt vor, um eine Starteranwendung in {{site.data.keyword.Bluemix_notm}} bereitzustellen:

1. Erstellen Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}}:

    a. Wählen Sie im {{site.data.keyword.Bluemix_notm}}-Menü **Cloud Foundry-Apps** aus und klicken Sie auf **Ressource erstellen**.

    b. Wählen Sie die {{site.data.keyword.sdk4node}}-Laufzeit für Ihre Anwendung aus.
1. Rufen Sie die Seite **Übersicht** Ihrer Anwendung auf, die über das {{site.data.keyword.Bluemix_notm}}-Dashboard verfügbar ist, stellen Sie eine Verbindung von der {{site.data.keyword.geospatialshort_Geospatial}}-Serviceinstanz zu Ihrer Anwendung her und führen Sie ein erneutes Staging für die Anwendung durch.
1. Laden Sie die [{{site.data.keyword.geospatialshort_Geospatial}}-Starteranwendung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) herunter und extrahieren Sie die Dateien.

1. Rufen Sie die Seite **Einführung** der Anwendung auf und führen Sie die Anweisungen auf dieser Seite aus, um die Anwendung per Push-Operation in {{site.data.keyword.Bluemix_notm}} bereitzustellen.

 **Hinweis:** Sie können den gesamten Schritt, in dem die Codeänderungen beschrieben werden, überspringen. Sie können die heruntergeladene Starteranwendung ohne Änderungen ausführen.

## Nächste Schritte
{: #next}

* Rufen Sie die Seite **Übersicht** Ihrer Anwendung auf, um sicherzustellen, dass die Anwendung erfolgreich gestartet wurde.
* Starten Sie die Anwendung, damit sie im Browser angezeigt wird. Sie finden die URL (oder "Route") der Anwendung auf der Seite **Übersicht** der Anwendung. Auf der Webseite für die Beispielanwendung werden Informationen zum Status der REST-API-Aufrufe im Anwendungscode und die Ereignisse angezeigt, die von {{site.data.keyword.geospatialshort_Geospatial}} erkannt wurden.
