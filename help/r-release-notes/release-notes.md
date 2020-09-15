---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 92f5953a96b92175784600d1b04a23ec4d7152ec
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 25%

---


# Note sulla versione di Target (corrente){#target-release-notes-current}

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di Target Standard e Target Premium. Inoltre, se applicabile, sono incluse anche le note sulla versione per le API Target, gli SDK, la libreria JavaScript (at.js) e altre modifiche alla piattaforma.

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


I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 20.8.3 (15 settembre 2020)

| Funzione | Dettagli |
| --- | --- |
| ![Supporto di Analytics](/help/assets/premium.png) Premium per Target (A4T) per le attività di Auto-Target | [!UICONTROL Le attività di Auto-Target] ora supportano [Analytics per Target](/help/c-integrating-target-with-mac/a4t/a4t.md).<br>Questa integrazione consente di utilizzare l&#39;algoritmo [!UICONTROL Auto-Target] per l&#39;apprendimento di un computer per scegliere l&#39;esperienza migliore per ogni visitatore in base al profilo, al comportamento e al contesto.<br>Se avete già [implementato A4T](/help/c-integrating-target-with-mac/a4t/a4timplementation.md) per l’utilizzo con le attività Test A/B e Targeting delle esperienze, siete tutti impostati!<br>Per ulteriori informazioni, consultate Supporto di [Analytics per Target (A4T) per le attività](/help/c-integrating-target-with-mac/a4t/campaign-creation.md#a4t-aa) di allocazione automatica e targeting automatico nella creazione *di* attività. |

## Target Standard/Premium 20.8.2 (10 settembre 2020)

| Funzione | Dettagli |
| --- | --- |
| ![Slot per il controllo dei simboli](/help/assets/premium.png) Premium nelle sequenze di criteri | Le sequenze di criteri ora consentono di controllare il numero di slot occupati da ogni criterio di raccomandazione, consentendo di combinare e far corrispondere diversi tipi di elementi o diverse logiche di algoritmo.<br>Consultate [Creare sequenze](/help/c-recommendations/c-algorithms/create-criteria-sequence.md#sequence) di criteri per ulteriori informazioni. |

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

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione - API lato server di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md) | Note sulla versione relative  API lato server Adobe Target. |
| [Note sulla versione - SDK Node.js di Target](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md) | Note sulla versione relative  SDK Node.js di Adobe Target. |
| [Note sulla versione - Java SDK di destinazione](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md) | Note sulla versione relative  Adobe Target Java SDK. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Informazioni dettagliate sulle modifiche in ciascuna versione della libreria JavaScript di Adobe Target . |
| [Dettagli sulle versioni di mbox.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md) | In questa pagina sono elencate le modifiche per ogni versione di mbox.js.<br>Tenete presente che la libreria mbox.js non è più in fase di sviluppo. Tutti i clienti devono migrare da mbox.js a at.js. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud {#section_1BC5F5208DA548E9B4344A0836E4B943}

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Informazioni dettagliate sugli aggiornamenti apportati a questa guida che potrebbero non essere incluse nelle note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](../r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Experience Cloud - Note](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)sulla versione. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[](https://www.adobe.com/subscription/priority-product-update.html)https://www.adobe.com/subscription/priority-product-update.html |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
