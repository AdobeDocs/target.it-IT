---
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Target Analytics;configurazione di suite di rapporti
description: Seguite i passaggi richiesti per implementare Analytics per Target (A4T) nelle soluzioni Adobe Target  e  Adobe Analytics.
title: Come posso implementare Analytics per Target (A4T)?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 48%

---


# Implementazione di Analytics for Target{#analytics-for-target-implementation}

Durante l&#39;implementazione di [!DNL Adobe Analytics] come origine di reporting per [!DNL Target] (A4T) sono necessari diversi passaggi.

## Passaggi di implementazione {#section_73961BAD5BB4430A95E073DE5C026277}

Le sezioni seguenti descrivono i passaggi necessari per implementare questa integrazione nel sito.

## Passaggio 1: Richiesta di provisioning per Analytics e Target

Dopo aver implementato [!DNL Analytics] come origine di reporting per [!DNL Target], è necessario eseguire il provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizza questo modulo per richiedere il provisioning](http://www.adobe.com/go/audiences).

## Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell&#39;account utente devono essere soddisfatti prima di poter creare un&#39;attività basata su [!DNL Analytics] in [!DNL Target]. Vedere [Requisiti delle autorizzazioni utente](/help/c-integrating-target-with-mac/a4t/account-reqs.md).

## Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni [!DNL Adobe Experience Cloud]. È necessario implementare o eseguire la migrazione alla versione richiesta del servizio ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Consulta [Implementazione del servizio ID Experience Cloud  per Target](https://experienceleague.adobe.com/docs/id-service/using/implementation-guides/setup-target.html) nella *Servizio ID visitatore del Experience Cloud* documentazione.

## Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

È necessario implementare o eseguire la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, vedi [Panoramica sull&#39;implementazione JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/javascript-implementation-overview.html) nella *Guida all&#39;implementazione di Analytics*.

Per una migrazione, vedete [Migrazione ad AppMeasurement per JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs-migrate.html) nella *Guida all&#39;implementazione di Analytics*.

## Passaggio 5: Scarica e aggiorna at.js

Devi implementare o migrare alla versione richiesta di at.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

## Passaggio 6: Host at.js

Se hai precedentemente distribuito at.js, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

## Passaggio 7: Riferimento a at.js su tutte le pagine del sito {#step7}

Includi at.js sotto VisitorAPI.js aggiungendo la seguente riga di codice nel tag in ogni pagina:

Per at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

È essenziale che VisitorAPI.js venga caricato prima di at.js. Se state aggiornando un file at.js o mbox.js esistente, accertatevi di verificare l&#39;ordine di caricamento.

Il modo in cui le impostazioni predefinite sono configurate per l&#39;integrazione [!DNL Target] e [!DNL Analytics] da un punto di vista di implementazione consiste nell&#39;utilizzare il codice SDID passato dalla pagina per unire automaticamente sul back-end la richiesta [!DNL Target] e [!DNL Analytics].

Tuttavia, se si desidera un maggiore controllo su come e quando inviare i dati di analisi relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting, e non si desidera optare per le impostazioni predefinite di [!DNL Target] e [!DNL Analytics] unire automaticamente i dati di analisi tramite SDID, è possibile impostare **analyticsLogging = client_side** tramite **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

Ad esempio:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Questa configurazione ha un effetto globale. In altre parole, con ogni chiamata effettuata da at.js, **analyticsLogging: &quot;client_side&quot;** verrà inviato all’interno delle richieste e per ogni richiesta viene restituito un payload di Analytics. [!DNL Target] Con questa impostazione, il formato del payload restituito sarà simile a quello riportato di seguito:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Il payload può quindi essere inoltrato ad Analytics tramite l&#39; [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Tenere presente che, per le attività [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target] sarà necessario inoltrare anche sessionId. Per ulteriori informazioni, vedi [Analytics for Target (A4T) reporting](https://adobetarget-sdks.gitbook.io/docs/integration-with-experience-cloud/analytics-for-target-a4t-reporting) nella *Adobe Target SDKs* guida.

Se non desideri usare un’impostazione globale a favore di un approccio di tipo on-demand, puoi utilizzare la funzione at.js [getOffers()](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md) per ottenere lo stesso risultato passando la chiamata **analyticsLogging: &quot;client_side&quot;**. Il payload di analisi verrà restituito solo per questa chiamata e il [!DNL Target] backend non inoltrerà il payload a [!DNL Analytics]. Seguendo questo approccio, ogni richiesta at.js [!DNL Target] non restituirà il payload per impostazione predefinita, ma solo quando desiderato e specificato.

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

Il payload può quindi essere inoltrato a [!DNL Analytics] tramite l&#39; [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

## Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri `mboxMCSDID`[!DNL Target] nelle chiamate di corrispondano al valore del parametro `sdid`[!DNL Analytics] nella chiamata di visualizzazione della pagina 

Tale conferma è particolarmente importante in applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

**Nota:** la corrispondenza di questi valori è necessaria per il corretto funzionamento di A4T.

## Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

È consigliabile rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice che potrebbe essere stato distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

## Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In [!DNL Target], fate clic su **[!UICONTROL Amministrazione > Visual Experience Composer (Compositore esperienza visivo)]** e scegliete **[!UICONTROL Seleziona per attività]** o **[!UICONTROL Adobe Analytics]** per attivare le opzioni.

* **[!UICONTROL Seleziona per attività consente di scegliere tra e per la creazione di ogni attività.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe imposta Analytics come origine dei rapporti per tutte le attività che hai creato.]**[!DNL Analytics]

