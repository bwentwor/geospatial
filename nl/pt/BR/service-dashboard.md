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

#Usando o painel de serviço
{: #service-dashboard}


É possível ver o status de sua instância de serviço do {{site.data.keyword.geospatialshort_Geospatial}} e parar ou reiniciá-la
a partir do painel de administração de serviços. Para obter o painel de administração de serviço, selecione o serviço do {{site.data.keyword.geospatialshort_Geospatial}} em seu painel do {{site.data.keyword.Bluemix_short}}. Se você estiver usando
o aplicativo de amostra e sua instância de serviço atingir o limite de eventos e for interrompida, será possível reiniciar o
serviço. Parar o serviço remove o limite de eventos. Ele continua a receber eventos até que você pare o serviço. O painel de administração de serviços exibe também o status de sua instância de serviço e
as estatísticas.
{:shortdesc}

##Verificações de
região
do {{site.data.keyword.geospatialshort_Geospatial}}

O
{{site.data.keyword.geospatialshort_Geospatial}}
monitora os dispositivos em movimentação da Internet das Coisas. Cada dispositivo monitorado envia mensagens de dispositivo que contêm um identificador exclusivo junto com sua posição atual, que inclui a latitude e a longitude. A posição do dispositivo é verificada com
relação às coordenadas de cada região geográfica definida. O serviço produz eventos quando os dispositivos entram, saem ou estão "em hangout" em uma região específica.

Uma Verificação de região é usada como uma unidade para medir o uso do {{site.data.keyword.geospatialshort_Geospatial}}. Para
cada mensagem do dispositivo, uma verificação de região é realizada
se entrada, saída ou detecção de ambos for especificada para a
região. Para cada mensagem do dispositivo, uma verificação de região
é realizada, se a detecção de hangout foi especificada para a
região. Se nenhuma região estiver definida, para cada mensagem do dispositivo, uma verificação de região será contada como uma região. Se você tiver 100 regiões definidas para verificação, entrada, saída e desligamento, uma única mensagem do dispositivo produzirá 200 verificações de região.
