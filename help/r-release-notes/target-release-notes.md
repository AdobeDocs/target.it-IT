---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates;prerelease
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL  Adobe Target più recenti o imminenti.
title: ' note sulla versione prerelease di Adobe Target'
feature: Release Notes
translation-type: tm+mt
source-git-commit: a85a5c10c31fb0d7eb00c21ff03b2012d044de45
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 20%

---


# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 14 gennaio 2021**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>**fine ciclo di vita** di mbox.js: Il 31 marzo 2021 non  [!DNL Adobe Target] supporterà più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività [!DNL Target] in esecuzione distribuendo contenuti predefiniti. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della nuova [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js prima di tale data, per evitare potenziali problemi con i siti.
>
>* **Adobe Experience Platform Web SDK**: L’ [!UICONTROL Adobe Experience Platform Web ] SDK consente di interagire con i vari servizi presenti nel  [!DNL Experience Cloud] (incluso  [!DNL Target]) tramite Adobe Experience Edge Network. Se scegli di eseguire la migrazione a [!DNL Adobe Experience Platform Web SDK], consulta [Cos&#39;è Adobe Experience Platform Web SDK](/help/c-implementing-target/c-implementing-target-for-client-side-web/aep-web-sdk.md) nella *Guida per l&#39;SDK Web*.
   >
   >
* **at.js**: La libreria JavaScript at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola. Se scegli di effettuare la migrazione a at.js, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [ Adobe Target Experience Builder: Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
>
>
Sebbene mbox.js sia attualmente supportato (fino al 31 marzo 2021), a partire da luglio 2017 non è disponibile alcun aggiornamento della funzione per questa libreria. Spostando tutti i clienti su [!UICONTROL Adobe Experience Platform Web SDK] o at.js, i nostri tecnici e personale di supporto saranno in grado di fornire nuove funzionalità e offrire il supporto che ci si aspetta da  Adobe.

## Target Standard/Premium 21.1.1 (19 gennaio 2021)

Questa versione di manutenzione contiene i seguenti miglioramenti, correzioni e modifiche.

I codici tra parentesi sono per uso interno di [!DNL Adobe].

* È stato aggiunto un avviso quando si seleziona una metrica [!DNL Adobe Analytics] quando si utilizza [!UICONTROL Analytics come origine di reporting] (A4T) in un&#39;attività [!UICONTROL Auto-Target]. [!UICONTROL I modelli di ] targeting automatico sono ottimizzati per funzionare con metriche binarie (basate sulla conversione). La selezione di una metrica continua, come le entrate, potrebbe avere risultati non ottimali e i report [!UICONTROL Personalization Insights] potrebbero non essere precisi. (TGT-38926)
* È stata aggiunta un&#39;icona di stato nel report [!UICONTROL Auto-Target Summary] per le attività [!UICONTROL Auto-Target] che utilizzano A4T. L&#39;icona di controllo verde accanto a ogni esperienza nel rapporto indica che per quell&#39;esperienza è stato generato un modello di apprendimento automatico personalizzato. L&#39;icona dell&#39;orologio indica che non è stato fornito abbastanza traffico per generare il modello. (TGT-38925)
* I report [!UICONTROL Segmenti automatizzati] e [!UICONTROL Attributi importanti] per le attività [!UICONTROL Auto-Target] che utilizzano le metriche di conversione A4T e [!DNL Analytics] vengono generati e hanno lo stesso aspetto di quando si utilizza [!DNL Target] come origine di reporting. (TGT-38931)
* Aggiunta un&#39;opzione di filtro dell&#39;ambiente all&#39;elenco [!UICONTROL Recommendations] [!UICONTROL Raccolte]. (TGT-38353)
* È stato risolto un problema che causava la visualizzazione del numero di prodotti errato nelle raccolte [!UICONTROL Recommendations]. (TGT-39162)
* È stato aggiunto un filtro [!UICONTROL Ultimo aggiornamento] alla [!UICONTROL Recommendations] [!UICONTROL Ricerca nel catalogo]. (TGT-38340)
* È stato risolto un problema in [!UICONTROL Recommendations] che causava il blocco della pagina [!UICONTROL Crea sequenza] dopo la modifica del settore verticale. (TGT-38160)
* È stato risolto un problema che impediva il salvataggio dell&#39;attività se Device Co-op era abilitato e l&#39;utente passava da [!DNL Target] come origine di reporting a [!DNL Analytics] (A4T). (TGT-38163)
* È stato risolto un problema che impediva agli utenti di rimuovere un&#39;audience da un&#39;offerta in un&#39;attività [!UICONTROL  Automated Personalization] (AP). (TGT-39058)
* È stato risolto un problema che causava la visualizzazione errata dell&#39;intervallo di tempo (date di inizio e fine) nelle schede [!UICONTROL Informazioni sull&#39;audience] per alcuni clienti. (TGT-39150)
* È stato risolto un problema che impediva ad alcuni clienti di visualizzare l&#39;elenco delle attività in [!UICONTROL Area di lavoro predefinita]. (TGT-38526)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
