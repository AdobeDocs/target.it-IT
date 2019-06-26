---
description: 'Informazioni sulla funzione targetGlobalSettings() per at.js. '
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Informazioni sulla funzione targetGlobalSettings() per la libreria JavaScript at.js di Adobe Target.
seo-title: Informazioni sulla funzione targetGlobalSettings() per la libreria JavaScript at.js di Adobe Target.
solution: Target
subtopic: Introduzione
title: targetGlobalSettings()
topic: Standard
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# targetGlobalSettings()

È possibile modificare le impostazioni nella libreria at.js con `targetGlobalSettings()`, anziché configurare le impostazioni nell’interfaccia utente [!DNL Target] di Standard/Premium o con le API REST.

In alcune situazioni, specialmente quando at.js viene fornito tramite [!DNL Dynamic Tag Management] (DTM) può essere necessario bypassare alcune impostazioni.

## Impostazioni {#section_42C759AE9B524A43B8659018677224B8}

È possibile modificare le seguenti impostazioni:

| Impostazioni | Tipo | Valore predefinito | Descrizione |
|--- |--- |--- |--- |
| clientCode | Stringa | Valore impostato tramite l&#39;interfaccia utente | Rappresenta il codice cliente |
| serverDomain | Stringa | Valore impostato tramite l&#39;interfaccia utente | Rappresenta il server Edge di Target |
| cookieDomain | Stringa | Se possibile impostato su dominio di primo livello | Rappresenta il dominio utilizzato quando si salvano i cookie |
| crossDomain | Stringa | Valore impostato tramite l&#39;interfaccia utente | Indica se il tracciamento tra domini diversi è abilitato o meno.<br>I valori consentiti sono:<ul><li>disabilitato</li><li>abilitato</li><li>solo x</li></ul> |
| timeout | Numero | Valore impostato tramite l&#39;interfaccia utente | Rappresenta il timeout della richiesta Edge di Target |
| globalMboxAutoCreate | Booleano | Valore impostato tramite l&#39;interfaccia utente | Indica se la richiesta mbox globale deve essere attivata o meno |
| visitorApiTimeout | Numero | 2000 ms = 2 s | Rappresenta il timeout della richiesta API dei visitatori |
| Abilitato | Booleano | true | Indica se at.js come libreria è abilitata, ovvero se deve eseguire operazioni o meno. Questa impostazione è utile per impostare i cookie di rinuncia o altre decisioni personalizzate che disabiliterebbero la funzionalità at.js |
| defaultContentHiddenStyle | Stringa | visibilità: nascosto | Utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()` o `mboxDefine()` per nascondere il contenuto predefinito |
| defaultContentVisibleStyle | Stringa | visibilità: visibile | Utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()` o `mboxDefine()` per rivelare l’offerta applicata, se del caso, o il contenuto predefinito |
| bodyHiddenStyle | Stringa | corpo {opacità: 0} | Utilizzato solo quando `globalMboxAutocreate === true` per minimizzare il rischio di visualizzazione momentanea di altro contenuto.<br>Per ulteriori informazioni, consulta [Gestione at.js della visualizzazione momentanea di altri contenuti](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md). |
| bodyHidingEnabled | Booleano | true | Utilizzato per controllare la visualizzazione momentanea di altri contenuti quando `target-global-mbox` viene utilizzato per fornire le offerte create nel Compositore esperienza visivo (offerte visive) |
| imsOrgId | Stringa | ID ORG IMS | Rappresenta l&#39;ID ORG di IMS |
| secureOnly | Booleano | false | Indica se at.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. |
| overrideMboxEdgeServer | Booleano | true (true a partire da at.js versione 1.6.2) | Indica se è necessario utilizzare il dominio `<clientCode>.tt.omtrdc.net` o `mboxedge<clusterNumber>.tt.omtrdc.net`.<br>Se questo valore è true, il dominio `mboxedge<clusterNumber>.tt.omtrdc.net` verrà salvato in un cookie |
| overrideMboxEdgeServerTimeout | Numero | 1860000 = &gt; 31 minuti | Indica la validità del cookie contenente il valore `mboxedge<clusterNumber>.tt.omtrdc.net`. |
| optoutEnabled | Booleano | false | Indica se Target deve richiamare la funzione dell’API Visitor `isOptedOut()`. Ciò fa parte dell&#39;abilitazione di Device Graph. |
| selectorsPollingTimeout | Numero | 5000 ms = 5 s | In at.js 0.9.6, Target ha introdotto questa nuova impostazione che può essere ignorata tramite `targetGlobalSettings`.<br>`selectorsPollingTimeout` rappresenta il tempo in cui il client è disposto ad attendere che tutti gli elementi identificati dai selettori vengano visualizzati nella pagina.<br>Le attività create tramite il Compositore esperienza visivo hanno offerte che contengono selettori. |
| dataProviders | Consulta “Fornitori di dati” di seguito. | Consulta “Fornitori di dati” di seguito. | Consulta “Fornitori di dati” di seguito. |

## Utilizzo {#section_9AD6FA3690364F7480C872CB55567FB0}

Questa funzione può essere definita prima che at.js sia caricato o in **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]** &gt; **[!UICONTROL Modifica impostazioni at.js]** &gt; **[!UICONTROL Impostazioni codice]** &gt; **[!UICONTROL Intestazione della libreria]**.

Il campo di intestazione della libreria consente di entrare in JavaScript in formato libero. Il codice di personalizzazione deve avere un aspetto simile all&#39;esempio seguente:

```
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## Fornitori di dati {#data-providers}

Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta globale di mbox. Supporta la raccolta di dati da più provider tramite async e le richieste di sincronizzazione. L&#39;utilizzo di questo approccio semplifica la gestione della visualizzazione momentanea del contenuto della pagina predefinito, inclusi i timeout indipendenti per ogni provider per limitare l&#39;impatto sulle prestazioni della pagina.

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
| version | Stringa | Versione del fornitore. Questa chiave verrà utilizzata per l&#39;evoluzione del fornitore. |
| timeout | Numero | Rappresenta il timeout del fornitore se si tratta di una richiesta di rete.  Questa chiave è facoltativa. |
| provider | Funzione | La funzione che contiene la logica di recupero dei dati del fornitore.<br>La funzione dispone di un solo parametro obbligatorio: `callback`. Il parametro di callback è una funzione che deve essere richiamata solo quando i dati sono stati recuperati correttamente o si visualizza un errore.<br>Il callback prevede due parametri:<ul><li>error: indica se si è verificato un errore. Se tutto è OK, questo parametro deve essere impostato su null.</li><li>parametri: oggetto JSON, che rappresenta i parametri che verranno inviati a una richiesta Target.</li></ul> |

Nell&#39;esempio seguente viene illustrato il punto in cui il fornitore di dati utilizza l&#39;esecuzione di sincronizzazione:

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

Nell&#39;esempio seguente vengono utilizzati fornitori di dati per raccogliere dati dell&#39;API meteo e inviarli parametri in una richiesta di Target. La richiesta di Target avrà parametri aggiuntivi, ad esempio `country` e `weatherCondition`.

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

Quando si lavora con l&#39;impostazione `dataProviders`, tieni presente quanto segue:

* Se i fornitori di dati aggiunti a `window.targetGlobalSettings.dataProviders` sono asincroni, verranno eseguiti in parallelo. La richiesta API dei visitatori verrà eseguita in parallelo con le funzioni aggiunte a `window.targetGlobalSettings.dataProviders` per consentire un tempo minimo di attesa.
* at.js non tenterà di memorizzare i dati nella cache. Se il fornitore di dati recupera i dati una sola volta, deve assicurarsi che i dati siano memorizzati nella cache e, quando viene invocata la funzione di fornitore di dati, deve servire i dati della cache per la seconda invocazione.
