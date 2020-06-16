---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni di Adobe Target DNL più recenti o imminenti .
title: Note sulla versione prerelease  Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 62a22032f45a7ae6c4d52b4d4170039ac5e5387d
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 17%

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 17 giugno 2020**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!NOTE]
>
>* **mbox.js obsoleto**: Il 30 agosto 2020  Adobe Target non supporterà più la libreria mbox.js. Dopo il 30 agosto 2020, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto sulle pagine che hanno attività Target in esecuzione. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Experience Builder (Funzionamento di At.js e Generatore di competenze di ): Chat sviluppatore, migrate  Adobe Target  mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Spostando tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni di Target Coffee Break. Per ulteriori informazioni, consultate Annunci [Target](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.5.1 (17 giugno 2020)

| Funzionalità/Miglioramento | Descrizione |
| --- | --- |
| Analytics for Target (A4T) supporto per le attività di allocazione automatica | Con la release di giugno, i test di allocazione automatica supporteranno [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md). Questa integrazione consente di utilizzare la funzionalità di allocazione automatica delle bande armate multiple per indirizzare il traffico verso esperienze vincenti, utilizzando al contempo una metrica di obiettivo Adobe  Analytics e/o funzionalità di reporting e analisi di Adobe  Analytics. Se avete già [implementato A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) per l’utilizzo con le attività Test A/B e Targeting delle esperienze, siete tutti impostati! |
| Ruolo editore | Questo nuovo ruolo è simile a quello corrente dell&#39;osservatore (può visualizzare le attività, ma non può crearle o modificarle). Tuttavia, il ruolo Editore dispone dell&#39;autorizzazione aggiuntiva per attivare le attività. |
| Supporto A4T nel 25 [!DNL Analysis Workspace]<br>giugno 2020 | [!UICONTROL Analytics per Target] (A4T) ora è supportato in [!DNL Analysis Workspace]. Il [!UICONTROL pannello] Analytics per Target (A4T) consente di analizzare le [!DNL Adobe Target] attività e le esperienze in [!DNL Analysis Workspace].<br>Per ulteriori informazioni, consultate [pannello](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/panels/a4t-panel.html) Analytics per Target (A4T) nella Guida *agli strumenti di* Analytics. |

### Miglioramenti, correzioni e modifiche

* È stato risolto un problema che causava la memorizzazione della metrica &quot;visitatori&quot; nella definizione dell&#39;attività invece di &quot;VisitatoriUnivoci&quot;. (TGT-37098)
* È stato risolto un problema nell&#39; [!DNL Target] interfaccia utente a causa del quale la barra di scorrimento verticale non funzionava correttamente nella pagina [!UICONTROL Audiences] . (TGT-36968)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
