---
keywords: implementare;implementazione;implementazione;adobe launch;launch;corsa;reindirizzamento;platform launch esperienza;platform launch;tag;adobe platform
description: Scopri come implementare la libreria Adobe [!DNL Target] at.js utilizzando Adobe Experience Platform Launch, il metodo preferito per implementare Adobe [!DNL Target].
title: Come si implementa [!DNL Target] utilizzando Adobe Launch?
feature: Implementare lato server
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
source-git-commit: 82629fb4c543220796fc99d9c034ebb725e1a645
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 5%

---

# Implementa [!DNL Target] utilizzando [!DNL Adobe Experience Platform]

I tag in [!DNL Adobe Experience Platform] sono la nuova generazione di funzionalità di gestione tag di [!DNL Adobe]. I tag forniscono ai clienti un modo semplice di implementare e gestire i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

>[!NOTE]
>
>[!DNL Adobe Experience Platform Launch] è stato riclassificato come suite di tecnologie di raccolta dati in  [!DNL Adobe Experience Platform]. Di conseguenza, sono state introdotte diverse modifiche terminologiche nella documentazione del prodotto. Fare riferimento al seguente [documento](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) per un riferimento consolidato delle modifiche terminologiche.

Nella tabella seguente sono elencate le varie sorgenti in cui è possibile ottenere ulteriori informazioni:

| Risorsa | Dettagli |
|--- |--- |
| [Aggiungi  [!UICONTROL Adobe Target]](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-websites-with-launch/implement-solutions/target.html#implement-solutions) | Questa esercitazione fornisce istruzioni dettagliate per implementare [!DNL Target] in un sito web con tag in [!DNL Adobe Experience Platform]. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un&#39;esercitazione più ampia che mostra come implementare [!DNL Adobe Experience Platform] e altre soluzioni [!DNL Adobe Experience Cloud] . |
| [Guida rapida](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html) | Informazioni sull’implementazione e la gestione dei tag di analisi, marketing e pubblicità necessari per fornire ai clienti esperienze personalizzate. |
| [ [!DNL Target] Panoramica di Adobe extension](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/target/overview.html) | Informazioni sull&#39;implementazione di [!DNL Target] utilizzando [!DNL Adobe Experience Platform]. |

## Vantaggi dell&#39;implementazione di at.js utilizzando l&#39;estensione [!DNL Target] {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se utilizzi i tag in [!DNL Adobe Experience Platform] per implementare at.js. Per questo motivo, [!DNL Adobe] consiglia vivamente di utilizzare i tag in [!DNL Adobe Experience Platform] anziché un’implementazione manuale di at.js.

* **Risolve  [!DNL Adobe Analytics] e  [!DNL Target] race condition:** poiché la  [!DNL Analytics] chiamata potrebbe essere attivata prima della  [!DNL Target] chiamata di , la  [!DNL Target] chiamata non viene unita alla  [!DNL Analytics] chiamata di . Questa sequenza può causare dati errati. L&#39;estensione [!DNL Target] assicura che la chiamata beacon [!DNL Analytics] attenda il completamento della chiamata [!DNL Target], con esito positivo o meno. L’utilizzo dei tag in [!DNL Adobe Experience Platform] risolve le incongruenze nei dati che i clienti possono riscontrare durante l’implementazione manuale.
* **Impedisce la gestione errata delle offerte di reindirizzamento:** se sulla pagina  [!DNL Target] e  [!DNL Analytics] in presenza di un’offerta di reindirizzamento eseguita da  [!DNL Target], si può verificare una situazione in cui il  [!DNL Analytics] tracciatore genera una richiesta quando non dovrebbe (perché l’utente viene reindirizzato a un URL diverso). Se implementi [!DNL Target] e [!DNL Analytics] tramite tag in [!DNL Adobe Experience Platform], questo problema non si verifica. Utilizzando i tag in [!DNL Adobe Experience Platform], [!DNL Target] indica a [!DNL Analytics] di interrompere la richiesta di beacon [!DNL Analytics].
