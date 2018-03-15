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


#Initiation à {{site.data.keyword.geospatialshort_Geospatial}}
{: #gettingstarted}

{{site.data.keyword.geospatialfull}} permet de surveiller les périphériques en mouvement depuis votre application dans {{site.data.keyword.Bluemix_notm}}.

Avant de commencer, assurez-vous que les conditions suivantes sont remplies :

* Choisissez un environnement d'exécution pour l'application dans {{site.data.keyword.Bluemix_notm}}, par exemple SDK for Node.js. Les exemples de code ci-après utilisent Node.js. L'application de démarrage est également écrite dans Node.js.
* [Installez l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}](https://console.bluemix.net/docs/cloud-platform/cli/reference/bluemix_cli/download_cli.html#download_install){:new_window} afin de pouvoir interagir avec {{site.data.keyword.Bluemix_notm}} depuis la ligne de commande. 
* Assurez-vous de disposer d'un courtier de messages [MQTT ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](http://mqtt.org/){:new_window} pour envoyer des données de périphérique géospatiales et recevoir des notifications d'événements pour ces périphériques. L'application de démarrage pointe sur un courtier de messages qui génère des informations de périphériques simulés. Le service [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform/){:new_window} dans {{site.data.keyword.Bluemix_notm}} est une solution possible pour répondre au besoin en courtier de message MQTT. Pour plus d'informations sur l'utilisation de {{site.data.keyword.geospatialshort_Geospatial}} avec le service Internet of Things Platform, voir [Build a connected-car IoT app with {{site.data.keyword.geospatialshort_Geospatial}} ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](http://www.ibm.com/developerworks/mobile/library/mo-connectedcar-app/index.html){:new_window}.

Consultez [Besoins des services](/docs/services/geospatial/requirements.html){:new_window} pour des informations sur les exigences et la configuration des messages d'appareil MQTT.


Pour commencer à utiliser {{site.data.keyword.geospatialshort_Geospatial}} :

1. Créez votre application dans {{site.data.keyword.Bluemix_notm}} avec un des contextes d'exécution compatibles. SDK for Node.js fonctionne avec les fragments de code fournis ici.

	Vous pouvez aussi vous initier à l'utilisation de {{site.data.keyword.geospatialshort_Geospatial}} en exécutant l'application de démarrage.

1. Ajoutez un service {{site.data.keyword.geospatialshort_Geospatial}} à votre application.
1. Ecrivez votre code d'application et incluez les actions suivantes :

	1. Dans votre application, obtenez les informations figurant dans la variable d'environnement VCAP_SERVICES pour {{site.data.keyword.geospatialshort_Geospatial}}. Ces informations sont indispensables pour l'utilisation de l'API REST. L'exemple de fragment de code suivant montre comment effectuer l'analyse syntaxique de la variable d'environnement [VCAP_SERVICES.](/docs/services/geospatial/vcap_services.html)
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
	1. Configurez et contrôlez le service {{site.data.keyword.geospatialshort_Geospatial}} via l'API REST. Vous devez au moins définir une région géographique et démarrer le service. La section [Référence d'API REST ![Icône de lien externe icon](../../icons/launch-glyph.svg "Icône de lien externe icon")](https://console.bluemix.net/apidocs/246) inclut des exemples de code pour d'autres fonctionnalités que vous pouvez utiliser afin de construire une application plus complexe. Fragment de code : définissez une région.
	<pre><code>

		//
		// Begin - PUT addRegion
		//
		console.log("About to call REST PUT-addRegion api");  

		// Create the JSON object
		jsonObject = JSON.stringify({
		  "regions" : [
		  {"region_type" : "regular", "name" : "Kiosk 3", "notifyOnExit" : "false", "center_latitude" : "36.229531", "center_longitude" : "-115.277874", "number_of_sides" : "10", "distance_to_vertices" : "150"}
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
	1. Démarrez le service pour commencer à recevoir des messages de périphérique de MQTT. Fragment de code : démarrez le service.

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
      
1. Déployez votre application dans {{site.data.keyword.Bluemix_notm}} avec des commandes de ligne de commande. Vous trouverez des informations supplémentaires sur le déploiement de votre application dans la section intitulée [Tutoriel d'initiation](/docs/services/geospatial/pushing_starter_app.html). 

1. Accédez à l'application à partir de votre navigateur. Vous trouverez l'adresse URL (ou "route") de votre application sur la page de présentation de l'application, accessible à partir du tableau de bord {{site.data.keyword.Bluemix_notm}}.
