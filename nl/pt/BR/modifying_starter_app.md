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

# Modificando o aplicativo iniciador para {{site.data.keyword.Bluemix_notm}}
{: #modifying_starter_app}

É possível modificar o aplicativo iniciador e, em seguida, reimplementá-lo no {{site.data.keyword.Bluemix_notm}} para ver os resultados.
{:shortdesc}


Uma modificação simples é aumentar ou remover o limite de eventos no aplicativo iniciador para que
        ele não seja mais executado.

1. Abra app.js em um editor de texto ou ambiente de desenvolvimento.
1. Mude a variável `eventTarget` ou exclua essa linha para remover completamente o limite de evento:
	 <pre><code>var eventTarget = 100;</code></pre>
1. Se você desejar remover o limite de evento, também precisará excluir a instrução IF a seguir:
	 <pre><code>  
	if (eventCount >= eventTarget) {
		    status_step[3] = "Completed";
		    console.log("\nTarget event count has been reached.  Geospatial Analytics service will be stopped.\n");
		    callback(null, null);
		    }
	</code></pre>
1. Reimplemente seu aplicativo modificado para {{site.data.keyword.Bluemix_notm}} com o comando cf push.
	 <pre><code>  
	bx app push mygeoapp
	</code></pre>
1. Insira a URL do aplicativo ou "roteie-a" em seu navegador ou ative-a a partir do painel do
              {{site.data.keyword.Bluemix_notm}}.
