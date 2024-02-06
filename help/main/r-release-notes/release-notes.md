---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 4395caa7e40717c59067eaedff5e53776768eda9
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 92%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Rimozione di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024)

| Rimozione | Dettagli |
|--- |--- |
| [!DNL iPad] e [!DNL iPhone] verranno rimossi dall’[attributo di browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzato durante la creazione di tipi di pubblico.<p>Data di rimozione:<P>30 aprile 2024 | [!DNL Adobe Target] consente di [eseguire il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che utilizzano [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) specifici quando visitano la tua pagina.<P><B>A partire dal 30 aprile 2024, iPad e iPhone verranno rimossi dall’elenco a discesa del tipo di [!UICONTROL browser] durante la creazione di categorie per i tipi di pubblico.</b><P>Tipi di pubblico incorporati creati utilizzando [!DNL Target] L’interfaccia utente, come &quot;Browser: iPad&quot; e &quot;Browser: iPhone&quot;, verrà automaticamente spostata nella nuova definizione del pubblico.<p>Per esempi di impostazioni alternative che devono essere modificate manualmente, vedere [Obsolescenza di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation). |

## [!DNL Target] Standard/Premium 24.1.1 (22, 23 e 25 gennaio 2024)

Questa versione è pianificata per i seguenti giorni:

* **22 gennaio**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **23 gennaio**: area geografica Asia-Pacifico (APAC)
* **25 gennaio**: area geografica delle Americhe

Questa versione include i miglioramenti e le correzioni seguenti:

* Le attività di[!UICONTROL Analytics for Target] (A4T) con metriche obiettivo di ricavo non visualizzavano “Ricavo” nel nome della colonna e la metrica di ricavo non veniva visualizzata nel formato ($) nel reporting. Si trattava di un problema estetico che è stato risolto. (TGT-46995)
* È stato risolto un problema che impediva il corretto funzionamento della reportistica degli intervalli di date. (TGT-47396)
* È stato risolto un problema che causava la visualizzazione dello stato errato nella pagina [!UICONTROL Tutte le attività] dopo che i clienti hanno attivato o disattivato un’attività utilizzando l’icona [!UICONTROL Altre azioni]. (TGT-47367)
* È stato risolto un problema che causava la mancata visualizzazione del rapporto [!UICONTROL Attributi importanti] per un singolo cliente. (TGT-47272)
* È stato risolto un problema che causava la visualizzazione di un messaggio di “payload non valido” quando un singolo cliente tentava di abilitare “Richiedi autenticazione”. (TGT-47195)
* Sono state aggiornate diverse stringhe localizzate nell’interfaccia utente di [!DNL Target].

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
