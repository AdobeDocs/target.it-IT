---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni di Adobe Target DNL più recenti o imminenti .
title: Note sulla versione prerelease  Adobe Target
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: d37cd2e93af576741dfd17f8e54dada06b8a64a3
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 19%

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 24 giugno 2020**

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


## Target Standard/Premium 20.7.1 (21 luglio 2020)

Questa versione include i seguenti miglioramenti:

###  supporto Analytics per Target (A4T) per le attività [!UICONTROL Auto-Target]

[!UICONTROL Le attività di Target] automatico ora supportano [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md).

Questa integrazione utilizza l&#39;machine learning avanzato per selezionare tra più esperienze definite dall&#39;esperto di marketing ad alte prestazioni per personalizzare i contenuti e stimolare le conversioni. La funzione Targeting automatico consegna a ogni visitatore l’esperienza più personalizzata in base al suo profilo cliente e al comportamento dei visitatori precedenti con profili simili.

Se avete già [implementato A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) per l&#39;utilizzo con le attività di test A/B, siete tutti impostati!

### [!UICONTROL Aggiornamento interfaccia utente della sezione Amministrazione]

Stiamo gradualmente riscrivendo l&#39;intera [!DNL Target] interfaccia utente utilizzando un nuovo stack tecnologico per offrire prestazioni migliori, ridurre il tempo di manutenzione necessario per rilasciare nuove funzioni e migliorare l&#39;esperienza dell&#39;utente nel prodotto. La prima sezione aggiornata è la sezione [!UICONTROL Configurazione] , che è stata rinominata [!UICONTROL Amministrazione].

Durante questo aggiornamento, sarà possibile eseguire facilmente molte azioni utilizzando le pagine della sezione [!UICONTROL Amministrazione] , ad esempio:

* Scaricate l&#39;ultimo file at.js dalla scheda [!UICONTROL Implementazione] (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**).
* Personalizza le impostazioni at.js ed è possibile rivedere facilmente le modifiche (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**).
* Modificare le impostazioni di reporting avanzate, ad esempio la valuta e il fuso orario predefiniti, gli IP da escludere dai rapporti, ecc. (**[!UICONTROL Amministrazione]** > **[!UICONTROL Rapporti]**)
* Indirizzi IP offuscati dei visitatori per motivi di privacy (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**)
* Visualizzate l’elenco esistente di utenti per area di lavoro e i relativi ruoli prima di gestirli in Adobe  Admin Console (**[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**).
* Cerca e filtra tutte le tabelle nella sezione [!UICONTROL Amministrazione] .

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
