---
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Target Analytics;configurazione di suite di rapporti
description: Segui i passaggi necessari per implementare Analytics for Target (A4T) nelle soluzioni Adobe Target e Adobe Analytics.
title: Come si implementa Analytics for Target (A4T)?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: 4abf975095c5e29eea42d67119a426a3922d8d79
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 29%

---


# Implementazione di Analytics for Target{#analytics-for-target-implementation}

Sono necessari diversi passaggi per implementare [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T).

## Passaggi di implementazione {#section_73961BAD5BB4430A95E073DE5C026277}

Le sezioni seguenti descrivono i passaggi necessari per implementare questa integrazione nel sito.

## Passaggio 1: Richiedere il provisioning per Analytics e Target

Dopo aver implementato [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], è necessario eseguire il provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizza questo modulo per richiedere il provisioning](http://www.adobe.com/go/audiences).

## Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell’account utente devono essere soddisfatti prima di poter creare un’attività basata su [!DNL Analytics] in [!DNL Target]. Consulta [Requisiti delle autorizzazioni utente](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni [!DNL Adobe Experience Cloud]. Implementa o effettua la migrazione alla versione richiesta del servizio ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Consulta [Implementare il servizio Experience Cloud ID per Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) nella documentazione *Servizio ID visitatore di Experience Cloud* .

## Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

Implementa o esegui la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, consulta [Panoramica sull&#39;implementazione JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) nella *Guida all&#39;implementazione di Analytics*.

Per una migrazione, consulta [Migrazione ad AppMeasurement per JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) nella *Guida all’implementazione di Analytics*.

## Passaggio 5: Scaricare e aggiornare at.js

Implementa o esegui la migrazione alla versione richiesta di at.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Passaggio 6: Host at.js

Se at.js è stato distribuito in precedenza, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

## Passaggio 7: Fai riferimento a at.js su tutte le pagine del sito {#step7}

Includi at.js sotto VisitorAPI.js aggiungendo la seguente riga di codice nel tag in ogni pagina:

Per at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Il file VisitorAPI.js deve essere caricato prima di at.js. Se stai aggiornando un file at.js o mbox.js esistente, assicurati di verificare l’ordine di caricamento.

L’impostazione predefinita per l’integrazione [!DNL Target] e [!DNL Analytics], dal punto di vista dell’implementazione, consiste nell’utilizzare l’identificatore SDID passato dalla pagina per unire automaticamente sul backend le richieste [!DNL Target] e [!DNL Analytics] .

Puoi controllare come e quando inviare i dati analitici relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting. Se non desideri accettare le impostazioni predefinite per l’unione automatica dei dati di analisi [!DNL Target] e [!DNL Analytics] tramite l’identificatore SDID, imposta **analyticsLogging = client_side** tramite **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

Ad esempio:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Questa configurazione ha un effetto globale, il che significa che ogni chiamata effettuata da at.js ha **analyticsLogging: &quot;client_side&quot;** inviato all&#39;interno delle richieste [!DNL Target] e viene restituito un payload di Analytics per ogni richiesta. Quando questa opzione è impostata, il formato del payload restituito è simile al seguente:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Il payload può quindi essere inoltrato ad Analytics tramite l’ [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Per le attività di Allocazione automatica e Targeting automatico, devi anche inoltrare l’ID sessione. Per ulteriori informazioni, consulta [Reporting di Analytics for Target (A4T)](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) nella guida *SDK di Adobe Target* .

Se non desideri usare un’impostazione globale e preferisci un approccio più on-demand, utilizza la funzione at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) passando **analyticsLogging: &quot;client_side&quot;**. Il payload di Analytics viene restituito solo per questa chiamata e il backend [!DNL Target] non inoltra il payload a [!DNL Analytics]. Seguendo questo approccio, ogni richiesta at.js [!DNL Target] restituisce il payload per impostazione predefinita, ma solo quando desiderato e specificato.

Ad esempio:

```javascript
adobe.target.getOffers({
      request: {
        experienceCloud: {
          analytics: {
            logging: "client_side"
          }
        },
        prefetch: {
          mboxes: [{
            index: 0,
            name: "a1-serverside-xt"
          }]
        }
      }
    })
    .then(console.log)
```

Questa chiamata richiama una risposta dalla quale è possibile estrarre il payload di Analytics.

La risposta si presenta come segue:

```javascript
{
  "prefetch": {
    "mboxes": [{
      "index": 0,
      "name": "a1-serverside-xt",
      "options": [{
        "content": "<img src=\"http://s7d2.scene7.com/is/image/TargetAdobeTargetMobile/L4242-xt-usa?tm=1490025518668&fit=constrain&hei=491&wid=980&fmt=png-alpha\"/>",
        "type": "html",
        "eventToken": "n/K05qdH0MxsiyH4gX05/2qipfsIHvVzTQxHolz2IpSCnQ9Y9OaLL2gsdrWQTvE54PwSz67rmXWmSnkXpSSS2Q==",
        "responseTokens": {
          "profile.memberlevel": "0",
          "geo.city": "bucharest",
          "activity.id": "167169",
          "experience.name": "USA Experience",
          "geo.country": "romania"
        }
      }],
      "analytics": {
        "payload": {
          "pe": "tnt",
          "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
        }
      }
    }]
  }
}
```

Il payload può quindi essere inoltrato a [!DNL Analytics] tramite l’ [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

## Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri `mboxMCSDID`[!DNL Target] nelle chiamate di corrispondano al valore del parametro `sdid`[!DNL Analytics] nella chiamata di visualizzazione della pagina 

È particolarmente importante confermare che questi valori corrispondono nelle applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

**Nota:** per il corretto funzionamento di A4T è necessaria la corrispondenza di questi valori.

## Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

Adobe consiglia di rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

## Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In [!DNL Target], fai clic su **[!UICONTROL Amministrazione > Compositore esperienza visivo]** e scegli **[!UICONTROL Seleziona per attività]** o **[!UICONTROL Adobe Analytics]** per abilitare le opzioni.

* **[!UICONTROL Seleziona per attività consente di scegliere tra e per la creazione di ogni attività.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe imposta Analytics come origine dei rapporti per tutte le attività che hai creato.]**[!DNL Analytics]

