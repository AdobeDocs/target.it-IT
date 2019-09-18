---
description: Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Target Analytics;configurazione di suite di rapporti
seo-description: Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).
seo-title: Implementazione di Analytics for Target
solution: Target
title: Implementazione di Analytics for Target
topic: Premium
uuid: da6498c8-1549-4c36-ae42-38c731a28f08
translation-type: tm+mt
source-git-commit: 8dc94ca1ed48366e6b3ac7a75b03c214f1db71d9

---


# Implementazione di Analytics for Target{#analytics-for-target-implementation}

Sono necessari diversi passaggi per implementare Adobe Analytics come origine per la generazione di rapporti per Target (A4T).

## Passaggi di implementazione {#section_73961BAD5BB4430A95E073DE5C026277}

Nella tabella seguente sono illustrati i passaggi necessari per implementare questa integrazione nel sito.

## Passaggio 1: Richiedere il provisioning per Analytics e Target

Dopo aver implementato Analytics come origine di reporting per Target, è necessario ottenere il provisioning per entrambi. [Utilizza questo modulo per richiedere il provisioning](http://www.adobe.com/go/audiences).

## Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell'account utente devono essere soddisfatti prima di procedere alla creazione di un'attività basata su Adobe Analytics in Adobe Target. Consulta [Requisiti delle autorizzazioni utente](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni Experience Cloud. È necessario implementare o eseguire la migrazione alla versione richiesta del servizio ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Consulta [Implementazione del servizio Experience Cloud ID per Target](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/setup-target.html) nella documentazione del servizio ID visitatore di Experience Cloud.

## Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

È necessario implementare o eseguire la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, consultate Panoramica [dell'implementazione](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) JavaScript nella Guida *all'implementazione di* Analytics.

Per una migrazione, vedi [Migrazione ad AppMeasurement per JavaScript](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) nella Guida *all'implementazione di* Analytics.

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

Dal punto di vista dell’implementazione, le impostazioni predefinite per l’integrazione di Target e Analytics sono configurate in modo che l’identificatore SDID passato dalla pagina unisca automaticamente nel backend le richieste di Target e Analytics.

Tuttavia, se desideri un maggiore controllo su come e quando inviare i dati di analisi di Target ad Analytics a scopo di reporting, senza accettare le impostazioni predefinite per l’unione automatica dei dati di analisi di Target e Analytics tramite l’identificatore SDID, puoi impostare **analyticsLogging = client_side** tramite **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

Ad esempio:

```
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Questa configurazione ha un effetto globale. In altre parole, con ogni chiamata effettuata da at.js, **analyticsLogging: "client_side"** verrà inviato all’interno delle richieste Target e per ogni richiesta viene restituito un payload di Analytics. Con questa impostazione, il formato del payload restituito sarà simile a quello riportato di seguito:

```
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Il payload può quindi essere inoltrato ad Analytics tramite l'API [di inserimento](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)dati.

Se non desideri usare un’impostazione globale a favore di un approccio di tipo on-demand, puoi utilizzare la funzione at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) per ottenere lo stesso risultato passando la chiamata **analyticsLogging: "client_side"**. Il payload di Analytics verrà restituito solo per questa chiamata e il backend di Target non inoltrerà il payload ad Analytics. Con questo approccio, ogni richiesta di at.js di Target non restituirà il payload per impostazione predefinita, ma solo quando questo viene specificato.

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

Il payload può quindi essere inoltrato ad Analytics tramite l'API [di inserimento](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html)dati.

## Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri mboxMCSDID nelle chiamate di Target corrispondano al valore del parametro sdid nella chiamata di visualizzazione della pagina Analytics.

Tale conferma è particolarmente importante in applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

**Nota:** la corrispondenza di questi valori è necessaria per il corretto funzionamento di A4T.

## Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

È consigliabile rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice che potrebbe essere stato distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

## Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In Target, fai clic su [!UICONTROL Configurazione &gt; Preferenze] e scegli [!UICONTROL Seleziona per attività] o [!UICONTROL Adobe Analytics].

* Seleziona per attività consente di scegliere tra Target e Analytics per la creazione di ogni attività.
* Adobe Analytics imposta Analytics come origine dei rapporti per tutte le attività che hai creato.

