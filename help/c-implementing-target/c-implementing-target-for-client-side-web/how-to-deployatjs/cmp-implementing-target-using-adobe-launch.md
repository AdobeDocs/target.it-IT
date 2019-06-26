---
description: Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.
keywords: implementare;implementazione;implementa;adobe launch;launch;corsa;redirect
seo-description: Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.
seo-title: Implementare Target con Adobe Launch
title: Implementare Target con Adobe Launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Implementare Target con Adobe Launch{#implement-target-using-adobe-launch}

Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

## Implementare Target con Adobe Launch {#topic_5234DDAEB0834333BD6BA1B05892FC25}

Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.

La tabella seguente elenca le diverse fonti da cui puoi ottenere ulteriori informazioni su Launch:

| Risorsa | Dettagli |
|--- |--- |
| [Implementazione di Target tramite l&#39;esercitazione di estensione Adobe Target](https://docs.adobe.com/content/help/en/experience-cloud/implementing-in-websites-with-launch/implement-solutions/target.html) | Questa esercitazione fornisce istruzioni dettagliate per implementare Adobe Target in un sito web con Launch. Gli argomenti includono l’aggiunta della libreria JavaScript at.js, l’attivazione della mbox globale, l’aggiunta di parametri e l’integrazione con altre soluzioni. Questo articolo fa parte di un’esercitazione più ampia che mostra come implementare Adobe Launch e le altre soluzioni Adobe Experience Cloud. |
| [Documentazione di Adobe Launch](https://docs.adobelaunch.com/getting-started) | Informazioni sull&#39;utilizzo e la gestione di tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate. |
| [Documentazione su Adobe Target Extension](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension) | Informazioni sull&#39;implementazione di Target mediante Launch. |

## Vantaggi dell&#39;implementazione di at.js con Target Launch Extension {#section_48B3F938B6F8491DAF798E0DB54EF304}

I seguenti vantaggi si applicano solo se si utilizza Adobe Launch per implementare at.js. Per questo motivo, si consiglia di utilizzare Adobe Launch anziché DTM o un&#39;implementazione manuale di at.js.

* **Solves Analytics and Target Race Condition:** Poiché la chiamata di Analytics potrebbe essere attivata prima della chiamata di Target, la chiamata di Target non è vincolata alla chiamata Analytics. Questo può portare a dati non corretti. A partire da 0.6.0, l&#39;estensione di Target Launch assicura che la chiamata beacon di Analytics attende che la chiamata di Target venga completata correttamente o meno. Questo dovrebbe risolvere le incongruenze dei dati che i clienti potrebbero aver riscontrato.
* **Impedisce la gestione delle offerte di reindirizzamento errato:** Se nella pagina hai Target e Analytics ed è presente un&#39;offerta di reindirizzamento eseguita da Target, potresti rilevare una situazione in cui il tracker di Analytics attiva una richiesta quando non dovrebbe (perché l&#39;utente viene reindirizzato a un URL diverso). Se implementi Target e Analytics tramite Launch, non potrai affrontare questo problema. Utilizzando Launch, Target fa in modo che Analytics interrompa la richiesta del beacon Analytics.