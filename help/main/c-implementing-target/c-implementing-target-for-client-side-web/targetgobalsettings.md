---
keywords: serverstate;targetGlobalSettings;targetglobalsettings;globalSettings;globalsettings;impostazioni globali;at.js;funzioni;funzione;clientCode;clientcode;serverDomain;serverdomain;cookieDomain;cookiedomain;crossDomain;crossdomain;timeout;globalMboxAutoCreate;visitorApiTimeout;defaultContentHiddenStyle;defaultContentVisibleStyle;bodyHiddenStyle;bodyHidingEnabled;imsOrgId;secureOnly;overrideMboxEdgeServer;overrideMboxEdgeServerTimeout;optoutEnabled;optout;opt out;selectorsPollingTimeout;dataProviders;Personalizzazione ibrida;deviceIdLifetime
description: Utilizza la funzione targetGlobalSettings() per l'Adobe [!DNL Target] libreria JavaScript at.js per sostituire le impostazioni anziché utilizzare la [!DNL Target] Interfaccia utente o API REST.
title: Come si utilizza la funzione targetGlobalSettings()?
feature: at.js
role: Developer
exl-id: 14080cf6-6a15-4829-b95d-62c068898564
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '2364'
ht-degree: 98%

---

# targetGlobalSettings()

È possibile modificare le impostazioni nella libreria at.js con `targetGlobalSettings()`, anziché configurare le impostazioni nell’interfaccia utente [!DNL Target] di Standard/Premium o con le API REST.

## Impostazioni {#section_42C759AE9B524A43B8659018677224B8}

È possibile modificare le seguenti impostazioni:

### bodyHiddenStyle

* **Tipo**: String
* **Valore predefinito**: body { opacity: 0 }
* **Descrizione**: utilizzato solo quando `globalMboxAutocreate === true` per minimizzare il rischio di sfarfallio.

   Per ulteriori informazioni, consulta [Gestione at.js della visualizzazione momentanea di altri contenuti](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/manage-flicker-with-atjs.md).

### bodyHidingEnabled

* **Tipo**: booleano
* **Valore predefinito**: true
* **Descrizione**: utilizzato per controllare lo sfarfallio quando `target-global-mbox` viene utilizzato per fornire le offerte create nel Compositore esperienza visivo (offerte visive).

### clientCode

* **Tipo**: String
* **Valore predefinito**: valore impostato tramite l’interfaccia utente.
* **Descrizione**: rappresenta il codice client.

### cookieDomain

* **Tipo**: String
* **Valore predefinito**: se possibile, imposta il dominio di primo livello.
* **Descrizione**: rappresenta il dominio utilizzato quando si salvano i cookie.

### crossDomain

* **Tipo**: String
* **Valore predefinito**: valore impostato tramite l’interfaccia utente.
* **Descrizione**: indica se il tracciamento tra domini diversi è abilitato o meno. I valori consentiti sono: disabilitato, abilitato o solo x.

### cspScriptNonce

* **Tipo**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.
* **Valore predefinito**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.
* **Descrizione**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.

### cspStyleNonce

* **Tipo**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.
* **Valore predefinito**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.
* **Descrizione**: consulta [Criteri di sicurezza dei contenuti](#content-security) di seguito.

### dataProviders

* **Tipo**: consulta [Fornitori di dati](#data-providers) di seguito.
* **Valore predefinito**: consulta [Fornitori di dati](#data-providers) di seguito.
* **Descrizione**: consulta [Fornitori di dati](#data-providers) di seguito.

### decisioningMethod {#on-device-decisioning}

* **Tipo**: String
* **Valore predefinito**: lato server
* **Altri valori**: su dispositivo, ibrido
* **Descrizione**: consulta Metodi di decisione di seguito.

   **Metodi di decisione**

   Con le decisioni sul dispositivo, in Target viene introdotta una nuova impostazione denominata [!UICONTROL Metodo di decisione] che determina il modo in cui at.js distribuisce le esperienze. `decisioningMethod` ha tre valori: solo lato server, solo su dispositivo e ibrido. Quando `decisioningMethod` viene impostato in `targetGlobalSettings()`, agisce come metodo di decisione predefinito per tutte le decisioni di [!DNL Target].

   **[!UICONTROL Solo lato server]**:

   [!UICONTROL Solo lato server] è il metodo decisionale predefinito impostato automaticamente quando at.js 2.5+ viene implementato e distribuito sulle proprietà web.

   Se si utilizza [!UICONTROL Solo lato server] come configurazione predefinita, tutte le decisioni vengono prese sulla rete Edge di [!DNL Target], il che comporta una chiamata di blocco al server. Questo approccio può introdurre una latenza incrementale, ma offre anche vantaggi significativi, come la possibilità di applicare le funzionalità di machine learning di Target, come le attività [Consigli](/help/main/c-recommendations/recommendations.md), [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) e [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Inoltre, l’ottimizzazione delle esperienze personalizzate mediante l’utilizzo del profilo utente di Target (che viene mantenuto tra sessioni e canali diversi) può fornire risultati molto efficaci per la tua azienda.

   Infine, [!UICONTROL Solo lato server] consente di utilizzare Adobe Experience Cloud e di perfezionare i tipi di pubblico a cui rivolgersi grazie ai segmenti di Audience Manager e Adobe Analytics.

   **[!UICONTROL Solo su dispositivo]**:

   [!UICONTROL Solo su dispositivo] è il metodo decisionale che deve essere impostato in at.js 2.5+ quando le decisioni su dispositivo devono essere utilizzate solo in tutte le pagine web.

   Le decisioni sul dispositivo possono fornire esperienze e attività di personalizzazione a una velocità sorprendente, perché derivano da un artefatto di regole memorizzate nella cache che contiene tutte le attività che si qualificano per le decisioni sul dispositivo.

   Per ulteriori informazioni sulle attività che si qualificano per le decisioni su dispositivo, consulta la sezione sulle funzionalità supportate.

   Questo metodo decisionale deve essere utilizzato solo se le prestazioni sono altamente critiche in tutte le pagine che richiedono decisioni da [!DNL Target]. Inoltre, ricorda che quando viene selezionato questo metodo decisionale, le attività [!DNL Target] che non possono avvalersi delle decisioni su dispositivo non verranno consegnate o eseguite. La libreria at.js 2.5+ è configurata per cercare solo l’artefatto delle regole memorizzate nella cache per prendere decisioni.

   **Ibrido**:

   [!UICONTROL Ibrido] è il metodo decisionale che deve essere impostato in at.js 2.5+ quando è necessario eseguire sia le decisioni su dispositivo che le attività che richiedono una chiamata alla rete Edge di Adobe Target.

   Quando gestisci sia le attività di decisione su dispositivo che quelle lato server, può essere un po’ complicato e noioso pensare a come distribuire ed eseguire il provisioning di [!DNL Target] sulle pagine. Con il metodo decisionale ibrido, [!DNL Target] sa quando deve effettuare una chiamata al server alla rete Edge di Adobe Target per le attività che richiedono l’esecuzione lato server e anche quando eseguire solo le decisioni su dispositivo.

   L’artefatto delle regole JSON include i metadati che informano at.js se una mbox ha un’attività lato server in esecuzione o un’attività decisionale su dispositivo. Questo metodo decisionale assicura che le attività che intendi consegnare rapidamente vengano eseguite tramite le decisioni su dispositivo, e che quelle che richiedono una personalizzazione basata su ML più potente vengano eseguite tramite la rete Edge di Adobe Target.

### defaultContentHiddenStyle

* **Tipo**: String
* **Valore predefinito**: visibilità: nascosto
* **Descrizione**: utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()`, o `mboxDefine()` per nascondere il contenuto predefinito.

### defaultContentVisibleStyle

* **Tipo**: String
* **Valore predefinito**: visibilità: visibile
* **Descrizione**: utilizzato solo per il wrapping di mbox che utilizzano DIV con il nome di classe “mboxDefault” e vengono eseguiti tramite `mboxCreate()`, `mboxUpdate()` o `mboxDefine()` per rivelare l’offerta applicata, se presente, o il contenuto predefinito.

### deviceIdLifetime

* **Tipo**: numero
* **Valore predefinito**: 63244800000 ms = 2 anni
* **Descrizione**: quantità di tempo in cui `deviceId` viene mantenuto nei cookie.

>[!NOTE]
>
>L’impostazione deviceIdLifetime è sovrascrivibile in at.js versione 2.3.1 o successiva.

### abilitato

* **Tipo**: booleano
* **Valore predefinito**: true
* **Descrizione**: quando questa opzione è abilitata, viene eseguita automaticamente una richiesta [!DNL Target] di recupero esperienze e di manipolazione DOM per il rendering delle esperienze. Inoltre, le chiamate di [!DNL Target] possono essere eseguite manualmente tramite `getOffer(s)` / `applyOffer(s)`.

   Se è disabilitata, le richieste di [!DNL Target] non vengono eseguite automaticamente o manualmente.

### globalMboxAutoCreate

* **Tipo**: numero
* **Valore predefinito**: valore impostato tramite l’interfaccia utente.
* **Descrizione**: indica se la richiesta mbox globale deve essere attivata o meno.

### imsOrgId

* **Tipo**: stringa
* **Valore predefinito**: true
* **Descrizione**: rappresenta l&#39;ID ORG di IMS.

### optinEnabled

* **Tipo**: booleano
* **Valore predefinito**: false
* **Descrizione**: [!DNL Target] fornisce supporto per la funzionalità di opt-in tramite [!DNL Adobe Experience Platform] per supportare la strategia di gestione dei consensi. La funzionalità opt-in consente ai clienti di controllare come e quando viene attivato il tag di [!DNL Target]. È inoltre presente un’opzione tramite [!DNL Adobe Experience Platform] per pre-approvare il tag di [!DNL Target]. Per abilitare la capacità di utilizzare la funzione di opt-in nella libreria at.js di [!DNL Target], aggiungi l’impostazione `optinEnabled=true`. In [!DNL Adobe Experience Platform], è necessario selezionare “abilita” dall’elenco a discesa [!UICONTROL Opt-In GDPR] nella visualizzazione di installazione dell’estensione. Per ulteriori informazioni, consulta la [documentazione di Adobe Experience Platform](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md). Per ulteriori informazioni su questa impostazione in relazione alle normative sulla privacy e la protezione dei dati, tra cui il Regolamento generale sulla protezione dei dati (GDPR) dell’Unione Europea e il California Consumer Privacy Act (CCPA), consulta [Normative sulla privacy e la protezione dei dati](/help/main/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).

### optoutEnabled

* **Tipo**: booleano
* **Valore predefinito**: false
* **Descrizione**: indica se Target deve richiamare la funzione `isOptedOut()` dell’API Visitor. Ciò fa parte dell&#39;abilitazione di Device Graph.

### overrideMboxEdgeServer

* **Tipo**: booleano
* **Valore predefinito**: true (true a partire dalla versione 1.6.2 di at.js)
* **Descrizione**: indica se è necessario utilizzare il dominio `<clientCode>.tt.omtrdc.net` o `mboxedge<clusterNumber>.tt.omtrdc.net`.

   Se questo valore è true, il dominio `mboxedge<clusterNumber>.tt.omtrdc.net` verrà salvato in un cookie. Attualmente non funziona con [CNAME](/help/main/c-implementing-target/c-considerations-before-you-implement-target/implement-cname-support-in-target.md) quando utilizzi versioni di at.js precedenti ad at.js 1.8.2 e at.js 2.3.1. Se questo è un problema, valuta l’[aggiornamento di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) a una versione più recente e supportata.

### overrideMboxEdgeServerTimeout

* **Tipo**: numero
* **Valore predefinito**: 1860000 => 31 minuti
* **Descrizione**: indica il periodo di vita del cookie contenente il valore `mboxedge<clusterNumber>.tt.omtrdc.net`.

### pageLoadEnabled

* **Tipo**: booleano
* **Valore predefinito**: true
* **Descrizione**: quando questa opzione è abilitata, recupera automaticamente le esperienze che devono essere restituite al caricamento della pagina.

### secureOnly

* **Tipo**: booleano
* **Valore predefinito**: false
* **Descrizione**: indica se at.js deve utilizzare solo HTTPS o può passare da HTTP a HTTPS in base al protocollo della pagina. Se è impostato su true, secureOnly imposta anche gli attributi Secure e SameSite sul cookie mbox.

### selectorsPollingTimeout

* **Tipo**: numero
* **Valore predefinito**: 5000 ms = 5 s
* **Descrizione**: in at.js 0.9.6, [!DNL Target] ha introdotto questa nuova impostazione che può essere sovrascritta tramite `targetGlobalSettings`.

   L’impostazione `selectorsPollingTimeout` rappresenta il tempo in cui il client è disposto ad attendere che tutti gli elementi identificati dai selettori vengano visualizzati nella pagina.

   Le attività create tramite il Compositore esperienza visivo hanno offerte che contengono selettori.

### serverDomain

* **Tipo**: String
* **Valore predefinito**: valore impostato tramite l’interfaccia utente.
* **Descrizione**: rappresenta il server Edge di Target.

### serverState

* **Tipo**: consulta [Personalizzazione ibrida](#server-state) di seguito.
* **Valore predefinito**: consulta [Personalizzazione ibrida](#server-state) di seguito.
* **Descrizione**: consulta [Personalizzazione ibrida](#server-state) di seguito.

### telemetryEnabled {#telemetry}

* **Tipo**: booleano
* **Valore predefinito**: true
* **Descrizione**: Quando abilitato, [!DNL Adobe] raccoglie dati di telemetria di prestazioni e utilizzo delle funzioni SDK. I dati personali non vengono raccolti.

### timeout

* **Tipo**: numero
* **Valore predefinito**: valore impostato tramite l’interfaccia utente.
* **Descrizione**: rappresenta il timeout della richiesta Edge di [!DNL Target].

### viewsEnabled

* **Tipo**: booleano
* **Valore predefinito**: true
* **Descrizione**: quando questa opzione è attivata, recupera automaticamente le visualizzazioni che devono essere restituite al caricamento della pagina. Le visualizzazioni sono supportate in at.js 2.*x.*

### visitorApiTimeout

* **Type**: numero
* **Valore predefinito**: 2000 ms = 2 s
* **Descrizione**: rappresenta il timeout della richiesta dell’[!UICONTROL API Visitor].

## Utilizzo {#section_9AD6FA3690364F7480C872CB55567FB0}

Questa funzione può essere definita prima che at.js sia caricato oppure in **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** > **[!UICONTROL Modifica impostazioni at.js]** > **[!UICONTROL Impostazioni codice]** > **[!UICONTROL Intestazione libreria]**.

Il campo di intestazione della libreria consente di entrare in JavaScript in formato libero. Il codice di personalizzazione deve avere un aspetto simile all&#39;esempio seguente:

```javascript
window.targetGlobalSettings = {  
   timeout: 200, // using custom timeout  
   visitorApiTimeout: 500, // using custom API timeout  
   enabled: document.location.href.indexOf('https://www.adobe.com') >= 0 // enabled ONLY on adobe.com  
};
```

## Fornitori dati  {#data-providers}

Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta globale di mbox. Supporta la raccolta di dati da più provider tramite richieste sincrone e asincrone. L&#39;utilizzo di questo approccio semplifica la gestione della visualizzazione momentanea del contenuto della pagina predefinito, inclusi i timeout indipendenti per ogni provider per limitare l&#39;impatto sulle prestazioni della pagina.

>[!NOTE]
>
>Fornitori di dati richiede [!DNL at.js] versione 1.3 o successive.

I video che seguono contengono ulteriori informazioni:

| Video | Descrizione |
|--- |--- |
| [Utilizzo di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-feature-video-use.html) | Fornitori di dati è una funzionalità che ti permette di trasmettere facilmente dati da terze parti a Target. Un esempio di terza parte potrebbe essere un servizio meteo, un DMP o persino il tuo servizio web. Puoi utilizzare questi dati per generare tipi di pubblico e contenuti mirati e per arricchire il profilo del visitatore. |
| [Implementazione di Fornitori di dati in Adobe Target](https://helpx.adobe.com/it/target/kt/using/dataProviders-atjs-technical-video-implement.html) | Dettagli di implementazione ed esempi di come utilizzare la funzione Fornitori di dati in Adobe Target per recuperare dati da fornitori di dati terzi e trasmetterli alla richiesta Target. |

L’impostazione `window.targetGlobalSettings.dataProviders` è un array dei fornitori di dati.

Ogni provider di dati dispone della struttura seguente:

| Chiave | Tipo | Descrizione |
|--- |--- |--- |
| name | Stringa | Nome del provider. |
| version | Stringa | Versione del fornitore. Questa chiave verrà utilizzata per l&#39;evoluzione del fornitore. |
| timeout | Numero | Rappresenta il timeout del fornitore se si tratta di una richiesta di rete.  Questa chiave è facoltativa. |
| provider | Funzione | La funzione che contiene la logica di recupero dei dati del fornitore.<br>La funzione dispone di un solo parametro obbligatorio: `callback`. Il parametro di callback è una funzione che deve essere richiamata solo quando i dati sono stati recuperati correttamente o si visualizza un errore.<br>Il callback prevede due parametri:<ul><li>error: indica se si è verificato un errore. Se tutto è OK, questo parametro deve essere impostato su null.</li><li>parametri: oggetto JSON, che rappresenta i parametri che verranno inviati a una richiesta Target.</li></ul> |

Nell&#39;esempio seguente viene illustrato il punto in cui il fornitore di dati utilizza l&#39;esecuzione di sincronizzazione:

```javascript
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

```javascript
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

```javascript
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

## Informativa sulla sicurezza dei contenuti {#content-security}

at.js 2.3.0+ supporta l’impostazione dei nonce della policy sulla sicurezza dei contenuti nei tag SCRIPT e STYLE aggiunti al DOM della pagina quando si applicano le offerte Target distribuite.

I nonce SCRIPT e STYLE devono essere impostati rispettivamente in `targetGlobalSettings.cspScriptNonce` e `targetGlobalSettings.cspStyleNonce` prima del caricamento di at.js 2.3.0+. Vedi un esempio qui sotto:

```javascript
...
<head>
 <script nonce="<script_nonce_value>">
window.targetGlobalSettings = {
  cspScriptNonce: "<csp_script_nonce_value>",
  cspStyleNonce: "<csp_style_nonce_value>"
};
 </script>
 <script nonce="<script_nonce_value>" src="at.js"></script>
...
</head>
...
```

Dopo aver specificato le impostazioni `cspScriptNonce` e `cspStyleNonce`, at.js 2.3.0+ le imposta come attributi nonce in tutti i tag SCRIPT e STYLE che aggiunge al DOM quando si applicano le offerte Target.

## Personalizzazione ibrida {#server-state}

`serverState` è un’impostazione disponibile in at.js v2.2+ che può essere utilizzata per ottimizzare le prestazioni della pagina quando è stata implementata un’integrazione ibrida di Target. Per integrazione ibrida si intende l’utilizzo sia di at.js v2.2+ sul lato client che dell’API di consegna o di un SDK Target sul lato server per distribuire le esperienze. `serverState` consente a at.js v2.2+ di applicare le esperienze direttamente dal contenuto recuperato sul lato server e restituito al client come parte della pagina trasmessa.

### Prerequisiti

È necessaria un’integrazione ibrida di [!DNL Target].

* **Lato server**: devi utilizzare la nuova [API di consegna](https://developers.adobetarget.com/api/delivery-api/) o gli [SDK di Target](https://developers.adobetarget.com/api/delivery-api/#section/SDKs).
* **Lato client**: devi utilizzare [at.js versione 2.2 o successiva](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

### Esempi di codice

Per capire meglio come funziona, vedi di seguito esempi di codice che potresti avere sul server. Il codice presuppone che tu stia utilizzando l’[SDK di Node.js di Target](https://github.com/adobe/target-nodejs-sdk).

```javascript
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

Ecco un esempio di oggetto JSON `serverState` per la preacquisizione della visualizzazione:

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

Dopo che la pagina è stata caricata nel browser, at.js applica immediatamente tutte le offerte [!DNL Target] da `serverState` senza attivare alcuna chiamata alla rete Edge di [!DNL Target]. Inoltre, at.js nasconde preventivamente solo gli elementi DOM per i quali sono disponibili delle offerte [!DNL Target] nel contenuto recuperato lato server, con un impatto positivo sulle prestazioni di caricamento delle pagine e sull’esperienza dell’utente finale.

### Note importanti

Quando utilizzi `serverState`, tieni presente quanto segue:

* Al momento, at.js v2.2 supporta solo la distribuzione di esperienze tramite serverState per:

   * Attività create dal Compositore esperienza visivo che vengono eseguite al caricamento della pagina.
   * Visualizzazioni preacquisite.

      Se utilizzi applicazioni a pagina singola con le visualizzazioni di [!DNL Target] e `triggerView()` nell’API at.js, at.js v2.2 memorizza in cache il contenuto di tutte le visualizzazioni preacquisite sul lato server e le applica non appena ogni visualizzazione viene attivata tramite `triggerView()`, di nuovo senza attivare altre chiamate a Target per il recupero dei contenuti.

   * **Nota**: attualmente, le mbox recuperate sul lato server non sono supportate in `serverState`.

* Quando applichi le offerte `serverState `, at.js prende in considerazione le impostazioni `pageLoadEnabled` e `viewsEnabled`, ad esempio le offerte di caricamento pagina non verranno applicate se `pageLoadEnabled` è impostato su false.

   Per attivare queste impostazioni, abilita l’opzione in **[!UICONTROL Amministrazione] > [!UICONTROL Implementazione] > [!UICONTROL Modifica] > [!UICONTROL Caricamento pagina abilitato]**.

   ![Impostazioni per Caricamento pagina attivato](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/assets/page-load-enabled-setting.png)

* Se utilizzi i tag `serverState` e `<script>` nel contenuto restituito, assicurati che il contenuto HTML utilizzi `<\/script>` invece di `</script>`. Se utilizzi `</script>`, il browser interpreta `</script>` come fine di uno SCRIPT in linea e potrebbe interrompere la pagina HTML.

### Risorse aggiuntive

Per ulteriori informazioni sul funzionamento di `serverState`, consulta le risorse seguenti:

* [Codice di esempio](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/advanced-atjs-integration-serverstate).
* [Esempio di applicazione a pagina singola con `serverState`](https://github.com/Adobe-Marketing-Cloud/target-node-client-samples/tree/master/react-shopping-cart-demo).
