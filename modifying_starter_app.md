---

copyright:
  years: 2015, 2018
lastupdated: "2017-12-15"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Modifying the starter application to {{site.data.keyword.Bluemix_notm}}
{: #modifying_starter_app}

You can modify the starter application and then redeploy it to {{site.data.keyword.Bluemix_notm}} to see the results.
{:shortdesc}


A simple modification is to raise or remove the event limit in the starter application so that it runs longer.

1. Open app.js in a text editor or development environment.
1. Change the `eventTarget` variable, or delete this line to remove the event limit entirely:
	 <pre><code>var eventTarget = 100;</code></pre>
1. If you would like to remove the event limit, you also need to delete the following if statement:
	 <pre><code>  
	if (eventCount >= eventTarget) {
		    status_step[3] = "Completed";
		    console.log("\nTarget event count has been reached.  Geospatial Analytics service will be stopped.\n");
		    callback(null, null);
		    }
	</code></pre>
1. Redeploy your modified application to {{site.data.keyword.Bluemix_notm}} with the cf push command.
	 <pre><code>  
	bx app push mygeoapp
	</code></pre>
1. Enter your application's URL or "route" into your browser or launch it from the {{site.data.keyword.Bluemix_notm}} dashboard.
