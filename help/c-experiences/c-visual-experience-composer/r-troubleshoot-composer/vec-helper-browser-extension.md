---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel Compositore esperienza visivo. L’estensione VEC Helper per il browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l’estensione helper del Compositore esperienza visivo?
feature: Compositore esperienza visivo
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: f028d2b439fee5c2a622748126bb0a34d550a395
workflow-type: tm+mt
source-wordcount: '869'
ht-degree: 55%

---

# Estensione Helper per Compositore esperienze visivo

L’estensione del browser Helper per Google Chrome [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo (VEC), per creare e verificare rapidamente le esperienze web.

>[!NOTE]
>
>Il browser VEC Helper è un’estensione Chrome. Questa estensione non è necessaria quando si utilizza Mozilla Firefox.

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità e/o il sito di stage del cliente non è disponibile nel mondo esterno (il sito è interno).
* Stai utilizzando Google Chrome 80+ con criteri di imposizione dei cookie SameSite migliorati. Per ulteriori informazioni, consulta [In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

L’estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato ](/help/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione VEC Helper

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

   Nota che utilizzando il Compositore esperienza avanzato (EEC), l’estensione non inserisce at.js, ma la funzionalità Cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [I ](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) visualizzatori per dispositivi mobili sono supportati anche senza il Compositore esperienza  [!UICONTROL avanzato]  (EEC).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Passa all’ estensione del browser [Adobe Target VEC Helper in Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Fai clic su **[!UICONTROL Aggiungi a Chrome > Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md).
1. (Condizionale) Fai scorrere l&#39;opzione **[!UICONTROL Inserisci librerie di Target]** nella posizione &quot;on&quot; se la pagina web non contiene ancora la libreria JavaScript at.js .[!DNL Target]

   La seguente illustrazione mostra VEC Helper con l’impostazione [!UICONTROL Inserisci librerie Target] abilitata:

   ![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Fai scorrere l&#39;interruttore **[!UICONTROL Cookie]** nella posizione &quot;on&quot; per aggiungere automaticamente la correzione per il browser degli attributi SameSite=None, quindi specifica il nome e il dominio del cookie.

   ![L’opzione Cookie nell’estensione VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   I seguenti collegamenti forniscono informazioni aggiuntive:

   * Per ulteriori informazioni sulla correzione del browser per gli attributi SameSite=None, consulta &quot;In che modo i criteri di imposizione dei cookie SameSite di Google Chrome annunciati di recente influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?&quot; in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

   * Il nome del cookie è &quot;mbox&quot; e il dominio del cookie è il secondo e il primo livello dei domini da cui distribuisci la mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. Per ulteriori informazioni, consulta [Cookie Adobe Target](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html?lang=it) nella *Guida utente dell&#39;interfaccia Experience Cloud*.

## Note

* Il flag [!UICONTROL Inserisci librerie di Target] nell’estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

   Questo flag è un’impostazione globale. Il flag viene attivato o disattivato per tutti i siti web aperti nel Compositore esperienza visivo. Ad esempio, se imposti questo flag su &quot;on&quot; e apri un sito web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. Adobe anticipa che la maggior parte dei clienti ha già implementato at.js sulle proprie pagine e utilizza l’impostazione predefinita &quot;off&quot;.

* L&#39;estensione carica la versione più recente di at.js disponibile da [!DNL Target UI] in [!UICONTROL Amministrazione > Implementazione].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.
