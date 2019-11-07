---
keywords: serverstate;targetGlobalSettings;targetGlobalSettings;globalSettings;global settings;global settings;at.js;function;clientCode;clientcode;serverDomain;serverDomain;cookieDomain;cookieDomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentContent ibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optoutEnabled;opt out;SeltorsPollingTimeout;dataProviders
description: Informazioni sulla funzione targetGlobalSettings() per la libreria JavaScript at.js di Adobe Target.
title: Informazioni sulla funzione targetGlobalSettings() per la libreria JavaScript at.js di Adobe Target.
subtopic: Introduzione
topic: Standard
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# targetGlobalSettings()

È possibile modificare le impostazioni nella libreria at.js con `targetGlobalSettings()`, anziché configurare le impostazioni nell’interfaccia utente [!DNL Target] di Standard/Premium o con le API REST.

In alcune situazioni, specialmente quando at.js viene fornito tramite [!DNL Dynamic Tag Management] (DTM) può essere necessario bypassare alcune impostazioni.

## Impostazioni {#section_42C759AE9B524A43B8659018677224B8}

È possibile modificare le seguenti impostazioni:

| Impostazioni | Tipo | Valore predefinito | Descrizione |
|--- |--- |--- |--- |
| serverState | Vedere "serverState" di seguito. | Vedere "serverState" di seguito. | Vedere "serverState" di seguito. |
| clientCode | Stringa | Valore impostato tramite l'interfaccia utente | Rappresenta il codice cliente |
| serverDomain | Stringa | Valore impostato tramite l'interfaccia utente | Rappresenta il server Edge di Target |
| cookieDomain | Stringa | Se possibile impostato su dominio di primo livello | Rappresenta il dominio utilizzato quando si salvano i cookie |
| crossDomain | Stringa | Valore impostato tramite l'interfaccia utente | Indica se il tracciamento tra domini diversi è abilitato o meno.<br>I valori consentiti sono:<ul><li>disabilitato</li><li>abilitato</li><li>solo x</li></ul> |
| timeout | Numero | Valore impostato tramite l'interfaccia utente | Rappresenta il timeout della richiesta Edge di Target |
| globalMboxAutoCreate | Booleano | Valore impostato tramite l'interfaccia utente | Indica se la richiesta mbox globale deve essere attivata o meno |
| visitorApiTimeout | Numero | 2000 ms = 2 s | Rappresenta il timeout della richiesta API dei visitatori |
| Abilitato | Booleano | true | Indica se at.js come libreria è abilitata, ovvero se deve eseguire operazioni o meno. Questa impostazione è utile per impostare i cookie di rinuncia o altre decisioni personalizzate che disabiliterebbero la funzionalità at.js |
| defaultContentHiddenStyle | Stringa | visibilità: nascosto | Utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()` o `mboxDefine()` per nascondere il contenuto predefinito |
| defaultContentVisibleStyle | Stringa | visibilità: visibile | Utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()` o `mboxDefine()` per rivelare l’offerta applicata, se del caso, o il contenuto predefinito |
| bodyHiddenStyle | Stringa | corpo {opacità: 0} | Utilizzato solo quando `globalMboxAutocreate === true` per minimizzare il rischio di visualizzazione momentanea di altro contenuto.<br>Per ulteriori informazioni, consulta [Gestione at.js della visualizzazione momentanea di altri contenuti](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md). |
| bodyHidingEnabled | Booleano | true | Utilizzato per controllare la visualizzazione momentanea di altri contenuti quando `target-global-mbox` viene utilizzato per fornire le offerte create nel Compositore esperienza visivo (offerte visive) |
| imsOrgId | Stringa | ID ORG IMS | Rappresenta l'ID ORG di IMS |
| secureOnly | Booleano | false | Indica se at.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. |
| overrideMboxEdgeServer | Booleano | true (true a partire da at.js versione 1.6.2) | Indica se è necessario utilizzare il dominio `<clientCode>.tt.omtrdc.net` o `mboxedge<clusterNumber>.tt.omtrdc.net`.<br>Se questo valore è true, il dominio `mboxedge<clusterNumber>.tt.omtrdc.net` verrà salvato in un cookie |
| overrideMboxEdgeServerTimeout | Numero | 1860000 = &gt; 31 minuti | Indica la validità del cookie contenente il valore `mboxedge<clusterNumber>.tt.omtrdc.net`. |
| optoutEnabled | Booleano | false | Indica se Target deve richiamare la funzione dell’API Visitor `isOptedOut()`. Ciò fa parte dell'abilitazione di Device Graph. |
| selectorsPollingTimeout | Numero | 5000 ms = 5 s | In at.js 0.9.6, Target ha introdotto questa nuova impostazione che può essere ignorata tramite `targetGlobalSettings`.<br>`selectorsPollingTimeout` rappresenta il tempo in cui il client è disposto ad attendere che tutti gli elementi identificati dai selettori vengano visualizzati nella pagina.<br>Le attività create tramite il Compositore esperienza visivo hanno offerte che contengono selettori. |
| dataProviders | Consulta “Fornitori di dati” di seguito. | Consulta “Fornitori di dati” di seguito. | Consulta “Fornitori di dati” di seguito. |

## Utilizzo {#section_9AD6FA3690364F7480C872CB55567FB0}

Questa funzione può essere definita prima che at.js sia caricato o in **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]** &gt; **[!UICONTROL Impostazioni codice]** &gt; **[!UICONTROL Intestazione della libreria]**.

Il campo di intestazione della libreria consente di entrare in JavaScript in formato libero. Il codice di personalizzazione deve avere un aspetto simile all'esempio seguente:

```
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## Fornitori di dati {#data-providers}

Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta globale di mbox. Supporta la raccolta di dati da più provider tramite richieste sincrone e asincrone. L'utilizzo di questo approccio semplifica la gestione della visualizzazione momentanea del contenuto della pagina predefinito, inclusi i timeout indipendenti per ogni provider per limitare l'impatto sulle prestazioni della pagina.

>[!NOTE]
>
>Fornitori di dati richiede [!DNL at.js] versione 1.3 o successive.

I video che seguono contengono ulteriori informazioni:

| Video | Descrizione |
|--- |--- |
| [Utilizzo di Fornitori di dati in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-feature-video-use.html) | Fornitori di dati è una funzionalità che ti permette di trasmettere facilmente dati da terze parti a Target. Un esempio di terza parte potrebbe essere un servizio meteo, un DMP o persino il tuo servizio web. Puoi utilizzare questi dati per generare tipi di pubblico e contenuti mirati e per arricchire il profilo del visitatore. |
| [Implementazione di Fornitori di dati in Adobe Target](https://helpx.adobe.com/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Dettagli di implementazione ed esempi di come utilizzare la funzione Fornitori di dati in Adobe Target per recuperare dati da fornitori di dati terzi e trasmetterli alla richiesta Target. |

L’impostazione `window.targetGlobalSettings.dataProviders` è un array dei fornitori di dati.

Ogni provider di dati dispone della struttura seguente:

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| name | Stringa | Nome del provider. |
| version | Stringa | Versione del fornitore. Questa chiave verrà utilizzata per l'evoluzione del fornitore. |
| timeout | Numero | Rappresenta il timeout del fornitore se si tratta di una richiesta di rete.  Questa chiave è facoltativa. |
| provider | Funzione | La funzione che contiene la logica di recupero dei dati del fornitore.<br>La funzione dispone di un solo parametro obbligatorio: `callback`. Il parametro di callback è una funzione che deve essere richiamata solo quando i dati sono stati recuperati correttamente o si visualizza un errore.<br>Il callback prevede due parametri:<ul><li>error: indica se si è verificato un errore. Se tutto è OK, questo parametro deve essere impostato su null.</li><li>parametri: oggetto JSON, che rappresenta i parametri che verranno inviati a una richiesta Target.</li></ul> |

Nell'esempio seguente viene illustrato il punto in cui il fornitore di dati utilizza l'esecuzione di sincronizzazione:

```
var syncDataProvider = { 
  name: "simpleDataProvider", 
  version: "1.0.0", 
  provider: function(callback) { 
    callback(null, {t1: 1}); 
  } 
}; 
  
window.targetGlobalSettings = { 
  dataProviders: [ 
    syncDataProvider 
  ] 
};
```

Dopo che at.js elabora `window.targetGlobalSettings.dataProviders`, la richiesta di Target conterrà un nuovo parametro: `t1=1`.

Di seguito è riportato un esempio se i parametri che desideri aggiungere alla richiesta di destinazione vengono recuperati da un servizio di terze parti, come Bluekai, Demandbase e così via:

```
var blueKaiDataProvider = { 
   name: "blueKai", 
   version: "1.0.0", 
   provider: function(callback) { 
      // simulating network request 
     setTimeout(function() { 
       callback(null, {t1: 1, t2: 2, t3: 3}); 
     }, 1000); 
   } 
} 
  
window.targetGlobalSettings = { 
   dataProviders: [ 
      blueKaiDataProvider 
   ] 
};
```

Dopo che at.js elabora `window.targetGlobalSettings.dataProviders`, la richiesta Target contiene parametri aggiuntivi: `t1=1`, `t2=2` e `t3=3`.

Nell'esempio seguente vengono utilizzati fornitori di dati per raccogliere dati dell'API meteo e inviarli parametri in una richiesta di Target. La richiesta di Target avrà parametri aggiuntivi, ad esempio `country` e `weatherCondition`.

```
var weatherProvider = { 
      name: "weather-api", 
      version: "1.0.0", 
      timeout: 2000, 
      provider: function(callback) { 
        var API_KEY = "caa84fc6f5dc77b6372d2570458b8699"; 
        var lat = 44.426767399999996; 
        var lon = 26.1025384; 
        var url = "//api.openweathermap.org/data/2.5/weather?lang=en"; 
        var data = { 
          lat: lat, 
          lon: lon, 
          appId: API_KEY 
        } 
 
        $.ajax({ 
          type: "GET", 
                url: url, 
          dataType: "json", 
          data: data, 
          success: function(data) { 
            console.log("Weather data", data); 
            callback(null, { 
              country: data.sys.country, 
              weatherCondition: data.weather[0].main 
            }); 
          }, 
          error: function(err) { 
            console.log("Error", err); 
            callback(err); 
          } 
        });         
      } 
    }; 
 
    window.targetGlobalSettings = { 
      dataProviders: [weatherProvider] 
    };
```

Quando si lavora con l'impostazione `dataProviders`, tieni presente quanto segue:

* Se i fornitori di dati aggiunti a `window.targetGlobalSettings.dataProviders` sono asincroni, verranno eseguiti in parallelo. La richiesta API dei visitatori verrà eseguita in parallelo con le funzioni aggiunte a `window.targetGlobalSettings.dataProviders` per consentire un tempo minimo di attesa.
* at.js non tenterà di memorizzare i dati nella cache. Se il fornitore di dati recupera i dati una sola volta, deve assicurarsi che i dati siano memorizzati nella cache e, quando viene invocata la funzione di fornitore di dati, deve servire i dati della cache per la seconda invocazione.

## serverState {#server-state}

`serverState` è un'impostazione disponibile in at.js v2.2+ che può essere utilizzata per ottimizzare le prestazioni della pagina quando viene implementata un'integrazione ibrida di Target. L'integrazione ibrida significa che stai utilizzando sia at.js v2.2+ sul lato client che l'API di consegna o un SDK Target sul lato server per distribuire esperienze. `serverState` consente a at.js v2.2+ di applicare esperienze direttamente dal contenuto recuperato sul lato server e restituito al client come parte della pagina che viene servita.

### Prerequisiti

Devi avere un'integrazione ibrida di [!DNL Target].

* **Lato** server:  Devi usare la nuova API [di](https://developers.adobetarget.com/api/delivery-api/) consegna o gli SDK [](https://developers.adobetarget.com/api/delivery-api/#section/SDKs)Target.
* **Lato** client: È necessario utilizzare [at.js versione 2.2 o successiva](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### Esempi di codice

Per capire meglio come funziona, vedi gli esempi di codice riportati di seguito che hai sul tuo server. Il codice presuppone che tu stia utilizzando l’SDK [](https://github.com/adobe/target-nodejs-sdk)Target Node.js.

```
// First, we fetch the offers via Target Node.js SDK API, as usual
const targetResponse = await targetClient.getOffers(options);
// A successfull response will contain Target Delivery API request and response objects, which we need to set as serverState
const serverState = {
  request: targetResponse.request,
  response: targetResponse.response
};
// Finally, we should set window.targetGlobalSettings.serverState in the returned page, by replacing it in a page template, for example
const PAGE_TEMPLATE = `
<!doctype html>
<html>
<head>
  ...
  <script>
    window.targetGlobalSettings = {
      overrideMboxEdgeServer: true,
      serverState: ${JSON.stringify(serverState, null, " ")}
    };
  </script>
  <script src="at.js"></script>
</head>
...
</html>
`;
// Return PAGE_TEMPLATE to the client ...
```

Un JSON dell'oggetto di esempio `serverState` per la preacquisizione della visualizzazione è il seguente:

```
{
 "request": {
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "context": {
   "channel": "web",
   "timeOffsetInMinutes": 0
  },
  "experienceCloud": {
   "analytics": {
    "logging": "server_side",
    "supplementalDataId": "7D3AA246CC99FD7F-1B3DD2E75595498E"
   }
  },
  "prefetch": {
   "views": [
    {
     "address": {
      "url": "my.testsite.com/"
     }
    }
   ]
  }
 },
 "response": {
  "status": 200,
  "requestId": "076ace1cd3624048bae1ced1f9e0c536",
  "id": {
   "tntId": "08210e2d751a44779b8313e2d2692b96.21_27"
  },
  "client": "testclient",
  "edgeHost": "mboxedge21.tt.omtrdc.net",
  "prefetch": {
   "views": [
    {
     "name": "home",
     "key": "home",
     "options": [
      {
       "type": "actions",
       "content": [
        {
         "type": "setHtml",
         "selector": "#app > DIV.app-container:eq(0) > DIV.page-container:eq(0) > DIV:nth-of-type(2) > SECTION.section:eq(0) > DIV.container:eq(1) > DIV.heading:eq(0) > H1.title:eq(0)",
         "cssSelector": "#app > DIV:nth-of-type(1) > DIV:nth-of-type(1) > DIV:nth-of-type(2) > SECTION:nth-of-type(1) > DIV:nth-of-type(2) > DIV:nth-of-type(1) > H1:nth-of-type(1)",
         "content": "<span style=\"color:#FF0000;\">Latest</span> Products for 2020"
        }
       ],
       "eventToken": "t0FRvoWosOqHmYL5G18QCZNWHtnQtQrJfmRrQugEa2qCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
       "responseTokens": {
        "profile.memberlevel": "0",
        "geo.city": "dublin",
        "activity.id": "302740",
        "experience.name": "Experience B",
        "geo.country": "ireland"
       }
      }
     ],
     "state": "J+W1Fq18hxliDDJonTPfV0S+mzxapAO3d14M43EsM9f12A6QaqL+E3XKkRFlmq9U"
    }
   ]
  }
 }
}
```

Dopo che la pagina è stata caricata nel browser, at.js applica tutte le [!DNL Target] offerte da `serverState` subito, senza attivare chiamate di rete contro il [!DNL Target] bordo. Inoltre, at.js prenasconde solo gli elementi DOM per i quali [!DNL Target] sono disponibili offerte nel contenuto recuperato lato server, con un impatto positivo sulle prestazioni di caricamento delle pagine e sull'esperienza dell'utente finale.

### Note importanti

Considerate quanto segue quando utilizzate `serverState`:

* Al momento, at.js v2.2 supporta solo la distribuzione di esperienze tramite serverState per:

   * Attività create VEC che vengono eseguite al caricamento della pagina.
   * Viste prerecuperate.

      Nel caso di SPA che utilizzano [!DNL Target] Visualizzazioni e `triggerView()` nell'API at.js, at.js v2.2 memorizza nella cache il contenuto per tutte le Visualizzazioni prerecuperate sul lato server e le applica non appena ogni Visualizzazione viene attivata tramite `triggerView()`, di nuovo senza attivare chiamate di recupero di contenuto aggiuntive a Target.

   * **Nota**:  Attualmente, le mbox recuperate sul lato server non sono supportate in `serverState`.

* Quando applicate `serverState `le offerte, at.js prende in considerazione `pageLoadEnabled` e `viewsEnabled` le impostazioni, ad esempio le offerte di caricamento pagina non verranno applicate se l' `pageLoadEnabled` impostazione è false.

   Per attivare queste impostazioni, attivate l’interruttore in Configurazione **[UICONTROL &gt; Implementazione &gt; Modifica impostazioni &gt; Caricamento pagina abilitato]**.

   ![Impostazioni abilitate per il caricamento della pagina](/help/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

### Risorse aggiuntive

Per ulteriori informazioni sul `serverState` funzionamento, consulta le risorse seguenti:

* [Codice](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate)di esempio.
* [App SPA (Single Page Application) con `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo)