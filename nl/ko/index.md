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


#{{site.data.keyword.geospatialshort_Geospatial}} 시작하기
{: #gettingstarted}

{{site.data.keyword.geospatialfull}}는 {{site.data.keyword.Bluemix_notm}}의 애플리케이션으로부터 이동 중인 디바이스를 모니터링합니다.

시작하기 전에 다음 요구사항을 충족하는지 확인하십시오.

* {{site.data.keyword.Bluemix_notm}}의 애플리케이션에 대한 런타임 환경을 결정하십시오(예: SDK for Node.js). 여기에 나와 있는 코드 예제에서는 모두 Node.js를 사용합니다. 스타터 애플리케이션도 Node.js로 작성되었습니다.
* 명령행에서 {{site.data.keyword.Bluemix_notm}}와 상호작용하도록 [{{site.data.keyword.Bluemix_notm}} CLI를 설치](https://console.bluemix.net/docs/cli/reference/bluemix_cli/get_started.html#getting-started){:new_window}하십시오. 
* [MQTT ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://mqtt.org/){:new_window} 메시지 브로커가 있으며 지리공간 디바이스 데이터를 제공하고 디바이스에 대한 이벤트 알림을 수신하는지 확인하십시오. 스타터 애플리케이션은 시뮬레이션된 디바이스 정보를 생성하는 메시지 브로커를 가리킵니다. {{site.data.keyword.Bluemix_notm}}의 [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform/){:new_window} 서비스는 MQTT 메시지 브로커의 필요를 충족시키는 솔루션입니다. Internet of Things Platform 서비스와 함께 {{site.data.keyword.geospatialshort_Geospatial}} 서비스를 사용하는 방법에 대한 자세한 정보는 [{{site.data.keyword.geospatialshort_Geospatial}} 서비스를 사용하여 커넥티드 카 IoT 앱 구축 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](http://www.ibm.com/developerworks/mobile/library/mo-connectedcar-app/index.html){:new_window}을 참조하십시오.

MQTT 디바이스 메시지 요구사항 및 구성에 대한 정보는 [서비스 요구사항](/docs/services/geospatial/requirements.html){:new_window}을 참조하십시오.


{{site.data.keyword.geospatialshort_Geospatial}}를 시작하려면 다음을 수행하십시오.

1. 호환되는 런타임 중 하나를 사용하여 {{site.data.keyword.Bluemix_notm}}에서 애플리케이션을 작성하십시오. SDK for Node.js™는 여기에 제공된 코드 스니펫으로 작동합니다.

	또한 스타터 애플리케이션을 실행하여 {{site.data.keyword.geospatialshort_Geospatial}}를 바로 시작할 수도 있습니다.

1. 애플리케이션에 {{site.data.keyword.geospatialshort_Geospatial}} 서비스를 추가하십시오.
1. 애플리케이션 코드를 작성하고 다음 조치를 포함하십시오.

	1. 애플리케이션 내에서 {{site.data.keyword.geospatialshort_Geospatial}}에 대한 VCAP_SERVICES 환경 변수 정보를 가져옵니다. 애플리케이션에서 REST API를 사용하려면 다음 정보가 필요합니다. 다음 코드 스니펫은 [VCAP_SERVICES 환경 변수](/docs/services/geospatial/vcap_services.html)를 구문 분석하는 방법에 대한 예제입니다.
	<pre><code>		 	
		var geo_props = {};
		// Parse VCAP_SERVICES if running in IBM Cloud
		if (process.env.VCAP_SERVICES)
		{
			var env = JSON.parse(process.env.VCAP_SERVICES);

			//debugging
			for (var svcName in env) {
				console.log(svcName);
			}
			console.log(env);
			//find the Streams Geo service
			if (env['Geospatial Analytics']) {
				geo_props = env['Geospatial Analytics'][0]['credentials'];
			}
			else {
				console.log('You must bind the Streams Geo service to this application');
			}
		}
	</code></pre>
	1. REST API를 통해 {{site.data.keyword.geospatialshort_Geospatial}} 서비스를 구성하고 제어합니다. 최소한 하나의 지리적 지역을 정의하고 서비스를 시작해야 합니다. [REST API 참조 ![외부 링크 아이콘](../../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/apidocs/246)에는 보다 복잡한 애플리케이션을 구축하는 데 사용할 수 있는 여러 기능의 코드 샘플이 포함되어 있습니다. 코드 스니펫: 지역 정의.
	<pre><code>

		//
		// Begin - PUT addRegion
		//
		console.log("About to call REST PUT-addRegion api");  

		// Create the JSON object
		jsonObject = JSON.stringify({
		  "regions" : [
		  {"region_type" : "regular", "name" : "Kiosk 3",
		   "notifyOnExit" : "false",
		   "center_latitude" : "36.229531",
		   "center_longitude" : "-115.277874",
		   "number_of_sides" : "10",
		   "distance_to_vertices" : "150"
		 }
		  ]
		});

		putheaders = {
		    'Content-Type' : 'application/json',
		    'Content-Length' : Buffer.byteLength(jsonObject, 'utf8'),
		    'Authorization' : authbuf
		};

		// The PUT options
		optionsput = {
		    host : geo_props.geo_host,
		    port : geo_props.geo_port,
		    path : geo_props.add_region_path,
		    method : 'PUT',
		    headers : putheaders
		};

		console.info('Options prepared:');
		console.info(optionsput);
		console.info('Do the PUT-addRegion call');

		// Do the PUT call
		reqPut = https.request(optionsput, function(res) {
		    console.log("statusCode: ", res.statusCode);

		    if (res.statusCode != 200)
		        runError = 1;

		    res.on('data', function(d) {
		        console.info('PUT result:\n');
		        process.stdout.write(d);
		        console.info('\n\nPUT completed');
		    });
		});

		// Write the JSON data
		reqPut.write(jsonObject);
		reqPut.end();
		reqPut.on('error', function(e) {
		    console.error(e);
		});

		//
		// PUT-addRegion end
		//

		</code></pre>
	1. 서비스를 시작하여 MQTT에서 디바이스 메시지 수신을 시작합니다. 코드 스니펫: 서비스를 시작합니다.

		<pre><code>							
				//
				// Begin - PUT start
				//
				console.log("About to call REST PUT-start api");  

				// Create the JSON object
				jsonObject = JSON.stringify({
				  "mqtt_uid" : "iamuser",
				  "mqtt_pw" : "thepass",
				  "mqtt_uri" :  "mqtt.myplace.com:1883",
				  "mqtt_input_topics" : "mytopic/cars/json/#",
				  "mqtt_notify_topic" : "demo-car-events",
				  "device_id_attr_name" : "ID",
				  "latitude_attr_name" : "lat",
				  "longitude_attr_name" : "lon"
				});

				// Prepare the header
				var authbuf = 'Basic ' + new Buffer(geo_props.userid + ':' + geo_props.password).toString('base64');

				var putheaders = {
				    'Content-Type' : 'application/json',
				    'Content-Length' : Buffer.byteLength(jsonObject, 'utf8'),
				    'Authorization' : authbuf
				};

				// The PUT options
				var optionsput = {
				    host : geo_props.geo_host,
				    port : geo_props.geo_port,
				    path : geo_props.start_path,
				    method : 'PUT',
				    headers : putheaders
				};

				console.info('Options prepared:');
				console.info(optionsput);
				console.info('Do the PUT-start call');

				// Do the PUT call
				var reqPut = https.request(optionsput, function(res) {

				    res.on('data', function(d) {
				        console.info('PUT result:\n');
				        process.stdout.write(d);
				        console.info('\n\nPUT completed');
				        console.log("statusCode: ", res.statusCode);
				    });
				    if (res.statusCode != 200)
				        runError = 1;

				});

				// Write the JSON data
				reqPut.write(jsonObject);
				reqPut.end();
				reqPut.on('error', function(e) {
				    console.error(e);
				});

				//
				// PUT-start end
				//
			</code></pre>
      
1. 명령행 명령을 사용하여 애플리케이션을 {{site.data.keyword.Bluemix_notm}}에 푸시하십시오. [시작하기 튜토리얼](/docs/services/geospatial/pushing_starter_app.html) 섹션에서 애플리케이션을 배치하는 방법에 대한 자세한 정보를 확인하십시오.

1. 브라우저에서 애플리케이션에 액세스하십시오. {{site.data.keyword.Bluemix_notm}} 대시보드를 통해 액세스할 수 있는 애플리케이션 개요 페이지에서 애플리케이션의 URL(또는 "라우트")을 찾을 수 있습니다.
