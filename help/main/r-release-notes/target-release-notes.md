---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: bdc2f76af2a1f1554556d56a983748aa2c9caf2c
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 24%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: sabato 14 marzo 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.3.7 (26 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva il salvataggio di attività multipagina se una pagina veniva eliminata dopo le modifiche. (TGT-51988)
* È stato risolto un errore che si verificava durante la modifica di un&#39;attività: `default message [Invalid optionLocalIds: xx]]`. (TGT-51985)
* È stato risolto un problema a causa del quale l’aggiunta di nuove modifiche a un’attività rimuoveva le modifiche esistenti. (TGT-51981)
* È stato risolto un problema a causa del quale la sostituzione di un pubblico con &quot;[!UICONTROL All visitors]&quot; durante la creazione o la modifica dell&#39;attività causava un errore &quot;I tipi di pubblico duplicati non sono consentiti&quot;. (TGT-51978)
* È stato risolto un problema che causava un errore &quot;Input utente non valido&quot; durante il salvataggio di un&#39;attività [!UICONTROL A/B Test]. (TGT-51976)
* È stato risolto un problema che impediva la corretta visualizzazione delle metriche calcolate sulla pagina [!UICONTROL Goals & Settings]. (TGT-51975)
* È stato risolto un problema che impediva la corrispondenza tra `companyName` e `reportSuite` nella configurazione [!DNL Analytics] per la metrica `pageviews`. (TGT-51965)
* È stato risolto un problema che causava la rimozione delle modifiche dal passaggio a un’esperienza in un’attività. (TGT-51945)
* È stato risolto un problema a causa del quale la rimozione di un pubblico di pagina causava la rimozione anche di [!UICONTROL ClickTrack] selettori. (TGT-51935)
* È stato risolto un problema che impediva la modifica di un&#39;attività dopo l&#39;apertura della relativa pagina [!UICONTROL Overview]. (TGT-51931)
* È stato risolto un problema che causava un errore `[Unused optionLocalIds: 0]]` durante la creazione dell&#39;attività. (TGT-51920)
* È stato risolto un problema a causa del quale alcune modifiche non venivano tradotte correttamente dopo la rimozione delle modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema che impediva il corretto aggiornamento dei tipi di pubblico di destinazione in [!UICONTROL Form-Based Experience Composer]. (TGT-51845)
* È stato risolto un problema che impediva l&#39;aggiornamento corretto dell&#39;URL in [!UICONTROL Visual Experience Composer] durante la navigazione dell&#39;attività. (TGT-51832)
* È stato risolto un problema che impediva la visualizzazione delle offerte nell&#39;interfaccia utente [!UICONTROL Offers], nonostante la corretta visualizzazione durante la creazione di un&#39;attività e l&#39;aggiunta di offerte. (TGT-51805)
* È stato risolto un problema a causa del quale alcune attività non disponevano di una schermata di fallback per visualizzare il contenuto predefinito quando non era possibile distribuire contenuto personalizzato o mirato. (TGT-51638)
* È stato risolto un problema che impediva la corretta visualizzazione delle offerte live e di alcune cartelle nell&#39;interfaccia utente [!UICONTROL Offers]. (TGT-51628)
* È stato risolto un problema che impediva la corretta localizzazione di alcune stringhe URL e goURL. (TGT-35741)
* È stato risolto un problema che impediva la corretta localizzazione dei ruoli ([!UICONTROL Approver], [!UICONTROL Editor] e [!UICONTROL Observer]) nell&#39;interfaccia utente [!DNL Target]. (TGT-29925)

## [!DNL Target Standard/Premium] 25.3.6 (14 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto l&#39;errore &quot;Input utente non valido&quot; nelle attività [!UICONTROL Visual Experience Composer] (VEC) con [!UICONTROL Click Tracking] abilitato quando lo stesso selettore [!UICONTROL ClickTrack] viene utilizzato più volte. (TGT-51921)
* È stato corretto l’errore &quot;Input utente non valido&quot; nelle attività del Compositore esperienza visivo con posizioni condivise (ad esempio, selettore HEAD) e offerte identiche. (TGT-51879)
* È stato risolto un problema che causava la condivisione delle modifiche dell’esperienza tra i vari tipi di pubblico. (TGT-51815)
* Sono stati risolti degli errori di convalida durante la creazione di attività a causa di conflitti di ID segmento. Gli errori si sono verificati quando [!DNL Target] ha rilevato attività esistenti utilizzando segmenti anonimi. (TGT-51784)
* È stato risolto un problema che impediva a [!DNL Target] di salvare attività con regole di esclusione in un pubblico. (TGT-51581)
* È stato risolto un problema che impediva ai clienti di creare, eliminare o spostare cartelle senza accedere all’area di lavoro predefinita. (TGT-51499)
* È stato risolto un problema che causava un errore nelle richieste di GET durante il recupero dell&#39;elenco delle metriche [!DNL Analytics]. (TGT-51106)

## [!DNL Target Standard/Premium] 25.3.5 (11 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva agli utenti di modificare le offerte nel pannello [!UICONTROL Modifications]. (TGT-51800)
* È stato risolto un problema che impediva la corretta visualizzazione delle azioni nel pannello sinistro per esperienze e tipi di pubblico, incluso in modalità [!UICONTROL ClickTrack]. (TGT-51895)
* È stato risolto un problema a causa del quale i selettori [!UICONTROL ClickTrack] non venivano applicati alla pagina corretta del pubblico. (TGT-51871)

## [!DNL Target Standard/Premium] 25.3.4 (7 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la modifica o il riutilizzo dei tipi di pubblico per sola attività nel pannello [!UICONTROL Audiences]. (TGT-51860)
* È stato risolto un problema che impediva ai clienti [!DNL Target Standard] di creare attività utilizzando reporting di [!UICONTROL Analytics for Target] (A4T). (TGT-51854)
* È stato risolto un problema che escludeva i contatori degli ID locali dal payload durante le operazioni di creazione e modifica in batch. (TGT-51867)

## [!DNL Target Standard/Premium] 25.3.2 (6 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che impediva la creazione di una nuova attività in seguito alla copia di un’attività con un pubblico per sola attività, utilizzando erroneamente il pubblico dell’attività originale. (TGT-51855)
* È stato risolto un problema che impediva la modifica delle attività [!UICONTROL Experience Targeting] (XT) con tipi di pubblico per sola attività. (TGT-51846)
* È stato risolto un problema che impediva al Compositore esperienza visivo di applicare correttamente le modifiche a un&#39;esperienza alla prima modifica. [!UICONTROL Visual Experience Composer] (TGT-51843)
* È stato risolto un problema che attivava un errore &quot;ID&quot; quando si faceva clic su alcuni elementi all’interno del Compositore esperienza visivo. (TGT-51814)
* È stata aggiornata la gestione degli errori nel Compositore esperienza visivo durante la creazione dell’attività. (TGT-51759)
* È stato risolto un problema che causava un errore di &quot;input utente non valido&quot; durante il salvataggio dell&#39;attività a causa di una visualizzazione mancante nel pannello [!UICONTROL Modifications]. (TGT-51827)
* È stato risolto un problema che impediva la creazione di criteri per i consigli. (TGT-51834)
* È stato aggiunto un messaggio di conferma prima del reindirizzamento a un URL diverso. (TGT-51703)
* Sono stati risolti dei problemi relativi ai test di integrazione di GraphQL in offerte e cartelle. (TGT-51839)

## [!DNL Target Standard/Premium] 25.3.1 (3 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Un pubblico combinato può includere sottogruppi, ciascuno contenente più tipi di pubblico. Questa versione ha risolto un problema che impediva la visualizzazione dei tipi di pubblico dei sottogruppi nella finestra di dialogo [!UICONTROL Rules]. (TGT-51813)
* È stato risolto un problema che causava la sostituzione di alcuni tipi di pubblico di esperienza con [!UICONTROL All Visitors] durante l&#39;apertura di attività precedenti. (TGT-51812)
* È stato risolto un problema che impediva la modifica di attività con tipi di pubblico per sola attività. (TGT-51807)
* È stato risolto un problema che impediva la modifica delle modifiche dell&#39;intestazione della pagina nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-51797)
* È stato risolto un errore Null che si verificava durante la duplicazione di un’esperienza, l’eliminazione di un’altra esperienza e il tentativo di salvare l’attività. (TGT-51796)
* È stato risolto un problema che impediva la visualizzazione delle regole di esclusione del pubblico nel pannello informazioni del pubblico durante il passaggio [!UICONTROL Targeting] della creazione delle attività. (TGT-51579)
* Aggiornati messaggi di errore localizzati in coreano. (TGT-51701 e TGT-51699)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
