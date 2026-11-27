---
keywords: vec;compositore esperienza visivo; vec;iframe;estensione;browser;faq
description: Scopri perché alcuni siti web potrebbero non essere aperti in modo affidabile nel [!UICONTROL Compositore esperienza visivo]. L'estensione del browser [!UICONTROL Helper per editing video] consente di caricare i siti Web in modo affidabile nel Compositore esperienza visivo.
title: Come si utilizza l'estensione [!UICONTROL Helper per editing video]?
feature: Visual Experience Composer (VEC)
exl-id: e5aeb8b9-fab5-4ad4-882e-2106d2c9daab
TQID: 'https://experienceleague.adobe.com/wUWUT-FvVIAo52PDaBMfmT7vxv8VOR71hSGhxFvylus'
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
source-wordcount: '829'
ht-degree: 4%
---
# Estensione [!UICONTROL Helper per editing video] {#visual-editing-helper}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri in che modo l&#39;estensione del browser **[!UICONTROL Helper per editing video]** carica i siti Web in modo affidabile nel **[!UICONTROL Compositore esperienza visivo]** e come installarlo e utilizzarlo.

>[!ENDSHADEBOX]

L&#39;estensione del browser [!DNL Adobe Experience Cloud] **[!UICONTROL Helper per editing video]** per [!DNL Google Chrome] carica i siti Web in modo affidabile nel [!DNL Adobe Target] **[!UICONTROL Compositore esperienza visivo]** (VEC), rendendo più rapida l&#39;authoring e il controllo delle esperienze Web.

>[!IMPORTANT]
>
>Questa estensione sostituisce la precedente [Estensione VEC Helper per browser Target](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md), come descritto nella nota importante nella parte superiore di tale articolo. Il manifesto V3 introduce miglioramenti di sicurezza, pertanto [!DNL Adobe] richiede il download di questa nuova estensione per continuare a creare siti Web visivamente in [!DNL Target].

## Perché alcuni siti web non si aprono in modo affidabile nel Compositore esperienza visivo

Un sito web potrebbe non aprirsi in modo affidabile nel Compositore esperienza visivo per i seguenti motivi:

* Il sito web dispone di criteri di sicurezza rigidi.
* Il sito web si trova in un iframe.
* Il sito di controllo qualità o di gestione temporanea del cliente è interno e non disponibile all’esterno della rete.

L&#39;estensione risolve questi problemi di caricamento del sito, per i quali i clienti si affidano altrimenti al [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) o ad estensioni di terze parti come Requestly.

## Vantaggi dell’estensione

* **Intestazioni non compatibili con Iframe rimosse:** l&#39;estensione rimuove implicitamente dal sito Web intestazioni quali `X-Frame-Options` e `Content-Security-Policy`, pertanto non sono necessarie regole complesse di Requestly.
* **iniezione at.js:** quando una pagina web non contiene ancora la libreria at.js [!DNL Target], l&#39;estensione può inserirla. Le esperienze possono quindi essere create per il sito web e le attività possono essere create e controllate con collegamenti di anteprima. Con [Compositore esperienza avanzato](/help/main/administrating-target/visual-experience-composer-set-up.md#eec) (EEC), l&#39;estensione non inserisce at.js, ma la funzionalità per cookie SameSite rimane. Per inserire at.js nella pagina web, disattiva il Compositore esperienza avanzato.
* **Riquadri di visualizzazione per dispositivi mobili:** [riquadri di visualizzazione per dispositivi mobili](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md) sono supportati anche senza il **[!UICONTROL Compositore esperienza avanzato]** (EEC).
* **Nuovi clienti [!DNL Target]:** l&#39;estensione consente di sperimentare [!DNL Target] anche quando gli sviluppatori IT non hanno ancora implementato [!DNL Target] sul sito Web.
* **Partner:** partner che gestiscono siti Web e [!DNL Target] account di più clienti ottengono un meccanismo per supportare il caricamento del Compositore esperienza visivo, invece di più regole in strumenti di terze parti.

## Ottenere e installare l’estensione

L&#39;installazione dell&#39;estensione in [!DNL Chrome] consente di caricare i siti Web in modo affidabile nel Compositore esperienza visivo, inclusi i siti Web che bloccano gli iframe o in cui non è ancora implementato at.js.

1. Vai all&#39;estensione del browser [[!DNL Adobe Experience Cloud] **[!UICONTROL Helper per editing video &#x200B;]**&#x200B;in Chrome Web Store](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}.
1. Fai clic su **[!UICONTROL Aggiungi a Chrome]** > **[!UICONTROL Aggiungi estensione]**.
1. Apri il Compositore esperienza visivo in [!DNL Target].
1. Nel Compositore esperienza visivo o in Modalità Controllo qualità, fai clic sull&#39;icona dell&#39;estensione del browser **[!UICONTROL Helper per editing video]** ( ![icona Helper editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/visual-editing-helper.png) ) nella barra degli strumenti di [!DNL Chrome].

   L&#39;estensione viene abilitata automaticamente quando un sito Web viene aperto nel Compositore esperienza visivo [!DNL Target] per l&#39;authoring potente. Non dispone di impostazioni condizionali e gestisce automaticamente tutte le impostazioni, incluse le impostazioni per cookie SameSite. Per ulteriori informazioni sulla correzione del browser per l&#39;attributo `SameSite=None`, vedere [Criteri per cookie SameSite di Google Chrome](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md#samesite).

## Note sull’utilizzo

* L&#39;estensione carica la versione più recente di at.js disponibile nell&#39;interfaccia utente [!DNL Target] in **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]** e at.js scarica le librerie di authoring.
* Per utilizzare l&#39;estensione per inserire at.js nella modalità [Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md), è necessario aprire un&#39;altra scheda di Chrome. Questa scheda deve essere autenticata nella stessa organizzazione [!DNL Adobe Experience Cloud] in cui è stata creata l&#39;attività.
* Il Compositore esperienza visivo visualizza messaggi che suggeriscono l’installazione dell’estensione nei seguenti casi:

  * Il caricamento di un sito web nel Compositore esperienza visivo non riesce.
  * at.js o alloy.js non è ancora implementato sul sito web.

* Se la nuova estensione è stata tentata e l&#39;estensione [vecchia](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md) viene nuovamente utilizzata, ma [!DNL Target] non riesce a caricare il sito Web, cancellare tutti i dati del browser e disabilitare la nuova estensione.

## Ultime modifiche dell’estensione (17 gennaio 2026)

L’estensione aggiunge una funzione sperimentale di pulizia dei cookie di avvio a VEC Helper. La funzione pulisce i cookie non partizionati una volta per scheda all’inizio dell’authoring, anziché in modo continuo, migliorando le prestazioni e l’affidabilità. Tiene traccia della cronologia di ogni scheda per evitare la pulizia ridondante e la cancella quando la scheda viene chiusa, in modo che la pulizia si comporti correttamente quando la scheda viene riaperta. Gli unit test garantiscono un comportamento coerente.

![Opzioni dell&#39;estensione VEC Helper, incluse le modalità di elaborazione dei cookie, l&#39;opzione di registrazione avanzata e le funzionalità sperimentali Ritarda il caricamento della pagina Web, la pulizia dei cookie e la pulizia dei cookie di avvio](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper.png)

## Domande frequenti

+++ L&#39;estensione esegue operazioni quando viene utilizzata al di fuori di [!DNL Adobe Target] o [!UICONTROL Adobe Journey Optimizer] (AJO)?

L&#39;estensione viene attivata solo quando il sito Web viene caricato all&#39;interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]). Al di fuori di questo flusso, l’estensione non tenta di aggiungere, rimuovere o modificare alcuna intestazione né di inserire codice all’interno del sito web.

+++

+++ Cosa fa l’estensione quando è attiva nel Compositore esperienza visivo [!DNL Adobe Target]?

Quando un sito Web viene caricato all&#39;interno di un iFrame nei prodotti [!DNL Adobe] ([!DNL Target], [!DNL AJO]), l&#39;estensione inserisce nel sito Web il codice associato all&#39;estensione e scarica i file helper dalla rete CDN [!DNL Adobe] per abilitare l&#39;authoring visivo.

+++
