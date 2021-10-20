---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 7cb6baeb7ef9e9cf0efb76866a3eae8dfd38af34
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 44%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## [!DNL Target Standard/Premium] 21.10.3 (19 ottobre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche:

* Sono stati risolti i problemi che impedivano ai clienti di aprire [!UICONTROL A4T] pannello in [!DNL Analysis Workspace] facendo clic sul pulsante [!UICONTROL Visualizzazione in Analytics] ingresso pulsante [!DNL Target] reporting delle attività. (TGT-42099, TGT-42100)
* È stato risolto un problema che causava il [!UICONTROL Modifica progettazione] pulsante per non visualizzare durante la modifica [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) attività che utilizzano [!UICONTROL Compositore esperienza basato su moduli]. (TGT-41980)
* È stato risolto un problema che impediva la [!UICONTROL Compatibile] visualizzazione di una casella di controllo nella selezione dei criteri durante la creazione di una nuova [!UICONTROL Recommendations] attività. (TGT-42053)
* È stato corretto un messaggio di errore errato visualizzato quando non era possibile selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per mancanza di [!DNL Analytics] autorizzazioni. (TGT-41954)
* Sono state implementate più correzioni di accessibilità per migliorare la navigazione da tastiera in tutti gli [!DNL Target] Interfaccia utente.

## [!DNL Target Standard/Premium] 21.10.2 (13 ottobre 2021)

Sono stati aggiunti i seguenti miglioramenti quando si utilizza [!DNL Target] [!UICONTROL Tipi di pubblico] con [!DNL Adobe Experience Platform Web SDK]:

* Sono state aggiunte icone di avviso, popovers e messaggi in diverse aree della [!DNL Target] Interfaccia utente per indicare che il pubblico è stato eliminato dal sorgente e non è più disponibile per l’utilizzo in [!DNL Target] attività.

   Le illustrazioni seguenti mostrano alcuni luoghi in cui vengono visualizzate le icone, i popovers e i messaggi:

   * [!UICONTROL Attività] pagina elenco

      ![Pubblico eliminato al messaggio sorgente nella pagina dell’elenco Attività](assets/deleted-at-source-audiences-list.png)

   * Attività [!UICONTROL Panoramica] pagine:

      ![Pubblico eliminato al messaggio sorgente nella pagina della panoramica](assets/deleted-at-source-overview.png)

   * [!UICONTROL Esperienze] passaggio del flusso di lavoro per la creazione di attività:

      ![Pubblico eliminato al messaggio sorgente su [!UICONTROL Esperienze] page](assets/deleted-at-source-experiences.png)

   * [!UICONTROL Targeting] passaggio del flusso di lavoro per la creazione di attività:

      ![Pubblico eliminato al messaggio sorgente su [!UICONTROL Targeting] page](assets/deleted-at-source-targeting.png)

   * [!UICONTROL Obiettivi e impostazioni] passaggio del flusso di lavoro per la creazione di attività:

      ![Pubblico eliminato al messaggio sorgente sul [!UICONTROL Obiettivi e impostazioni] page](assets/deleted-at-source-goals-settings.png)

   * Ottimizzazioni del pubblico ([!UICONTROL Sostituisci pubblico] sulla [!UICONTROL Targeting] passaggio del flusso di lavoro per la creazione di attività):

* Se tenti di utilizzare la funzione Combina pubblico e uno dei tipi di pubblico è stato eliminato all&#39;origine, [!UICONTROL Salva] è disabilitato.

## [!DNL Target Standard/Premium] 21.10.1 (6 ottobre 2021)

Questa versione include le seguenti nuove funzionalità:

| Funzione | Dettagli |
| --- | --- |
| [!UICONTROL Aggiornamento dell’interfaccia utente di Audiences] | Come parte del [!DNL Adobe Target] sforzi continui del team per migliorare l&#39;esperienza utente per [!DNL Target] utenti, questa versione aggiorna il [!UICONTROL Tipi di pubblico] e [!UICONTROL Script di profilo] nelle pagine [!DNL Target] Interfaccia utente. Questo aggiornamento unisce e standardizza i pattern di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Un rinfrescato [progettazione di audience builder](/help/c-target/c-audiences/create-audience.md)</li><li>Supporto delle regole di esclusione nel [!UICONTROL Pubblico] generatore di regole libreria</li><li>Un nuovo filtro &quot;Audience Source&quot; per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti della sessione</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/c-target/target.md).<br>**NOTA**: Il nuovo [!UICONTROL Tipi di pubblico] L’interfaccia utente è stata temporaneamente disabilitata per tutti i clienti eccetto quelli attualmente in un [!DNL Target] Programma beta. Questo aggiornamento dell’interfaccia utente verrà riabilitato per un sottoinsieme di clienti martedì 19 ottobre e per tutti i clienti rimanenti giovedì 21 ottobre 2021. |
| [!UICONTROL Script di profilo] Aggiornamento dell&#39;interfaccia | La [!UICONTROL Script di profilo] è stata aggiornata anche la libreria e include un&#39;interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all&#39;interno dell&#39;editor di codice</li><li>Parametri dei token (mbox o profilo) completi automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md). |
| ![Badge Premium](/help/assets/premium.png) Creare e modificare i criteri di Recommendations | La [!UICONTROL Criteri di Recommendations] il flusso di lavoro di creazione e modifica è stato semplificato per semplificare la scelta dell’algoritmo e delle impostazioni consigliate per raggiungere gli obiettivi.<br>Per ulteriori informazioni, consulta [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Badge Premium](/help/assets/premium.png) Miglioramenti della frequenza di aggiornamento dell’intervallo di lookback e dell’algoritmo di Recommendations | È ora possibile eseguire gli algoritmi &quot;Più visualizzato&quot; e &quot;Più venduti&quot; con un intervallo di lookback di sei ore per acquisire il contenuto con tendenze più recenti. Quando l’intervallo di lookback di sei ore è selezionato, i risultati delle raccomandazioni vengono aggiornati ogni 3-6 ore nel corso della giornata.<br>Per ulteriori informazioni, consulta [Origine dati](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in *Creare criteri*. |

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/r-release-notes/target-release-notes.md). |
