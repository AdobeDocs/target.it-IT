---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser;domande frequenti
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Compositore esperienza visivo]. L’estensione del browser [!UICONTROL Helper per editing video] consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l’estensione [!UICONTROL Helper per editing video]?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
source-git-commit: 30ad6712d9722854384721ca20d38a605930c4d7
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 100%

---

# Estensione [!UICONTROL Helper per editing video]

L’estensione del browser [!DNL Adobe Experience Cloud] [!UICONTROL Helper per editing video] per Google Chrome consente di caricare i siti web in modo affidabile all’interno del [!UICONTROL Compositore esperienza visivo] di [!UICONTROL Adobe Target] per creare e verificare rapidamente le esperienze web.

>[!IMPORTANT]
>
>Questa nuova estensione sostituisce la precedente [Estensione Target VEC Helper per browser](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md). Consulta la nota importante nella parte superiore di quell’articolo.

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).

L’estensione del browser [!DNL Adobe Experience Cloud] [!UICONTROL Helper per editing video] per Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano al [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione [!UICONTROL Helper per editing video]

* Tutte le intestazioni non compatibili con iframe, come `X-Frame-Options` e `Content-Security-Policy` vengono rimosse implicitamente dal sito web. Non è necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

   Utilizzando il [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec), l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [I riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il [!UICONTROL Compositore esperienza avanzato].
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottieni e installa l’estensione del browser [!UICONTROL Helper per editing video]

1. Passa a [[!DNL Adobe Experience Cloud] [!UICONTROL Visual Editing Helper] estensione del browser nel Chrome web store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione del browser [!UICONTROL Helper per editing video] (![icona Estensione editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in Modalità Controllo qualità.

   L’estensione [!UICONTROL Helper per editing video] viene attivata automaticamente quando un sito web viene aperto nel Compositore esperienza visivo di [!UICONTROL Target] per l’authoring potente. L’estensione non dispone di impostazioni condizionali. L’estensione gestisce automaticamente tutte le impostazioni, incluse le impostazioni dei cookie SameSite.

   Per ulteriori informazioni sulla correzione dell’attributo del browser `SameSite=None`, consulta “In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).

## Note

* Per [!DNL Target], l’estensione carica la versione più recente di at.js disponibile nell’Interfaccia utente di [!DNL Target] in [!UICONTROL Amministrazione] > [!UICONTROL Implementazione] e at.js scarica le librerie di authoring.
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda di Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione di [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione del browser [!UICONTROL Helper per editing video].
   * Se at.js o alloy.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
* Se provi a utilizzare la nuova estensione e poi torni all’[estensione precedente](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) e [!DNL Target] non riesci a caricare il sito web, cancella tutti i dati del browser e disabilita la nuova estensione.

## Domande frequenti

### Quando l’estensione è attiva, esegue una qualsiasi operazione quando viene utilizzata al di fuori di [!DNL Adobe Target] o di [!UICONTROL Adobe Journey Optimizer] (AJO)?

L’estensione si attiva solo quando il sito web in questione viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]). Al di fuori di questo flusso, l’estensione non cerca di aggiungere, rimuovere o modificare alcuna intestazione né di inserire alcun codice all’interno del sito web.

### Cosa fa l’estensione quando è attiva nel Compositore esperienza visivo [!DNL Adobe Target]?

Quando un sito web viene caricato all’interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]), l’estensione inserisce il codice (in bundle con l’estensione) nel sito web e scarica i file Helper dal CDN [!DNL Adobe] per abilitare l’authoring visivo.
