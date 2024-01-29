---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 99152f66217f66174e8b6a5a7319f11b22c74b8e
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 100%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: 22 gennaio 2024**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Rimozione di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024)

| Rimozione | Dettagli |
|--- |--- |
| [!DNL iPad] e [!DNL iPhone] verranno rimossi dall’[attributo di browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzato durante la creazione di tipi di pubblico.<p>Data di rimozione:<P>30 aprile 2024 | [!DNL Adobe Target] consente di [eseguire il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che utilizzano [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) specifici quando visitano la tua pagina.<P><B>A partire dal 30 aprile 2024, iPad e iPhone verranno rimossi dall’elenco a discesa del tipo di [!UICONTROL browser] durante la creazione di categorie per i tipi di pubblico.</b><P>Se hai tipi di pubblico che eseguono il targeting di iPad o iPhone utilizzando come attributo il [!UICONTROL browser], è necessario modificare queste impostazioni prima del 30 aprile 2024 per garantire che tali tipi di pubblico continuino a funzionare come previsto.<p>Per esempi di impostazioni alternative, consulta [Rimozione di iPad e iPhone dall’attributo di pubblico Browser (30 aprile 2024)](/help/main/c-target/c-audiences/c-target-rules/browser.md#deprecation). |

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
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
