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

# Tutoriel d'initiation 
{: #pushing_starter_app}

Repoussez les limites de votre application. Optimisez l'analyse géospatiale en temps réel pour effectuer le suivi des entrées, des sorties et des stagnations des périphériques dans des régions définies. Au cours de ce tutoriel d'initiation, vous allez déployer l'application de démarrage et apprendre rapidement à utiliser le service {{site.data.keyword.geospatialshort_Geospatial}} :
{:shortdesc}

## Avant de commencer 
{: #prereqs}

Avant de déployer les applications de démarrage, vous devez effectuer les opérations suivantes : 

* Vous enregistrer pour un compte [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](https://console.{DomainName}/registration){:new_window}
* Créer une instance du service {{site.data.keyword.geospatialshort_Geospatial}} dans votre organisation {{site.data.keyword.Bluemix_notm}}. Vous pouvez créer l'instance directement depuis la [page {{site.data.keyword.geospatialshort_Geospatial}} dans le catalogue des services {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Installer l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Etape 1 : Création d'une application et connexion de l'application à votre service 
{: #create_connect}

1. Créez une application dans {{site.data.keyword.Bluemix_notm}} :

    a. Dans le menu {{site.data.keyword.Bluemix_notm}}, sélectionnez **Applis Cloud Foundry** et cliquez sur **Créer une ressource**.

    b. Sélectionnez le contexte d'exécution {{site.data.keyword.sdk4node}} pour votre application.
    **Remarque :** ces instructions sont également valables pour le conteneur boilerplate de Starter Node-RED. 

      Mémorisez le nom que vous attribuez à votre application ; vous en aurez besoin ultérieurement.

## Etape 2 : Configuration de l'application de démarrage 
{: #setup_app}

1. Téléchargez l'[application de démarrage {{site.data.keyword.geospatialshort_Geospatial}} ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip).

1. Renommez le répertoire avec le nom que vous avez attribué à votre application dans {{site.data.keyword.Bluemix_notm}}.
1. Connectez l'instance de service {{site.data.keyword.geospatialshort_Geospatial}} à votre application et reconstituez l'application en préproduction. 

## Etape 3 : Déploiement de l'application de démarrage 
{: #deploy_app}

1. Accédez au répertoire de l'application de démarrage : 
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Connectez-vous à {{site.data.keyword.Bluemix_notm}} et définissez votre organisation cible lorsque vous y
êtes invité :
  <pre><code>bx login</code></pre>
  {:pre}

1. Envoyez votre application par commande push dans {{site.data.keyword.Bluemix_notm}} :
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## Etape suivante
{: #next}

* Consultez la page de présentation de votre application, accessible depuis le tableau de bord {{site.data.keyword.Bluemix_notm}} pour vérifier que l'application a démarré.
* Lancez votre application pour l'afficher dans votre navigateur. Vous trouverez l'adresse URL (ou "route") de votre application dans la page de présentation de l'application. La page Web du modèle d'application affiche des informations sur le statut des appels d'API REST dans le code de l'application et les événements que {{site.data.keyword.geospatialshort_Geospatial}} détecte.
