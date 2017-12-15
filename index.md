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


#Getting started with {{site.data.keyword.geospatialshort_Geospatial}}
{: #gettingstarted}

{{site.data.keyword.geospatialfull}} monitors moving devices from your application in {{site.data.keyword.Bluemix_notm}}.

Before you begin, make sure that you meet the following requirements:

* Decide on a runtime environment for the application in {{site.data.keyword.Bluemix_notm}}, such as SDK for Node.js. The code examples that are shown here all use Node.js. The starter application is also written in Node.js.
* [Install the {{site.data.keyword.Bluemix_notm}} CLI](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install){:new_window} to interact with {{site.data.keyword.Bluemix_notm}} from the command line.
* Ensure that you have an [MQTT ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://mqtt.org/){:new_window} message broker to supply geospatial device data and receive event notifications for devices. The starter application points to a message broker that generates simulated device information. The [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform/){:new_window} service in {{site.data.keyword.Bluemix_notm}} is a solution to fulfill the need of an MQTT message broker. For more information on how to use {{site.data.keyword.geospatialshort_Geospatial}} with the Internet of Things Platform  service, see [Build a connected-car IoT app with {{site.data.keyword.geospatialshort_Geospatial}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://www.ibm.com/developerworks/mobile/library/mo-connectedcar-app/index.html){:new_window}.

See [Service requirements](/docs/services/geospatial/requirements.html){:new_window} for information about the MQTT device message requirements and configuration.


To get started with {{site.data.keyword.geospatialshort_Geospatial}}:

1. Create your application in {{site.data.keyword.Bluemix_notm}} with one of the compatible runtimes. SDK for Node.js™ works with the code snippets provided here.

	You can also get started with {{site.data.keyword.geospatialshort_Geospatial}} right away by running the starter application.

1. Add a {{site.data.keyword.geospatialshort_Geospatial}} service to your application.
1. Write your application code and include the following actions:

	1. Within your application, obtain the VCAP_SERVICES environment variable information for {{site.data.keyword.geospatialshort_Geospatial}}. Your application needs this information to use the REST API. The following code snippet is an example of how to parse the [VCAP_SERVICES environment variable.](/docs/services/geospatial/vcap_services.html)
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
	1. Configure and control the {{site.data.keyword.geospatialshort_Geospatial}} service through the REST API. At a minimum, you must define a geographic region and start the service. The [REST API reference ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/apidocs/246) includes code examples for more features that you can use to build a more complex application. Code snippet: Define a region.
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
	1. Start the service to begin receiving device messages from MQTT. Code snippet: Start the service.

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
1. Push your application to {{site.data.keyword.Bluemix_notm}} with command-line commands. Find more information on how to do deploy your application in the section titled [Getting started tutorial](/docs/services/geospatial/pushing_starter_app.html).

1. Access the application in your browser.You can find your application's URL (or "route") on the application overview page, which is accessible from the {{site.data.keyword.Bluemix_notm}} dashboard.
