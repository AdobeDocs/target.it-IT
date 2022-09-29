---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel Compositore esperienza visivo. L’estensione VEC Helper per il browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l’estensione helper del Compositore esperienza visivo?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 8612928e647c6c11a40b499001261be3a8521648
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 58%

---

# Estensione Helper per Compositore esperienze visivo

La [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) L’estensione Helper per per il browser Google Chrome consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo (VEC), per creare e verificare rapidamente le esperienze web.

Il browser VEC Helper è un’estensione Chrome. Questa estensione non è necessaria quando si utilizza Mozilla Firefox.

>[!IMPORTANT]
>
>A partire da gennaio 2023, la [!DNL Target] L’estensione VEC Helper smetterà di funzionare in Google Chrome perché Google non consente le estensioni che utilizzano Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno. Per ulteriori informazioni, consulta [Estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md).

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità e/o il sito di stage del cliente non è disponibile nel mondo esterno (il sito è interno).
* Attualmente esistono alcune limitazioni riguardanti l’utilizzo del Compositore esperienza visivo per aprire un sito web che utilizza [processi di lavoro dei servizi](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) {target=_blank} (SW, Service Workers).

Un SW è una tecnologia web che può essere utilizzata per intercettare le richieste verso il dominio in cui è installato da una pagina web. SW sopravvive alla visita della pagina e si attiva nelle visite successive. SW decide quali richieste passare e quali vengono invece intercettate e servite da una cache.

SW può controllare la memorizzazione in cache; può memorizzare in cache la pagina web stessa, le risorse statiche come JS, CSS, IMG, le richieste AJAX, il loro contenuto e le relative intestazioni di risposta, incluse quelle che l’[estensione VEC Helper di Target](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) tenta di rimuovere, come X-Frame-Options: SAMEORIGIN, CSP (Content-Security-Policy) o Set-Cookie.

Sfortunatamente, le API di estensione Chrome che intercettano richieste web non ricevono le richieste intercettate e gestite da un SW. Pertanto, l’estensione non può correggere le intestazioni e i cookie se la richiesta di pagina web è stata servita da una cache da un SW perché la pagina web non viene caricata all’interno del VEC a causa delle intestazioni X-Frame-Options o CSP anch’esse memorizzate nella cache.

Come potenziale soluzione alternativa, puoi disabilitare i processi di lavoro dei serivizi dalla scheda Chrome Developer Tools > Application, quindi abilitare la casella di controllo “Bypass for network” nella sezione Service Workers.

* Stai utilizzando Google Chrome 80+ con criteri di imposizione dei cookie SameSite migliorati. Per ulteriori informazioni, consulta [In che modo i criteri di implementazione dei cookie SameSite di Google Chrome annunciati di recente influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

L’estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato ](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione VEC Helper

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

   Nota che utilizzando il Compositore esperienza avanzato (EEC), l’estensione non inserisce at.js, ma la funzionalità Cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [Riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza [!UICONTROL Compositore esperienza avanzato] (CEE) n.
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Passa a [Estensione Adobe Target VEC Helper per browser in Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Fai clic su **[!UICONTROL Aggiungi a Chrome > Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md).
1. (Condizionale) Fai scorrere il **[!UICONTROL Inserisci librerie di Target]** passa alla posizione &quot;on&quot; se la pagina web non contiene ancora [!DNL Target] Libreria JavaScript at.js.

   La seguente illustrazione mostra VEC Helper con l’impostazione [!UICONTROL Inserisci librerie Target] abilitata:

   ![VEC Helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![VEC Helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Fai scorrere il **[!UICONTROL Cookie]** passa alla posizione &quot;on&quot; per aggiungere automaticamente il `SameSite=None` correzione dell&#39;attributo browser.

   ![L’opzione Cookie nell’estensione VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Per ulteriori informazioni sulla `SameSite=None` correzione dell’attributo del browser, vedi &quot;In che modo i criteri di imposizione dei cookie SameSite di Google Chrome annunciati di recente influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?&quot; in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Note

* Il flag [!UICONTROL Inserisci librerie di Target] nell’estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

   Questo flag è un’impostazione globale. Il flag viene attivato o disattivato per tutti i siti web aperti nel Compositore esperienza visivo. Ad esempio, se imposti questo flag su &quot;on&quot; e apri un sito web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. Adobe anticipa che la maggior parte dei clienti ha già implementato at.js sulle proprie pagine e utilizza l’impostazione predefinita &quot;off&quot;.

* L’estensione carica la versione più recente di at.js disponibile dal [!DNL Target UI] in [!UICONTROL Amministrazione > Implementazione].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.
