---
description: Questa pagina elenca i profili, le variabili e i parametri utili negli script dei profili.
keywords: variabili;profili;parametri;profili incorporati;metodi;variabili URL;profili geo;profili di terze parti;variabili mbox;variabili di campagna;attributi dei clienti
seo-description: Questa pagina elenca i profili, le variabili e i parametri utili negli script dei profili.
seo-title: Glossario di profili e variabili
solution: Target
title: Glossario di profili e variabili
topic: Standard
uuid: 9286467c-cbb5-42be-99c0-6687ffab0969
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Glossario di profili e variabili{#profile-and-variable-glossary}

Questa pagina elenca i profili, le variabili e i parametri utili negli script dei profili.

## Profili incorporati {#section_2B694370003C4F8E8E29E0B2F6E52045}

| Profilo | Note |
|--- |--- |
| user.activeActivities<br>user.activeCampaigns | Restituisce l'ID della campagna per tutte le campagne/attività in cui si trova l'utente, anche se non ha interagito con la campagna/attività nella sessione corrente. |
| user.pcId |  |
| User.sessionId |  |
| user.categoryAffinity |  |
| user.categoryAffinities | Restituisce un array delle affinità che un visitatore ha popolato |
| user.isFirstSession |  |
| user.isNewSession |  |
| user.daysSinceLastVisit |  |
| User.browser | Agente utente |
| User.header | Tutti i profili `user.header` sono incorporati dai dati di intestazione di richiesta mbox |
| user.header('x-cluster-client-ip') | L'indirizzo IP pubblico della connessione di rete che in cui si trova il visitatore.<br>È possibile ottenerlo in diversi modi, ad esempio con [whatismyip.com](https://www.whatismyip.com/). L'indirizzo IP non è l'indirizzo NAT (indirizzo interno), che inizia con 10., 192,168., o 172. |
| user.header('host') | Hostname del sito web |
| user.header('cookie') | Dati cookie del visitatore |
| user.header('user-agent') | Agente utente del browser del visitatore |
| user.header('accept-language') | Lingua del visitatore |
| user.header('accept-encoding') | Codifica del carattere del visitatore |
| user.header('accept') | Lingua del visitatore e codifica del carattere |
| user.header('connection') | Connessione server. Ad esempio: keep-live |
| user.header('referrer') | URL del sito web della pagina corrente del visitatore. Non funziona per Internet Explorer. |
| user.getLocal('param_name','value'); |  |
| user.setLocal('param_name','value'); |  |
| user.get('param_name') |  |
| user.parameter | Attributi permanenti del profilo creati dagli script di profilo. Fa anche riferimento a profili “di sistema” come geolocalizzazione, conteggio delle visite, ecc. |
| profile.get('param_name') |  |
| profile.param('param_name'); |  |
| profile.parameter('parameter_name'); | Parametri mbox che sono resi persistenti a causa del loro profilo.  Prefisso. |
| profile.browserTime | Ora locale del browser del visitatore. Per l'ora di sistema, creare un nuovo oggetto di data nello script del profilo |
| profile.averageDaysBetweenVisits |  |
| profile.sessionCount |  |
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
| mbox.param('param_name') |  |
| I parametri passano automaticamente con ogni richiesta:<ul><li>mbox.param('browserHeight')</li><li>mbox.param('browserTimeOffset')</li><li>mbox.param('browserWidth')</li><li>mbox.param('colorDepth')</li><li>mbox.param('mboxXDomain')</li><li>mbox.param('mboxTime')</li><li>mbox.param('screenHeight')</li><li>mbox.param('screenWidth')</li></ul> |
| Parametri passati con mbox di ordine:<ul><li>mbox.param('orderId')</li><li>mbox.param('orderTotal')</li><li>mbox.param('productPurchasedId')</li></ul> |
| mbox3rdPartyId | Parametro mbox per sincronizzare un ID cliente per mboxPCID di Target. Un ID cliente è un ID utilizzato dalla società per tenere traccia dei visitatori, ad esempio un ID CRM, un ID di appartenenza o qualcosa di simile. Questo ID può quindi essere utilizzato per aggiungere informazioni tramite le API di profilo e [Attributi del cliente](/help/c-target/c-visitor-profile/working-with-customer-attributes.md). |
| mboxPageValue | In ogni mbox chiamata alla pagina viene assegnato un valore. |
| mboxDebug | Utilizzato solo per informazioni di debug. Aggiunto all'URL della pagina in cui lo cerca il mbox.js. |
| mboxOverride.browserIp | Imposta un geo diverso rispetto alla posizione effettiva in modo da poter testare come qualcosa apparirebbe in un'altra posizione.<br>**Nota:** l'utilizzo dei parametri mboxOverride deve essere utilizzato solo durante il test dell'attività e non in produzione. L’utilizzo di eventuali parametri  mboxOverride  può causare discrepanze nella creazione di rapporti quando si utilizza [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Utilizza la [modalità di controllo qualità delle attività](/help/c-activities/c-activity-qa/activity-qa.md) durante il test per garantire che l’attività funzioni come previsto prima di pubblicarla nell’ambiente live. |

## Attributi del cliente {#section_62B4821EB6564FF4A14159A837AD4EDB}

Gli attributi del cliente possono essere indicati in script di profilo, formattati come `crs.get('<Datasource Name>.<Attribute name>')`.

Questi attributi sono disponibili anche come token negli script di profilo e direttamente nelle offerte senza prima richiedere uno script di profilo. Il token deve essere nel formato: `$crs.datasourceName.attributeName`.
