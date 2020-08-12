---
keywords: A4T;Adobe Analytics;Analytics-based activity;Analytics report suite;report suite;Analytics Target integration;configure report suite
description: Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).
title: Implementazione di Analytics for Target
feature: null
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 63%

---


# Implementazione di Analytics for Target{#analytics-for-target-implementation}

Several steps are required when implementing [!DNL Adobe Analytics] as the reporting source for [!DNL Target] (A4T).

## Implementation steps {#section_73961BAD5BB4430A95E073DE5C026277}

Le sezioni seguenti descrivono i passaggi necessari per implementare questa integrazione nel sito.

## Passaggio 1: Richiesta di provisioning per Analytics e Target

After you implement [!DNL Analytics] as the reporting source for [!DNL Target], you must be provisioned for [!DNL Analytics] and [!DNL Target]. [Utilizza questo modulo per richiedere il provisioning](http://www.adobe.com/go/audiences).

## Passaggio 2: Configurare le autorizzazioni utente

User account requirements must be met before you can create an [!DNL Analytics]-based activity in [!DNL Target]. See [User permission requirements](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni [!DNL Adobe Experience Cloud]. È necessario implementare o eseguire la migrazione alla versione richiesta del servizio ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

See [Implement the Experience Cloud ID Service for Target](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-target.html) in the *Experience Cloud Visitor ID Service* documentation.

## Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

È necessario implementare o eseguire la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, consultate Panoramica [dell&#39;implementazione](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript nella Guida *all&#39;implementazione di* Analytics.

Per una migrazione, vedi [Migrazione ad AppMeasurement per JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) nella Guida *all&#39;implementazione di* Analytics.

## Passaggio 5: Scaricare e aggiornare at.js o mbox.js

Devi implementare o eseguire la migrazione alla versione richiesta di at.js o mbox.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Passaggio 6: Hosting di at.js o mbox.js

Se at.js o mbox.js è stato distribuito in precedenza, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

## Passaggio 7: Includere un riferimento a at.js o mbox.js in tutte le pagine del sito {#step7}

Includi at.js o mbox.js sotto VisitorAPI.js aggiungendo la seguente riga di codice al tag in ogni pagina:

Per at.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Per mbox.js:

```
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/mbox.js"></script>
```

È essenziale che VisitorAPI.js sia caricato prima di at.js o mbox.js. Se stai aggiornando un file at.js o mbox.js esistente, assicurati di verificare l’ordine di caricamento.

The way the out-of-the-box settings are configured for [!DNL Target] and [!DNL Analytics] integration from an implementation perspective is to use the SDID that is passed from the page to stitch the [!DNL Target] and [!DNL Analytics] request together on the backend automatically for you.

However, if you want more control on how and when to send analytics data related to [!DNL Target] to [!DNL Analytics] for reporting purposes, and you do not want to opt-in to the default settings of having [!DNL Target] and [!DNL Analytics] automatically stitch the analytics data via the SDID, then you can set **analyticsLogging = client_side** via **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

Ad esempio:

```
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Questa configurazione ha un effetto globale. In altre parole, con ogni chiamata effettuata da at.js, **analyticsLogging: &quot;client_side&quot;** verrà inviato all’interno delle richieste e per ogni richiesta viene restituito un payload di Analytics. [!DNL Target] Con questa impostazione, il formato del payload restituito sarà simile a quello riportato di seguito:

```
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Il payload può quindi essere inoltrato ad Analytics tramite l&#39;API [di inserimento](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)dati.

Se non desideri usare un’impostazione globale a favore di un approccio di tipo on-demand, puoi utilizzare la funzione at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) per ottenere lo stesso risultato passando la chiamata **analyticsLogging: &quot;client_side&quot;**. The analytics payload will be returned for only this call and the [!DNL Target] backend will not forward the payload to [!DNL Analytics]. By pursuing this approach, every at.js [!DNL Target] request will not return the payload by default, but instead only when desired and specified.

Ad esempio:

```
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

```
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

Il payload può quindi essere inoltrato [!DNL Analytics] tramite l&#39;API [di inserimento](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)dati.

## Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri `mboxMCSDID`[!DNL Target] nelle chiamate di corrispondano al valore del parametro `sdid`[!DNL Analytics] nella chiamata di visualizzazione della pagina 

Tale conferma è particolarmente importante in applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

**Nota:** la corrispondenza di questi valori è necessaria per il corretto funzionamento di A4T.

## Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

È consigliabile rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice che potrebbe essere stato distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

## Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In [!DNL Target], click **[!UICONTROL Administation > Visual Experience Composer]** and choose either **[!UICONTROL Select per activity]** or **[!UICONTROL Adobe Analytics]** to enable the options.

* **[!UICONTROL Seleziona per attività consente di scegliere tra e per la creazione di ogni attività.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe imposta Analytics come origine dei rapporti per tutte le attività che hai creato.]**[!DNL Analytics]

