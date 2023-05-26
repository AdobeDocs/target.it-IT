---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel Compositore esperienza visivo. L’estensione VEC Helper per browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l’estensione VEC Helper?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 3456da329e25f3d8e8f591fce0b851580d385455
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 59%

---

# Estensione Helper per Compositore esperienze visivo

Il [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] (VEC) L’estensione Helper per il browser Google Chrome consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo (VEC), per creare e verificare rapidamente le esperienze web.

Il browser VEC Helper è un’estensione di Chrome. Questa estensione non è necessaria quando si utilizza Mozilla Firefox.

>[!IMPORTANT]
>
>L&#39;attuale [!DNL Target] L’estensione VEC Helper documentata in questo articolo è stata creata utilizzando Manifest v2. Google ha recentemente annunciato che non consentirà più la creazione di nuove estensioni tramite Manifest v2.
>
>L’estensione esistente funziona ancora in Google Chrome. In futuro, [!DNL Adobe] renderà obsoleta l’estensione helper documentata in questo argomento e richiederà ai clienti di passare alla più recente [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). Quando l’estensione smetterà di funzionare, riceverai una notifica tramite le note sulla versione e il testo in questo articolo. Tuttavia, a causa dei miglioramenti alla sicurezza in Manifest v3, [!DNL Adobe] consiglia di scaricare la nuova estensione per continuare a creare visivamente i siti web in [!DNL Target].

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).
* Attualmente esistono alcune limitazioni riguardanti l’utilizzo del Compositore esperienza visivo per aprire un sito web che utilizza [Lavoratori del servizio](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW)

Un SW è una tecnologia web che può essere utilizzata per intercettare le richieste verso il dominio in cui è installato da una pagina web. SW sopravvive alla visita della pagina e si attiva nelle visite successive. SW decide quali richieste passare e quali vengono invece intercettate e servite da una cache.

SW può controllare la memorizzazione in cache; può memorizzare in cache la pagina web stessa, le risorse statiche come JS, CSS, IMG, le richieste AJAX, il loro contenuto e le relative intestazioni di risposta, incluse quelle che l’[estensione VEC Helper di Target](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) tenta di rimuovere, come X-Frame-Options: SAMEORIGIN, CSP (Content-Security-Policy) o Set-Cookie.

Sfortunatamente, le API di estensione di Chrome che intercettano le richieste web non ricevono le richieste intercettate e gestite da un SW. Pertanto, l’estensione non può correggere le intestazioni e i cookie se la richiesta di pagina web è stata servita da una cache da un SW, perché la pagina web non viene caricata nel Compositore esperienza visivo a causa delle intestazioni X-Frame-Options o CSP anch’esse memorizzate nella cache.

Come potenziale soluzione alternativa, puoi disabilitare i processi di lavoro dei serivizi dalla scheda Chrome Developer Tools > Application, quindi abilitare la casella di controllo “Bypass for network” nella sezione Service Workers.

* Stai utilizzando Google Chrome 80+ con criteri di imposizione dei cookie SameSite migliorati. Per ulteriori informazioni, consulta [In che modo i criteri di implementazione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

L’estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato ](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione VEC Helper

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

   Tieni presente che utilizzando il Compositore esperienza avanzato, l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [I riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il [!UICONTROL Compositore esperienza avanzato].
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Accedi a [Estensione del browser Adobe Target VEC Helper nel Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak).
1. Fai clic su **[!UICONTROL Aggiungi a Chrome > Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md).
1. (Condizionale) Scorri il **[!UICONTROL Inserisci librerie di Target]** passa alla posizione &quot;on&quot; se la pagina web non contiene ancora [!DNL Target] Libreria JavaScript at.js.

   La seguente illustrazione mostra VEC Helper con l’impostazione [!UICONTROL Inserisci librerie Target] abilitata:

   ![VEC Helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![VEC Helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Scorri il **[!UICONTROL Cookie]** attiva per aggiungere automaticamente `SameSite=None` correzione del browser attributi.

   ![Attivazione/disattivazione dei cookie nell’estensione VEC helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Per ulteriori informazioni sulla correzione dell’attributo del browser `SameSite=None`, consulta “In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Note

* Il flag [!UICONTROL Inserisci librerie di Target] nell’estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

   Questo flag è un&#39;impostazione globale. Il flag viene attivato o disattivato per tutti i siti web aperti nel Compositore esperienza visivo. Quindi, ad esempio, se imposti questo flag su &quot;on&quot; e apri un sito web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. L’Adobe prevede che la maggior parte dei clienti abbia già at.js implementato nelle proprie pagine e utilizzi l’impostazione predefinita &quot;off&quot;.

* L&#39;estensione carica la versione più recente di at.js disponibile nella [!DNL Target UI] in [!UICONTROL Amministrazione > Implementazione].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.
