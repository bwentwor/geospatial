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

# Tutorial de introdução
{: #pushing_starter_app}

Expanda os limites de seu aplicativo. Aproveite as análises geoespaciais em tempo real para rastrear quando os dispositivos entram, saem ou são interrompidos em regiões definidas. Neste tutorial de introdução, você implementará o aplicativo iniciador e aprenderá rapidamente a usar o serviço {{site.data.keyword.geospatialshort_Geospatial}}:{:shortdesc}

## Antes de Começar
{: #prereqs}

Antes de implementar os aplicativos iniciadores, deve-se seguir estas etapas:

* Registre-se em uma conta do [{{site.data.keyword.Bluemix_notm}} ![Ícone de linkexterno](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/registration){:new_window}

* Crie uma instância do serviço {{site.data.keyword.geospatialshort_Geospatial}} em sua organização do {{site.data.keyword.Bluemix_notm}}. É possível criar a instância diretamente da página do [{{site.data.keyword.geospatialshort_Geospatial}} no catálogo de serviços do {{site.data.keyword.Bluemix_notm}}![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}.  
* [Instale a CLI do {{site.data.keyword.Bluemix_notm}} ](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## Etapa 1: Criar e conectar aplicativo ao seu serviço
{: #create_connect}

1. Crie um aplicativo no {{site.data.keyword.Bluemix_notm}}:

    a. No menu do {{site.data.keyword.Bluemix_notm}}, selecione **Apps Cloud Foundry** e clique em **Criar recurso**.

    b. Selecione o tempo de execução do {{site.data.keyword.sdk4node}} para seu aplicativo.
    **Observação:** essas instruções também funcionam para o texto padrão do iniciador do Node-RED.

      Lembre-se do nome que você deu ao aplicativo; você precisará dele posteriormente.

## Etapa 2: Configurar o aplicativo iniciador
{: #setup_app}

1. Faça download do [ aplicativo iniciador {{site.data.keyword.geospatialshort_Geospatial}}  ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip).

1. Renomeie o diretório para corresponder ao nome que você deu ao aplicativo no {{site.data.keyword.Bluemix_notm}}.
1. Conecte a instância de serviço do {{site.data.keyword.geospatialshort_Geospatial}} ao seu aplicativo e remonte o aplicativo.

## Etapa 3: Implementar o aplicativo iniciador
{: #deploy_app}

1. Acesse o diretório do aplicativo iniciador:
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. Efetue login no {{site.data.keyword.Bluemix_notm}} e configure sua organização de destino quando solicitada:
  <pre><code>bx login</code></pre>
  {:pre}

1. Envie seu aplicativo por push para o {{site.data.keyword.Bluemix_notm}}:
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## O que fazer em seguida
{: #next}

* Acesse a página de visão geral do aplicativo, acessível a partir do painel do {{site.data.keyword.Bluemix_notm}}, para verificar se
            seu aplicativo foi iniciado com êxito.
* Ative seu aplicativo para vê-lo em seu navegador. É possível localizar (ou "rotear") a URL do aplicativo
            na página de visão geral do aplicativo. A página da web do aplicativo de amostra exibe informações
            sobre o status das chamadas da API REST no código do aplicativo e os eventos
            que o {{site.data.keyword.geospatialshort_Geospatial}}
            detecta.
