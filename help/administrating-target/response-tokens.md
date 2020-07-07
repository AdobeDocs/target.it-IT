---
keywords: response tokens;tokens;plugins;plug-ins;at.js;response
description: I token di risposta consentono di restituire automaticamente informazioni specifiche di Target (dettagli dell'attività, informazioni del profilo utente, informazioni geografiche e così via) da utilizzare per il debug o l'integrazione con sistemi di terze parti (ad esempio, Clicktale)
title: Token di risposta in Adobe Target
subtopic: Getting Started
topic: Standard
uuid: 20561673-d762-4c3d-bedc-94aeab5053d7
translation-type: tm+mt
source-git-commit: dda60f13ee351428504fcebfbbfb1dd824319d65
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 81%

---


# Token di risposta{#response-tokens}

Response tokens let you automatically output information specific to [!DNL Target] (activity details, user profile information, geo information, and so forth) to use in debugging or integrating with 3rd-party systems (such as Clicktale).

>[!NOTE]
>
>The information in this topic has been updated to give you a sneak peak at the UI changes coming in the Target Standard/Premium 20.6.1 release (July 2020). La maggior parte delle informazioni presentate in questo argomento si applica all’interfaccia utente corrente; tuttavia, le opzioni potrebbero trovarsi in posizioni leggermente diverse.

I token di risposta consentono di scegliere quali variabili sfruttare e quindi di inviarle come parte di una risposta Target. Per fare ciò, è sufficiente abilitare una variabile utilizzando lo switch e la variabile verrà inviata con risposte Target, che possono essere convalidate nelle chiamate di rete. Response tokens work in [!UICONTROL Preview] mode as well.

Una differenza fondamentale tra i plug-in e i token di risposta è che i plug-in recapitano alla pagina un codice JavaScript che viene eseguito al momento del recapito. I token di risposta, invece, recapitano un oggetto che può quindi essere letto e utilizzato mediante i listener di eventi. Per ulteriori informazioni, consulta [Eventi personalizzati di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) e gli esempi forniti più avanti in questo articolo. L’approccio dei token di risposta è più sicuro e dovrebbe consentire uno sviluppo e una manutenzione più agevoli delle integrazioni di terze parti.

>[!NOTE]
>
>I token di risposta sono disponibili con at.js 1.1 o versione successiva. I token di risposta non sono supportati con mbox.js.

| Libreria di Target in uso | Azioni consigliate |
|--- |--- |
| at.js | Assicurati di utilizzare at.js nella versione 1.1 o successiva. Per informazioni su come scaricare l’ultima versione di at.js, consulta [Scaricare at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md). Per informazioni sulle nuove funzionalità in ogni versione di at.js, vedi [Dettagli sulla versione di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).<br>I clienti che utilizzano at.js sono incoraggiati a utilizzare i token di risposta e ad abbandonare i plug-in. Alcuni plug-in che si basano su metodi interni di mbox.js che non sono presenti in at.js verranno consegnati, ma non avranno esito positivo. Per ulteriori informazioni, consulta [Limitazioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-limitations.md). |
| mbox.js | I plug-in continueranno a essere supportati e consegnati utilizzando mbox.js.<br>Tuttavia, i clienti che utilizzano mbox.js e i plug-in sono invitati a passare ad at.js e ai token di risposta. Per informazioni sui vantaggi dell’utilizzo di at.js rispetto a mbox.js, consulta [Domande frequenti su at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/target-atjs-faq.md). Per informazioni sulla migrazione, consulta [Migrare a at.js da mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-migrate-atjs.md).<br>Dopo che Target Classic è stato dichiarato obsoleto (novembre 2017), potrebbe essere necessario contattare l’Assistenza clienti per modificare o disabilitare i plug-in esistenti. Dovresti aver controllato i plug-in prima che Target Classic venisse dichiarato obsoleto, e aver disabilitato i plug-in indesiderati.<br>Non è possibile creare nuovi plug-in in Target Standard/Premium. Al loro posto, utilizza piuttosto i token.<br>I plug-in obsoleti di SiteCatalyst devono essere disattivati e sostituiti con [Adobe Analytics come origine per la generazione di rapporti per Adobe Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T). Il plug-in ttMeta deve essere disabilitato e sostituito con [Adobe Experience Cloud Debugger](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). |

## Utilizzo dei token di risposta {#section_A9E141DDCBA84308926E68D05FD2AC62}

1. Assicurati di utilizzare [!DNL at.js] nella versione 1.1 o successiva.

   Per ulteriori informazioni, consulta [Scarica at.js](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_1E1F958F9CCC4E35AD97581EFAF659E2).

1. In [!DNL Target], click **[!UICONTROL Administration]** > **[!UICONTROL Response Tokens]**.

   ![](assets/response_tokens-new.png)

1. Attiva i token di risposta desiderati, ad esempio `activity.id`, `option.id` e così via.

   Per impostazione predefinita sono disponibili i seguenti parametri:

   | Tipo | Parametro | Note |
   |--- |--- |--- |
   | Profili incorporati | `profile.activeActivities` | Restituisce una matrice dei codici `activityIds` per i quali il visitatore si qualifica. Viene incrementato man mano che gli utenti si qualificano. Ad esempio, in una pagina con due mbox che forniscono due diverse attività, la seconda mbox includerà entrambe le attività. |
   |  | `profile.isFirstSession` | Restituisce “vero” o “falso”. |
   |  | `profile.isNewSession` | Restituisce “vero” o “falso”. |
   |  | `profile.daysSinceLastVisit` | Restituisce il numero di giorni dall’ultima visita del visitatore. |
   |  | `profile.tntId` | Restituisce il codice tntID del visitatore. |
   |  | `profile.marketingCloudVisitorId` | Restituisce l’ID visitatore di Experience Cloud per il visitatore in oggetto. |
   |  | `profile.thirdPartyId` | Restituisce l’ID di terze parti del visitatore. |
   |  | `profile.categoryAffinity` | Restituisce la categoria preferita del visitatore. |
   |  | `profile.categoryAffinities` | Restituisce una matrice delle 5 categorie principali del visitatore, sotto forma di stringhe. |
   | Attività | `activity.name`<br>`activity.id`<br>`experience.name`<br>`experience.id`<br>`option.name`<br>`option.id` | Dettagli dell’attività corrente. “Opzione” equivale a “offerta”. |
   | Geo | `geo.country`<br>`geo.state`<br>`geo.city`<br>`geo.zip`<br>`geo.dma`<br>`geo.domainName`<br>`geo.ispName`<br>`geo.connectionSpeed`<br>`geo.mobileCarrier` | Consulta [Geo](/help/c-target/c-audiences/c-target-rules/geo.md) per ulteriori informazioni sull’utilizzo del geotargeting nelle attività. |
   | Metodo<br>di allocazione del traffico (applicabile solo alle attività [!UICONTROL Auto-Target] e [!UICONTROL Automated Personalization (Personalizzazione] automatizzata). | `experience.trafficAllocationId` | Restituisce 0 se un visitatore ha ricevuto un&#39;esperienza dal traffico &quot;di controllo&quot; e 1 se ha ricevuto un&#39;esperienza dalla distribuzione del traffico &quot;di destinazione&quot;. |
   |  | `experience.trafficAllocationType` | Restituisce &quot;control&quot; o &quot;target&quot;. |

   Nell’elenco vengono visualizzati anche gli attributi del profilo utente e gli attributi del cliente.

   >[!NOTE]
   >
   >I parametri con caratteri speciali non vengono visualizzati nell’elenco. Sono supportati solo caratteri alfanumerici e il trattino basso.

1. (Conditional) If you want to use a profile parameter as a response token, but the parameter has not been passed through an mbox call and, thus, has not loaded into the Target UI, you can use the [!UICONTROL Add Response Token] button to add the profile to the UI.

   Fate clic su **[!UICONTROL Aggiungi token]** di risposta, fornite il nome del token, quindi fate clic su **[!UICONTROL Attiva]**.

   ![](assets/response_token_create.png)

1. Crea un’attività.

Usa gli [eventi personalizzati di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) per ascoltare la risposta della mbox e leggere i token di risposta.

Il codice di esempio seguente aggiunge un gestore di eventi personalizzati di [!DNL at.js] direttamente alla pagina HTML:

```
<html> 
  <head> 
    .... 
    <script src="at.js"></script> 
    <script> 
      document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
        console.log("Request succeeded", e.detail); 
      }); 
    </script> 
  <head> 
  <body> 
  ... 
  </body> 
</html>
```

Le istruzioni seguenti spiegano come aggiungere un gestore di eventi personalizzati di [!DNL at.js] utilizzando Adobe Dynamic Tag Manager (DTM):

1. Accedi a DTM.
1. Individua la proprietà appropriata.
1. Apri lo strumento Target.

   Poiché DTM non supporta at.js nativamente, è necessario utilizzare l’editor di codice.

1. Nell’editor di codice aggiungi il seguente codice a [!DNL at.js]:

   ```
   document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
     console.log("Request succeeded", e.detail); 
   });
   ```

Se desideri avere tutto in un singolo file, aggiungi lo snippet seguente al piè di pagina della libreria nella [pagina Configurazione di at.js](../c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/implementing-target-without-a-tag-manager.md#concept_2FA0456607D04F82B0539C5BF5309812).

```
document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
  console.log("Request succeeded", e.detail); 
});
```

## Domande frequenti sui token di risposta {#section_3DD5F32C668246289CDF9B4CDE1F536D}

**Quale ruolo è autorizzato ad attivare o disattivare i token di risposta?**

I token di risposta possono essere attivati o disattivati solo dagli utenti con il ruolo Amministratore di Target.

**Cosa succede se eseguo at.js 1.0 o versione precedente?**

Potrai visualizzare i token di risposta, ma at.js non sarà in grado di utilizzarli.

**Che cosa succede se uso at.js 1.1 (o versione successiva) su alcune pagine del sito e mbox.js su altre?**

I token di risposta verranno recapitati alle risposte mbox di [!DNL at.js], ma non alle risposte [!DNL mbox.js].

**È possibile avere attivi allo stesso tempo sia plug-in di Target Classic che i token di risposta?**

Plug-in e token di risposta saranno disponibili in parallelo; tuttavia, i plug-in diventeranno obsoleti in futuro.

**I token di risposta sono consegnati attraverso tutte le risposte mbox o solo attraverso le mbox che forniscono un’attività?**

I token di risposta vengono consegnati solo tramite le mbox che forniscono un’attività.

**Il mio plug-in di Target Classic comprendeva JavaScript. Come posso riprodurne la funzionalità utilizzando i token di risposta?**

Quando esegui la migrazione ai token di risposta, questo tipo di JavaScript dovrà essere mantenuto nel codebase o nella soluzione di gestione dei tag. Puoi attivare il codice utilizzando gli eventi personalizzati [!DNL at.js] e trasmettere i valori del token di risposta alle funzioni JavaScript.

**Perché il mio parametro profilo/attributi del cliente non viene visualizzato nell’elenco dei token di risposta?**

Target normalmente aggiorna i parametri ogni 15 minuti. L’aggiornamento dipende dall’azione dell’utente e i dati vengono aggiornati solo quando visualizzi la pagina dei token di risposta. Se i parametri non vengono visualizzati nell’elenco dei token di risposta, probabilmente Target non ha ancora aggiornato i dati.

Inoltre, se il parametro contiene caratteri non alfanumerici o un simbolo diverso dal trattino basso, il parametro non verrà visualizzato nell’elenco. Attualmente sono supportati solo caratteri alfanumerici e il trattino basso.

**Se creo un token di risposta utilizzando uno script di profilo o un parametro di profilo e poi elimino lo script o il parametro del profilo, il token di risposta consegnerà comunque il contenuto?**

I token di risposta estraggono informazioni dai profili utente e quindi recapitano tali informazioni. Se elimini uno script o un parametro di profilo, le informazioni non vengono necessariamente rimosse dai profili utente. I profili utente contengono ancora i dati corrispondenti allo script del profilo e il token di risposta continuerà a fornire il contenuto. Per gli utenti nel cui profilo non sono salvate tali informazioni oppure per i nuovi visitatori, il token non verrà consegnato perché i dati non sono presenti nei profili.

Target non disattiva automaticamente il token. Se elimini uno script di profilo e non desideri più che il token venga consegnato, devi disattivare il token manualmente.

**Ho rinominato il mio script di profilo, ma il token che utilizza lo script è ancora attivo con il vecchio nome. Perché?**

Come accennato in precedenza, i token di risposta funzionano sulle informazioni del profilo salvate per gli utenti. Anche se hai rinominato il tuo script di profilo, gli utenti che hanno visitato il tuo sito web hanno ancora il vecchio valore dello script di profilo salvato nel loro profilo, pertanto il token continua a prendere il vecchio valore dai profili utente. Se ora desideri consegnare il contenuto del nuovo nome, devi disattivare il token precedente e attivare quello nuovo.

**Se i miei attributi sono cambiati, quando saranno rimossi dall’elenco?**

Target esegue un aggiornamento degli attributi a intervalli regolari. Tutti gli attributi non attivati vengono rimossi durante l’aggiornamento successivo. Tuttavia, se hai un attributo che era stato attivato e quindi è stato rimosso (ad esempio, hai rimosso uno script di profilo che veniva utilizzato come token), lo script non viene rimosso dall’elenco degli attributi finché non sarà stato disattivato. Target rimuove dall’elenco solo gli attributi disattivati quando vengono eliminati o rinominati.

## Invio di dati a Google Analytics tramite at.js {#section_04AA830826D94D4EBEC741B7C4F86156}

Puoi inviare dati a Google Analytics tramite at.js aggiungendo il seguente codice alla pagina HTML:

```
<script type="text/javascript"> 
  (function(i, s, o, g, r, a, m) { 
    i['GoogleAnalyticsObject'] = r; 
    i[r] = i[r] || function() { 
      (i[r].q = i[r].q || []).push(arguments) 
    }, i[r].l = 1 * new Date(); 
    a = s.createElement(o), 
      m = s.getElementsByTagName(o)[0]; 
    a.async = 1; 
    a.src = g; 
    m.parentNode.insertBefore(a, m) 
  })(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga'); 
  ga('create', 'Google Client Id', 'auto'); 
</script> 
 
<script type="text/javascript"> 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function(e) { 
    var tokens = e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
 
    var activityNames = []; 
    var experienceNames = []; 
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      activityNames.push(token["activity.name"]); 
      experienceNames.push(token["experience.name"]); 
    }); 
 
    ga('send', 'event', { 
      eventCategory: "target", 
      eventAction: experienceNames, 
      eventLabel: activityNames 
    }); 
  }); 
 
  function isEmpty(val) { 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## Debug (simile al plug-in ttMeta) {#section_DB3392B6E80749C1BFB520732EDF3BCE}

L’equivalente del plug-in ttMeta per scopi di debug può essere creato aggiungendo il seguente codice alla pagina HTML:

```
<script type="text/javascript" > 
  document.addEventListener(adobe.target.event.REQUEST_SUCCEEDED, function (e) { 
    window.ttMETA= typeof(window.ttMETA)!="undefined" ? window.ttMETA : []; 
 
    var tokens=e.detail.responseTokens; 
 
    if (isEmpty(tokens)) { 
      return; 
    } 
     
    var uniqueTokens = distinct(tokens); 
 
    uniqueTokens.forEach(function(token) { 
      window.ttMETA.push({ 
        'CampaignName': token["activity.name"], 
        'CampaignId' : token["activity.id"], 
        'RecipeName': token["experience.name"], 
        'RecipeId': token["experience.id"], 
        'OfferId': token["option.id"], 
        'OfferName': token["option.name"], 
        'MboxName': e.detail.mbox}); 
      console.log(ttMETA); 
    }); 
  }); 
 
  function isEmpty(val){ 
    return (val === undefined || val == null || val.length <= 0) ? true : false; 
  } 
 
  function key(obj) { 
     return Object.keys(obj) 
    .map(function(k) { return k + "" + obj[k]; }) 
    .join(""); 
  } 
 
  function distinct(arr) { 
    var result = arr.reduce(function(acc, e) { 
      acc[key(e)] = e; 
      return acc; 
    }, {}); 
   
    return Object.keys(result) 
    .map(function(k) { return result[k]; }); 
  } 
</script>
```

## Video di formazione: Token di risposta ed eventi personalizzati at. js {#section_3AA0A6C8DBD94A528337A2525E3E05D5} ![Badge di esercitazione](/help/assets/tutorial.png)

Guarda il video seguente e scopri come utilizzare i token di risposta e gli eventi personalizzati at.js per condividere le informazioni del profilo da Target a sistemi di terze parti.

>[!VIDEO](https://video.tv.adobe.com/v/23253/)
