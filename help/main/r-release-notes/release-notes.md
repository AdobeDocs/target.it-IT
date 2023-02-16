---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: abf4c005a3c0e3b2e0e9f1402bb2af3444634942
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 89%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.14.5 (13-15 febbraio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **13 febbraio**: Regione delle Americhe
* **15 febbraio**: Area Europa, Medio Oriente e Africa (EMEA)
* **15 febbraio**: regione Asia-Pacifico (APAC)

Questa versione include le seguenti correzioni:

* È stato risolto un problema che causava il seguente messaggio di errore anche se una proprietà era specificata nelle attività di Automated Personalization (AP): &quot;Errori: Almeno una proprietà deve appartenere a un&#39;area di lavoro non predefinita&quot; (TGT-44607)
* È stato risolto un potenziale problema di sicurezza che influisce sui feed Recommendations lato server. (TGT-43769)

## at.js versione 2.10.1 (2 febbraio 2023)

* È stato corretto un bug a causa del quale le attività che coinvolgono regole di pubblico contenenti parametri nel cui nome è presente il carattere punto non restituivano l’esperienza prevista per le decisioni sul dispositivo.
* È stato corretto un bug introdotto in at.js 2.6.0 a causa del quale at.js attivava una chiamata di consegna, anche quando `mboxDisable` è stato abilitato.

Per informazioni su tutte le versioni di at.js, vedi [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.

## [!DNL Target] Standard/Premium 22.13.3 (25-26 gennaio 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **25 gennaio**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **25 gennaio**: area geografica Asia-Pacifico (APAC)
* **26 gennaio**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [Offerta JSON](/help/main/c-experiences/c-manage-content/create-json-offer.md) per il supporto in Automated Personalization (AP) | È stato aggiunto il supporto per le offerte JSON nelle attività di [!UICONTROL Automated Personalization] (AP) utilizzando il Compositore esperienza basato su moduli. (TGT-41460) |
| [Frammenti di esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) | È stata aggiunta la possibilità di distinguere tra tipi di frammento di [!DNL Adobe Experience Manager] (AEM XF) esportati in [!DNL Target]. Invece dell’opzione “Frammento esperienza”, [!DNL Target] ora consente di filtrare e cercare i dati utilizzando “HTML XF” e “JSON XF”. (TGT-44132) |

* È stato risolto un problema che causava un “errore 500” nelle attività [!UICONTROL Test A/B] e di [!UICONTROL Targeting dell’esperienza] (XT) che contengono consigli. Questo problema si verificava quando [!DNL Target] non riusciva a eliminare correttamente gli oggetti di criteri dall’interfaccia utente di [!DNL Target] e dal back-end di [!DNL Recommendations] non più in uso. (TGT-44383)
* È stata rimossa la posizione dal nome dell’offerta visualizzato nel rapporto [!UICONTROL Livello di offerta] delle attività di [!UICONTROL Automated Personalization]. Questa modifica rende il rapporto più leggibile. (TGT-44294)
* Sono state rimosse le opzioni del calendario di 45 giorni e 90 giorni da AP e [!UICONTROL Targeting automatico] [!UICONTROL Approfondimenti personalizzazione] e rapporti [!UICONTROL Attributi importanti] nell’[!DNL Target] Interfaccia utente. A causa dei pattern di utilizzo e nel tentativo di migliorare le prestazioni, questi intervalli di date sono stati dichiarati obsoleti. L’interfaccia utente è stata aggiornata per riflettere gli intervalli attualmente consentiti: 15, 30 e 60 giorni. (TGT-39357)
* È stata rimossa la possibilità di modificare l’impostazione [!UICONTROL Identica all’obiettivo di ottimizzazione] sulla pagina [!UICONTROL Obiettivi e impostazioni] dopo che l’attività è in esecuzione. (TGT-43923)
* È stato risolto un problema che causava errori con l’ambiente di lavoro predefinito nel back-end di [!DNL Target] in caso di aggiornamento da [!DNL Target Standard] a [!DNL Target Premium]. (TGT-44081 e TGT-44306)
* È stata apportata una modifica per consentire le suite di rapporti di [!DNL Analytics] che contengono il carattere punto “.” nei nomi da utilizzare nell’interfaccia utente di [!DNL Target] per creare feed di classificazione in [!DNL Analytics].
* È stato modificato il collegamento sulla pagina [!UICONTROL Implementazione] ([!UICONTROL Amministrazione] > [!UICONTROL Implementazione]) per “Metodi di implementazione con Decisioning sul dispositivo”, in modo che indichi la pagina di spiegazione su come utilizzare Decisioning sul dispositivo per tutti gli SDK supportati: Node.js, Java, .NET e Python. Per ulteriori informazioni, consulta [Guida introduttiva agli SDK di Target](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* È stato risolto un problema che causava errori durante il caricamento dei file utilizzando [!DNL Scene7] e [!DNL Target].
* È stata migliorata l’accessibilità dell’interfaccia utente di [!DNL Target] per le persone con disabilità utilizzando i risultati di una verifica interna in termini di usabilità. I miglioramenti dell’accessibilità includono l’accesso a funzioni che in precedenza non erano raggiungibili tramite la tastiera, miglioramenti al testo alternativo, la possibilità di eseguire lo zoom di parti dell’interfaccia utente per renderle più utilizzabili, l’attivazione della tastiera migliorata e molto altro ancora.   (TGT-42759)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

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
