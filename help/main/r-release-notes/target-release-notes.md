---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 2c4f5666b65bfc36885aad3907639a309e8c69f2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 59%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 14 marzo 2023**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.15.1 (8-9 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **8 marzo**: area geografica delle Americhe
* **9 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **9 marzo**: area geografica Asia Pacifico (APAC)

>[!NOTE]
>
>A causa di problemi che sono stati risolti nel frattempo, le metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]&quot; la funzionalità rilasciata l&#39;8 e il 9 marzo è stata temporaneamente rimossa. Dopo ulteriori test interni, la funzione verrà rilasciata di nuovo nelle prossime settimane.

Questa versione include le seguenti correzioni:

* Aggiornamenti per la creazione di componenti web personalizzati con la [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo):

   * È stata corretta la selezione degli elementi DOM ombra nel Compositore esperienza visivo, ottimizzando il processo di authoring in modo che non vi sia alcuna dipendenza dal [!DNL Target] tipo di implementazione durante la creazione della radice shadow. Ora, la selezione degli elementi DOM ombra nel Compositore esperienza visivo dovrebbe funzionare per qualsiasi sito web.
   * È stato risolto un problema che impediva il caricamento di elementi HTML utilizzando #Shadow DOM nel Compositore esperienza visivo. (TGT-35801)
   * Sono stati risolti i problemi del Compositore esperienza visivo con SPA siti web che utilizzano ShadowDOM. (TGT-43169)
   * È stato risolto un problema relativo all’obiettivo di ottimizzazione: &quot;clic su un elemento&quot; che non identificava correttamente il selettore CSS in ShadowDOM.

>[!NOTE]
>
>Per garantire la consegna delle modifiche create nel Compositore esperienza visivo, assicurati di utilizzare un [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) con una versione maggiore di 2.8.

**Problema noto**: Tracciamento dei clic su un elemento radice ombra quando si utilizza [!DNL Adobe Experience Platform Web SDK] non funziona correttamente. (TNT-47012)

## at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la restituzione di un errore della funzione `trackEvent`.

Per informazioni su tutte le versioni di at.js, consulta [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
