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

# Esercitazione introduttiva
{: #pushing_starter_app}

Espandi i limiti della tua applicazione. Avvaliti dell'analisi geospaziale in tempo reale per tenere traccia di quando i dispositivi accedono, escono o permangono in specifiche regioni. In questa esercitazione introduttiva, distribuirai l'[applicazione starter](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) e imparerai rapidamente come utilizzare il servizio {{site.data.keyword.geospatialshort_Geospatial}}.
{:shortdesc}

## Prima di iniziare
{: #prereqs}

Prima di distribuire le applicazioni starter, devi attenerti alla seguente procedura:

* Esegui la registrazione per un account [{{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.{DomainName}/registration){:new_window}
* Crea un'istanza del servizio {{site.data.keyword.geospatialshort_Geospatial}} nella tua organizzazione {{site.data.keyword.Bluemix_notm}}. Puoi creare l'istanza direttamente dalla pagina [{{site.data.keyword.geospatialshort_Geospatial}} nel catalogo servizi {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Installa la CLI {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Procedura
{: #procedure}

Per distribuire l'applicazione starter in {{site.data.keyword.Bluemix_notm}}:

1. Crea un'applicazione in {{site.data.keyword.Bluemix_notm}}:

    a. Nel menu {{site.data.keyword.Bluemix_notm}}, seleziona **Applicazioni Cloud Foundry** e fai clic su **Crea risorsa**.

    b. Seleziona il runtime {{site.data.keyword.sdk4node}} per la tua applicazione.
1. Vai alla pagina **Panoramica** dell'applicazione, accessibile dal dashboard {{site.data.keyword.Bluemix_notm}}, connetti l'istanza del servizio {{site.data.keyword.geospatialshort_Geospatial}} alla tua applicazione e prepara di nuovo l'applicazione.
1. Scarica l'[applicazione starter {{site.data.keyword.geospatialshort_Geospatial}}![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) ed estrai i file.

1. Vai alla pagina **Introduzione** dell'applicazione a attieniti alle istruzioni contenute in tale pagina per eseguire il push della tua applicazione a {{site.data.keyword.Bluemix_notm}}.

 **Nota:** puoi tralasciare l'intero passo che menziona l'apporto di modifiche al tuo codice. Puoi eseguire l'applicazione starter che hai scaricato senza alcuna modifica.

## Operazioni successive
{: #next}

* Vai alla pagina **Panoramica** della tua applicazione per verificare che sia stata avviata correttamente.
* Avvia l'applicazione per visualizzarla nel browser. Puoi trovare l'URL dell'applicazione (o "rotta") nella pagina **Panoramica** dell'applicazione. La pagina Web per l'applicazione di esempio
            visualizza informazioni sullo stato delle chiamate dell'API REST nel codice applicativo e degli eventi
            che {{site.data.keyword.geospatialshort_Geospatial}}
            rileva.
