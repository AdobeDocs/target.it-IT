---
description: Informazioni utili per il personale tecnico, per comprendere l’implementazione di mbox.js e come potrebbe influenzare il sito.
keywords: implementazione;mbox.js;libreria di manipolazione dom;target.js;compositore di esperienza visivo;iframe;siti angular;applicazioni a pagina singola;app a singola pagina;SPA
seo-description: Informazioni utili per il personale tecnico, per comprendere l’implementazione di mbox.js e come potrebbe influenzare il sito.
seo-title: Funzionamento di mbox.js
solution: Target
subtopic: Introduzione
title: Funzionamento di mbox.js
topic: Standard
uuid: 5529d620-4a33-479c-871f-18dcd59abb07
translation-type: ht
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Funzionamento di mbox.js{#what-mbox-js-does}

Informazioni utili per il personale tecnico, per comprendere l’implementazione di mbox.js e come potrebbe influenzare il sito.

Target Standard richiede [!DNL mbox.js] versione 58 o successiva. Per istruzioni sul download e l’aggiornamento di [!DNL mbox.js], consulta [Implementazione della mbox](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).

Per Target Standard, [!DNL mbox.js] esegue una chiamata a un altro file JavaScript, [!DNL target.js]. [!DNL Target.js] è in hosting presso Adobe e viene aggiornato automaticamente da Adobe. Non è necessario eseguire alcuna operazione per aggiornare [!DNL target.js], e non sono presenti personalizzazioni specifiche per cliente.

[!DNL Target.js] crea una mbox denominata `target-global-mbox` nella sezione `<head>` della pagina.

[!DNL Target.js] viene richiamato da [!DNL mbox.js] tramite una riga di codice JavaScript aggiunto al campo [!UICONTROL Extra JavaScript] in [!DNL mbox.js]. L’unico modo per disabilitare [!DNL target.js] consiste nel non includere questa riga di codice; così facendo viene disabilitato anche [!DNL Target].

[!DNL Target.js] ha due funzioni in [!DNL Target]:

* Manipolazione di DOM
* Abilita gli elementi visivi del [!UICONTROL Compositore esperienza visivo]

## Manipolazione di DOM {#section_169F8D4C077948DCB4F891ABBB03FF63}

[!DNL Target.js] controlla la libreria di manipolazione DOM utilizzata da Standard. Per visualizzare il contenuto di un sito web, [!DNL target.js] fa riferimento a [!DNL sizzle.js] (versione 1.10.8-pre). [!DNL Sizzle.js] abilita i selettori degli elementi HTML. A parte [!DNL sizzle.js], viene utilizzato solo JavaScript nativo. Non sono richieste jquery.

Inoltre, il frammento seguente viene utilizzato per il polling del DOM:
`https://github.com/dperini/ContentLoaded`

## Target.js e il Compositore esperienza visivo {#section_2B3FF6AC5B8D431C83D9EDCF53CB1472}

Quando si utilizza il [!UICONTROL Compositore esperienza visivo] per impostare l’esperienza per un’attività, la pagina web viene aperta in un iFrame. Una volta caricato l’iFrame, Standard invia una chiamata API `postMessage` HTML5. [!DNL Target.js] rileva eventuali chiamate `postMessage` e include le seguenti librerie JavaScript sul sito web:

* Per la generazione delle miniature: [!DNL https://html2canvas.hertzen.com/]
* Per query interdominio: [!DNL Admin.js], [!DNL CDQ.base.js], [!DNL CDQ.host.js], [!DNL admin.css], utilizzati per inviare messaggi tra iFrame. Questi script consentono ad Adobe l’invio di dati tra pagine.

## Considerazioni per siti Angular e applicazioni a pagina singola {#section_16D76F16077A434FAE8CEC6FD43BE6D7}

Se si implementa Target in un sito Angular o in applicazioni a pagina singola, è necessario utilizzare la libreria at.js invece di mbox.js.

Per ulteriori informazioni, consulta [Implementazione di at.js](../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-target-atjs-implementation/target-atjs-implementation.md#concept_8AC8D169E02944B1A547A0CAD97EAC17).
