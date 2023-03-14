---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 8cdf362d9e45153b26bca5a45ed59ef557adc016
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 44%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 14 marzo 2023**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.15.1 (8 e 9 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **8 marzo**: area geografica delle Americhe
* **9 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **9 marzo**: area geografica Asia-Pacifico (APAC)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] | [!DNL Target] consente di scegliere metriche basate su eventi binomiali o metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività.<P>Tieni presente le seguenti modifiche nelle metriche supportate:<ul><li>[!DNL Target] ha mantenuto il comportamento precedente per le attività esistenti fino a (DATA DA DETERMINARE). Dopo questa data, le attività che utilizzano metriche non supportate verranno interrotte per forzare la migrazione delle attività esistenti al nuovo comportamento.</li></ul>Per ulteriori informazioni, consulta [Metriche obiettivo supportate](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md#supported) in *Supporto A4T per attività di allocazione automatica e targeting automatico*. |
| [!UICONTROL Allocazione automatica] utilizzo [!UICONTROL Analytics for Target] (A4T) | Nuovo tutorial:<ul><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Allocazione automatica] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html){target=_blank}</li></ul> |
| [!UICONTROL Targeting automatico] utilizzo [!UICONTROL Analytics for Target] (A4T) | Nuovo tutorial:<ul><li>[Configurazione dei rapporti A4T in [!DNL Analysis Workspace] per [!UICONTROL Targeting automatico] attività](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html){target=_blank}</li></ul> |

Questa versione include le seguenti correzioni:

* Aggiornamenti per la creazione di componenti web personalizzati con [!UICONTROL Compositore esperienza visivo] (VEC):

   * È stata corretta la selezione degli elementi DOM dell’ombreggiatura nel Compositore esperienza visivo, migliorando il processo di authoring in modo che non vi sia alcuna dipendenza da [!DNL Target] tipo di implementazione durante la creazione della directory principale shadow. Ora, la selezione degli elementi DOM ombra nel Compositore esperienza visivo dovrebbe funzionare per qualsiasi sito web.
   * È stato risolto un problema che impediva il caricamento di elementi HTML utilizzando #Shadow DOM nel Compositore esperienza visivo. (TGT-35801)
   * Sono stati risolti i problemi relativi al Compositore esperienza visivo con i siti web SPA che utilizzavano ShadowDOM. (TGT-43169)
   * È stato risolto un problema relativo all’obiettivo di ottimizzazione: &quot;clic su un elemento&quot; che non identificava correttamente il selettore CSS in ShadowDOM.

>[!NOTE]
>
>Per garantire la trasmissione delle modifiche create nel Compositore esperienza visivo, assicurati di utilizzare una [!DNL Target] SDK ([at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} or [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html){target=_blank} (alloy.js)) con una versione superiore a 2.8.

**Problema noto**: tracciamento dei clic su un elemento principale ombra quando si utilizza [!DNL Adobe Experience Platform Web SDK] non funziona correttamente. (TNT-47012)

## at.js versione 2.10.2 (7 marzo 2023)

* È stato risolto un problema che causava la `trackEvent` per restituire sempre un errore.

Per informazioni su tutte le versioni di at.js, vedi [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
