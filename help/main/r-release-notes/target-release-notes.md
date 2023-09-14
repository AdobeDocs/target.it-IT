---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b103d912b1ae953c44f2ad35da8a7ae83e7be2ae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 64%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 11 settembre 2023**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.9.3 (18 settembre 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato migliorato il Compositore esperienza visivo (VEC) per supportare Lightning DOM (Web Components). (TGT-45422)
* È stato risolto un problema che causava l’applicazione delle azioni del Compositore esperienza visivo in un ordine errato. In alcuni casi, il Compositore esperienza visivo ha applicato alcune modifiche in modo asincrono e l’aggiunta di modifiche aggiuntive a un elemento ha causato errori se tale elemento viene visualizzato dopo un’ [!UICONTROL Inserisci] azione. (TGT-45983)
* È stato risolto un problema relativo al Compositore esperienza visivo [!UICONTROL Sovrapposizione] funzionalità per il supporto di elementi in DOM shadow. (TGT-46217)
* È stato risolto un problema che si verificava all’apertura di una pagina di un’applicazione a pagina singola (SPA) nel Compositore esperienza visivo, quando si passava alla modalità Sfoglia, causava il malfunzionamento delle frecce Indietro e Avanti. (TGT-45956)
* È stato risolto un problema che impediva il caricamento di alcune pagine web nel Compositore esperienza visivo.

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
