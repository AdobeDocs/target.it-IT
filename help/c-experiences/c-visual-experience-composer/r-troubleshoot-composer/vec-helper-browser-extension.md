---
keywords: vec;visual experience composer; vec;iframe;extension;browser
description: Informazioni sull’uso dell’estensione Adobe Target VEC Helper per il browser per caricare i siti web in modo affidabile all’interno del Compositore esperienza visivo per creare ed effettuare il controllo qualità sulle esperienze.
title: Estensione Adobe Target VEC Helper
feature: Visual Experience Composer (VEC)
translation-type: tm+mt
source-git-commit: 8110807a73e4d6d9848a52224db04faba033c98c
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 59%

---


# Estensione Adobe Target VEC Helper

L&#39;estensione del browser helper [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) per Google Chrome consente di caricare siti Web in modo affidabile all&#39;interno del VEC per creare rapidamente esperienze Web QA.

>[!NOTE]
>
>Il browser VEC Helper è un&#39;estensione Chrome. Questa estensione non è necessaria quando si utilizza Mozilla Firefox.

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità e/o il sito di stage del cliente non è disponibile nel mondo esterno (il sito è interno).
* State utilizzando Google Chrome 80+ con criteri di imposizione dei cookie SameSite avanzati. Per ulteriori informazioni, vedere [In che modo le politiche di applicazione dei cookie Google Chrome SameSite annunciate di recente influiscono sulle politiche VEC e EEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

L’estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato ](/help/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione VEC Helper

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse in Requestly per farlo.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

   Tenere presente che quando si utilizza Enhanced Experience Composer (EEC), l&#39;estensione non viene iniettata at.js, ma la funzionalità Cookie SameSite è ancora presente. Per inserire at.js nella pagina Web, disattivare la CEE.

* [I ](/help/c-experiences/c-visual-experience-composer/mobile-viewports.md) visualizzatori per dispositivi mobili sono supportati anche senza  [!UICONTROL Enhanced Experience Composer] (EEC).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Andate alla [ estensione del browser Adobe Target VEC Helper in Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Fai clic su **[!UICONTROL Aggiungi a Chrome > Aggiungi estensione]**.
1. Aprire il VEC in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md).
1. (Condizionale) Fate scorrere l&#39;interruttore **[!UICONTROL Inserisci librerie di destinazione]** nella posizione &quot;on&quot; se la pagina Web non contiene ancora la libreria JavaScript at.js.[!DNL Target]

   La seguente illustrazione mostra VEC Helper con l’impostazione [!UICONTROL Inserisci librerie Target] abilitata:

   ![VEC Helper 1](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![VEC Helper 2](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Fate scorrere l&#39;interruttore **[!UICONTROL Cookies]** nella posizione &quot;on&quot; per aggiungere automaticamente la correzione del browser per gli attributi SameSite=None, quindi specificate il nome e il dominio del cookie.

   ![I cookie si attivano nell&#39;estensione del supporto VEC](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   I seguenti collegamenti forniscono informazioni aggiuntive:

   * Per ulteriori informazioni sulla correzione del browser SameSite=None dell&#39;attributo, vedere &quot;How do the Google Chrome SameSite Cookie Enforcement Policies (Come possono le politiche di imposizione dei cookie dello stesso sito Google recentemente annunciate avere un impatto sul VEC e CEE?&quot; in [Risoluzione dei problemi relativi a Visual Experience Composer (Compositore esperienza visivo) e Enhanced Experience Composer (Compositore esperienza avanzato)](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

   * Il nome del cookie è &quot;mbox&quot; e il dominio del cookie è il secondo e il primo livello dei domini da cui viene distribuita la mbox. Dato che viene distribuito dal dominio della società, il cookie è un cookie dei siti Web visualizzati. Esempio: `mycompany.com`. Per ulteriori informazioni, vedere [ Adobe Target Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-target.html) nella *Guida utente dell&#39;interfaccia del Experience Cloud*.

## Note

* Utilizza la libreria [!DNL Target] at.js nella tua implementazione. Non utilizzare un’implementazione mbox.js con l’estensione.
* Il flag [!UICONTROL Inserisci librerie di Target] nell’estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

   Tieni presente che questo flag è un’impostazione globale. Il flag viene attivato o disattivato per tutti i siti web aperti nel Compositore esperienza visivo. Così, ad esempio, se imposti questo flag su &quot;on&quot; e apri un sito Web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. Prevediamo che la maggior parte dei clienti avrà già implementato at.js sulle proprie pagine e utilizzerà l&#39;impostazione predefinita &quot;off&quot;.

* L&#39;estensione carica l&#39;ultima versione di at.js disponibile da [!DNL Target UI] in [!UICONTROL Amministrazione > Implementazione].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.

