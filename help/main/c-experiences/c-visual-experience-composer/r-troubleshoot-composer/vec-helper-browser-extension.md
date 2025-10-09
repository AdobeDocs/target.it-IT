---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Visual Experience Composer] (VEC). L’estensione VEC Helper per browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l'estensione helper [!UICONTROL Visual Experience Composer] (VEC)?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
source-git-commit: 6f4fd14a46f06c1366c02cfaf5a0cee5edbb00c4
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 50%

---

# Estensione helper [!UICONTROL Visual Experience Composer]

L&#39;estensione [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) Helper per il browser [!DNL Google Chrome] consente di caricare i siti Web in modo affidabile nel Compositore esperienza visivo per creare e verificare rapidamente le esperienze Web.

VEC Helper è un&#39;estensione [!DNL Chrome]. Questa estensione non è necessaria quando si utilizza [!DNL Mozilla Firefox].

>[!IMPORTANT]
>
>* L&#39;estensione VEC Helper legacy [!DNL Target] documentata in questo articolo è stata creata utilizzando Manifest V2. [!DNL Google] ha annunciato che non consentirà più le estensioni create utilizzando Manifest V2 a partire da giugno 2024. Per ulteriori informazioni, vedere l&#39;annuncio della sequenza temporale del supporto di [Manifest V2](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} da [!DNL Google] nel sito *Chrome for Developers*.
>
>* A partire da giugno 2024, [!DNL Google] inizierà a disabilitare le estensioni create utilizzando Manifest V2, inclusa l&#39;estensione documentata in questo argomento. [!DNL Adobe] consiglia ai clienti di passare al più recente [estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non appena possibile.

## Motivi per cui alcuni siti web potrebbero non aprirsi in modo affidabile nel Compositore esperienza visivo

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito per il controllo qualità o il sito di staging del cliente non è disponibile nel mondo esterno (è un sito interno).
* Attualmente esistono alcune limitazioni riguardanti l&#39;utilizzo del Compositore esperienza visivo per aprire un sito Web che utilizza [processi di lavoro dei servizi](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW).

Un SW è una tecnologia web che può essere utilizzata per intercettare le richieste verso il dominio in cui è installato da una pagina web. SW sopravvive alla visita della pagina e si attiva nelle visite successive. SW decide quali richieste passare e quali vengono invece intercettate e servite da una cache.

SW può controllare la memorizzazione in cache; può memorizzare in cache la pagina web stessa, le risorse statiche come JS, CSS, IMG, le richieste AJAX, il loro contenuto e le relative intestazioni di risposta, incluse quelle che l’[estensione VEC Helper di Target](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) tenta di rimuovere, come X-Frame-Options: SAMEORIGIN, CSP (Content-Security-Policy) o Set-Cookie.

Sfortunatamente, le API di estensione Chrome che intercettano le richieste web non ricevono le richieste intercettate e gestite da un SW. Pertanto, l’estensione non può correggere le intestazioni e i cookie se la richiesta di pagina web è stata servita da una cache da un SW, perché la pagina web non viene caricata nel Compositore esperienza visivo a causa delle intestazioni X-Frame-Options o CSP anch’esse memorizzate nella cache.

Come potenziale soluzione alternativa, è possibile disabilitare i processi di lavoro dei servizi dalla scheda Chrome Developer Tools > Application (Strumenti di sviluppo di > Applicazione), quindi abilitare la casella di controllo &quot;Bypass for network&quot; (Ignora per rete) nella sezione Service Workers (Lavoratori dei servizi).

* Stai utilizzando Google Chrome 80+ con criteri di imposizione dei cookie SameSite migliorati. Per ulteriori informazioni, consulta [In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite)?

L&#39;estensione VEC Helper per il browser Chrome risolve problemi di caricamento del sito, per i quali i clienti in genere si affidano a [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti, come Requestly.

## Vantaggi dell’utilizzo dell’estensione VEC Helper

* Tutte le intestazioni dei siti non compatibili con iframe, come X-Frame-Options e Content-Security-Policy, vengono rimosse implicitamente dal sito web. Non è più necessario creare regole complesse di Requestly.
* Se una pagina web non contiene ancora la libreria JavaScript di [!DNL Target] at.js, puoi utilizzare l’estensione per inserire la libreria in modo da creare esperienze per il sito web. Puoi quindi creare attività e controlli qualità tramite collegamenti di anteprima.

  Tieni presente che utilizzando il Compositore esperienza avanzato, l’estensione non inserisce at.js, ma la funzionalità per cookie SameSite è ancora presente. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.

* [I riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il [!UICONTROL Enhanced Experience Composer] (EEC).
* I clienti non ancora pratici di [!DNL Target] possono utilizzare l’estensione per fare prove con [!DNL Target] anche se i loro sviluppatori IT non hanno ancora implementato [!DNL Target] sui loro siti web.
* I partner che gestiscono siti web e account [!DNL Target] di più clienti ora hanno a disposizione un meccanismo semplice per supportare il caricamento del Compositore esperienza visivo, anziché gestire più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

1. Passa all&#39;estensione [Adobe Target VEC Helper per browser in Chrome Web Store](https://chromewebstore.google.com/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca).
1. Fare clic su **[!UICONTROL Add to Chrome > Add Extension]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Per utilizzare l’estensione, fai clic sull’icona dell’estensione VEC Helper per browser (![icona di VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png)) nella barra degli strumenti del browser Chrome quando sei nel Compositore esperienza visivo o in [Modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md).
1. (Facoltativo) Fai scorrere l&#39;opzione **[!UICONTROL Inject Target Libraries]** per attivare la pagina Web se non contiene ancora la libreria JavaScript at.js di [!DNL Target].

   Nella figura seguente viene illustrato VEC Helper con l&#39;impostazione [!UICONTROL Inject Target Libraries] abilitata:

   ![VEC Helper 1](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   La seguente illustrazione mostra VEC Helper che chiede se desideri inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![VEC Helper 2](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Far scorrere l&#39;interruttore **[!UICONTROL Cookies]** fino alla posizione &quot;on&quot; per aggiungere automaticamente la correzione dell&#39;attributo del browser `SameSite=None`.

   ![Attivazione/disattivazione dei cookie nell&#39;estensione VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Per ulteriori informazioni sulla correzione dell’attributo del browser `SameSite=None`, consulta “In che modo i criteri di imposizione dei cookie SameSite di Google Chrome recentemente annunciati influiscono sul Compositore esperienza visivo e sul Compositore esperienza avanzato?” in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Note

* Il flag [!UICONTROL Inject Target libraries] nell&#39;estensione è disattivato per impostazione predefinita. Abilita questo flag se desideri utilizzare il Compositore esperienza visivo su un sito non ancora implementato per [!DNL Target].

  Questo flag è un&#39;impostazione globale. Il flag viene abilitato o disabilitato per tutti i siti web aperti nel Compositore esperienza visivo. Quindi, ad esempio, se imposti questo flag su &quot;on&quot; e apri un sito web già implementato con at.js, riceverai un messaggio per informarti che at.js è già caricato. Adobe prevede che la maggior parte dei clienti abbia già at.js implementato nelle proprie pagine e utilizzi l’impostazione predefinita &quot;off&quot;.

* L&#39;estensione carica la versione più recente di at.js disponibile da [!DNL Target UI] in [!UICONTROL Administration > Implementation].
* Quando utilizzi l’estensione per inserire at.js durante la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), apri un’altra scheda Chrome. Questa scheda di Chrome deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l’attività.
* I messaggi seguenti ti mantengono informato:

   * Se il caricamento di un sito web utilizzando il Compositore esperienza visivo non riesce, appare un messaggio per suggerirti di installare l’estensione VEC Helper per browser.
   * Se at.js non è ancora implementato sul sito web, nel Compositore esperienza visivo appare un messaggio per suggerirti di installare l’estensione.
   * Se l’estensione è abilitata e il caricamento è migliorato, i messaggi appaiono quando l’estensione inserisce la libreria at.js (se necessario) o aiuta ad aprire il sito web in modo affidabile all’interno del Compositore esperienza visivo.
