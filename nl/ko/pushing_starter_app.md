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

# 시작하기 튜토리얼
{: #pushing_starter_app}

애플리케이션의 경계를 펼치십시오. 실시간 지리공간 분석을 활용하여 정의된 지역으로 디바이스가 들어가거나, 나오거나, 머무는 시간을 추적하십시오. 이 시작하기 튜토리얼에서는 [스타터 애플리케이션](https://developer.ibm.com/streamsdev/docs/build-real-time-location-monitoring-application-ibm-cloud-geospatial-analytics-node-js/)을 배치하고 {{site.data.keyword.geospatialshort_Geospatial}} 서비스의 사용 방법을 빠르게 학습합니다.
{:shortdesc}

## 시작하기 전에
{: #prereqs}

스타터 앱을 배치하기 전에 다음 단계를 따르십시오.

* [{{site.data.keyword.Bluemix_notm}} 계정 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/registration){:new_window}을 등록하십시오.
* {{site.data.keyword.geospatialshort_Geospatial}} 서비스의 인스턴스를 {{site.data.keyword.Bluemix_notm}} 조직에 작성하십시오. [{{site.data.keyword.Bluemix_notm}} 서비스 카탈로그의 {{site.data.keyword.geospatialshort_Geospatial}} 페이지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}에서 인스턴스를 직접 작성할 수 있습니다.  
* [{{site.data.keyword.Bluemix_notm}} CLI를 설치하십시오](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## 프로시저
{: #procedure}

{{site.data.keyword.Bluemix_notm}}에 스타터 애플리케이션을 배치하려면 다음을 수행하십시오. 

1. {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 작성하십시오.

    a. {{site.data.keyword.Bluemix_notm}} 메뉴에서 **Cloud Foundry 앱**을 선택하고 **리소스 작성**을 클릭하십시오.

    b. 애플리케이션에 대한 {{site.data.keyword.sdk4node}} 런타임을 선택하십시오.
1. {{site.data.keyword.Bluemix_notm}} 대시보드에서 액세스할 수 있는 애플리케이션 **개요** 페이지로 이동하고 {{site.data.keyword.geospatialshort_Geospatial}} 서비스 인스턴스를 애플리케이션에 연결한 후에 애플리케이션을 다시 스테이징하십시오. 
1. [{{site.data.keyword.geospatialshort_Geospatial}} 스타터 애플리케이션 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2018/06/geo-starter.zip)을 다운로드하고 파일의 압축을 푸십시오. 

1. 애플리케이션의 **시작하기** 페이지로 이동하고 해당 페이지의 지시사항에 따라 애플리케이션을 {{site.data.keyword.Bluemix_notm}}에 푸시하십시오. 

 **참고:** 코드에 대한 변경사항 작성을 언급하는 전체 단계를 건너뛸 수 있습니다. 변경 없이 다운로드한 스타터 애플리케이션을 그대로 실행할 수 있습니다. 

## 다음에 수행할 작업
{: #next}

* 애플리케이션 **개요** 페이지로 이동하여 애플리케이션이 성공적으로 시작되었는지 확인하십시오. 
* 브라우저에서 애플리케이션을 시작하여 확인하십시오. 애플리케이션 **개요** 페이지에서 애플리케이션의 URL(또는 "라우트")을 찾을 수 있습니다. 샘플 애플리케이션의 웹 페이지에는 애플리케이션 코드에 있는 REST API 호출의 상태 및 {{site.data.keyword.geospatialshort_Geospatial}}에서 발견한 이벤트에 대한 정보가 표시됩니다.
