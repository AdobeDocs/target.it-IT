---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Compositore esperienza visivo]. L’estensione VEC Helper per browser consente di caricare i siti web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l'estensione Helper [!UICONTROL Compositore esperienza visivo]?
feature: Visual Experience Composer (VEC)
exl-id: 3f38db69-046d-42c9-8c09-eca11d404b12
TQID: 'https://experienceleague.adobe.com/lqZGGWG1NVtKDzNGPq5k2bDPzxDfNWqPtJ-bYfLCr3Q'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: c93393a4-e558-47e1-992e-c91ed4d480ce
    internal-label: Implementation
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
subfeature_v2:
  - id: fd0ff162-b6d3-4a11-8aeb-e165a01c0f0a
    internal-label: at.js
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
    internal-label: Web experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 5%
---
# Estensione helper [!UICONTROL Compositore esperienza visivo] {#vec-helper-extension}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri in che modo l&#39;estensione legacy VEC Helper del browser carica i siti Web nel **[!UICONTROL Compositore esperienza visivo]** (VEC) e come installarlo e utilizzarlo.

>[!ENDSHADEBOX]

L&#39;estensione del browser Helper [!DNL Adobe Target] **[!UICONTROL Compositore esperienza visivo]** per [!DNL Google Chrome] carica i siti Web in modo affidabile nel Compositore esperienza visivo, velocizzando l&#39;authoring e il controllo delle esperienze Web. Estensione non necessaria in [!DNL Mozilla Firefox].

>[!IMPORTANT]
>
>* L&#39;estensione VEC Helper [!DNL Target] legacy, documentata in questo articolo, è stata creata con Manifest V2. [!DNL Google] ha annunciato che non consentirà più le estensioni create con Manifest V2 a partire da giugno 2024. Per ulteriori informazioni, vedere l&#39;annuncio della sequenza temporale del supporto di [Manifest V2](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline){target=_blank} da [!DNL Google] nel sito *Chrome for Developers*.
>
>* A partire da giugno 2024, [!DNL Google] disabilita le estensioni create con Manifest V2, inclusa l&#39;estensione documentata in questo articolo. [!DNL Adobe] consiglia di passare al più recente [estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non appena possibile.

## Perché alcuni siti web non si aprono in modo affidabile nel Compositore esperienza visivo

Un sito web potrebbe non aprirsi in modo affidabile nel Compositore esperienza visivo per i seguenti motivi:

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* La libreria at.js non è ancora implementata sul sito web.
* Il sito di controllo qualità o di gestione temporanea del cliente è interno e non disponibile all’esterno della rete.
* Il sito Web utilizza [processi di lavoro dei servizi](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API){target=_blank} (SW), attualmente supportati dal Compositore esperienza visivo con limitazioni. Consulta la sezione seguente.
* Il sito Web viene aperto in [!DNL Chrome] 80 o versione successiva, che applica i criteri per cookie SameSite. Per ulteriori informazioni, vedere [Criteri per cookie SameSite di Google Chrome](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

L&#39;estensione VEC Helper per il browser [!DNL Chrome] risolve i problemi di caricamento del sito, per i quali i clienti altrimenti si affidano a [!DNL Target] [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o estensioni di terze parti come Requestly.

### Lavoratori del servizio

Un service worker (SW) è una tecnologia web che una pagina web installa per intercettare le richieste per il proprio dominio. SW sopravvive alla visita della pagina e si attiva nelle visite successive. Decide quali richieste passare e quali vengono intercettate e servite da una cache.

Un SW può memorizzare in cache la pagina web stessa, le risorse statiche come JS, CSS, IMG e le richieste di AJAX, il loro contenuto e le relative intestazioni di risposta. Queste intestazioni includono quelle che l&#39;estensione [Target VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) tenta di rimuovere, ad esempio `X-Frame-Options: SAMEORIGIN`, CSP (`Content-Security-Policy`) e `Set-Cookie`.

Le API dell&#39;estensione [!DNL Chrome] che intercettano le richieste Web non ricevono le richieste intercettate e gestite da un SW. Quando un SW invia la richiesta di pagina web da una cache, l’estensione non può correggere le intestazioni e i cookie e la pagina non viene caricata nel Compositore esperienza visivo a causa delle intestazioni `X-Frame-Options` o CSP memorizzate nella cache.

Come potenziale soluzione alternativa, disabilitare i processi di lavoro dei servizi nella scheda [!DNL Chrome] Developer Tools > **Application**, quindi abilitare la casella di controllo &quot;Bypass for network&quot; nella sezione Service Workers.

## Vantaggi dell’estensione VEC Helper

* **Intestazioni non compatibili con Iframe rimosse:** l&#39;estensione rimuove implicitamente dal sito Web intestazioni quali `X-Frame-Options` e `Content-Security-Policy`, pertanto non sono necessarie regole complesse di Requestly.
* **Iniezione at.js:** quando una pagina web non contiene ancora la libreria JavaScript at.js di [!DNL Target], l&#39;estensione può inserirla. Le esperienze possono quindi essere create per il sito web e le attività possono essere create e controllate con collegamenti di anteprima. Con il Compositore esperienza avanzato, l’estensione non inserisce at.js, ma rimane la funzionalità per cookie SameSite. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.
* **Riquadri di visualizzazione per dispositivi mobili:** [riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il **[!UICONTROL Compositore esperienza avanzato]** (EEC).
* **Nuovi clienti [!DNL Target]:** l&#39;estensione consente di sperimentare [!DNL Target] anche quando gli sviluppatori IT non hanno ancora implementato [!DNL Target] sul sito Web.
* **Partner:** partner che gestiscono siti Web e [!DNL Target] account di più clienti ottengono un meccanismo per supportare il caricamento del Compositore esperienza visivo, invece di più regole in strumenti di terze parti.

## Ottenere e installare l’estensione VEC Helper per browser

L&#39;installazione dell&#39;estensione in [!DNL Chrome] consente di caricare i siti Web in modo affidabile nel Compositore esperienza visivo, inclusi i siti Web che bloccano gli iframe o in cui non è ancora implementato at.js.

1. Vai all&#39;estensione [Adobe Target VEC Helper per browser nel Chrome Web Store](https://chromewebstore.google.com/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca).
1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Nel Compositore esperienza visivo o in modalità [Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), fai clic sull&#39;icona dell&#39;estensione VEC Helper per browser ( ![icona VEC Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension.png) ) nella barra degli strumenti di [!DNL Chrome].
1. (Condizionale) Se la pagina Web non contiene ancora la libreria JavaScript at.js di [!DNL Target], attiva l&#39;opzione **[!UICONTROL Inserisci librerie di destinazione]**.

   La figura seguente mostra VEC Helper con l&#39;impostazione **[!UICONTROL Inserisci librerie di destinazione]** abilitata:

   ![Pannello dell&#39;estensione VEC Helper con l&#39;opzione Inserisci librerie di Target attivata e l&#39;opzione Cookie disattivata, a indicare che l&#39;impostazione Cookie imposta i flag SameSite=None e Secure su tutti i cookie per le richieste all&#39;interno del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-help-extension-1.png)

   VEC Helper chiede quindi se inserire le librerie [!DNL Target] nella pagina per abilitare l’authoring:

   ![Viene visualizzato il messaggio di richiesta Inserisci librerie di Target per indicare che l&#39;estensione VEC Helper di Target desidera inserire le librerie di Target nella pagina per abilitare l&#39;authoring, con i pulsanti Annulla e Consenti](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/vec-helper.png)

1. (Condizionale) Attiva **[!UICONTROL Cookie]** per aggiungere automaticamente la correzione dell&#39;attributo del browser `SameSite=None`.

   ![Pannello dell&#39;estensione VEC Helper con l&#39;opzione Cookie attivata ed evidenziata, sopra il Compositore esperienza visivo che mostra una pagina di esempio](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/cookies-vec-helper.png)

   Per ulteriori informazioni sulla correzione del browser per l&#39;attributo `SameSite=None`, vedere [Criteri per cookie SameSite di Google Chrome](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Note sull’utilizzo

* Il flag **[!UICONTROL Inserisci librerie di destinazione]** nell&#39;estensione è disattivato per impostazione predefinita. Attivarlo per utilizzare il Compositore esperienza visivo su un sito in cui [!DNL Target] non è ancora implementato.

  Il flag è un’impostazione globale e pertanto è abilitato o disabilitato per tutti i siti web aperti nel Compositore esperienza visivo. Ad esempio, con il flag on, quando si apre un sito web in cui è già implementato at.js viene visualizzato un messaggio che informa che at.js è già caricato. [!DNL Adobe] prevede che la maggior parte dei clienti abbia già at.js implementato nelle proprie pagine e utilizzi l&#39;impostazione predefinita off.

* L&#39;estensione carica la versione più recente di at.js disponibile nell&#39;interfaccia utente [!DNL Target] in **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
* Per utilizzare l&#39;estensione per inserire at.js nella modalità [Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), è necessario aprire un&#39;altra scheda di Chrome. Questa scheda deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l&#39;attività.
* Il Compositore esperienza visivo visualizza i messaggi nei casi seguenti:

  * Il caricamento di un sito web nel Compositore esperienza visivo non riesce. Il messaggio suggerisce di installare l’estensione VEC Helper per browser.
  * at.js non è ancora implementato sul sito web. Il messaggio suggerisce di installare l’estensione.
  * L&#39;estensione è abilitata e attiva il caricamento. I messaggi vengono visualizzati quando l’estensione inserisce la libreria at.js di, se necessario, o aiuta ad aprire il sito web in modo affidabile nel Compositore esperienza visivo.
