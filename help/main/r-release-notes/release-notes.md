---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramento;miglioramenti;correzioni;correzioni di bug;aggiornamenti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: 784f41a73941877135a5902f2331972ba9d0e880
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 65%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamenti per `Browser:iPad` e `Browser:iPhone` in [!UICONTROL Browser] attributi del pubblico (30 aprile 2024)

| Aggiornamenti | Dettagli |
|--- |--- |
| [!UICONTROL Browser:iPad] e [!UICONTROL Browser:iPhone] aggiornato in [Attributi del browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzato durante la creazione di tipi di pubblico. | [!DNL Adobe Target] consente di: [esegui il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi i visitatori che utilizzano un [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) quando visitano la tua pagina.<P>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), tipi di pubblico incorporati creati utilizzando l’interfaccia utente di Target, ad esempio `Browser:iPad` e `Browser:iPhone` verrà aggiornato per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzo `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.<P>Questo aggiornamento non richiede alcuna azione da parte dei clienti.<p><B>Importante</b>: per consentire ai clienti di eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] negli script di profilo (e nei segmenti JavaScript), il cliente deve apportare modifiche manuali tramite **30 aprile 2024**. Per esempi di impostazioni alternative che devono essere modificate manualmente, vedere [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi del pubblico](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

## [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024)

Questa versione è pianificata per i seguenti giorni:

* **4 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **5 marzo**: area geografica Asia Pacifico (APAC)
* **6 marzo**: area geografica delle Americhe

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata corretta la logica che calcola il numero di selettori univoci in un’attività. (TGT-47878)
* È stato risolto un problema che causava [!UICONTROL Multivariate] (MVT) attività configurate con [!UICONTROL Analytics for Target] (A4T) generazione di rapporti per non essere visualizzati correttamente. (TGT-47490)
* È stato migliorato il messaggio di avviso visualizzato nel reporting quando un’esperienza senza traffico viene utilizzata come esperienza di controllo. (TGT-47537)
* Sono state aggiunte numerose correzioni di back-end e localizzazione.

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
