---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser;faq
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Visual Experience Composer] (VEC). L'estensione del browser [!UICONTROL Visual Editing Helper] consente di caricare i siti Web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l'estensione [!UICONTROL Visual Editing Helper]?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: c41580bcbecf2eb2c14f13ce8e66e854c655d059
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 64%

---

# Estensione [!UICONTROL Visual Editing Helper]

L&#39;estensione del browser [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] per [!DNL Google Chrome] consente di caricare i siti Web in modo affidabile all&#39;interno del [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) per creare e verificare rapidamente le esperienze Web.

>[!IMPORTANT]
>
>* Questa nuova estensione sostituisce la precedente [Estensione Target VEC Helper per browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Consulta la nota importante nella parte superiore di tale articolo. A causa dei miglioramenti della sicurezza in Manifest v3, [!DNL Adobe] richiede il download di questa nuova estensione per continuare a creare visivamente i siti Web in [!DNL Target].

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).

L&#39;estensione del browser [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] per risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano al [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell&#39;utilizzo dell&#39;estensione [!UICONTROL Visual Editing Helper]

* Tutte le intestazioni non compatibili con iframe, come `X-Frame-Options` e `Content-Security-Policy` vengono rimosse implicitamente dal sito web. Non è necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

  Utilizzando il [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [I riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il [!UICONTROL Enhanced Experience Composer] (EEC).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l&#39;estensione del browser [!UICONTROL Visual Editing Helper]

1. Passare all&#39;estensione del browser [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] nel Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Fare clic su **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l&#39;estensione, fai clic sull&#39;icona dell&#39;estensione del browser [!UICONTROL Visual Editing Helper] ( ![icona Estensione editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in Modalità Controllo qualità.

   [!UICONTROL Visual Editing Helper] viene abilitato automaticamente quando un sito Web viene aperto nel Compositore esperienza visivo [!UICONTROL Target] per l&#39;authoring potente. L’estensione non dispone di impostazioni condizionali. L’estensione gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

   Per ulteriori informazioni sulla correzione dell’attributo del browser `SameSite=None`, consulta “In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Note

* Per [!DNL Target], l&#39;estensione carica la versione più recente di at.js disponibile nell&#39;interfaccia utente [!DNL Target] in [!UICONTROL Administration] > [!UICONTROL Implementation] e at.js scarica le librerie di authoring.
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda di Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione di [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l&#39;estensione del browser [!UICONTROL Visual Editing Helper].
   * Se at.js o alloy.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
* Se provi a utilizzare la nuova estensione e poi torni all’[estensione precedente](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) e [!DNL Target] non riesci a caricare il sito web, cancella tutti i dati del browser e disabilita la nuova estensione.

## Domande frequenti

### L&#39;estensione, se attiva, esegue operazioni al di fuori di [!DNL Adobe Target] o [!UICONTROL Adobe Journey Optimizer] (AJO)?

L’estensione si attiva solo quando il sito web in questione viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]). Al di fuori di questo flusso, l’estensione non cerca di aggiungere, rimuovere o modificare alcuna intestazione né di inserire alcun codice all’interno del sito web.

### Cosa fa l’estensione quando è attiva nel Compositore esperienza visivo [!DNL Adobe Target]?

Quando un sito web viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]), l’estensione inserisce il codice (in bundle con l’estensione) nel sito web e scarica i file Helper dal CDN [!DNL Adobe] per abilitare l’authoring visivo.
