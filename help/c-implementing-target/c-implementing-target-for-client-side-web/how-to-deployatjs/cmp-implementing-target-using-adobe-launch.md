---
keywords: implementare;implementazione;implementazione;adobe launch;launch;corsa;reindirizzamento;platform launch esperienza
description: Scopri come implementare la libreria Adobe [!DNL Target] at.js utilizzando Adobe Experience Platform Launch, il metodo preferito per implementare Adobe [!DNL Target].
title: Come si implementa [!DNL Target] utilizzando Adobe Launch?
feature: Implementare lato server
role: Developer
exl-id: 7cc1d3ab-4a68-4454-95b0-04fa547a6d9e
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 75%

---

# Implementare [!DNL Target] utilizzando Adobe Launch

Adobe Experience Platform Launch è la piattaforma di gestione tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

## Implementare [!DNL Target] utilizzando Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

La tabella seguente elenca le diverse fonti da cui puoi ottenere ulteriori informazioni su Launch:

| Risorsa | Dettagli |
|--- |--- |
| [Tutorial sull’implementazione di Target tramite l’estensione Adobe Target](https://experienceleague.adobe.com/docs/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Questa esercitazione fornisce istruzioni dettagliate per implementare Adobe Target in un sito web con Launch. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un’esercitazione più ampia che mostra come implementare Adobe Launch e le altre soluzioni Adobe Experience Cloud. |
| [Documentazione di Adobe Launch](https://experienceleague.adobe.com/docs/launch/using/intro/get-started/quick-start.html) | Informazioni sull’utilizzo e la gestione di tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate. |
| [Documentazione sull’estensione di Adobe Target](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informazioni sull&#39;implementazione di Target mediante Launch. |

## Vantaggi dell&#39;implementazione di at.js utilizzando l&#39; [!DNL Target] estensione Launch {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se si utilizza Adobe Launch per implementare at.js. Per questo motivo, si consiglia di utilizzare Adobe Launch anziché DTM o un&#39;implementazione manuale di at.js.

* **Risolve una situazione di tipo “race condition” tra Analytics e Target:** poiché la chiamata di Analytics potrebbe essere attivata prima della chiamata di Target, la chiamata di Target non viene unita alla chiamata di Analytics e si potrebbero generare dei dati errati. A partire dalla versione 0.6.0, l’estensione Target Launch garantisce che la chiamata beacon di Analytics attenda il completamento della chiamata di Target, sia che avvenga con successo oppure no. Questo dovrebbe risolvere incongruenze nei dati che i clienti potrebbero aver riscontrato.
* **Impedisce la gestione errata delle offerte di reindirizzamento:** se sulla pagina sono utilizzati sia Target che Analytics ed è presente un’offerta di reindirizzamento eseguita da Target, si potrebbero riscontrare dei problemi se la funzione di tracciamento di Analytics genera una richiesta quando non dovrebbe (perché l’utente viene reindirizzato a un URL diverso). Se implementi Target e Analytics tramite Launch, questo problema non si verifica. Utilizzando Launch, Target comunica ad Analytics di interrompere la richiesta beacon di Analytics.
