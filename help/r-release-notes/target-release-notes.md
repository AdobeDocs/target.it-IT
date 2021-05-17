---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b14c9bb4bc0363c77de084c7ae7110e73c5f2f13
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 36%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 17 maggio 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere le stesse, a seconda della data di rilascio delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js hanno esito negativo e hanno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## at.js versione 2.5.0 (13 maggio 2021)

Questa versione di at.js include i miglioramenti e le modifiche seguenti:

* [Supporto ](/help/c-implementing-target/c-implementing-target-for-client-side-web/on-device-decisioning/on-device-decisioning.md) decisionale su dispositivo per at.js.
* [Supporto dei ](/help/c-activities/c-activity-qa/activity-qa.md) collegamenti di anteprima per le attività di  [!UICONTROL Automated Personalization]  (AP)

Questa versione rimuove anche il supporto per Microsoft Internet Explorer 10, Internet Explorer 11 e tutte le versioni precedenti. Microsoft Edge continua a essere supportato in at.js 2.5.0 e versioni successive. Per ulteriori informazioni, consulta [Browser supportati](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## [!DNL Adobe Experience Platform Web SDK] versione 2.5.0 (24 maggio 2021)

Questa versione di [!DNL Platform Web SDK] include il supporto per [!UICONTROL Analytics for Target] (A4T) per i reindirizzamenti [!DNL Target].

## [!DNL Target Standard/Premium] 21.5.1 (8 giugno 2021)

Il contenuto verrà aggiunto con l’approssimarsi della data di rilascio.

## [!DNL Target Standard/Premium] 21.5.2 (Data da determinare)

Questa versione contiene le nuove funzioni e i miglioramenti seguenti. I codici tra parentesi sono per uso interno di [!DNL Adobe].

| Funzione | Dettagli |
| --- | --- |
| ![Premium](/help/assets/premium.png) [!DNL Recommendations] | I seguenti miglioramenti si applicano agli algoritmi di popolarità [!DNL Recommendations]:<ul><li>Una nuova opzione &quot;Intervallo di lookback&quot; (intervallo di dati) di sei ore sarà disponibile per tutti gli algoritmi di popolarità (Più venduti/Più venduti) quando [!DNL Target] è l’origine dei dati comportamentali. (Questo intervallo di lookback è *non* disponibile quando [!DNL Adobe Analytics] è l’origine dei dati comportamentali.)</li><li>Se selezionato, i seguenti algoritmi verranno eseguiti approssimativamente ogni tre ore (anziché ogni 12 ore).<ul><li>Più visualizzati</li><li>Più acquistati</li><li>Più visualizzate per categoria</li><li>Più acquistati per categoria</li><li>Visualizzato più da attributo personalizzato (utilizzando la funzione groupBy)</li><li>La maggior parte degli acquisti effettuati dall&#39;attributo personalizzato (utilizzando la funzione groupBy)</li></ul></ul>(TOP-1086) |

Questa versione contiene le seguenti correzioni.

* Il contenuto verrà aggiunto con l’approssimarsi della data di rilascio.

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
