---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: e0e12caec1cf9db713d56983f3697d80bea72015
workflow-type: ht
source-wordcount: '977'
ht-degree: 100%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 22.8.1 (rilascio graduale 17-18 agosto 2022)

Questa versione di manutenzione include correzioni di back-end e localizzazione.

## Versione della piattaforma [!DNL Target] (20 luglio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | --- |
| Miglioramento della precisione di valutazione del pubblico e riduzione della latenza per l’utente finale tramite il supporto IPv6 (TNT-43364, TNT-44692) | Le geolocalizzazioni dei visitatori ora sono determinate dagli indirizzi IPv6, se disponibili, anziché solo dagli indirizzi IPv4. Le API di consegna supportano anche i parametri di input IPv6. I filtri e l’elenco Consentiti supportano sia gli indirizzi IPv4 che IPv6. Grazie al supporto di IPv6 in questa versione, i visitatori verranno inclusi in modo più preciso nei tipi di pubblico (verranno qualificati per le attività o inclusi nei criteri di filtro in modo più accurato). Anche la latenza dei dati risulterà migliorata, in quanto i client IPv6 verranno instradati direttamente, evitando il sovraccarico del gateway IPv6-IPv4. |
| È stato risolto un problema di gestione del payload lato client di A4T (TNT-44926) | Con l’integrazione lato server di A4T, se Adobe Target identifica una richiesta come proveniente da un bot, il payload non viene inoltrato ad Analytics e nei registri di [!DNL Target] non viene registrato alcun evento mod_stats. Con questa versione, la registrazione lato client di A4T è stata migliorata in modo che il comportamento relativo al payload A4T corrisponda a quello lato server di A4T: i visitatori identificati come bot vengono esclusi dal conteggio e dal reporting di [!DNL Target]. (Il problema in questione era limitato alle implementazioni che utilizzavano la gestione del payload lato client; il lato server non ne era interessato. Con questa versione, il comportamento è ora coerente sia per la gestione del payload lato server che per quello lato client.) |

## [!DNL Target Standard/Premium] 22.6.2 (30 giugno 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

| Funzione | Descrizione |
| --- | ---  |
| Notifiche interne al prodotto | Ottieni le seguenti notifiche interne al prodotto:<ul><li>**Attività**: notifiche per tutti i tipi di attività quando un&#39;attività viene approvata o disattivata, manualmente o alla sua data di inizio o di fine. La notifica include il nome dell’attività e un collegamento per accedere alla pagina di panoramica dell’attività.</li><li>**Script di profilo**: notifiche quando uno script di profilo viene attivato o disattivato, manualmente o da Target.</li><li>**Feed di Recommendations**: notifiche quando un feed di Recommendations viene attivato o disattivato, manualmente o da Target. Le notifiche vengono inviate anche quando un feed di Recommendations non riesce.</li></ul> Per impostazione predefinita, le notifiche vengono ricevute dagli amministratori di prodotto, e dagli utenti che pubblicano e che approvano. Le notifiche possono essere configurate nelle preferenze di Experience Cloud.<br>Per ulteriori informazioni consulta [Notifiche e annunci](/help/main/c-intro/understand-the-target-ui.md#notifications-announcements). |
| *Guida per gli sviluppatori di Adobe Target* | La *Guida per gli sviluppatori di Adobe Target* consolida tutti i contenuti per sviluppatori di [!DNL Target] in un’unica pratica guida. La guida include informazioni sull’implementazione di [!DNL Target] e [!DNL Recommendations], sugli SDK di [!DNL Target] e sulle API di [!DNL Target].<br>Per ulteriori informazioni, consulta la [Guida per gli sviluppatori di Adobe Target](https://developer.adobe.com/target/){target=_blank}. |

* Gli utenti con il ruolo di [!UICONTROL editor] non possono più modificare i tipi di pubblico nelle attività live. (TGT-43582)
* Viene visualizzato un messaggio di avvertenza se un cliente tenta di salvare un pubblico il cui nome contiene un punto esclamativo ( ! ) come primo carattere (esempio: !Londra). (TGT-43643)
* È stato risolto un problema a causa del quale alcune schede dei dettagli di definizione del pubblico per alcuni clienti indicavano che un’attività terminata è ancora in esecuzione. (TGT-43527)

## [!DNL Target Standard/Premium] 22.6.1 (rilascio graduale: 7-9 giugno 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **7 giugno**: area geografica Asia Pacifico (APAC)
* **8 giugno**: area geografica delle Americhe
* **9 giugno**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato introdotto un miglioramento per la nuova pagina [!UICONTROL Tipi di pubblico] per evitare uno stato di mancata coerenza tra il vecchio database, in cui erano precedentemente archiviati i tipi di pubblico, e la nuova architettura, che recupera le informazioni direttamente dal back-end. (TGT-43552)
* È stato risolto un problema che impediva ad alcuni clienti di salvare i tipi di pubblico combinati a causa dell’interfaccia di Target che creava contenitori “vuoti”. (TGT-43588)

## Versione della piattaforma Target (25 maggio 2022)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto per [User Agent Client Hints](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank}.
* È stato risolto un problema che causava timeout in modo intermittente durante il rendering [!UICONTROL Decisioni di offerta] nelle attività di [!UICONTROL Experience Targeting] (XT). (TNT-44611)

## at.js versione 2.9.0 (27 maggio 2022)

* È stato aggiunto il supporto per [User Agent Client Hints](https://developer.adobe.com/target/implement/client-side/atjs/user-agent-and-client-hints/){target=_blank}.
* È stato corretto un errore per cui più richieste di mbox sulla stessa pagina avevano ID di impression diversi.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

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
