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

# Tutoriel d'initiation
{: #pushing_starter_app}

Repoussez les limites de votre application. Optimisez l'analyse géospatiale en temps réel pour effectuer le suivi des entrées, des sorties et des stagnations des périphériques dans des régions définies. Au cours de ce tutoriel d'initiation, vous allez déployer l'[application de démarrage](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) et apprendre rapidement à utiliser le service {{site.data.keyword.geospatialshort_Geospatial}}.
{:shortdesc}

## Avant de commencer
{: #prereqs}

Avant de déployer les applications de démarrage, vous devez effectuer les opérations suivantes :

* Vous enregistrer pour un compte [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}/registration){:new_window}
* Créer une instance du service {{site.data.keyword.geospatialshort_Geospatial}} dans votre organisation {{site.data.keyword.Bluemix_notm}}. Vous pouvez créer l'instance directement depuis la [page {{site.data.keyword.geospatialshort_Geospatial}} dans le catalogue des services {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Installer l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Procédure
{: #procedure}

Pour déployer l'application de démarrage dans {{site.data.keyword.Bluemix_notm}} :

1. Créez une application dans {{site.data.keyword.Bluemix_notm}} :

    a. Dans le menu {{site.data.keyword.Bluemix_notm}}, sélectionnez **Applis Cloud Foundry** et cliquez sur **Créer une ressource**.

    b. Sélectionnez le contexte d'exécution {{site.data.keyword.sdk4node}} pour votre application.
1. Accédez à la page **Vue d'ensemble**, accessible depuis le tableau de bord {{site.data.keyword.Bluemix_notm}}, connectez l'instance de service {{site.data.keyword.geospatialshort_Geospatial}} à votre application et reconstituez l'application.
1. Téléchargez l'[{{site.data.keyword.geospatialshort_Geospatial}} ![Icône de lien externe](../../icons/launch-glyph.svg "Icône de lien externe")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) et extrayez les fichiers.

1. Accédez à la page **Initiation** de l'application et suivez les instructions indiquées pour envoyer votre application à {{site.data.keyword.Bluemix_notm}}.

 **Remarque :** vous pouvez ignorer totalement l'étape concernant la modification de votre code.  L'application de démarrage que vous avez téléchargée est exécutable sans aucune modification.

## Etape suivante
{: #next}

* Accédez à la page **Vue d'ensemble** de votre application pour vérifier que celle-ci a démarré.
* Lancez votre application pour l'afficher dans votre navigateur. Vous trouverez l'adresse URL (ou "route") de votre application dans la page **Vue d'ensemble** de l'application. La page Web du modèle d'application affiche des informations sur le statut des appels d'API REST dans le code de l'application et les événements que {{site.data.keyword.geospatialshort_Geospatial}} détecte.
