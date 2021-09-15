---
keywords: Note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Quali nuove funzioni sono incluse nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 5a5b39db9b9b4ffd95573d643dcff52fe562c0c2
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 57%

---

# Note sulla versione di Target (corrente)

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione per API di Target, SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

>[!IMPORTANT]
>
>**Terminazione di mbox.js**: a partire dal 31 marzo 2021, [!DNL Adobe Target] non supporta più la libreria mbox.js. Dopo il 31 marzo 2021, tutte le chiamate effettuate da mbox.js avranno esito negativo e le pagine che hanno attività [!DNL Target] in esecuzione, si troveranno a utilizzare il contenuto predefinito.
>
>Per evitare potenziali problemi con i siti, passa alla versione più recente del nuovo [!DNL Adobe Experience Platform Web SDK] o della libreria JavaScript at.js. Per ulteriori informazioni, consulta [Panoramica: implementare Target per web lato client](/help/c-implementing-target/c-implementing-target-for-client-side-web/implement-target-for-client-side-web.md).

(I codici tra parentesi sono per uso interno di [!DNL Adobe].)

## [!DNL Target Standard/Premium] 21.9.1 (14 settembre 2021)

Questa versione di manutenzione include i seguenti miglioramenti, correzioni e modifiche.

* Sono stati risolti dei problemi che impedivano ai clienti di accedere al [!UICONTROL Compositore esperienza visivo] (VEC) a causa di nuovi criteri di sicurezza per i cookie di terze parti in alcuni browser web. Questo problema è stato discusso in &quot;Pagine non caricate nel Compositore esperienza visivo o Compositore esperienza avanzato (EEC) quando si utilizza Google Chrome versione 80+&quot; in [Risoluzione dei problemi relativi al Compositore esperienza visivo e al Compositore esperienza avanzato](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/issues-related-to-the-visual-experience-composer-vec-and-enhanced-experience-composer-eec.md).
* È stato risolto un problema a causa del quale i nomi delle offerte nel Compositore esperienza visivo visualizzavano il percorso dell’offerta invece del nome descrittivo dell’offerta. (TGT-41300)
* I nomi delle esperienze ora si riflettono in [!DNL Analysis Workspace] per le attività A4T (TGT-38674)
* È stato risolto un problema in [!DNL Recommendations] a causa del quale l’ID entità veniva erroneamente applicato a una promozione in un’attività duplicata all’attività originale. (TGT-41482)
* È stato risolto un problema che impediva la corretta visualizzazione del pulsante &quot;Modifica criteri&quot; nella pagina [!UICONTROL Esperienze] per le attività [!DNL Recommendations] nel Compositore esperienza visivo. (TGT-39512)
* È stato risolto un problema che impediva la sincronizzazione delle attività quando venivano duplicate e copiate in un’area di lavoro di test. (TGT-40686)
* È stato risolto un problema che impediva modifiche a un selettore con [frammenti esperienza](/help/c-experiences/c-manage-content/aem-experience-fragments.md) quando si utilizzava &quot;[!UICONTROL Inserisci dopo]&quot; nel Compositore esperienza visivo. (TGT-41802)
* È stato risolto un problema che impediva l’invio al backend di contenuto JSON vuoto in un’offerta. [!DNL Target] ora invia l’oggetto JSON anche se è vuoto. (TGT-41555)
* È stato risolto un problema che causava l&#39;apertura del reporting precedente [!DNL Analytics] invece di [!DNL Analysis Workspace] quando i clienti facevano clic su &quot;[!UICONTROL Visualizza in Analytics]&quot; durante la visualizzazione di un rapporto. (TGT-41867)
* Sono stati aggiunti ulteriori chiarimenti al messaggio dell’interfaccia utente visualizzato quando un cliente tenta di selezionare [!DNL Analytics] come origine per la generazione di rapporti (A4T) per un’attività [!UICONTROL Automated Personalization]. Il messaggio indica che &quot;[!DNL Target] è l&#39;unica origine supportata per le attività [!UICONTROL Automated Personalization].&quot; (TGT-41954)
* È stato aggiunto un ulteriore chiarimento al messaggio di errore quando i clienti tentano di separare gli host con &quot;nuova riga&quot; invece delle virgole. (TGT-40671)
* È stato risolto un problema che causava alcune date di &quot;[!UICONTROL Ultimo aggiornamento]&quot; delle attività diverse dall&#39;interfaccia utente inglese per i clienti spagnoli e giapponesi (quando visualizzavano l&#39;interfaccia utente in spagnolo e giapponese). (TGT-38980)

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
