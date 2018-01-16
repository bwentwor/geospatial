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

# Lernprogramm zur Einführung
{: #pushing_starter_app}

Erweitern Sie die Grenzen Ihrer Anwendung. Nutzen Sie die Echtzeitanalyse von Geodaten, um zu verfolgen, wann Geräte in definierte Regionen kommen, wann sie sie verlassen und wie lange sie sich darin aufhalten. In diesem Lernprogramm zur Einführung stellen Sie die Starteranwendung bereit und lernen in kurzer Zeit, wie Sie den {{site.data.keyword.geospatialshort_Geospatial}}-Service einsetzen können:
{:shortdesc}

## Vorbereitung
{: #prereqs}

Führen Sie vor dem Bereitstellen der Starter-Apps diese Schritte aus:

* Nehmen Sie eine Registrierung für ein [{{site.data.keyword.Bluemix_notm}}-Konto ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link") vor. ](https://console.{DomainName}/registration){:new_window}
* Erstellen Sie eine Instanz des {{site.data.keyword.geospatialshort_Geospatial}}-Service in Ihrer {{site.data.keyword.Bluemix_notm}}-Organisation. Sie können die Instanz direkt auf der [{{site.data.keyword.geospatialshort_Geospatial}}-Seite im {{site.data.keyword.Bluemix_notm}}-Servicekatgalog ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window} erstellen.  
* [Installieren Sie die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Schritt 1: App erstellen und mit dem Service verbinden
{: #create_connect}

1. Erstellen Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}}:

    a. Wählen Sie im {{site.data.keyword.Bluemix_notm}}-Menü **Cloud Foundry-Apps** aus und klicken Sie auf **Ressource erstellen**.

    b. Wählen Sie die {{site.data.keyword.sdk4node}}-Laufzeit für Ihre Anwendung aus.
    **Hinweis:** Diese Anweisungen funktionieren auch für Node-RED-Starter-Boilerplates.

      Notieren Sie sich den Namen, den Sie der Anwendung geben; er wird später benötigt.

## Schritt 2: Starter-App einrichten
{: #setup_app}

1. Laden Sie die [{{site.data.keyword.geospatialshort_Geospatial}}-Starteranwendung ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip) herunter.

1. Benennen Sie das Verzeichnis so um, dass es dem Namen entspricht, den Sie Ihrer Anwendung in {{site.data.keyword.Bluemix_notm}} gegeben haben.
1. Stellen Sie eine Verbindung von der {{site.data.keyword.geospatialshort_Geospatial}}-Serviceinstanz zu Ihrer Anwendung her und führen Sie ein erneutes Staging für die Anwendung durch.

## Schritt 3: Starter-App bereitstellen
{: #deploy_app}

1. Rufen Sie das Verzeichnis der Starteranwendung auf:
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Melden Sie sich bei {{site.data.keyword.Bluemix_notm}} an und legen Sie die Zielorganisation fest, wenn Sie dazu aufgefordert werden:
  <pre><code>bx login</code></pre>
  {:pre}

1. Übertragen Sie die Anwendung mit einer Push-Operation an {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## Nächste Schritte
{: #next}

* Wechseln Sie zur Übersichtsseite für die Anwendung, die über das {{site.data.keyword.Bluemix_notm}}-Dashboard verfügbar ist, um zu überprüfen, ob die Anwendung erfolgreich gestartet wurde.
* Starten Sie die Anwendung, damit sie im Browser angezeigt wird. Sie finden die URL (oder "Route") der Anwendung auf der Übersichtsseite der Anwendung. Auf der Webseite für die Beispielanwendung werden Informationen zum Status der REST-API-Aufrufe im Anwendungscode und die Ereignisse angezeigt, die von {{site.data.keyword.geospatialshort_Geospatial}} erkannt wurden.
