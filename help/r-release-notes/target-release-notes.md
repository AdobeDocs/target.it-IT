---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni saranno incluse nella prossima versione?
feature: Note sulla versione
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: ea5a451e71f390ddacc6ccea583112dd831184dc
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 30%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 28 maggio 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere le stesse, a seconda della data di rilascio delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: A partire dal 31 marzo 2021,  [!DNL Adobe Target] non supporta più la libreria mbox.js . Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js hanno esito negativo e hanno un impatto positivo sulle pagine che hanno [!DNL Target] attività in esecuzione servendo il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, effettua la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

## ![Badgeversion 2.6.0 di Adobe Experience Platform Web SDK (1° giugno 2021) ](/help/assets/platform.png) [!DNL Adobe Experience Platform Web SDK] 

Questa versione di [!DNL Platform Web SDK] include il supporto per i seguenti elementi:

| Funzione | Dettagli |
| --- | --- |
| Supporto dei reindirizzamenti con [!UICONTROL Analytics for Target] (A4T) | L’SDK per web di Platform ora supporta i reindirizzamenti [!DNL Target] quando si utilizza [A4T](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Per ulteriori informazioni, consulta  [Analytics  [!DNL Target] for implementation](/help/c-integrating-target-with-mac/a4t/a4timplementation.md). |
| Token di risposta | L’SDK per web di Platform ora supporta i token di risposta [!DNL Target] .<br>Per ulteriori informazioni, consulta Token di  [risposta](/help/administrating-target/response-tokens.md). |

## [!DNL Target Standard/Premium] 21.5.1 (8 giugno 2021)

| Funzione | Dettagli |
| --- | --- |
| ![Badge Premium ](/help/assets/premium.png) [!DNL Recommendations] [!UICONTROL Catalog ] SearchAPI | Cerca nel catalogo di prodotti e contenuti [!DNL Recommendations] a livello di programmazione tramite API per identificare gli elementi che corrispondono a un criterio di ricerca e semplificare l’amministrazione del catalogo.<br>**Limitazioni e note**:<ul><li>La ricerca nel catalogo tramite API non è supportata per gli ambienti con più di 2.000.000 elementi.</li><li>I risultati della ricerca nel catalogo tramite API vengono aggiornati più rapidamente dei risultati della ricerca nel catalogo tramite l’ [!DNL Target] interfaccia utente. La ricerca nel catalogo nell’ [!DNL Target] interfaccia utente può richiedere altro tempo per riflettere i risultati più recenti.</li></ul>Per ulteriori informazioni, consulta [Ricerca di entità](http://developers.adobetarget.com/api/recommendations/#tag/Searching-Entities) nella guida *[!DNL Adobe Target][!DNL Recommendations] API* . |

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
