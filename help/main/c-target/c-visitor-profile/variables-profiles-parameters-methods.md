---
keywords: variabili;profili;parametri;profili incorporati;metodi;variabili URL;profili geo;profili di terze parti;variabili mbox;variabili di campagna;attributi dei clienti
description: Visualizza un elenco di vari profili, variabili e parametri utili negli script di profilo in Adobe Target.
title: Quali profili, variabili e parametri vengono utilizzati in  [!DNL Target]?
feature: Audiences
exl-id: 96ef9a56-fe76-428e-a164-c01829fdf45d
source-git-commit: 4395caa7e40717c59067eaedff5e53776768eda9
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 67%

---

# Glossario di profili e variabili

Questa pagina elenca i profili, le variabili e i parametri utili negli script dei profili.

## Profili incorporati {#section_2B694370003C4F8E8E29E0B2F6E52045}

| Profilo | Note |
|--- |--- |
| user.activeActivities<br>user.activeCampaigns | Restituisce l&#39;ID della campagna per tutte le campagne/attività in cui si trova l&#39;utente, anche se non ha interagito con la campagna/attività nella sessione corrente. |
| user.pcId |  |
| User.sessionId |  |
| user.categoryAffinity |  |
| user.categoryAffinities | Restituisce un array delle affinità che un visitatore ha popolato |
| user.isFirstSession |  |
| user.isNewSession |  |
| user.daysSinceLastVisit |  |
| User.browser | Agente utente |
| user.browserType | Restituisce il tipo di browser, ad esempio safari, chrome e così via. |
| User.header | Tutti i profili `user.header` sono incorporati dai dati di intestazione di richiesta mbox |
| user.header(&#39;x-forwarded-for&#39;) | L&#39;indirizzo IP pubblico della connessione di rete che in cui si trova il visitatore.<br>È possibile ottenerlo in diversi modi, ad esempio [whatismyip.com](https://www.whatismyip.com/). L&#39;indirizzo IP non è l&#39;indirizzo NAT (indirizzo interno), che inizia con 10., 192,168., o 172.<br>Nota: user.header(&#39;x-cluster-client-ip&#39;) è stato dichiarato obsoleto. |
| user.header(&#39;host&#39;) | Hostname del sito web |
| user.header(&#39;cookie&#39;) | Dati cookie del visitatore |
| user.header(&#39;user-agent&#39;) | Agente utente del browser del visitatore |
| user.header(&#39;accept-language&#39;) | Lingua del visitatore |
| user.header(&#39;accept-encoding&#39;) | Codifica del carattere del visitatore |
| user.header(&#39;accept&#39;) | Lingua del visitatore e codifica del carattere |
| user.header(&#39;connection&#39;) | Connessione server. Ad esempio: keep-live |
| user.header(&#39;referrer&#39;) | URL del sito web della pagina corrente del visitatore. Non funziona per Internet Explorer. |
| user.getLocal(&#39;param_name&#39;); | Recuperare il valore impostato utilizzando `user.setLocal`. |
| user.setLocal(&#39;param_name&#39;,&#39;value&#39;) | Crea valori di profilo persistenti all’interno di uno script di profilo. Questi valori persistono come uno script di profilo, ma puoi accedervi solo all’interno dello script in cui sono stati impostati. |
| user.get(&#39;param_name&#39;) |  |
| user.parameter | Attributi permanenti del profilo creati dagli script di profilo. Fa inoltre riferimento a profili di &quot;sistema&quot; come geolocalizzazione, conteggio delle visite e così via. |
| profile.get(&#39;param_name&#39;) | Il modo corretto per ottenere un parametro di profilo da utilizzare in uno script di profilo è il metodo profile.get(&#39;param_name&#39;). |
| profile.param(&#39;param_name&#39;); |  |
| profile.parameter(&#39;parameter_name&#39;); | Parametri mbox che sono resi persistenti a causa del loro profilo.  Prefisso. |
| profile.browserTime | Ora locale del browser del visitatore. Per l&#39;ora di sistema, creare un nuovo oggetto di data nello script del profilo |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
| profile.mobile.isTablet | Il dispositivo del visitatore è un tablet.<P>**NOTA**: questo profilo sostituisce l&#39;elemento legacy obsoleto. Il browser legacy è una categoria di pubblico iPad. Per ulteriori informazioni, vedere [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md#profile-scripts). |
| profile.mobile.isMobilePhone | Il dispositivo visitatore è un telefono cellulare.<P>**NOTA**: questo profilo sostituisce l&#39;elemento legacy obsoleto. Il browser legacy è una categoria di pubblico iPhone. Per ulteriori informazioni, vedere [Browser](/help/main/c-target/c-audiences/c-target-rules/browser.md#profile-scripts). |
| parameter= | Termine generico per valori aggiuntivi passati con una mbox, di solito come coppie nome/valore. Non persistente a meno che non sia fatto con `profile.parameter` o `user.parameter`. |

## Variabili di URL {#section_8F25958273164EBAA6DC659302993FD3}

| `landing` | `referrer` | `page` |
|---|---|---|
| `landing.url` | `referrer.url` | `page.url` |
| `landing.domain` | `referrer.domain` | `page.domain` |
| `landing.protocol` | `referrer.protocol` | `page.protocol` |
| `landing.param` | `referrer.param` | `page.param` |
| `landing.query` | `referrer.query` | `page.query` |

## Profili carrier geo e mobili {#section_08441DA42E7346918FBB345818854997}

* `profile.geolocation.country`
* `profile.geolocation.state`
* `profile.geolocation.city`
* `profile.geolocation.zip`
* `profile.geolocation.dma`
* `profile.geolocation.domainName`
* `profile.geolocation.ispName`
* `profile.geolocation.connectionSpeed`
* `profile.geolocation.mobileCarrier`
* `profile.geolocation.latitude`
* `profile.geolocation.longitude`

## Variabili di mbox {#section_C42F0D33BD8044BE812FA0B7905CC0ED}

| Variabile | Note |
|--- |--- |
| `mbox.name` |  |
| mbox.param(&#39;param_name&#39;) |  |
| I parametri passano automaticamente con ogni richiesta:<ul><li>mbox.param(&#39;browserHeight&#39;)</li><li>mbox.param(&#39;browserTimeOffset&#39;)</li><li>mbox.param(&#39;browserWidth&#39;)</li><li>mbox.param(&#39;colorDepth&#39;)</li><li>mbox.param(&#39;mboxXDomain&#39;)</li><li>mbox.param(&#39;mboxTime&#39;)</li><li>mbox.param(&#39;screenHeight&#39;)</li><li>mbox.param(&#39;screenWidth&#39;)</li></ul> |
| Parametri passati con mbox di ordine:<ul><li>mbox.param(&#39;orderId&#39;)</li><li>mbox.param(&#39;orderTotal&#39;)</li><li>mbox.param(&#39;productPurchasedId&#39;)</li></ul> |
| mbox3rdPartyId | Parametro mbox per sincronizzare un ID cliente per mboxPCID di Target. Un ID cliente è un ID utilizzato dalla società per tenere traccia dei visitatori, ad esempio un ID CRM, un ID di appartenenza o qualcosa di simile. Questo ID può quindi essere utilizzato per aggiungere informazioni tramite le API del profilo e [Attributi del cliente](https://experienceleague.adobe.com/docs/target-dev/developer/implementation/methods/customer-attributes.html?lang=it){target=_blank}. |
| mboxPageValue | In ogni mbox chiamata alla pagina viene assegnato un valore. |
| mboxDebug | Utilizzato solo per informazioni di debug. Aggiunto all’URL della pagina in cui lo cerca at.js. |
| mboxOverride.browserIp | Imposta un geo diverso rispetto alla posizione effettiva in modo da poter testare come qualcosa apparirebbe in un&#39;altra posizione.<br>**Nota:** l&#39;utilizzo dei parametri mboxOverride deve essere utilizzato solo durante il test dell&#39;attività e non in produzione. L’utilizzo di eventuali parametri  mboxOverride  può causare discrepanze nella creazione di rapporti quando si utilizza [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Utilizza la [modalità di controllo qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md) durante il test per garantire che l’attività funzioni come previsto prima di pubblicarla nell’ambiente live. |

## Attributi del cliente {#section_62B4821EB6564FF4A14159A837AD4EDB}

Gli attributi del cliente possono essere indicati in script di profilo, formattati come `crs.get('<Datasource Name>.<Attribute name>')`.

Questi attributi sono disponibili anche come token negli script di profilo e direttamente nelle offerte senza prima richiedere uno script di profilo. Il token deve essere nel formato: `${crs.datasourceName.attributeName}`. Tieni presente che gli spazi in `datasourceName` devono essere rimossi da qualsiasi chiamata API.
