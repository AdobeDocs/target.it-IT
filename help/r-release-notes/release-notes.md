---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5d3e5a15a262d29bd1d95af71baae52ed288b33e
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 90%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Target Standard/Premium 22.2.1 (1° febbraio 2022)

Questa versione di manutenzione contiene le correzioni e i miglioramenti seguenti relativi alla nuova interfaccia [!UICONTROL Tipi di pubblico], annunciata in Target Standard/Premium versione 22.1.2, che nelle prossime sei settimane verrà gradualmente implementata per i clienti in tutte le aree geografiche. Le correzioni apportate allineano le funzionalità dei tipi di pubblico creati in [!DNL Adobe Target Standard/Premium].

* È stato risolto un problema che impediva ai tipi di pubblico importati da [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] e [!DNL Adobe Target Classic] di essere assegnati come tipi di pubblico nella generazione dei rapporti. (TGT-43140)
* È stata aggiunta l’opzione [!UICONTROL Elimina] nell’elenco [!UICONTROL Tipi di pubblico] per i tipi di pubblico importati da [!DNL Adobe Experience Platform], [!DNL Adobe Experience Cloud] e [!DNL Adobe Target Classic]. È stata aggiunta anche la funzionalità di eliminazione in blocco. (TGT-42914)

## at.js versione 2.8.1 (28 gennaio 2022)

* È stato corretto un problema che impediva la mappatura di `pageLoad` su target-global-mbox nella funzione [!UICONTROL Decisioning sul dispositivo] in modalità di esecuzione ibrida.
* È stato risolto un problema relativo ai dettagli di analisi per richieste mbox.
* Sono state aggiornate le dipendenze di sviluppo per correggere alcune vulnerabilità di sicurezza.

## [!DNL Target Standard/Premium] 22.1.2 (26 gennaio 2022)

| Funzione | Dettagli |
| --- | --- |
| Tipi di pubblico [!DNL Adobe Experience Platform] in [!DNL Target] | Ora puoi sfruttare e utilizzare i tipi di pubblico [!DNL Adobe Experience Platform] in [!DNL Target]. I team [!DNL Target], [!DNL Experience Platform] [!DNL Destinations] e [!DNL Unified Profile Service] sono lieti di annunciare la disponibilità generale dei casi d’uso “Personalizzazione della stessa pagina/pagina successiva”.<br>L’utilizzo dei tipi di pubblico creati in [!DNL Adobe Experience Platform] fornisce dati più completi sui clienti, per una personalizzazione più incisiva. La [Real-time Customer Data Platform](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html?lang=it){target=_blank} (RTCDP), costruito su [!DNL Adobe Experience Platform] consente alle aziende di unire dati noti e anonimi provenienti da più fonti aziendali per creare profili cliente da utilizzare in tempo reale per fornire esperienze cliente personalizzate su tutti i canali e dispositivi.<br>Per ulteriori informazioni, consulta [Utilizzare i tipi di pubblico da Adobe Experience Platform](/help/c-target/c-audiences/audiences.md#aep) in *Creare un pubblico* e [Casi d’uso per la personalizzazione tra pagine uguali e successive](https://www.adobe.com/go/destinations-edge-personalization-en){target=_blank} nel *Panoramica sulle destinazioni* guida. |
| Aggiornamento dell’interfaccia utente di [!UICONTROL Audiences] | Come parte degli sforzi continui del team di [!DNL Adobe Target] per migliorare l’esperienza utente per gli utenti [!DNL Target], questa versione aggiorna le pagine [!UICONTROL Tipi di pubblico] e [!UICONTROL Script di profilo] nell’interfaccia utente [!DNL Target]. Questo aggiornamento unisce e standardizza i disegni di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:<ul><li>Possibilità di selezionare ed eliminare più tipi di pubblico contemporaneamente</li><li>Una [progettazione di audience builder](/help/c-target/c-audiences/create-audience.md) rinnovata</li><li>Supporto della regola di esclusione nel generatore di regole della libreria [!UICONTROL Pubblico]</li><li>Un nuovo filtro “Origine pubblico” per consentire un rilevamento più rapido del pubblico</li><li>Opzioni di ricerca e filtro persistenti nella sessione</li><li>Possibilità di spostare i tipi di pubblico tra aree di lavoro diverse per i clienti [!DNL Target Premium].</li></ul>Per ulteriori informazioni, consulta [Tipi di pubblico](/help/c-target/target.md).<br>**NOTA**: questa funzione verrà implementata gradualmente nelle prossime otto settimane per i clienti in diverse aree geografiche. |
| Aggiornamento dell’interfaccia [!UICONTROL Script di profilo] | Anche la libreria [!UICONTROL Script di profilo] è stata aggiornata e include un’interfaccia aggiornata insieme a diversi aggiornamenti di produttività:<ul><li>Possibilità di selezionare ed eliminare contemporaneamente più script di profilo</li><li>Un nuovo editor di codice per gli script di profilo</li><li>Evidenziazione della sintassi e controllo degli errori all’interno dell’editor di codice</li><li>Parametri dei token (mbox o profilo) che si completano automaticamente tramite scelte rapide da tastiera</li></ul>Per ulteriori informazioni, consulta [Profili dei visitatori](/help/c-target/c-visitor-profile/visitor-profile.md).<br>**NOTA**: questa funzione verrà implementata gradualmente nelle prossime otto settimane per i clienti in diverse aree geografiche. |

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
