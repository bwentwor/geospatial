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

# Esercitazione introduttiva
{: #pushing_starter_app}

Espandi i limiti della tua applicazione. Avvaliti dell'analisi geospaziale in tempo reale per tenere traccia di quando i dispositivi accedono, escono o permangono in specifiche regioni. In questa esercitazione introduttiva, distribuirai l'applicazione starter e imparerai rapidamente come utilizzare il servizio {{site.data.keyword.geospatialshort_Geospatial}}:
{:shortdesc}

## Prima di iniziare
{: #prereqs}

Prima di distribuire le applicazioni starter, devi attenerti alla seguente procedura:

* Esegui la registrazione per un account [{{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.{DomainName}/registration){:new_window}
* Crea un'istanza del servizio {{site.data.keyword.geospatialshort_Geospatial}} nella tua organizzazione {{site.data.keyword.Bluemix_notm}}. Puoi creare l'istnza direttamente dalla pagina [{{site.data.keyword.geospatialshort_Geospatial}} nel catalogo servizi {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Installa la CLI {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Passo 1: crea un'applicazione e connettila al tuo servizio
{: #create_connect}

1. Crea un'applicazione in {{site.data.keyword.Bluemix_notm}}:

    a. Nel menu {{site.data.keyword.Bluemix_notm}}, seleziona **Applicazioni Cloud Foundry** e fai clic su **Crea risorsa**.

    b. Seleziona il runtime {{site.data.keyword.sdk4node}} per la tua applicazione.
    **Nota:** queste istruzioni funzionano anche per il contenitore tipo starter Node-RED.

      Ricordati il nome che dai alla tua applicazione; ti servirà più tardi.

## Passo 2: configura l'applicazione starter
{: #setup_app}

1. Scarica l'[applicazione starter {{site.data.keyword.geospatialshort_Geospatial}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip).

1. Rinomina la directory in modo che corrisponda al nome che hai dato alla tua applicazione in {{site.data.keyword.Bluemix_notm}}.
1. Connetti l'istanza del servizio {{site.data.keyword.geospatialshort_Geospatial}} alla tua applicazione e prepara di nuovo l'applicazione.

## Passo 3: distribuisci l'applicazione starter
{: #deploy_app}

1. Vai alla directory dell'applicazione starter:
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Accedi a {{site.data.keyword.Bluemix_notm}} e, quando richiesto, imposta
            la tua organizzazione di destinazione:
  <pre><code>bx login</code></pre>
  {:pre}

1. Distribuisci la tua applicazione a {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## Operazioni successive
{: #next}

* Passa alla pagina della panoramica della tua applicazione, accessibile dal dashboard {{site.data.keyword.Bluemix_notm}}, per verificare che
            l'applicazione venga avviata correttamente.
* Avvia l'applicazione per visualizzarla nel browser. Puoi trovare l'URL (o "rotta") della
            tua applicazione nella pagina della panoramica dell'applicazione. La pagina Web per l'applicazione di esempio
            visualizza informazioni sullo stato delle chiamate dell'API REST nel codice applicativo e degli eventi
            che {{site.data.keyword.geospatialshort_Geospatial}}
            rileva.
