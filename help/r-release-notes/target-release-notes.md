---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b897829595ef1cdda28a995481fa1d2d5d1616f4
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 79%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 24 giugno 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.6.1 (30 giugno 2021)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| Analytics for Target (A4T) | Facendo clic sul collegamento &quot;[!UICONTROL Visualizza in Analytics]&quot; sulla pagina [!UICONTROL Rapporti] da un&#39;attività che utilizza [!DNL Analytics] come origine per la generazione di rapporti (A4T), [!DNL Analysis Workspace] viene ora aperto. In precedenza, il collegamento apriva il rapporto [!DNL Analytics] . (TGT-36959) |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | I seguenti miglioramenti si applicano agli algoritmi di popolarità di [!DNL Recommendations]:<ul><li>È disponibile una nuova opzione &quot;intervallo di lookback&quot; (intervallo di dati) di sei ore per tutti gli algoritmi di popolarità (Più venduti/Più venduti) quando [!DNL Target] è l’origine dei dati comportamentali. (Questo intervallo di lookback *non* è disponibile quando l’origine dei dati comportamentali è [!DNL Adobe Analytics].)</li><li>Quando è selezionata questa opzione, i seguenti algoritmi vengono eseguiti approssimativamente ogni tre ore (anziché ogni 12 ore).<ul><li>Articoli più visualizzati</li><li>Più acquistati</li><li>Più visualizzati per categoria</li><li>Più acquistati per categoria</li><li>Più visualizzati per attributo personalizzato (utilizzando la funzione groupBy)</li><li>Più acquistati per attributo personalizzato (utilizzando la funzione groupBy)</li></ul></ul>Data di rilascio da annunciare. (TOP-1086) |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
