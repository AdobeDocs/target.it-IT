---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: b76a0541b181ee5ebe88f2d11f5556c6c7b91126
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 50%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: mercoledì 16 gennaio 2024**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Obsolescenza di iPad e iPhone dall’attributo di pubblico del browser (30 aprile 2024)

| Obsolescenza | Dettagli |
|--- |--- |
| [!DNL iPad] e [!DNL iPhone] da rendere obsoleto a partire dal [Attributo browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzato durante la creazione di tipi di pubblico.<p>Data obsoleta:<P>mercoledì 30 aprile 2024 | [!DNL Adobe Target] consente di: [esegui il targeting su uno qualsiasi dei vari attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi gli utenti che utilizzano un [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) quando visitano la tua pagina.<P><B>A partire dal 30 aprile 2024, iPad e iPhone verranno rimossi dal [!UICONTROL Browser] digita l’elenco a discesa durante la creazione di categorie per i tipi di pubblico.</b><P>Se hai tipi di pubblico che eseguono il targeting di iPad o iPhone utilizzando [!UICONTROL Browser] , è necessario modificare queste impostazioni prima del 30 aprile 2024 per garantire che tali tipi di pubblico continuino a funzionare come previsto.<P>In futuro è necessario utilizzare le seguenti impostazioni:<ul><li>[!UICONTROL Dispositivi mobili] > [!UICONTROL è un tablet]<P>![mobile è tablet](/help/main/r-release-notes/assets/is-tablet.png)</li><li>[!UICONTROL Dispositivi mobili] > [!UICONTROL Nome marketing del dispositivo] [!UICONTROL corrisponde a] [!DNL iPad]<P>![iPad](/help/main/r-release-notes/assets/ipad.png)</li><li>[!UICONTROL Dispositivi mobili] > [!UICONTROL Nome marketing del dispositivo] [!UICONTROL corrisponde a] [!DNL iPhone]<p>![iPhone](/help/main/r-release-notes/assets/iphone.png)</li></ul> |

## [!DNL Target] Standard/Premium 24.1.1 (22, 23 e 25 gennaio 2024)

Questa versione è pianificata per i seguenti giorni:

* **22 gennaio**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **23 gennaio**: area geografica Asia-Pacifico (APAC)
* **25 gennaio**: area geografica delle Americhe

Questa versione include i miglioramenti e le correzioni seguenti:

* È stato risolto un problema che impediva il corretto funzionamento degli intervalli di date per la generazione di rapporti. (TGT-47396)
* È stato risolto un problema che causava la visualizzazione dello stato errato su [!UICONTROL Tutte le attività] dopo che i clienti hanno attivato o disattivato un’attività utilizzando [!UICONTROL Altre azioni] icona. (TGT-47367)
* È stato risolto un problema che causava la [!UICONTROL Attributi importanti] rapporto da non visualizzare per un cliente. (TGT-47272)
* È stato risolto un problema che causava la visualizzazione di un messaggio di &quot;payload non valido&quot; quando un cliente tentava di abilitare &quot;Richiedi autenticazione&quot;. (TGT-47195)
* Sono state aggiornate numerose stringhe localizzate in [!DNL Target] UI.

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.corp.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
