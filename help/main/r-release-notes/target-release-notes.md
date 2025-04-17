---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cd25bda52b7a1b916a73ca5e531a7134ba8cef4e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 43%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: venerdì 17 aprile 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.4.4 (17 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato aggiunto un messaggio di errore per guidare gli utenti nella risoluzione delle opzioni duplicate in un’attività. (TGT-51927)
* È stato risolto un problema che impediva la rimozione di `ClickTrack` selettori durante l&#39;eliminazione di pagine o esperienze con offerte di reindirizzamento. (TGT-51952)
* È stato risolto un problema che causava l&#39;autorizzazione di selettori `ClickTrack` vuoti. [!DNL Target] ora richiede che il campo del selettore non sia vuoto. (TGT-52107)
* È stato risolto un problema che consentiva erroneamente le metriche con nomi duplicati. Le metriche ora richiedono nomi univoci. (TGT-52201)
* È stato risolto un problema a causa del quale le definizioni dei tipi di pubblico non erano visibili durante la modifica del targeting a livello di offerta nelle attività [!UICONTROL Automated Personalization] (AP). (TGT-52148)
* È stato risolto un problema che impediva ai clienti con diritti [!UICONTROL Editor] di salvare le attività. (TGT-52227)
* `OptionLocalIDs` non incrementa più in modo errato quando l&#39;opzione rimane invariata. (TGT-52139)
* È stato risolto un problema che causava un messaggio &quot;Non valido `optionLocalIds`&quot; durante il tentativo di creare un&#39;attività. (TGT-52154)
* Sono state corrette le discrepanze tra `OptionLocalIDs` definiti per un&#39;attività e quelli utilizzati per definire le esperienze. (TGT-52215)
* È stato risolto un problema che causava un errore di convalida durante il tentativo di creazione di un’attività A/B. (TGT-51923)

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
