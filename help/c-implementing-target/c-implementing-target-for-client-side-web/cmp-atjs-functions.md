---
description: Elenco di funzioni che possono essere utilizzate con at.js.
keywords: adobe.target.notification;element;selector;notification;extension
seo-description: Elenco di funzioni che possono essere utilizzate con la libreria JavaScript di at.js in Adobe Target.
seo-title: Funzioni di at.js in Adobe Target
solution: Target
subtopic: Introduzione
title: Funzioni di at.js
topic: Standard
uuid: ec5f27a7-b22a-48c9-968c-9eb02830a2a6
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Funzioni di at.js{#at-js-functions}

Elenco di funzioni che possono essere utilizzate con la libreria JavaScript di at.js in Adobe Target. Per ulteriori informazioni ed esempi, fate clic sui collegamenti nella colonna Funzione.

| Funzione | Dettagli |
| --- | --- | 
| [adobe.target.getoffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffer.md) | Questa funzione genera una richiesta per ottenere un’offerta di Target. Puoi utilizzarlo con `adobe.target.applyOffer()` per elaborare la risposta o usare la tua gestione di successo. |
| [adobe. target. getoffer (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-getoffers-atjs-2.md)<br>(at. js 2. x) | Questa funzione ti consente di recuperare più offerte passando più mbox. Inoltre, è possibile recuperare più offerte per tutte le visualizzazioni nelle attività attive.<br>**Nota:** Questa funzione è stata introdotta con at. js 2. x. Questa funzione non è disponibile per at. js versione 1.*x*. |
| [adobe.target.applyOffer(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffer.md) | Questa funzione applica il contenuto di risposta. |
| [adobe. target. applyoffer (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-applyoffers-atjs-2.md)<br>(at. js 2. x) | Questa funzione consente di applicare più di un&#39;offerta recuperata da adobe. target. getoffers ().<br>**Nota:** Questa funzione è stata introdotta con at. js 2. x. Questa funzione non è disponibile per at. js versione 1.*x*. |
| [adobe. target. triggerview (viewname, options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-triggerview-atjs-2.md)<br>(at. js 2. x) | È possibile chiamare questa funzione a ogni caricamento di una nuova pagina o quando si esegue di nuovo il rendering di un componente di una pagina.<br> Questa funzione deve essere implementata per le applicazioni di pagina singole (SPAS) per utilizzare Visual Experience Composer (Compositore esperienza visivo) per creare attività A/B e Targeting delle esperienze (XT). |
| [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) | Questa funzione genera una richiesta per segnalare le azioni dell&#39;utente, ad esempio clic e conversioni. Non recapita le attività nella risposta. |
| [Mboxcreate (mbox, params)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxcreate-atjs.md)<br>(at. js 1. x) | Esegue una richiesta e applica l’offerta all’elemento DIV più vicino con il nome della classe mboxDefault.<br>**Nota:** Questa funzione è disponibile per. js versione 1.Solo *x*. Questa funzione è stata rimossa dal rilascio di at. js 2. x. Questa funzione restituisce il contenuto predefinito se utilizzato con at. js 2. x. |
| [Mboxdefine (options) e mboxupdate (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/mboxdefine-mboxupdate-atjs-1x.md)<br>(at. js 1. x) | Definisci e aggiorna una mbox.<br>**Nota:** Questa funzione è disponibile per. js versione 1.Solo *x*. Questa funzione è stata rimossa dal rilascio di at. js 2. x. Questa funzione restituisce il contenuto predefinito se utilizzato con at. js 2. x. |
| [Targetglobalsettings (opzioni)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetgobalsettings.md) | Potete ignorare le impostazioni nella libreria. js utilizzando `targetGlobalSettings()`, piuttosto che configurare le impostazioni nell&#39;interfaccia utente di Target Standard/Premium o utilizzando REST API.<ul><li>Fornitori di dati: Questa impostazione consente ai clienti di raccogliere dati da fornitori di dati terze parti, come Demandbase, bluekai e servizi personalizzati, e trasmettere i dati a Target come parametri mbox nella richiesta mbox globale.</li></ul> |
| [Targetpageparams (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparams.md) | Questo metodo consente di allegare i parametri alla mbox globale dall’esterno del codice di richiesta. |
| [Targetpageparamsall (opzioni)](/help/c-implementing-target/c-implementing-target-for-client-side-web/targetpageparamsall.md) | Questo metodo consente di allegare i parametri a tutte le mbox dall’esterno del codice di richiesta. |
| [Registerextension (options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/registerextension-atjs-1x.md)<br>(at. js 1. x) | Fornisce un metodo standard per registrare un’estensione specifica.<br>**Nota:** Questa funzione è disponibile per. js versione 1.Solo *x*. Questa funzione è stata rimossa dal rilascio di at. js 2. x. Questa funzione restituisce il contenuto predefinito se utilizzato con at. js 2. x. |
| [Eventi personalizzati at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/atjs-custom-events.md) | eventi personalizzati at. js consentono di sapere quando una richiesta o un&#39;offerta mbox ha esito positivo o negativo. |
