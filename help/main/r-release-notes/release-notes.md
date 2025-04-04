---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 0618d39fc5966c64cceea8f5bcccb625fc243ebb
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 47%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.1 (2 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la scomparsa dei tipi di pubblico dell’esperienza dalle attività di. (TGT-52003)
* È stato risolto un problema che causava elementi imprevisti durante la consegna. (TGT-52011)
* È stato risolto un problema che impediva ai clienti di visualizzare il pubblico nel grafico di targeting nella pagina Ove[!UICONTROL r]view e durante la modifica dell&#39;attività. (TGT-52050)
* È stato risolto un problema che impediva ai clienti di riordinare le esperienze in ordine di priorità nelle attività [!UICONTROL Experience Targeting] (XT). (TGT-52054)
* È stato risolto un problema che causava un rendering errato quando si annullavano le modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema a causa del quale durante la modifica di un&#39;offerta di reindirizzamento, [!DNL Target] rimuove anche i selettori [!UICONTROL ClickTrack] associati a tale offerta. (TGT-51936)
* È stato risolto un problema che causava il salvataggio errato del selettore da parte di [!DNL Target] durante l&#39;annullamento di [!UICONTROL ClickTrack]. (TGT-51937)
* È stato risolto un problema che causava un errore di nome non valido dopo l&#39;apertura e la chiusura del selettore mbox sulla pagina [!UICONTROL Goals & Settings] senza apportare modifiche. (TGT-51983)
* È stato risolto un problema che impediva la modifica delle offerte ad hoc create nell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-51984)
* È stato risolto un problema che bloccava le attività di modifica con offerte ad hoc contenenti codice personalizzato. (TGT-51995)
* È stato risolto un problema che causava la visualizzazione delle regole di esclusione come regole di inclusione durante la modifica delle definizioni di pubblico combinato. (TGT-51999)
* È stato risolto un problema che impediva la corretta visualizzazione del codice personalizzato durante la modifica dell’esperienza. (TGT-52005)
* È stato risolto un problema che rendeva l&#39;opzione [!UICONTROL Insert Before] non disponibile per l&#39;inserimento di contenuto prima della barra di navigazione. (TGT-52031)
* È stato risolto un problema che impediva la corretta evidenziazione dell’esperienza predefinita nel reporting. (TGT-51716)
* È stato risolto un problema che attivava un messaggio `default message [Invalid optionLocalIds: xx]]` durante la creazione di un&#39;attività. (TGT-52038)

## at.js versione 2.11.8 (31 marzo 2025)

* È stata risolta una vulnerabilità identificata da CodeQL nella convalida del suffisso di stringa per evitare casi edge durante le operazioni di ridimensionamento e spostamento. (TNT-51516)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
