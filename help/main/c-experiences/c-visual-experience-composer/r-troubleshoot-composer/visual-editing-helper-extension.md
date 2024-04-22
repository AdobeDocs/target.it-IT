---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser;faq
description: Scopri perché alcuni siti web potrebbero non aprirsi in modo affidabile nel [!UICONTROL Visual Experience Composer] (VEC). Il [!UICONTROL Visual Editing Helper] l’estensione del browser consente di caricare i siti web in modo affidabile all’interno del Compositore esperienza visivo.
title: Come si utilizza [!UICONTROL Visual Editing Helper] Estensione?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 8edae6a197a3ac82b85fcce4d99c8b0d5f45c712
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 64%

---

# [!UICONTROL Visual Editing Helper] estensione

Il [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] estensione browser per [!DNL Google Chrome] consente di caricare i siti web in modo affidabile all’interno di [!UICONTROL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) per creare e verificare rapidamente le esperienze web.

>[!IMPORTANT]
>
>Questa nuova estensione sostituisce la precedente [Estensione Target VEC Helper per browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Consulta la nota importante nella parte superiore di tale articolo. Grazie ai miglioramenti apportati alla sicurezza in Manifest v3, [!DNL Adobe] richiede il download di questa nuova estensione per continuare a creare visivamente i siti web in [!DNL Target].

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).

Il [!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] l&#39;estensione del browser per risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell&#39;utilizzo di [!UICONTROL Visual Editing Helper] estensione

* Tutte le intestazioni non compatibili con iframe, come `X-Frame-Options` e `Content-Security-Policy` vengono rimosse implicitamente dal sito web. Non è necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

  Utilizzando il [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [Riquadri di visualizzazione mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportate anche senza [!UICONTROL Enhanced Experience Composer] (CEE).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare [!UICONTROL Visual Editing Helper] estensione browser

1. Accedi a [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] estensione del browser nel Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Clic **[!UICONTROL Add to Chrome]** > **[!UICONTROL Add Extension]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l&#39;estensione, fai clic su [!UICONTROL Visual Editing Helper] icona estensione browser ( ![Icona dell’estensione per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) nella barra degli strumenti del browser Chrome quando si è nel Compositore esperienza visivo o in Modalità Controllo qualità.

   Il [!UICONTROL Visual Editing Helper] viene attivato automaticamente quando un sito web viene aperto in [!UICONTROL Target] Compositore esperienza visivo per l’authoring potente. L’estensione non dispone di impostazioni condizionali. L’estensione gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

   Per ulteriori informazioni sulla correzione dell’attributo del browser `SameSite=None`, consulta “In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Note

* Per [!DNL Target], l&#39;estensione carica la versione più recente di at.js disponibile nella [!DNL Target] Interfaccia utente in [!UICONTROL Administration] > [!UICONTROL Implementation] e at.js scarica le librerie di authoring.
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda di Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione di [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare il [!UICONTROL Visual Editing Helper] estensione del browser.
   * Se at.js o alloy.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
* Se provi a utilizzare la nuova estensione e poi torni all’[estensione precedente](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) e [!DNL Target] non riesci a caricare il sito web, cancella tutti i dati del browser e disabilita la nuova estensione.

## Domande frequenti

### L’estensione, se attiva, esegue qualsiasi operazione se utilizzata al di fuori di [!DNL Adobe Target] o [!UICONTROL Adobe Journey Optimizer] (AJO)

L’estensione si attiva solo quando il sito web in questione viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]). Al di fuori di questo flusso, l’estensione non cerca di aggiungere, rimuovere o modificare alcuna intestazione né di inserire alcun codice all’interno del sito web.

### Cosa fa l’estensione quando è attiva nel Compositore esperienza visivo [!DNL Adobe Target]?

Quando un sito web viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]), l’estensione inserisce il codice (in bundle con l’estensione) nel sito web e scarica i file Helper dal CDN [!DNL Adobe] per abilitare l’authoring visivo.
