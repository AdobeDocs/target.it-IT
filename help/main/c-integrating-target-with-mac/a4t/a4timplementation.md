---
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Analytics Target;configurare suite di rapporti;at.js;atjs;adobe experience platform web sdk;aep web sdk;platform web sdk
description: Segui i passaggi necessari per implementare Analytics per [!DNL Target] (A4T) nell’Adobe [!DNL Target] e le soluzioni Adobe Analytics.
title: Come si implementa Analytics per [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 26%

---

# Implementazione di Analytics per [!DNL Target]

Sono necessari diversi passaggi per implementare [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T). Il processo varia a seconda che implementi A4T con [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it) o con at.js.

## ![Badge Adobe Experience Platform Web SDK](/help/main/assets/platform.png) Passaggi per l’implementazione di un’implementazione Adobe Experience Platform Web SDK {#platform}

Le sezioni seguenti descrivono i passaggi necessari per implementare questa integrazione nel sito se intendi utilizzare Platform Web SDK:

### Passaggio 1: Richiedi il provisioning per [!DNL Analytics] e [!DNL Target]

Prima di implementare A4T, è necessario eseguire il provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizza questo modulo per richiedere il provisioning](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell’account utente devono essere soddisfatti prima di poter creare un’attività basata su [!DNL Analytics] in [!DNL Target]. Vedi [Requisiti delle autorizzazioni utente](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Passaggio 3: Creare una configurazione Edge

Creare una configurazione Edge utilizzando [!DNL Adobe Experience Platform] mediante lo strumento di configurazione del bordo. Configura le [[!DNL Analytics] and [!DNL Target] impostazioni di configurazione del bordo](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html).

### Passaggio 4: Installare e configurare l’SDK per web di Platform

Per iniziare a consegnare [!DNL Target] esperienze e applicazione [!DNL Analytics] a fini di tracciamento e di analisi, [Installa](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html) e [configurare](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html) l’SDK per web di Platform sulle pagine del sito.

### Passaggio 5: Abilitare le opzioni per l’utilizzo di A4T

In [!DNL Target] Interfaccia utente, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Compositore esperienza visivo]**, quindi scegli **[!UICONTROL Seleziona per attività]** o **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Seleziona per attività consente di scegliere tra e per la creazione di ogni attività.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe imposta Analytics come origine dei rapporti per tutte le attività che hai creato.]**[!DNL Analytics]

## ![Badge at.js](/help/main/assets/atjs.png) Passaggi di implementazione per un’implementazione at.js{#section_73961BAD5BB4430A95E073DE5C026277}

Le sezioni seguenti descrivono i passaggi necessari per implementare questa integrazione nel sito se intendi utilizzare at.js:

### Passaggio 1: Richiedere il provisioning per Analytics e Target

Dopo l’implementazione [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], è necessario effettuare il provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizza questo modulo per richiedere il provisioning](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell’account utente devono essere soddisfatti prima di poter creare un [!DNL Analytics]attività basata su in [!DNL Target]. Vedi [Requisiti delle autorizzazioni utente](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti attraverso le diverse soluzioni [!DNL Adobe Experience Cloud]. Implementa o effettua la migrazione alla versione richiesta dell’ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Vedi [Implementazione del servizio Experience Cloud ID per Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html) in *Servizio ID visitatore di Experience Cloud* documentazione.

### Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

Implementa o esegui la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, vedi [Panoramica sull&#39;implementazione JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) in *Guida all’implementazione di Analytics*.

Per una migrazione, vedi [Migrazione ad AppMeasurement per JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html) in *Guida all’implementazione di Analytics*.

### Passaggio 5: Scaricare e aggiornare at.js

Implementa o esegui la migrazione alla versione richiesta di at.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

### Passaggio 6: Host at.js

Se at.js è stato distribuito in precedenza, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

### Passaggio 7: Fai riferimento a at.js in tutte le pagine del sito {#step7}

Includi at.js sotto VisitorAPI.js aggiungendo la seguente riga di codice nel tag in ogni pagina:

Per at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

Il file VisitorAPI.js deve essere caricato prima di at.js. Se stai aggiornando un file at.js esistente, assicurati di verificare l’ordine di caricamento.

L&#39;impostazione predefinita per [!DNL Target] e [!DNL Analytics] Dal punto di vista dell&#39;implementazione, l&#39;integrazione consiste nell&#39;utilizzare il codice SDID passato dalla pagina per unire [!DNL Target] e [!DNL Analytics] richiedi automaticamente insieme sul backend .

Puoi controllare come e quando inviare i dati di analisi relativi a [!DNL Target] a [!DNL Analytics] a fini di segnalazione. Se non desideri accettare le impostazioni predefinite di [!DNL Target] e [!DNL Analytics] unisce automaticamente i dati di analisi tramite SDID, imposta **analyticsLogging = client_side** tramite **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

Ad esempio:

```javascript
window.targetGlobalSettings = {
  analyticsLogging: "client_side"
};
```

Questa configurazione ha un effetto globale, il che significa che ogni chiamata effettuata da at.js ha **analyticsLogging: &quot;client_side&quot;** inviato all&#39;interno del [!DNL Target] per ogni richiesta vengono restituite richieste e un payload di Analytics. Quando questa opzione è impostata, il formato del payload restituito è simile al seguente:

```javascript
"analytics": {
   "payload": {
      "pe": "tnt",
      "tnta": "167169:0:0|0|100,167169:0:0|2|100,167169:0:0|1|100"
   }
}
```

Il payload può quindi essere inoltrato ad Analytics tramite il [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Per le attività di Allocazione automatica e Targeting automatico, devi anche inoltrare l’ID sessione. Per ulteriori informazioni, consulta [Reporting di Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html){target=_blank} in *SDK per Adobe Target* guida.

Se non desideri usare un’impostazione globale e preferisci un approccio più on-demand, utilizza la funzione at.js [getOffers()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html){target=_blank} di passaggio **analyticsLogging: &quot;client_side&quot;**. Il payload di Analytics viene restituito solo per questa chiamata e il [!DNL Target] il backend non inoltra il payload a [!DNL Analytics]. Con questo approccio, ogni at.js [!DNL Target] La richiesta restituisce il payload per impostazione predefinita, ma solo se desiderato e specificato.

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

Il payload può quindi essere inoltrato a [!DNL Analytics] tramite [API di inserimento dati](https://helpx.adobe.com/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri `mboxMCSDID`[!DNL Target] nelle chiamate di corrispondano al valore del parametro `sdid`[!DNL Analytics] nella chiamata di visualizzazione della pagina 

È particolarmente importante confermare che questi valori corrispondono nelle applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

>[!NOTE]
>
>Per il corretto funzionamento di A4T è necessaria la corrispondenza di questi valori.

### Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

Adobe consiglia di rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. Puoi rimuovere eventuale codice distribuito da una precedente integrazione tra SC e T&amp;T, tra cui `mboxLoadSCPlugin`.

### Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In [!DNL Target], fai clic su **[!UICONTROL Amministrazione > Reporting]** e scegli **[!UICONTROL Seleziona per attività]** o **[!UICONTROL Adobe Analytics]** per abilitare le opzioni.

* **[!UICONTROL Seleziona per attività consente di scegliere tra e per la creazione di ogni attività.]**[!DNL Target][!DNL Analytics]
* **[!UICONTROL Adobe imposta Analytics come origine dei rapporti per tutte le attività che hai creato.]**[!DNL Analytics]


