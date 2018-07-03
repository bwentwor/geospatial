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

#Usando o aplicativo iniciador do {{site.data.keyword.geospatialshort_Geospatial}}
{: #starter_app}


O {{site.data.keyword.geospatialshort_Geospatial}} inclui um [aplicativo iniciador ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de ícone")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip) para você usar como modelo para experimento e fazer e enviar mudanças por push para o ambiente do {{site.data.keyword.Bluemix_short}}.
{:shortdesc}

O aplicativo iniciador usa mensagens de um broker do MQTT de demonstração para um conjunto simulado de
    dispositivos em movimento próximo a Las Vegas. O aplicativo gera informações sobre o status
    de suas operações e os eventos que ele detecta para uma única página da web.


Um visualizador que está vinculado a partir dessa página da web monitora dispositivos à medida que eles se movem de um local ao outro em um mapa. O
    visualizador não está vinculado ao aplicativo iniciador, portanto ele não é afetado pelas mudanças feitas na cópia do
    aplicativo iniciador. O código do aplicativo iniciador, que é gravado em
    Node.js, mostra como configurar e controlar o serviço {{site.data.keyword.geospatialshort_Geospatial}} por meio de sua API REST.


É possível executar o aplicativo
iniciador sem modificação. Se desejar experimentar mais com o serviço, também é possível modificar o código e enviar por push as mudanças de volta ao ambiente do  {{site.data.keyword.Bluemix_short}}. Confira [Desenvolver um aplicativo de monitoramento de localização em tempo real no {{site.data.keyword.Bluemix_short}} com o {{site.data.keyword.geospatialshort_Geospatial}} e o Node.js ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/) para saber como executar e ampliar o aplicativo iniciador.
