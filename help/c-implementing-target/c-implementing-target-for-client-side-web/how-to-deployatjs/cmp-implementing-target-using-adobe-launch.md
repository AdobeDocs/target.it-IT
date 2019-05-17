---
description: Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.
keywords: implementare;implementazione;implementa;adobe launch;launch;corsa;redirect
seo-description: Launch è la piattaforma di gestione dei tag di nuova generazione di Adobe ed è il metodo preferito per implementare Adobe Target. Launch offre ai clienti un modo semplice di implementare e gestire tutti i tag di analisi, marketing e annunci pubblicitari necessari per fornire ai clienti esperienze personalizzate.
seo-title: Implementare Target con Adobe Launch
title: Implementare Target con Adobe Launch
uuid: c8cd855b-bed1-4fc2-a0e3-f1ea6ab620e6
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

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

* **Consente la distribuzione asincrona di Target:** Per ulteriori informazioni, consultate &quot;Adobe Target Extension with an Asynchronous Deployment&quot; (Estensione asincrona con distribuzione asincrona) nella documentazione di [Adobe Target Extension](https://docs.adobelaunch.com/extension-reference/web/adobe-target-extension).
* **Risolve le corse critiche tra Analytics e Target:** poiché la chiamata di Analytics potrebbe essere attivata prima della chiamata di Target, la chiamata di Target non è ancorata alla chiamata di Analytics e si potrebbero generare dei dati errati. A partire da Launch 0.6.0, l&#39;estensione Target Launch garantisce che il segnale di Analytics venga messo in attesa fino al completamento della chiamata di Target, sia che avvenga con successo oppure no. Questo dovrebbe risolvere le incongruenze dei dati che i clienti potrebbero aver riscontrato.
* **Impedisce la gestione errata delle offerte di reindirizzamento:** quando si dispone sia di Target che Analytics sulla pagina e si è verificata un’offerta di reindirizzamento da parte di Target, si potrebbero riscontrare dei problemi se il Tracker Analytics genera una richiesta quando non dovrebbe perché l’utente viene reindirizzato a un URL diverso. Se si implementano Target e Analytics, non si verifica questo problema, poiché usando di Launch, Target determina l&#39;arresto della richiesta di segnale di Analytics.

