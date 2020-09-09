---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes;updates
description: Note sulla versione che forniscono informazioni su funzioni, miglioramenti e correzioni per le versioni DNL  Adobe Target più recenti o imminenti.
title: ' note sulla versione prerelease di Adobe Target'
feature: null
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
translation-type: tm+mt
source-git-commit: 419825546dd5bf26f7a5a5498014c01bae65bd7b
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 11%

---


# Note sulla versione di Target (prerelease){#target-release-notes-prerelease}

Questo articolo contiene informazioni prerelease. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 9 settembre 2020**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni presenti in queste pagine potrebbero essere le stesse, a seconda della data di rilascio. I codici tra parentesi sono per uso interno di [!DNL Adobe].

>[!IMPORTANT]
>
>* **Adobe nuovamente denominato Leader nel Gartner Magic Quadrant per i motori** di personalizzazione:  Adobe è stato nuovamente nominato leader nel terzo rapporto annuale Gartner Magic Quadrant for Personalization Engines, 2020. Il Magic Quadrant di Gartner per i motori di personalizzazione ha valutato i fornitori in 15 criteri che rientrano in due categorie: completezza della vista e capacità di esecuzione. [Leggetelo su The  Adobe Blog](https://theblog.adobe.com/adobe-again-named-leader-in-gartner-magic-quadrant-for-personalization-engines/).
   >
   >
* **mbox.js obsoleto**: Il 18 gennaio 2021  Adobe Target non supporterà più la libreria mbox.js. Dopo il 18 gennaio 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e avranno un impatto positivo sulle pagine che hanno attività Target in esecuzione distribuendo contenuto predefinito. È consigliabile che tutti i clienti effettuino la migrazione alla versione più recente della libreria at.js prima di tale data, in modo da evitare potenziali problemi con i siti. Per ulteriori informazioni, consulta [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md) and [Adobe Target Skill Builder (Funzionamento di At.js e generazione di competenze): Chat sviluppatore, migrate  Adobe Target mbox.js in at.js](https://seminars.adobeconnect.com/ptdo6mfo6qn6/?proto=true).
   >
   >   
   Sebbene mbox.js sia attualmente supportato, a partire da luglio 2017 non sono stati forniti aggiornamenti di funzionalità per questa libreria. Il più recente at.js offre molti vantaggi rispetto a mbox.js. Tra gli altri vantaggi, at.js migliora i tempi di caricamento delle pagine per le implementazioni Web, migliora la sicurezza e offre migliori opzioni di implementazione per le applicazioni a pagina singola.
   >
   >   
   Trasferendo tutti i clienti a at.js, i nostri tecnici e il nostro staff di supporto saranno in grado di fornirvi nuove funzionalità e di offrire il supporto che vi aspettate da  Adobe.
   >
   >
* **Annunci** Target: Consultate la pagina degli annunci di Target per informazioni sugli eventi in programma, comprese le sessioni di Target Experience Builder, le chat per sviluppatori, i webinar e le sessioni Target Coffee Break. Per ulteriori informazioni, vedi Annunci [Target](/help/r-release-notes/target-announcements.md).


## Target Standard/Premium 20.8.2 (10 settembre 2020)

| Funzione | Dettagli |
| --- | --- |
| Controllare gli slot delle raccomandazioni nelle sequenze di criteri | Le sequenze di criteri ora consentono di controllare il numero di slot occupati da ogni criterio di raccomandazione, consentendo di combinare e far corrispondere diversi tipi di elementi o diverse logiche di algoritmo.<br>Consultate [Creare sequenze](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) di criteri per ulteriori informazioni. |

## Target Standard/Premium 20.8.1 (2 settembre 2020)

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che causava la visualizzazione di errori durante il caricamento delle nuove pagine di [!UICONTROL amministrazione] dopo il passaggio a un&#39;organizzazione. (TGT-37730)
* È stato risolto un problema di visualizzazione che causava la visualizzazione del codice client errato nella pagina [!UICONTROL Amministrazione > Implementazione] . (TGT-37849)
* È stato risolto un problema che a volte impediva agli utenti di utilizzare le funzioni di modifica in [!UICONTROL Visual Experience Composer (VEC) dopo il corretto caricamento del VEC] . (TGT-37162)
* È stato risolto un problema che impediva il caricamento delle pagine in VEC e Enhanced Experience Composer (EEC) anche se era installata l&#39;estensione VEC Helper. Questo è stato dovuto a modifiche in Google Chrome 80+. Scaricate l&#39;estensione [VEC Helper](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md)aggiornata. (TGT-37893)
* È stato risolto un problema che a volte impediva agli utenti di scaricare at.js dalla pagina [!UICONTROL Amministrazione > Implementazione] dopo il passaggio a un&#39;organizzazione. (TGT-37668)
* Il pulsante di download at.js ora è disattivato durante il caricamento per impedire [!DNL Target] l&#39;invio di più richieste se gli utenti fanno clic più volte sul pulsante di download. (TGT-37633)
* È stato risolto un problema nelle attività [!UICONTROL Experience Targeting] (XT) che causava la visualizzazione dei &quot;risultati del recupero&quot; delle esperienze per un periodo di tempo prolungato. (TGT-37684)
* Navigazione e funzionalità migliorate per gli utenti che utilizzano solo la tastiera. (TGT-34479 e TGT-34473)
* Sono state aggiunte etichette nell’interfaccia utente per aiutare gli utenti che utilizzano tecnologie di assistenza. (TGT-34480)
* È stato migliorato il messaggio di errore durante l&#39;eliminazione di una finestra mobile attualmente utilizzata in un&#39;attività. Il messaggio di errore ora riporta: &quot;Questa finestra è attualmente associata a una o più attività. È necessario rimuovere la finestra da tali attività prima di poterla eliminare.&quot; (TGT-37030)
* È stato aggiunto il supporto nel VEC per consentire il monitoraggio dei clic su un selettore css che corrisponde a più di un elemento nella pagina. (TGT-37323)
* È stato risolto un problema che impediva ad alcuni utenti di visualizzare l&#39;elenco [!UICONTROL Attività] . È stato visualizzato il seguente messaggio di errore: &quot;Impossibile recuperare i suggerimenti URL.&quot; L&#39;errore si verificava per gli utenti che utilizzavano il ritorno a capo nel proprio Nome (Nome/r/n) nel sistema di back-end del Adobe . (TGT-37330)
* È stato risolto un problema che impediva agli utenti di visualizzare la pagina [!UICONTROL Attività] se il nome dell&#39;area di lavoro (specificato in [!UICONTROL Adobe Admin Console per Enterprise]) conteneva un apostrofo. (TGT-37709)
* È stato risolto un problema nelle attività di allocazione [!UICONTROL automatica] durante la selezione delle metriche di ottimizzazione e conversione in cui un messaggio di errore informava erroneamente gli utenti di selezionare una suite di rapporti, anche se era già stata specificata una suite di rapporti. (TGT-37689)
* È stato risolto un problema che a volte causava la visualizzazione delle metriche nella pagina [!UICONTROL Obiettivi e impostazioni] dopo aver navigato sulla pagina [!UICONTROL Targeting] e poi di nuovo. (TGT-37691)
* È stato risolto un problema che causava un valore di ultima modifica non corretto per [!DNL Recommendations] i criteri. (TGT-37666)
* È stato risolto un problema che causava la visualizzazione degli ID mbox nell&#39;elenco a discesa Mbox invece dei nomi mbox. (TGT-37739)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
