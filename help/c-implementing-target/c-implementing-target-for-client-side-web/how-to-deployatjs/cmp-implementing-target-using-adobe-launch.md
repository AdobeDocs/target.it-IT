---
keywords: implement;implementing;implementation;adobe launch;launch;race;redirect;experience platform launch
description: ' Adobe Experience Platform Launch è la piattaforma di gestione tag di nuova generazione  Adobe ed è il metodo preferito per implementare  Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.'
title: Implementare Target con Adobe Launch
feature: null
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 82%

---


# Implementare Target con Adobe Launch{#implement-target-using-adobe-launch}

 Adobe Experience Platform Launch è la piattaforma di gestione tag di nuova generazione  Adobe ed è il metodo preferito per implementare  Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

## Implementare Target con Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

La tabella seguente elenca le diverse fonti da cui puoi ottenere ulteriori informazioni su Launch:

| Risorsa | Dettagli |
|--- |--- |
| [Implementazione di Target tramite l’ Adobe Target Extension Tutorial](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Questa esercitazione fornisce istruzioni dettagliate per implementare Adobe Target in un sito web con Launch. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un’esercitazione più ampia che mostra come implementare Adobe Launch e le altre soluzioni Adobe Experience Cloud. |
| [Documentazione di Adobe Launch](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html) | Informazioni sull’utilizzo e la gestione di tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate. |
| [Adobe Target Extension Documentazione](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/target-extension/overview.html) | Informazioni sull&#39;implementazione di Target mediante Launch. |

## Vantaggi dell&#39;implementazione di at.js con Target Launch Extension {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se si utilizza Adobe Launch per implementare at.js. Per questo motivo, si consiglia di utilizzare Adobe Launch anziché DTM o un&#39;implementazione manuale di at.js.

* **Risolve una situazione di tipo “race condition” tra Analytics e Target:** poiché la chiamata di Analytics potrebbe essere attivata prima della chiamata di Target, la chiamata di Target non viene unita alla chiamata di Analytics e si potrebbero generare dei dati errati. A partire dalla versione 0.6.0, l’estensione Target Launch garantisce che la chiamata beacon di Analytics attenda il completamento della chiamata di Target, sia che avvenga con successo oppure no. Questo dovrebbe risolvere incongruenze nei dati che i clienti potrebbero aver riscontrato.
* **Impedisce la gestione errata delle offerte di reindirizzamento:** se sulla pagina sono utilizzati sia Target che Analytics ed è presente un’offerta di reindirizzamento eseguita da Target, si potrebbero riscontrare dei problemi se la funzione di tracciamento di Analytics genera una richiesta quando non dovrebbe (perché l’utente viene reindirizzato a un URL diverso). Se implementi Target e Analytics tramite Launch, questo problema non si verifica. Utilizzando Launch, Target comunica ad Analytics di interrompere la richiesta beacon di Analytics.
