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

# スターター・アプリケーションを {{site.data.keyword.Bluemix_notm}} 用に変更する
{: #modifying_starter_app}

スターター・アプリケーションを変更し、{{site.data.keyword.Bluemix_notm}} に再デプロイしてその結果を確認することができます。
{:shortdesc}


単純な変更は、スターター・アプリケーション内のイベント限度を上げるか、削除して、アプリケーションの実行期間を長くすることです。

1. テキスト・エディターまたは開発環境で app.js を開きます。
1. `eventTarget` 変数を変更するか、または、イベント限度を完全に削除する場合はこの行を削除します。
	 <pre><code>var eventTarget = 100;</code></pre>
1. イベント限度を削除する場合は、次の if ステートメントも削除する必要があります。
	 <pre><code>  
	if (eventCount >= eventTarget) {
		    status_step[3] = "Completed";
		    console.log("\nTarget event count has been reached.  Geospatial Analytics service will be stopped.\n");
		    callback(null, null);
		    }
	</code></pre>
1. cf push コマンドを使用して、変更後のアプリケーションを {{site.data.keyword.Bluemix_notm}} に再デプロイします。
	 <pre><code>  
	bx app push mygeoapp
	</code></pre>
1. アプリケーションの URL または「経路」をブラウザーに入力するか、または、{{site.data.keyword.Bluemix_notm}} ダッシュボードからアプリケーションを起動します。
