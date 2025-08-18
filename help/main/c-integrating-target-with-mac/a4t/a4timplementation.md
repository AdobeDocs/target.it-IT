---
keywords: A4T;Adobe Analytics;attività basata su Analytics;suite di rapporti di Analytics;suite di rapporti;integrazione di Analytics Target;configurare suite di rapporti;at.js;atjs;adobe experience platform web sdk;aep web sdk;platform web sdk
description: Segui i passaggi necessari per implementare Analytics for [!DNL Target] (A4T) nelle tue soluzioni Adobe [!DNL Target] e Adobe Analytics.
title: Come si implementa Analytics per  [!DNL Target] (A4T)?
feature: Analytics for Target (A4T)
exl-id: b5269b9e-01ef-449a-bb03-3dcc2cd68af7
source-git-commit: ddfb06a17a24200b2aa4f01d370cc0e92ff5f180
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 17%

---

# Implementazione di Analytics per [!DNL Target]

Sono necessari diversi passaggi per implementare [!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Adobe Target] (A4T). Il processo varia a seconda che tu implementi A4T con [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it) o con at.js.

## ![Badge Adobe Experience Platform Web SDK](/help/main/assets/platform.png) Passaggi per l&#39;implementazione di Adobe Experience Platform Web SDK {#platform}

Nelle sezioni seguenti vengono descritti i passaggi necessari per distribuire questa integrazione nel sito se si intende utilizzare Platform Web SDK:

### Passaggio 1: richiesta del provisioning per [!DNL Analytics] e [!DNL Target]

Prima di implementare A4T, è necessario disporre del provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizzare questo modulo per richiedere il provisioning](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y).

### Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell&#39;account utente devono essere soddisfatti prima di creare un&#39;attività basata su [!DNL Analytics] in [!DNL Target]. Consulta [Requisiti delle autorizzazioni utente](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Passaggio 3: creare una configurazione di Edge

Creare una configurazione di Edge utilizzando [!DNL Adobe Experience Platform] utilizzando lo strumento di configurazione Edge. Configura [Creare e configurare gli stream di dati](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html?lang=it).

### Passaggio 4: installare e configurare Platform Web SDK

Per iniziare a distribuire [!DNL Target] esperienze e applicare [!DNL Analytics] a scopo di monitoraggio e analisi, [Installa](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=it) e [configura](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/configuring-the-sdk.html?lang=it) Platform Web SDK nelle pagine del sito.

### Passaggio 5: abilitare le opzioni per l’utilizzo di A4T

Nell&#39;interfaccia utente di [!DNL Target], fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Visual Experience Composer]**, quindi scegliere **[!UICONTROL Select per activity]** o **[!UICONTROL Adobe Analytics]**.

* **[!UICONTROL Select per activity]** consente di scegliere tra [!DNL Target] e [!DNL Analytics] durante la creazione di ogni attività.
* **[!UICONTROL Adobe Analytics]** imposta [!DNL Analytics] come origine per la generazione di rapporti per tutte le attività create.

## ![Badge at.js](/help/main/assets/atjs.png) Passaggi per l&#39;implementazione di at.js{#section_73961BAD5BB4430A95E073DE5C026277}

Le sezioni seguenti descrivono i passaggi necessari per distribuire questa integrazione al sito se intendi utilizzare at.js:

### Passaggio 1: richiesta del provisioning per Analytics e Target

Dopo aver implementato [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], è necessario disporre del provisioning per [!DNL Analytics] e [!DNL Target]. [Utilizzare questo modulo per richiedere il provisioning](https://survey.adobe.com/jfe/form/SV_ekBHTLSoP5Zki2y){target=_blank}.

### Passaggio 2: Configurare le autorizzazioni utente

I requisiti dell&#39;account utente devono essere soddisfatti prima di creare un&#39;attività basata su [!DNL Analytics] in [!DNL Target]. Consulta [Requisiti delle autorizzazioni utente](/help/main/c-integrating-target-with-mac/a4t/account-reqs.md).

### Passaggio 3: Implementare il servizio ID visitatore di Experience Cloud

Il servizio ID visitatore consente di identificare gli utenti nelle soluzioni [!DNL Adobe Experience Cloud]. Implementa o esegui la migrazione alla versione richiesta dell’ID visitatore di Experience Cloud. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Consulta [Implementazione del servizio Experience Cloud ID per Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=it) nella documentazione del *servizio ID visitatore di Experience Cloud*.

### Passaggio 4: Aggiornare AppMeasurement per JavaScript o s_code

Implementa o esegui la migrazione alla versione richiesta di appMeasurement.js. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

Per le nuove implementazioni, consulta [Panoramica sull&#39;implementazione di JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=it) nella *Guida all&#39;implementazione di Analytics*.

Per una migrazione, vedere [Migrazione ad AppMeasurement per JavaScript](https://experienceleague.adobe.com/docs/analytics/implementation/js/migrate-from-hcode.html?lang=it) nella *Guida all&#39;implementazione di Analytics*.

### Passaggio 5: Scaricare e aggiornare at.js

Implementa o esegui la migrazione alla versione richiesta di at.js utilizzando il tuo account di produzione. Non sono richieste modifiche al codice.

Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

### Passaggio 6: Hosting di at.js

Se at.js è stato distribuito in precedenza, puoi sostituire il file esistente con la versione aggiornata. Per ulteriori informazioni, consulta “Requisiti di implementazione” in [Prima dell’implementazione](/help/main/c-integrating-target-with-mac/a4t/before-implement.md).

In caso contrario, il file può essere incluso in hosting insieme al servizio ID visitatore e AppMeasurement per file JavaScript. Questi file devono essere in hosting su un server web accessibile a tutte le pagine del sito. È necessario definire il percorso di questi file nella fase successiva.

### Passaggio 7: Includere un riferimento a at.js in tutte le pagine del sito {#step7}

Includi at.js sotto VisitorAPI.js aggiungendo la seguente riga di codice al tag in ogni pagina:

Per at.js:

```javascript
<script language="JavaScript" type="text/javascript"
src="http://INSERT-DOMAIN-AND-PATH-TO-CODE-HERE/at.js"></script>
```

VisitorAPI.js deve essere caricato prima di at.js. Se stai aggiornando un file at.js esistente, accertati di verificare l’ordine di caricamento.

L&#39;impostazione predefinita per l&#39;integrazione di [!DNL Target] e [!DNL Analytics], dal punto di vista dell&#39;implementazione, consiste nell&#39;utilizzare l&#39;identificatore SDID passato dalla pagina per unire automaticamente nel backend le richieste di [!DNL Target] e [!DNL Analytics].

È possibile controllare come e quando inviare i dati di analisi relativi a [!DNL Target] a [!DNL Analytics] a scopo di reporting. Se non desideri fornire il consenso alle impostazioni predefinite per l&#39;unione automatica di [!DNL Target] e [!DNL Analytics] dei dati di analisi tramite l&#39;identificatore SDID, imposta **analyticsLogging = client_side** tramite **window.targetGlobalSettings**. Nota: questo approccio non è supportato dalle versioni precedenti alla versione 2.1.

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

Il payload può quindi essere inoltrato ad Analytics tramite l&#39;[API di inserimento dati](https://helpx.adobe.com/it/analytics/kb/data-insertion-api-post-method-adobe-analytics.html). Per le attività Allocazione automatica e Targeting automatico, devi anche inoltrare il sessionId. Per ulteriori informazioni, consulta [Generazione rapporti di Analytics for Target (A4T)](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/integration/a4t-reporting.html?lang=it){target=_blank} nella guida *SDK per Adobe Target*.

Se non desideri usare un&#39;impostazione globale e preferisci un approccio di tipo on-demand, usa la funzione at.js [getOffers()](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/adobe-target-getoffers-atjs-2.html?lang=it){target=_blank} passando **analyticsLogging: &quot;client_side&quot;**. Il payload di Analytics viene restituito solo per questa chiamata e il backend [!DNL Target] non inoltra il payload a [!DNL Analytics]. Seguendo questo approccio, ogni richiesta di at.js [!DNL Target] restituisce il payload per impostazione predefinita, ma solo quando desiderato e specificato.

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

Il payload può quindi essere inoltrato a [!DNL Analytics] tramite l&#39;[API di inserimento dati](https://helpx.adobe.com/it/analytics/kb/data-insertion-api-post-method-adobe-analytics.html).

### Passaggio 8: Convalidare l’implementazione {#step8}

Carica le pagine dopo aver aggiornato le librerie JavaScript per confermare che i valori dei parametri `mboxMCSDID` nelle chiamate [!DNL Target] corrispondano al valore del parametro `sdid` nella chiamata di visualizzazione pagina [!DNL Analytics].

È particolarmente importante confermare che questi valori corrispondano nelle applicazioni a pagina singola (SPA) in cui l’ordine delle chiamate non è sempre prevedibile.

>[!NOTE]
>
>La corrispondenza di questi valori è necessaria per il corretto funzionamento di A4T.

### Passaggio 9: (Facoltativo) Rimuovere il codice di integrazione precedente

Adobe consiglia di rimuovere l’integrazione precedente per semplificare l’implementazione ed eliminare la necessità di risolvere eventuali discrepanze tra i sistemi. È possibile rimuovere il codice distribuito da una precedente integrazione tra SC e T&amp;T, incluso `mboxLoadSCPlugin`.

### Passaggio 10: Abilitare le opzioni per l’utilizzo di Analytics come origine per la creazione di rapporti per Target

In [!DNL Target], fare clic su **[!UICONTROL Administration > Reporting]** e scegliere **[!UICONTROL Select per activity]** o **[!UICONTROL Adobe Analytics]** per abilitare le opzioni.

* **[!UICONTROL Select per activity]** consente di scegliere tra [!DNL Target] e [!DNL Analytics] durante la creazione di ogni attività.
* **[!UICONTROL Adobe Analytics]** imposta [!DNL Analytics] come origine per la generazione di rapporti per tutte le attività create.


