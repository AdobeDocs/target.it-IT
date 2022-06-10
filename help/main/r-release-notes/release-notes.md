---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 4251832a5983ea8950e54d52df5d27bf395894e0
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 89%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] correzioni per l&#39;ingegneria dei clienti (rilascio scaglionato: (7-9 giugno 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **7 giugno**: regione Asia-Pacifico (APAC)
* **8 giugno**: Regione delle Americhe
* **9 giugno**: Area Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* Utenti con [!UICONTROL Editor] Il ruolo non può più modificare i tipi di pubblico nelle attività live. (TGT-43582)
* È stato introdotto un miglioramento per il nuovo [!UICONTROL Tipi di pubblico] per evitare uno stato incoerente tra il vecchio database in cui i tipi di pubblico sono stati memorizzati in passato e la nuova architettura che recupera le informazioni direttamente dal back-end. (TGT-43552)
* È stato risolto un problema che impediva ad alcuni clienti di salvare il pubblico combinato causato dalla creazione di contenitori &quot;vuoti&quot; da parte dell’interfaccia utente di Target. (TGT-43588)

## Versione della piattaforma di destinazione (25 maggio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto [per i User Agent Client Hints](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md).
* È stato risolto un problema che causava timeout in modo intermittente durante il rendering [!UICONTROL Decisioni di offerta] nelle attività di [!UICONTROL Experience Targeting] (XT). (TNT-44611)

## at.js versione 2.9.0 (27 maggio 2022)

* È stato aggiunto il supporto [per i User Agent Client Hints](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/user-agent-and-client-hints.md).
* È stato corretto un errore per cui più richieste di mbox sulla stessa pagina avevano ID di impression diversi.

## [!DNL Target Standard/Premium] 22.5.1 (rilascio scaglionato; 11-13 maggio 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **11 maggio**: area geografica Asia-Pacifico (APAC)
* **12 maggio**: area geografica delle Americhe
* **13 maggio**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava un errore JavaScript e impediva ad alcuni clienti di accedere ai dettagli di alcune attività [!UICONTROL Automated Personalization] (AP). (TGT-43526)
* È stato risolto un problema che impediva ad alcuni clienti di aggiungere (o modificare) un’offerta specifica a un’attività AP. (TGT-43503)
* È stato risolto un problema nell’interfaccia utente di [!DNL Target] a causa del quale veniva visualizzato il seguente messaggio di errore: “La mbox globale potrebbe non essere sincronizzata. Prova a salvarla di nuovo.” Questo problema era relativo alla sola interfaccia utente e non aveva alcun impatto sulle implementazioni dei clienti. (TGT-43475)
* È stato risolto un problema che impediva a un cliente di modificare perfezionamenti e tipi di pubblico a livello di esperienza per un’attività, se questi erano stati creati prima dell’implementazione della nuova interfaccia utente [!UICONTROL Tipi di pubblico]. (TGT-43433)
* È stato risolto un problema a causa del quale i clienti potevano selezionare tipi di pubblico [!DNL Adobe Audience Manager] (AAM) duplicati durante la modifica dei tipi di pubblico di reporting per un’attività. (TGT-43430)
* È stato risolto un problema che impediva ai clienti di creare tipi di pubblico duplicati, ma in aree di lavoro diverse. (TGT-43423)
* È stato risolto un problema che impediva ai clienti di eliminare le posizioni con offerte ad hoc nelle attività create nel [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43315)
* È stato risolto un problema che impediva ai clienti di accedere alle offerte con codice dopo aver fatto clic su offerte con immagini e aver quindi aggiornato l’interfaccia utente. (TGT-43566)
* È stato risolto un problema che causava il ripristino dello script originale non modificato dopo che uno script di profilo veniva modificato, attivato e quindi disattivato. Ora vengono mantenute le modifiche applicate allo script di profilo. (TGT-43249)
* È stato risolto un problema che generava il seguente errore se si tentava di spostare un pubblico in un’altra area di lavoro: “Impossibile completare la richiesta. Se il problema persiste, contatta l’Assistenza clienti di Adobe.” (TGT-43212)
* È stato corretto un errore che si verificava se si clonavano modifiche al codice personalizzato per le pagine di app a pagina singola (SPA). (TGT-43137)
* È stato risolto un problema che interessava la modifica della promozione originale dopo la duplicazione di un’esperienza e la successiva modifica della promozione. (TGT-41775)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md) | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| Modifiche alla documentazione | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione.<br>Per ulteriori informazioni, consulta [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C). |
| Note sulla versione per le versioni precedenti | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium.<br>Per ulteriori informazioni, consulta [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). |
| Note sulla versione di Adobe Experience Cloud | Ultime note sulla versione per le soluzioni Adobe Experience Cloud.<br>Per ulteriori informazioni, consulta [Note sulla versione di Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it). |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| Adobe Priority Product Update | Per ricevere notifiche prioritarie sui prossimi miglioramenti per Target e altre soluzioni Adobe Experience Cloud, iscriviti ad Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) |
| Note sulle prossime versioni | Per informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease, consulta la pagina [Note sulla versione di Target (prerelease)](/help/main/r-release-notes/target-release-notes.md). |
