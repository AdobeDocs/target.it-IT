---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Informazioni sull’uso dell’estensione Adobe Target VEC Helper per il browser per caricare i siti web in modo affidabile all’interno del Compositore esperienza visivo per creare ed effettuare il controllo qualità sulle esperienze.
title: Estensione Adobe Target VEC Helper
topic: Standard
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 94%

---


# Estensione Adobe Target VEC Helper

L’estensione [!DNL Adobe Target] VEC Helper per il browser Google Chrome consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo (VEC), per creare e verificare rapidamente le esperienze web.

Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo:

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità e/o il sito di stage del cliente non è disponibile nel mondo esterno (il sito è interno).

L’estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [!UICONTROL Compositore esperienza avanzato ] o estensioni di terze parti, come Requestly

Vantaggi dell’utilizzo dell’estensione VEC Helper:

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse in Requestly per farlo.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.
* I riquadri di visualizzazione per dispositivi mobili sono supportate anche senza il [!UICONTROL Compositore esperienza avanzato] (EEC).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Navigate to the [Adobe Target VEC Helper browser extension in the Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Fai clic su [!UICONTROL Aggiungi a Chrome > Aggiungi estensione].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md).

La seguente illustrazione mostra VEC Helper con l’impostazione [!UICONTROL Inserisci librerie Target] abilitata:

![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

## Note

* Utilizza la libreria [!DNL Target] at.js nella tua implementazione. Non utilizzare un’implementazione mbox.js con l’estensione.
* Il flag [!UICONTROL Inserisci librerie di Target] nell’estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

   Tieni presente che questo flag è un’impostazione globale. Il flag viene attivato o disattivato per tutti i siti web aperti nel Compositore esperienza visivo. Quindi, ad esempio, se imposti questo flag su ON e apri un sito web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. Si suppone che la maggior parte dei clienti avrà già at.js implementato nelle loro pagine e userà l’impostazione predefinita (OFF).

* The extension loads the latest version of at.js that is available from the [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.