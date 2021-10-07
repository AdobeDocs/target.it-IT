---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: bd7032b915bf1b333fa5cc3cb4825eaa7e4f83fb
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 59%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## [!DNL Target Standard/Premium] 21.10.1 (6 ottobre 2021)

Questa versione include le seguenti nuove funzionalità:

| Funzione | Dettagli |
| --- | --- |
|  Aggiornamento di Audiences UI | Come parte del continuo sforzo del team [!DNL Adobe Target] per migliorare l&#39;esperienza utente per gli utenti [!DNL Target], questa versione aggiorna le pagine [!UICONTROL Audiences] e [!UICONTROL Script di profilo] nell&#39;interfaccia utente [!DNL Target] . Questo aggiornamento unisce e standardizza i pattern di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Un [progetto di audience builder aggiornato](/help/c-target/c-audiences/create-audience.md)</li><li>Supporto delle regole di esclusione nel generatore di regole di libreria [!UICONTROL Audience]</li><li>Un nuovo filtro &quot;Audience Source&quot; per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti della sessione</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/c-target/target.md).<br>**Nota**: La nuova interfaccia utente   Audiences e  [!UICONTROL Script ] di profilo verrà implementata in tutte le aree geografiche la prossima settimana. |
| [!UICONTROL Aggiornamento ] dell&#39;interfaccia utente Script di profilo | Anche la libreria [!UICONTROL Script di profilo] è stata aggiornata e include un&#39;interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all&#39;interno dell&#39;editor di codice</li><li>Parametri dei token (mbox o profilo) completi automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**Nota**: La nuova interfaccia utente   Audiences e  [!UICONTROL Script ] di profilo verrà implementata in tutte le aree geografiche la prossima settimana. |
| ![Badge ](/help/assets/premium.png) PremiumCriteri di Recommendations creazione e modifica | Il flusso di lavoro [!UICONTROL Recommendations Criteria] per la creazione e la modifica dei criteri è stato semplificato per semplificare la scelta dell&#39;algoritmo e delle impostazioni consigliate per raggiungere gli obiettivi.<br>Per ulteriori informazioni, consulta  [Creare criteri](/help/c-recommendations/c-algorithms/create-new-algorithm.md). |
| ![Miglioramenti ](/help/assets/premium.png) della frequenza di aggiornamento degli algoritmi e dell&#39;intervallo di lookback di Premium | È ora possibile eseguire gli algoritmi &quot;Più visualizzato&quot; e &quot;Più venduti&quot; con un intervallo di lookback di sei ore per acquisire il contenuto con tendenze più recenti. Quando l’intervallo di lookback di sei ore è selezionato, i risultati delle raccomandazioni vengono aggiornati ogni 3-6 ore nel corso della giornata.<br>Per ulteriori informazioni, consulta  [Origine dati ](/help/c-recommendations/c-algorithms/create-new-algorithm.md#data-source) in  *Creare criteri*. |

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
