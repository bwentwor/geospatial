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

#使用服务仪表板
{: #service-dashboard}


您可以查看 {{site.data.keyword.geospatialshort_Geospatial}} 服务实例的状态，并从服务管理仪表板停止或重新启动它。要进入服务管理仪表板，请在 {{site.data.keyword.Bluemix_short}} 仪表板上选择 {{site.data.keyword.geospatialshort_Geospatial}} 服务。如果使用的是样本应用程序，并且服务实例达到事件限制且停止，您可以重新启动该服务。停止服务将除去事件限制。将继续接收事件，直到停止服务为止。服务管理仪表板还显示服务实例和统计信息的状态。
{:shortdesc}

##{{site.data.keyword.geospatialshort_Geospatial}} 区域检查

{{site.data.keyword.geospatialshort_Geospatial}} 会监视物联网中的移动设备。每个受监视设备都会发送设备消息，其中包含唯一标识以及设备的当前位置（经度和纬度）。首先，根据每个定义的地理区域的坐标来检查设备位置。然后，该服务在设备进入、退出或“聚集”在某个特定区域时生成事件。

区域检查是用于度量 {{site.data.keyword.geospatialshort_Geospatial}} 使用情况的单位。如果为区域指定了入口和/或出口检测，那么对于每条设备消息，会执行一次区域检查。如果为区域指定了聚集位置检测，那么对于每条设备消息，会执行一次区域检查。如果未定义区域，那么对于每条设备消息，会将一次区域检查算作一个区域。如果有 100 个区域定义了检查（入口、出口和聚集位置），那么单条设备消息将会生成 200 次区域检查。
