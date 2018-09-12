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

# Tutorial de introdução
{: #pushing_starter_app}

Expanda os limites de seu aplicativo. Aproveite as análises geoespaciais em tempo real para rastrear quando os dispositivos entram, saem ou são interrompidos em regiões definidas. Neste tutorial de introdução, você implementará o [aplicativo iniciador](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) e aprenderá rapidamente como usar o serviço do {{site.data.keyword.geospatialshort_Geospatial}}.
{:shortdesc}

## Antes de Começar
{: #prereqs}

Antes de implementar os aplicativos iniciadores, deve-se seguir estas etapas:

* Registre-se em uma conta do [{{site.data.keyword.Bluemix_notm}} ![Ícone de linkexterno](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/registration){:new_window}

* Crie uma instância do serviço {{site.data.keyword.geospatialshort_Geospatial}} em sua organização do {{site.data.keyword.Bluemix_notm}}. É possível criar a instância diretamente da página do [{{site.data.keyword.geospatialshort_Geospatial}} no catálogo de serviços do {{site.data.keyword.Bluemix_notm}}![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Instale a CLI do {{site.data.keyword.Bluemix_notm}} ](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Procedure
{: #procedure}

Para implementar o aplicativo iniciador no {{site.data.keyword.Bluemix_notm}}:

1. Crie um aplicativo no {{site.data.keyword.Bluemix_notm}}:

    a. No menu do {{site.data.keyword.Bluemix_notm}}, selecione **Apps Cloud Foundry** e clique em **Criar recurso**.

    b. Selecione o tempo de execução do {{site.data.keyword.sdk4node}} para seu aplicativo.
1. Acesse a página **Visão geral** do aplicativo, acessível por meio do painel do {{site.data.keyword.Bluemix_notm}}, conecte a instância de serviço do {{site.data.keyword.geospatialshort_Geospatial}} ao seu aplicativo e remonte o aplicativo.
1. Faça download do [aplicativo iniciador {{site.data.keyword.geospatialshort_Geospatial}}![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) e extraia os arquivos.

1. Acesse a página **Introdução** do aplicativo e siga as instruções nessa página para enviar por push seu aplicativo para o {{site.data.keyword.Bluemix_notm}}.

 **Nota:** é possível ignorar toda a etapa que menciona fazer mudanças em seu código. É possível executar o aplicativo iniciador transferido por download sem mudanças.

## O que fazer em seguida
{: #next}

* Acesse a página **Visão geral** do aplicativo para verificar se o aplicativo foi iniciado com sucesso.
* Ative seu aplicativo para vê-lo em seu navegador. É possível localizar a URL do aplicativo (ou "rotear") na página **Visão geral** do aplicativo. A página da web do aplicativo de amostra exibe informações
            sobre o status das chamadas da API REST no código do aplicativo e os eventos
            que o {{site.data.keyword.geospatialshort_Geospatial}}
            detecta.
