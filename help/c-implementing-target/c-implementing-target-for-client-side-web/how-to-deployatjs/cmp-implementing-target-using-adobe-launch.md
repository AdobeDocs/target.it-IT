---
keywords: implementare;implementazione;implementazione;adobe launch;launch;corsa;reindirizzamento;platform launch esperienza;platform launch
description: Scopri come implementare la libreria Adobe [!DNL Target] at.js utilizzando Adobe Experience Platform Launch, il metodo preferito per implementare Adobe [!DNL Target].
title: Come si implementa [!DNL Target] utilizzando Adobe Launch?
feature: Implementare lato server
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
translation-type: tm+mt
source-git-commit: a69737f49a52cde703627f91d4b97609c1796ee6
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 10%

---

# Implementa [!DNL Target] utilizzando [!DNL Adobe Platform Launch]

[!DNL Adobe Experience Platform Launch] è la piattaforma di gestione tag di nuova generazione di  [!DNL Adobe] ed è il metodo preferito da implementare  [!DNL Adobe Target]. [!DNL Platform Launch] offre ai clienti un modo semplice di implementare e gestire i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

## Implementa [!DNL Target] utilizzando [!DNL Platform Launch] {#topic_5234DDAEB0834333BD6BA1B05892FC25}

La tabella seguente elenca le diverse fonti da cui puoi ottenere ulteriori informazioni su [!DNL Platform Launch]:

| Risorsa | Dettagli |
|--- |--- |
| [ [!DNL Target] Implementazione tramite il tutorial sull’estensione di  [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Questa esercitazione fornisce istruzioni dettagliate per implementare [!DNL Target] in un sito web con [!DNL Platform Launch]. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un&#39;esercitazione più ampia che mostra come implementare [!DNL Platform Launch] e altre soluzioni [!DNL Adobe Experience Cloud] . |
| [[!DNL Adobe Platform Launch] Documentazione](https://experienceleague.adobe.com/docs/launch/using/get-started/quick-start.html#get-started) | Informazioni sull’implementazione e la gestione dei tag di analisi, marketing e pubblicità necessari per fornire ai clienti esperienze personalizzate. |
| [ [!DNL Target] Documentazione di AdobeExtension](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informazioni sull&#39;implementazione di [!DNL Target] utilizzando [!DNL Platform Launch]. |

## Vantaggi dell&#39;implementazione di at.js utilizzando l&#39;estensione [!DNL Target] [!DNL Platform Launch] {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se utilizzi [!DNL Platform Launch] per implementare at.js. Per questo motivo, [!DNL Adobe] consiglia vivamente di utilizzare [!DNL Platform Launch] anziché un’implementazione manuale di at.js.

* **Risolve  [!DNL Adobe Analytics] e  [!DNL Target] race condition:** poiché la  [!DNL Analytics] chiamata potrebbe essere attivata prima della  [!DNL Target] chiamata di , la  [!DNL Target] chiamata non viene unita alla  [!DNL Analytics] chiamata di . Questa sequenza può causare dati errati. A partire dalla versione 0.6.0, l’ estensione [!DNL Platform Launch] assicura che la chiamata beacon [!DNL Analytics] attenda il completamento della chiamata [!DNL Target], sia che avvenga con successo o meno. Utilizzando [!DNL Platform Launch] è possibile risolvere le incongruenze nei dati che i clienti possono riscontrare durante l’implementazione manuale.
* **Impedisce la gestione errata delle offerte di reindirizzamento:** se sulla pagina  [!DNL Target] e  [!DNL Analytics] in presenza di un’offerta di reindirizzamento eseguita da  [!DNL Target], si può verificare una situazione in cui il  [!DNL Analytics] tracciatore genera una richiesta quando non dovrebbe (perché l’utente viene reindirizzato a un URL diverso). Se implementi [!DNL Target] e [!DNL Analytics] tramite [!DNL Platform Launch], questo problema non si verifica. Utilizzando [!DNL Platform Launch], [!DNL Target] indica a [!DNL Analytics] di interrompere la richiesta di beacon [!DNL Analytics].
