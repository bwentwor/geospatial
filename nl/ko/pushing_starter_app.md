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

# 시작하기 튜토리얼
{: #pushing_starter_app}

애플리케이션의 경계를 펼치십시오. 실시간 지리공간 분석을 활용하여 정의된 지역으로 디바이스가 들어가거나, 나오거나, 머무는 시간을 추적하십시오. 이 시작하기 튜토리얼에서, 스타터 애플리케이션을 배치하게 되고 {{site.data.keyword.geospatialshort_Geospatial}} 서비스를 사용하는 방법을 빠르게 학습합니다.
{:shortdesc}

## 시작하기 전에
{: #prereqs}

스타터 앱을 배치하기 전에 다음 단계를 따르십시오. 

* [{{site.data.keyword.Bluemix_notm}} 계정 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/registration){:new_window}을 등록하십시오. 
* {{site.data.keyword.geospatialshort_Geospatial}} 서비스의 인스턴스를 {{site.data.keyword.Bluemix_notm}} 조직에 작성하십시오. [{{site.data.keyword.Bluemix_notm}} 서비스 카탈로그의 {{site.data.keyword.geospatialshort_Geospatial}} 페이지 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}/catalog/services/geospatial-analytics/){:new_window}에서 인스턴스를 직접 작성할 수 있습니다.   
* [{{site.data.keyword.Bluemix_notm}} CLI를 설치하십시오](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install).

## 1단계: 앱 작성 및 서비스에 앱 연결
{: #create_connect}

1. {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 작성하십시오. 

    a. {{site.data.keyword.Bluemix_notm}} 메뉴에서 **Cloud Foundry 앱**을 선택하고 **리소스 작성**을 클릭하십시오. 

    b. 애플리케이션에 대한 {{site.data.keyword.sdk4node}} 런타임을 선택하십시오.
    **참고:** 이러한 지시사항은 Node-RED 스타터 표준 유형에도 적용됩니다. 

      나중에 필요할 수 있으므로 애플리케이션에 지정한 이름을 기억하십시오. 

## 2단계: 스타터 앱 설정
{: #setup_app}

1. [{{site.data.keyword.geospatialshort_Geospatial}} 스타터 애플리케이션 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://developer.ibm.com/streamsdev/wp-content/uploads/sites/15/2017/09/geo-starter.zip)을 다운로드하십시오. 

1. {{site.data.keyword.Bluemix_notm}}의 애플리케이션에 지정한 이름과 일치하도록 디렉토리의 이름을 바꾸십시오.
1. {{site.data.keyword.geospatialshort_Geospatial}} 서비스 인스턴스를 애플리케이션에 연결하고 애플리케이션을 다시 스테이징하십시오.

## 3단계: 스타터 앱 배치
{: #deploy_app}

1. 스타터 애플리케이션 디렉토리로 이동하십시오.
  <pre><code>cd mygeoapp</code></pre>
  {:pre}

1. 프롬프트가 표시되면 {{site.data.keyword.Bluemix_notm}}에 로그인하고 대상 조직을 설정하십시오.
  <pre><code>bx login</code></pre>
  {:pre}

1. 애플리케이션을 {{site.data.keyword.Bluemix_notm}}에 푸시하십시오.
  <pre><code>bx app push mygeoapp</code></pre>
  {:pre}

## 다음에 수행할 작업
{: #next}

* {{site.data.keyword.Bluemix_notm}} 대시보드를 통해 액세스할 수 있는 애플리케이션 개요 페이지로 이동하여 애플리케이션이 성공적으로 시작되었는지 확인하십시오.
* 브라우저에서 애플리케이션을 시작하여 확인하십시오. 애플리케이션 개요 페이지에서 애플리케이션의 URL(또는 "라우트")을 찾을 수 있습니다. 샘플 애플리케이션의 웹 페이지에는 애플리케이션 코드에 있는 REST API 호출의 상태 및 {{site.data.keyword.geospatialshort_Geospatial}}에서 발견한 이벤트에 대한 정보가 표시됩니다.
