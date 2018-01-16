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


#Einführung in {{site.data.keyword.geospatialshort_Geospatial}}
{: #gettingstarted}

Mit {{site.data.keyword.geospatialfull}} werden sich bewegende Geräte über Ihre Anwendung in {{site.data.keyword.Bluemix_notm}} überwacht.

Stellen Sie vor Beginn sicher, dass die folgenden Voraussetzungen erfüllt sind:

* Entscheiden Sie sich für eine Laufzeitumgebung für die Anwendung in {{site.data.keyword.Bluemix_notm}}, z. B. SDK for Node.js. In allen nachfolgend aufgeführten Codebeispielen wird Node.js verwendet. Auch die Starteranwendung ist in Node.js geschrieben.
* [Installieren Sie die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install){:new_window} für die Interaktion mit {{site.data.keyword.Bluemix_notm}} über die Befehlszeile.
* Stellen Sie sicher, dass Sie über einen [MQTT-Nachrichtenbroker ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://mqtt.org/){:new_window} zur Bereitstellung von Geogerätedaten und zum Empfangen von Ereignisbenachrichtigungen für Geräte verfügen. Von der Starteranwendung wird auf einen Nachrichtenbroker verwiesen, von dem simulierte Gerätedaten generiert werden. Der Service [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform/){:new_window} in {{site.data.keyword.Bluemix_notm}} ist eine Lösung, mit der der Bedarf eines MQTT-Nachrichtenbrokers abgedeckt wird. Weitere Informationen zur Verwendung von {{site.data.keyword.geospatialshort_Geospatial}} mit dem Internet of Things Platform-Service finden Sie in [IoT-App 'connected-car' mit {{site.data.keyword.geospatialshort_Geospatial}} erstellen![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](http://www.ibm.com/developerworks/mobile/library/mo-connectedcar-app/index.html){:new_window}.

Im Abschnitt zu den [Serviceanforderungen](/docs/services/geospatial/requirements.html){:new_window} finden Sie Informationen zu den Voraussetzungen für Nachrichten von MQTT-Geräten sowie zur entsprechenden Konfiguration.


Gehen Sie wie folgt vor, um mit der Verwendung von {{site.data.keyword.geospatialshort_Geospatial}} zu beginnen:

1. Erstellen Sie eine Anwendung in {{site.data.keyword.Bluemix_notm}} mit kompatiblen Laufzeiten. SDK for Node.js™ kann mit den hier bereitgestellten Code-Snippets verwendet werden.

	Sie können auch unmittelbar mit der Verwendung von {{site.data.keyword.geospatialshort_Geospatial}} beginnen, indem Sie die Starteranwendung ausführen.

1. Fügen Sie einen {{site.data.keyword.geospatialshort_Geospatial}}-Service zur Anwendung hinzu.
1. Schreiben Sie den Anwendungscode und schließen Sie die folgenden Aktionen ein:

	1. Rufen Sie in der Anwendung die Informationen zur Umgebungsvariable VCAP_SERVICES für {{site.data.keyword.geospatialshort_Geospatial}} ab. Für die Anwendung sind diese Informationen zur Verwendung der REST-API erforderlich. Das folgende Code-Snippet ist ein Beispiel dafür, wie die [Umgebungsvariable VCAP_SERVICES](/docs/services/geospatial/vcap_services.html) geparst wird.
	<pre><code>		 	
		var geo_props = {};
		// Analysieren von VCAP_SERVICES bei Ausführung in IBM Cloud
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
	1. Konfigurieren und steuern Sie den {{site.data.keyword.geospatialshort_Geospatial}}-Service über die REST-API. Sie müssen mindestens eine geografische Region definieren und den Service starten. Die [REST-API-Referenz ![Symbol für externen Link](../../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/apidocs/246) enthält Codebeispiele für weitere Features, die Sie zur Erstellung einer komplexeren Anwendung verwenden können. Code-Snippet: Definieren einer Region.
	<pre><code>

		//
		// Anfang - PUT addRegion
		//
		console.log("About to call REST PUT-addRegion api");  

		// JSON-Objekt erstellen
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

		// PUT-Optionen
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

		// PUT-Aufruf ausführen
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

		// JSON-Daten schreiben
		reqPut.write(jsonObject);
		reqPut.end();
		reqPut.on('error', function(e) {
		    console.error(e);
		});

		//
		// Ende PUT-addRegion
		//

		</code></pre>
	1. Starten Sie den Service, um mit dem Empfangen von Gerätenachrichten von MQTT zu beginnen. Code-Snippet: Starten des Service.

		<pre><code>							
				//
				// Anfang - PUT start
				//
				console.log("About to call REST PUT-start api");  

				// JSON-Objekt erstellen
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

				// Header vorbereiten
				var authbuf = 'Basic ' + new Buffer(geo_props.userid + ':' + geo_props.password).toString('base64');

				var putheaders = {
				    'Content-Type' : 'application/json',
				    'Content-Length' : Buffer.byteLength(jsonObject, 'utf8'),
				    'Authorization' : authbuf
				};

				// PUT-Optionen
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

				// PUT-Aufruf ausführen
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

				// JSON-Daten schreiben
				reqPut.write(jsonObject);
				reqPut.end();
				reqPut.on('error', function(e) {
				    console.error(e);
				});

				//
				// Ende PUT-Start
				//
	</code></pre>
      
1. Übertragen Sie die Anwendung mit einer Push-Operation mithilfe von Befehlen in der Befehlszeile an {{site.data.keyword.Bluemix_notm}}. Weitere Informationen zum Bereitstellen Ihrer Anwendung finden Sie im Abschnitt [Lernprogramm zur Einführung](/docs/services/geospatial/pushing_starter_app.html).

1. Greifen Sie auf die Anwendung im Browser zu. Sie finden die URL (oder "Route") der Anwendung auf der Übersichtsseite der Anwendung, die im {{site.data.keyword.Bluemix_notm}}-Dashboard verfügbar ist.
