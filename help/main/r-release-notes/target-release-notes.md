---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 82b75b8ef293b3243c0b2528020dced4654b2688
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 56%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 8 novembre 2023**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.11.1 (13 e 14 novembre 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **Novembre 13**: area geografica Asia-Pacifico (APAC)
* **Novembre 14**: area geografica delle Americhe
* **Novembre 14**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include le seguenti correzioni:

* È stata migliorata la [Controllo di qualità delle attività](/help/main/c-activities/c-activity-qa/activity-qa.md) per consentire ai clienti di non consentire offerte duplicate per le esperienze in [!UICONTROL Automated Personalization] attività. (TGT-46627)
* È stata aggiunta una descrizione comando in [!DNL Target] Interfaccia utente per aiutare i clienti a comprendere il motivo per cui potrebbero non essere disponibili dati nei rapporti sulle attività se non viene allocato traffico all’esperienza di controllo. Nella descrizione comando è incluso un collegamento a ulteriori informazioni: [Perché non sono disponibili dati per il rapporto della mia attività?](/help/main/c-reports/reporting-frequently-asked-questions.md#section_E4722F6445884130951DF79981C8289B). (TGT-46610)
* È stato risolto un problema che impediva la corretta visualizzazione delle attività in [!UICONTROL Attività] per alcuni clienti. (TGT-46830)

* Sono stati risolti i seguenti problemi che interessavano le attività che utilizzavano [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) come origine per la generazione di rapporti:
   * È stato risolto un problema che impediva ad alcuni clienti di visualizzare i dati di reporting. (TGT-46557)
   * È stato risolto un problema che a volte causava la [!UICONTROL Visualizza in Analytics] sulle pagine di reporting delle attività per non funzionare correttamente. (TGT-46731)
   * È stato risolto un problema che impediva l’utilizzo di dati per [!UICONTROL Incremento] e [!UICONTROL Affidabilità] per visualizzare correttamente in [!DNL Target] UI. (TGT-46592, TGT-46554, TGT-46586)

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
