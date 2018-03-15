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

#서비스 관리 대시보드
{: #service-dashboard}


서비스 관리 대시보드에서 {{site.data.keyword.geospatialshort_Geospatial}} 서비스 인스턴스의 상태를 보고 해당 인스턴스를 중지하거나 다시 시작할 수 있습니다. {{site.data.keyword.Bluemix_short}} 대시보드에서 {{site.data.keyword.geospatialshort_Geospatial}} 서비스를 선택하여 서비스 관리 대시보드에 액세스할 수 있습니다. 샘플 애플리케이션을 사용 중인 경우 서비스 인스턴스가 이벤트 한계에 도달하여 중지되면 서비스를 다시 시작할 수 있습니다. 서비스를 중지하면 이벤트 한계가 제거됩니다. 서비스를 중지하기 전까지는 계속해서 이벤트를 수신합니다. 서비스 관리 대시보드에는 서비스 인스턴스 상태 및 통계도 표시됩니다.
{:shortdesc}

##{{site.data.keyword.geospatialshort_Geospatial}} 지역 확인

{{site.data.keyword.geospatialshort_Geospatial}}는 IoT(Internet of Things)를 통해 이동 중인 디바이스를 모니터링합니다. 모니터링된 각 디바이스는 위도와 경도로 구성된 현재 위치와 함께 고유한 ID를 포함하는 디바이스 메시지를 전송합니다. 디바이스 위치는 정의된 각 지리적 영역의 좌표에 대해 확인됩니다. 그런 다음 서비스는 디바이스가 특정 지역에 들어가거나, 나오거나, 머무를 때 이벤트를 생성합니다.

지역 확인은 {{site.data.keyword.geospatialshort_Geospatial}}의 사용량을 측정하는 단위로 사용됩니다. 지역에 대해 들어감, 나감 또는 들어감과 나감 둘 다에 대해 발견이 지정된 경우, 각 디바이스 메시지는 한 개 지역 확인을 수행합니다. 각 디바이스 메시지의 경우 해당 지역에 행아웃 발견이 지정된 경우 한 개 지역 확인이 수행됩니다. 지역이 정의되지 않은 경우 각 디바이스 메시지의 경우 지역이 하나인 것처럼 한 개 지역 확인이 계산됩니다. 즉 100개 지역에 들어감, 나감 및 행아웃이 정의되어 있는 경우 단일 디바이스 메시지는 200개 지역 확인을 생성하게 됨을 의미합니다.
