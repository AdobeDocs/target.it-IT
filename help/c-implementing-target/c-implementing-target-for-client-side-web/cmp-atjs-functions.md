---
keywords: at.js;funzioni;libreria javascript
description: Visualizzare un elenco delle funzioni utilizzabili con le versioni 1.x e 2.x della libreria JavaScript at.js in  Adobe Target.
title: Quali funzioni posso utilizzare con at.js?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 94%

---


# Funzioni di at.js{#at-js-functions}

Elenco di funzioni che possono essere utilizzate con la libreria JavaScript at.js di Adobe Target. Per ulteriori informazioni ed esempi, fai clic sui collegamenti nella colonna Funzione.

| Funzione | Dettagli |
| --- | --- | 
| [adobe.target.getOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | Questa funzione genera una richiesta per ottenere un’offerta di Target. Puoi utilizzarlo con `adobe.target.applyOffer()` per elaborare la risposta o usare la tua gestione di successo. |
| [adobe.target.getOffers(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at.js 2.x) | Questa funzione ti consente di recuperare più offerte passando più mbox. Inoltre, è possibile recuperare più offerte per tutte le visualizzazioni nelle attività attive.<br>**Nota:** questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*. |
| [adobe.target.applyOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | Questa funzione applica il contenuto di risposta. |
| [adobe.target.applyOffers(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at.js 2.x) | Questa funzione consente di applicare più di un’offerta recuperata da adobe.target.getOffers().<br>**Nota:** questa funzione è stata introdotta con at.js 2.x e non è disponibile per at.js versione 1.*x*. |
| [adobe.target.triggerView (viewName, options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at.js 2.x) | È possibile chiamare questa funzione a ogni caricamento di una nuova pagina o quando si esegue di nuovo il rendering di un componente di una pagina.<br> Questa funzione dovrebbe essere implementata per le applicazioni a pagina singola per utilizzare il Compositore esperienza visiva per creare test A/B e attività di targeting delle esperienze (XT). |
| [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | Questa funzione genera una richiesta per segnalare le azioni dell&#39;utente, ad esempio clic e conversioni. Non recapita le attività nella risposta. |
| [mboxCreate(mbox,params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at.js 1.x) | Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [mboxDefine(options) e mboxUpdate(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at.js 1.x) | Definisci e aggiorna una mbox.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [targetGlobalSettings(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Puoi sovrascrivere le impostazioni nella libreria at.js utilizzando`targetGlobalSettings()`, anziché configurare le impostazioni nell’interfaccia utente di Target Standard/Premium o utilizzando le API REST.<ul><li>Fornitori di dati: questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terzi, come Demandbase, BlueKai e servizi personalizzati, e di passare i dati a Target come parametri mbox nella richiesta mbox globale.</li></ul> |
| [targetPageParams(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta. |
| [targetPageParamsAll(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | Questo metodo consente di allegare i parametri a tutte le mbox dall’esterno del codice di richiesta. |
| [registerExtension(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at.js 1.x) | Fornisce un metodo standard per registrare un’estensione specifica.<br>**Nota:** questa funzione è disponibile per at.js versione 1.*x*. Questa funzione è stata rimossa con il rilascio di at.js 2.x e restituisce il contenuto predefinito se utilizzata con at.js 2.x. |
| [Eventi personalizzati at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | Eventi personalizzati at.js consentono di sapere quando una richiesta o un’offerta mbox ha esito negativo o positivo. |
| [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md)<br>(at.js 2.1.0) | Questa funzione invia una notifica al server Edge di Target quando viene eseguito il rendering di un’esperienza senza utilizzare `adobe.target.applyOffer()` o `adobe.target.applyOffers()`.<br>**Nota**: questa funzione è stata introdotta in at.js 2.1.0 e sarà disponibile per tutte le versioni successive alla versione 2.1.0. |

