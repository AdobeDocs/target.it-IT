---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 351ed1e51b0a253476c6cda456781351333e8da5
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 98%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.5.2 (31 maggio 2023)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che causava la visualizzazione di una pagina vuota durante la generazione di un token di autorizzazione di un profilo API. (TGT-45387 e TGT-45423)
* È stato risolto un problema che impediva la visualizzazione di un’immagine nel pannello [!UICONTROL Crea progettazione] se il nome dell’immagine conteneva caratteri GB 18030. (TGT-44614)
* È stato risolto un problema a causa del quale in alcuni caratteri dei simboli GB 18030 veniva erroneamente applicato l’escape nel Testo/HTML nelle esperienze. (TGT-44600)
* È stato risolto un problema che causava il blocco dei rapporti delle attività di [!UICONTROL Personalizzazione automatica] durante l’analisi. (TGT-44820)
* È stato risolto un problema che impediva la ricerca di un’attività sulla pagina [!UICONTROL Attività] se il nome conteneva una parentesi quadra ( [ o ] ). (TGT-44777)
* È stato risolto un problema che impediva la sincronizzazione di un’attività se il relativo obiettivo conteneva caratteri speciali. (TGT-44982)
* È stato risolto un problema che impediva ad alcuni clienti la visualizzazione delle attività nell’interfaccia utente di [!DNL Target] per l’area di lavoro predefinita. (TGT-45286)
* È stato aggiornato il comportamento del flag “Disabilita duplicati”. I flag di esclusione offerte ripetute sono stati aggiornati per consentire tali offerte in caso di offerta di contenuto predefinita (per API v3 e v4) e per consentire le opzioni duplicate se tali opzioni fanno riferimento all’offerta di contenuto predefinita e non hanno modelli definiti. (TNT-46617)
* È stato risolto un problema a causa del quale un parametro di query veniva aggiunto a un URL che impediva il caricamento della pagina nel [!UICONTROL Compositore esperienza visivo]. (TGT-44873)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

## Attributi del profilo di Real-Time CDP condivisi con [!DNL Target]|[!UICONTROL Attributi del profilo di Real-Time CDP] (13 giugno 2023)

Questa versione contiene i seguenti miglioramenti:

| Funzione | Dettagli |
|--- |--- |
| Attributi di profilo Real-Time CDP condivisi con [!DNL Target] | Gli [!UICONTROL attributi di profilo Real-Time CDP] possono essere condivisi con [!DNL Target] per l’utilizzo nelle offerte HTML e JSON.<P>Per ulteriori informazioni, consulta [Condividere gli attributi di profilo Real-Time CDP con [!DNL Target]](/help/main/c-integrating-target-with-mac/integrating-with-rtcdp.md#rtcdp-profile-attributes). |

## [!DNL Target] Standard/Premium 23.5.1 (23-25 maggio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

23 maggio: area geografica Europa, Medio Oriente e Africa (EMEA)
24 maggio: area geografica Asia-Pacifico (APAC)
25 maggio: area geografica delle Americhe

Questa versione include i nuovi miglioramenti e le correzioni seguenti:

* È stato risolto un problema che impediva ad alcuni clienti di creare tipi di pubblico con profili di visitatori utilizzando gli operatori “maggiore di” o “minore di”. (TGT-45271)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].
* L’interfaccia utente di Target è stata aggiornata in diverse posizioni in vista di un prossimo aggiornamento (le modifiche sono dietro un flag di funzione fino al rilascio degli aggiornamenti).

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

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
