---
keywords: at.js;funzioni;libreria javascript
description: Visualizza un elenco di funzioni che possono essere utilizzate con le versioni 1.x e 2.x della libreria JavaScript at.js in Adobe Target.
title: Quali funzioni posso utilizzare con at.js?
feature: at.js
role: Developer
exl-id: a386e478-16f4-4bf6-9771-6b1e75f2e362
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 78%

---

# Funzioni di at.js

Elenco di funzioni che possono essere utilizzate con la libreria JavaScript at.js di Adobe Target. Per ulteriori informazioni ed esempi, fai clic sui collegamenti nella colonna Funzione.

| Funzione | Dettagli |
| --- | --- | 
| [adobe.target.getOffer(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffer/) | Questa funzione genera una richiesta per ottenere un’offerta di Target. Puoi utilizzarlo con `adobe.target.applyOffer()` per elaborare la risposta o usare la tua gestione di successo. |
| [adobe.target.getOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-getoffers-atjs-2/)<br>(at.js 2.x) | Questa funzione ti consente di recuperare più offerte passando più mbox. Inoltre, è possibile recuperare più offerte per tutte le visualizzazioni nelle attività attive.<br>**Nota:** questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*. |
| [adobe.target.applyOffer(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffer/) | Questa funzione applica il contenuto di risposta. |
| [adobe.target.applyOffers(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-applyoffers-atjs-2/)<br>(at.js 2.x) | Questa funzione consente di applicare più di un’offerta recuperata da adobe.target.getOffers().<br>**Nota:** questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*. |
| [adobe.target.triggerView (viewName, options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-triggerview-atjs-2/)<br>(at.js 2.x) | È possibile chiamare questa funzione a ogni caricamento di una nuova pagina o quando si esegue di nuovo il rendering di un componente di una pagina.<br> Questa funzione dovrebbe essere implementata per le applicazioni a pagina singola per utilizzare il Compositore esperienza visiva per creare test A/B e attività di targeting delle esperienze (XT). |
| [adobe.target.trackEvent(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-trackevent/) | Questa funzione genera una richiesta per segnalare le azioni dell&#39;utente, ad esempio clic e conversioni. Non recapita le attività nella risposta. |
| [mboxCreate(mbox,params)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxcreate-atjs/)<br>(at.js 1.x) | Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [mboxDefine(options) e mboxUpdate(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/mboxdefine-mboxupdate-atjs-1x/)<br>(at.js 1.x) | Definisci e aggiorna una mbox.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [targetGlobalSettings(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetglobalsettings/) | Puoi sovrascrivere le impostazioni nella libreria at.js utilizzando`targetGlobalSettings()`, anziché configurare le impostazioni nell’interfaccia utente di Target Standard/Premium o utilizzando le API REST.<ul><li>Fornitori di dati: questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta mbox globale.</li></ul> |
| [targetPageParams(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparams/) | Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta. |
| [targetPageParamsAll(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/targetpageparamsall/) | Questo metodo consente di allegare i parametri a tutte le mbox dall’esterno del codice di richiesta. |
| [registerExtension(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/registerextension-atjs-1x/)<br>(at.js 1.x) | Fornisce un metodo standard per registrare un’estensione specifica.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [Eventi personalizzati at.js](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/atjs-custom-events/) | Eventi personalizzati at.js consentono di sapere quando una richiesta o un’offerta mbox ha esito negativo o positivo. |
| [adobe.target.sendNotifications(options)](https://developer.adobe.com/target/implement/client-side/atjs/atjs-functions/adobe-target-sendnotifications-atjs-21/)<br>(at.js 2.1.0) | Questa funzione invia una notifica al server Edge di Target quando viene eseguito il rendering di un’esperienza senza utilizzare `adobe.target.applyOffer()` o `adobe.target.applyOffers()`.<br>**Nota**: questa funzione è stata introdotta in at.js 2.1.0 e sarà disponibile per tutte le versioni successive alla versione 2.1.0. |
