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

# Guía de aprendizaje de iniciación
{: #pushing_starter_app}

Expanda los límites de su aplicación. Aproveche la analítica geoespacial en tiempo real para realizar el seguimiento de cuándo entran, salen o se mantienen los dispositivos en regiones definidas. En esta guía de aprendizaje de iniciación desplegará la aplicación de inicio y aprenderá rápidamente a utilizar el servicio de {{site.data.keyword.geospatialshort_Geospatial}}:
{:shortdesc}

## Antes de empezar
{: #prereqs}

Antes de desplegar las apps de inicio, debe seguir estos pasos:

* Regístrese para una cuenta de [{{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}/registration){:new_window}
* Cree una instancia del servicio de {{site.data.keyword.geospatialshort_Geospatial}} en la organización de {{site.data.keyword.Bluemix_notm}}. Puede crear la instancia directamente desde la página de [{{site.data.keyword.geospatialshort_Geospatial}} en el Catálogo de servicios de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Instale la CLI de {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Paso 1: Crear la app y conectarla al servicio
{: #create_connect}

1. Cree una aplicación en {{site.data.keyword.Bluemix_notm}}:

    a. En el menú de {{site.data.keyword.Bluemix_notm}}, seleccione **Apps de Cloud Foundry** y pulse **Crear recurso**.

    b. Seleccione el tiempo de ejecución de {{site.data.keyword.sdk4node}} para su aplicación.
    **Nota:** Estas instrucciones también funcionan para el contenedor modelo de iniciador Node-RED.

      Recuerde el nombre que asigna a la aplicación; lo necesitará más adelante.

## Paso 2: Configurar la app de inicio
{: #setup_app}

1. Descargue la aplicación de inicio [{{site.data.keyword.geospatialshort_Geospatial}}  ![Icono de enlace externo](../../icons/launch-glyph.svg "Icono de enlace externo")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip).

1. Cambie el nombre del directorio para que coincida con el nombre asignado a la aplicación en {{site.data.keyword.Bluemix_notm}}.
1. Conecte la instancia de servicio de {{site.data.keyword.geospatialshort_Geospatial}} a la aplicación y vuelva a transferir la aplicación.

## Paso 3: Desplegar la app de inicio
{: #deploy_app}

1. Vaya al directorio de la aplicación de inicio:
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Inicie la sesión en {{site.data.keyword.Bluemix_notm}} y establezca la organización de destino cuando se le solicite:
  <pre><code>bx login</code></pre>
  {:pre}

1. Envíe por push la aplicación a {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## Qué hacer a continuación
{: #next}

* Vaya a la página de visión general de la aplicación, a la que puede acceder desde el panel de control de {{site.data.keyword.Bluemix_notm}}, para comprobar que la aplicación se ha iniciado correctamente.
* Inicie la aplicación para verla en el navegador. Encontrará el URL de la aplicación (o "route") en la página de visión general de la aplicación. La página web de la aplicación de ejemplo muestra información sobre el estado de las llamadas a la API REST en el código de la aplicación y los sucesos que {{site.data.keyword.geospatialshort_Geospatial}} detecta.
