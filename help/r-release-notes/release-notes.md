---
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes;updates
description: Queste note sulla versione forniscono informazioni su funzioni, miglioramenti, correzioni e problemi noti per ciascuna versione di Adobe Target Standard e Target Premium.
title: 'Note sulla versione di Adobe Target (corrente) '
feature: release notes
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
translation-type: tm+mt
source-git-commit: 81b9735ea1fa6c42aa9c73565efd68a4d474622c
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 31%

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

## at.js 2.3.2 (24 luglio 2020)

Questa versione di at.js è una versione di manutenzione e include le seguenti correzioni:

* È stato corretto un bug a causa del quale uno script o un codice aggiungeva proprietà predefinite alla finestra o al documento.

## Target Standard/Premium 20.7.1 (27 luglio 2020)

Questa versione include le seguenti modifiche:

### [!UICONTROL Aggiornamento interfaccia utente della sezione Amministrazione]

Stiamo gradualmente riscrivendo l&#39;intera [!DNL Target] interfaccia utente utilizzando un nuovo stack tecnologico per offrire prestazioni migliori, ridurre il tempo di manutenzione necessario per rilasciare nuove funzioni e migliorare l&#39;esperienza dell&#39;utente nel prodotto. La prima sezione aggiornata è la sezione [!UICONTROL Configurazione] , che è stata rinominata [!UICONTROL Amministrazione].

Durante questo aggiornamento, sarà possibile eseguire facilmente molte azioni utilizzando le pagine della sezione [!UICONTROL Amministrazione] , ad esempio:

* Scaricate l&#39;ultimo file at.js dalla scheda [!UICONTROL Implementazione] (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**).
* Personalizza le impostazioni at.js ed è possibile rivedere facilmente le modifiche (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**).
* Modificare le impostazioni di reporting avanzate, ad esempio la valuta e il fuso orario predefiniti, gli IP da escludere dai rapporti, ecc. (**[!UICONTROL Amministrazione]** > **[!UICONTROL Rapporti]**)
* Indirizzi IP offuscati dei visitatori per motivi di privacy (**[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**)
* Visualizzate l’elenco esistente di utenti per area di lavoro e i relativi ruoli prima di gestirli in Adobe Admin Console (**[!UICONTROL Amministrazione]** > **[!UICONTROL Utenti]**).
* Cerca e filtra tutte le tabelle nella sezione [!UICONTROL Amministrazione] .

Per ulteriori informazioni, consulta [Amministrazione di Target Overview (Panoramica](/help/administrating-target/administrating-target.md)di Target).

### Miglioramenti, correzioni e modifiche

Questa versione contiene i seguenti miglioramenti, correzioni e modifiche:

* È stato risolto un problema che impediva il mantenimento delle preferenze del sito dopo l&#39;aggiornamento. (TGT-37239)
* È stato risolto un problema che impediva il corretto funzionamento di [!UICONTROL Inserisci dopo] > [!UICONTROL Immagine] con immagini SVG (Scalable Vector Graphics). (TGT-37242)
* È stato risolto un problema per gli utenti con il ruolo [!UICONTROL Editore] che impediva l&#39;eliminazione delle bozze di attività. (TGT-37358)
* È stato risolto un problema che impediva agli utenti di modificare un&#39;attività quando si selezionava [!UICONTROL Tutte le aree di lavoro] personali. (TGT-37276)

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
