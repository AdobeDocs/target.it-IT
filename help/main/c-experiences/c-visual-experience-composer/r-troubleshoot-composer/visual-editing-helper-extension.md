---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo). La [!UICONTROL Helper per editing video] l’estensione del browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizzano i [!UICONTROL Helper per editing video] Estensione?
feature: Visual Experience Composer (VEC)
source-git-commit: 70ab1ec7f5313d8c1f8ecaa9b436d95919cf479a
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 30%

---

# [!UICONTROL Helper per editing video] estensione

La [!DNL Adobe Experience Cloud] [!UICONTROL Helper per editing video] l’estensione del browser per Google Chrome consente di caricare i siti web in modo affidabile all’interno di [!UICONTROL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) per creare e verificare rapidamente le esperienze web.

>[!IMPORTANT]
>
>Questa nuova estensione sostituisce la precedente [Estensione del browser VEC Helper Target](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* Il sito di controllo qualità o stage del cliente non è disponibile nel mondo esterno (il sito è interno).

La [!DNL Adobe Experience Cloud] [!UICONTROL Helper per editing video] l’estensione del browser per Chrome risolve i problemi di caricamento del sito per i quali i clienti ora si affidano a [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, ad esempio Requestly.

## Vantaggi dell&#39;utilizzo [!UICONTROL Helper per editing video] estensione

* Tutte le intestazioni di busting iframe, come `X-Frame-Options` e `Content-Security-Policy`, vengono rimossi implicitamente dal sito web. Non è necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

Tieni presente che utilizzando [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [Riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza [!UICONTROL Compositore esperienza avanzato] (CEE) n.
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottieni e installa la [!UICONTROL Helper per editing video] estensione browser

1. Passa a [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] estensione del browser in Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l&#39;estensione, fai clic sul pulsante [!UICONTROL Helper per editing video] icona dell&#39;estensione del browser ( ![Icona dell’estensione di modifica visiva](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) nella barra degli strumenti del browser Chrome in modalità Compositore esperienza visivo o Controllo qualità.

   La [!UICONTROL Helper per editing video] viene attivato automaticamente quando un sito web viene aperto nella [!UICONTROL Target] Compositore esperienza visivo per l’authoring. L&#39;estensione non dispone di impostazioni condizionali. L’estensione gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

   Per ulteriori informazioni sulla `SameSite=None` correzione dell’attributo del browser, vedi &quot;In che modo i criteri di imposizione dei cookie SameSite di Google Chrome annunciati di recente influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?&quot; in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Note

* Per [!DNL Target], l’estensione carica la versione più recente di at.js disponibile nel [!DNL Target] Interfaccia utente in [!UICONTROL Amministrazione] > [!UICONTROL Implementazione] e at.js scarica le librerie di authoring.
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata allo stesso [!DNL Adobe Experience Cloud] organizzazione in cui hai creato l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se si tenta di caricare un sito web utilizzando il Compositore esperienza visivo che non riesce a caricarsi, viene visualizzato un messaggio per suggerirti di installare il [!UICONTROL Helper per editing video] estensione del browser.
   * Se at.js o alloy.js non è ancora implementato sul sito web, nel Compositore esperienza visivo viene visualizzato un messaggio per suggerirti di installare l’estensione.

## Ulteriore aiuto su questa funzione

* [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)
* [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-visual-experience-composer-vec.md)
* [Risoluzione dei problemi relativi al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshooting-issues-related-to-the-enhanced-experience-composer-eec.md)



