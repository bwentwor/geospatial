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

# Modifica dell'applicazione starter per {{site.data.keyword.Bluemix_notm}}
{: #modifying_starter_app}

Puoi modificare l'applicazione starter e quindi ridistribuirla a {{site.data.keyword.Bluemix_notm}} per visualizzarne i risultati.
{:shortdesc}


Una semplice modifica consiste nell'aumentare o rimuovere il limite di eventi nell'applicazione starter in modo da
        prolungarne l'esecuzione.

1. Apri app.js in un editor di testo o un ambiente di sviluppo.
1. Modifica la variabile `eventTarget` oppure elimina questa riga per rimuovere del tutto il limite di eventi:
	 <pre><code>var eventTarget = 100;</code></pre>
1. Se vuoi rimuovere il limite di eventi, dovrai eliminare anche la seguente condizione if:
	 <pre><code>  
	if (eventCount >= eventTarget) {
		    status_step[3] = "Completed";
		    console.log("\nTarget event count has been reached.  Geospatial Analytics service will be stopped.\n");
		    callback(null, null);
		    }
	</code></pre>
1. Distribuisci nuovamente la tua applicazione modificata a {{site.data.keyword.Bluemix_notm}} con il comando cf push.
	 <pre><code>  
	bx app push mygeoapp
	</code></pre>
1. Immetti l'URL o "rotta" della tua applicazione nel browser o avviala dal
             dashboard {{site.data.keyword.Bluemix_notm}}.
