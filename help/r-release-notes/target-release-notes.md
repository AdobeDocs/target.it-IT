---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 146395f5453093ca34b259a143ff4e4c63be949b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 7 giugno 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Termine del ciclo di vita di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività [!DNL Target] in esecuzione, che presenteranno il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## [!DNL Target Standard/Premium] 21.5.2 (data da definire)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | I seguenti miglioramenti si applicano agli algoritmi di popolarità di [!DNL Recommendations]:<ul><li>Una nuova opzione “Intervallo di lookback” (intervallo di dati) di sei ore sarà disponibile per tutti gli algoritmi di popolarità (Più visualizzati/Più venduti) quando si utilizza [!DNL Target] come origine dei dati comportamentali. (Questo intervallo di lookback *non* è disponibile quando l’origine dei dati comportamentali è [!DNL Adobe Analytics].)</li><li>Se selezionato, i seguenti algoritmi verranno eseguiti approssimativamente ogni tre ore (anziché ogni 12 ore).<ul><li>Articoli più visualizzati</li><li>Più acquistati</li><li>Più visualizzati per categoria</li><li>Più acquistati per categoria</li><li>Più visualizzati per attributo personalizzato (utilizzando la funzione groupBy)</li><li>Più acquistati per attributo personalizzato (utilizzando la funzione groupBy)</li></ul></ul>(TOP-1086) |

Questa versione include le seguenti correzioni.

* Il contenuto verrà aggiunto con l’approssimarsi della data di rilascio.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
