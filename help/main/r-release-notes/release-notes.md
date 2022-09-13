---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 3d8da94a52046e70a89dc24d7923f743bee5c458
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 78%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.9.1 (rilascio scaglionato dal 13 all’15 settembre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **13 settembre**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **14 settembre**: area geografica delle Americhe
* **15 settembre**: area geografica Asia-Pacifico (APAC)

Questa versione include i miglioramenti e le correzioni seguenti:

* Aggiunta di un [!UICONTROL Tra domini] durante il download di at.js 2.10.0 (e versioni successive) per consentire o disabilitare l’impostazione dei cookie di terze parti. (TGT-43674)
* Notifiche aggiornate nel [!DNL Target] Interfaccia utente per informare i clienti se l’importazione di [!DNL Recommendations] i feed non riescono. (TGT-35811)
* È stato risolto un problema che causava il mal funzionamento di [!UICONTROL Offerte decisionali] all’interno del [!UICONTROL Compositore esperienza visivo] (VEC). (TGT-43866)
* È stato risolto un problema che causava la visualizzazione di un messaggio di errore durante la selezione dell’obiettivo di conversione [!UICONTROL Clic su un elemento] durante la creazione di un’attività [!UICONTROL Multivariate Testing] (MVT). (TGT-43842)
* È stato risolto un problema che impediva la visualizzazione della colonna [!UICONTROL Impression] nel file di rapporto CSV scaricato per le attività [!UICONTROL Automated Personalization] (AP). (TGT-43780)
* È stato risolto un problema che impediva ai clienti di modificare le offerte HTML/JSON dopo la duplicazione delle esperienze durante l’utilizzo del [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43633)
* È stato risolto un problema che impediva ai clienti di copiare un’attività di [!UICONTROL Test A/B] da un’area di lavoro non predefinita a un’altra area di lavoro non predefinita. (TGT-41910)
* È stato risolto un problema per garantire che i clienti possano visualizzare correttamente gli utilizzi di [!DNL Recommendations] oggetti (progettazioni, criteri, raccolte e così via) in [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) attività che contengono consigli ed eliminano anche oggetti criteri non più in uso da [!DNL Target] Interfaccia utente e [!DNL Recommendations] backend. (TGT-42331)
* È stato risolto un problema che causava la visualizzazione di un avviso di timeout di rete nel [!DNL Target] Interfaccia utente per il recupero dei parametri. (TGT-43737)
* Sono stati apportati aggiornamenti all’interfaccia utente per garantire che alcune azioni di trascinamento della selezione siano accessibili da tastiera. (TGT-42969)
* Sono stati apportati aggiornamenti all’interfaccia utente per garantire che le stringhe di testo siano localizzate correttamente.

## at.js versione 2.10.0 (13 settembre 2022)

* Aggiunta di un [!UICONTROL Tra domini] durante il download di at.js 2.10.0 (e versioni successive) per consentire o disabilitare l’impostazione dei cookie di terze parti. (TGT-43674)

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
