---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 5ad7427df49f6091f69fadac96fd55e7b48a4cda
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 19 gennaio 2023**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.13.3 (25 gennaio 2023)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto per le offerte JSON nelle attività di [!UICONTROL Automated Personalization] (AP) utilizzando il Compositore esperienza basato su moduli. (TGT-41460)
* È stata implementata la [modalità Controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) per le attività Automated Personalization. (TGT-44341)
* I nomi di esperienza nelle attività [!DNL Recommendations] ora vengono visualizzati con nomi descrittivi in modo che i clienti possano correlare meglio i dati in [!DNL Adobe Analytics] con l’interfaccia utente di [!DNL Target]. (TGT-41853)
* È stato risolto un problema che causava un “errore 500” nelle attività [!UICONTROL Test A/B] e di [!UICONTROL Targeting dell’esperienza] (XT) che contengono consigli. Questo problema si verificava quando [!DNL Target] non riusciva a eliminare correttamente gli oggetti di criteri dall’interfaccia utente di [!DNL Target] e dal back-end di [!DNL Recommendations] non più in uso. (TGT-44383)
* È stata rimossa la posizione dal nome dell’offerta visualizzato nel rapporto [!UICONTROL Livello di offerta] delle attività di [!UICONTROL Automated Personalization]. Questa modifica rende il rapporto più leggibile. (TGT-44294)
* È stata rinominata l’opzione “[!UICONTROL Frammento di esperienza]” nel flusso di lavoro del [!UICONTROL Compositore esperienza visivo]. L&#39;opzione è ora “[!UICONTROL HTML XF]”. (TGT-44132)
* È stata ggiunta la possibilità di visualizzare i metadati dell’offerta del frammento esperienza nella descrizione dei comandi per le informazioni sull’offerta. (TGT-43838)
* Sono state rimosse le opzioni del calendario di 45 giorni e 90 giorni da AP e [!UICONTROL Targeting automatico] [!UICONTROL Approfondimenti personalizzazione] e rapporti [!UICONTROL Attributi importanti] nell’[!DNL Target] Interfaccia utente. A causa dei pattern di utilizzo e nel tentativo di migliorare le prestazioni, questi intervalli di date sono stati dichiarati obsoleti. L’interfaccia utente è stata aggiornata per riflettere gli intervalli attualmente consentiti: 15, 30 e 60 giorni. (TGT-39357)
* È stata rimossa la possibilità di modificare l’impostazione [!UICONTROL Identica all’obiettivo di ottimizzazione] sulla pagina [!UICONTROL Obiettivi e impostazioni] dopo che l’attività è in esecuzione. (TGT-43923)
* È stato risolto un problema che causava errori con l’ambiente di lavoro predefinito nel back-end di [!DNL Target] in caso di aggiornamento da [!DNL Target Standard] a [!DNL Target Premium]. (TGT-44081 e TGT-44306)
* È stato modificato il collegamento sulla pagina [!UICONTROL Implementazione] ([!UICONTROL Amministrazione] > [!UICONTROL Implementazione]) per “Metodi di implementazione con Decisioning sul dispositivo”, in modo che indichi la pagina di spiegazione su come utilizzare Decisioning sul dispositivo per tutti gli SDK supportati: Node.js, Java, .NET e Python. Per ulteriori informazioni, consulta [Guida introduttiva agli SDK di Target](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* È stato risolto un problema che causava errori durante il caricamento dei file utilizzando [!DNL Scene7] e [!DNL Target].
* È stata migliorata l’accessibilità dell’interfaccia utente di [!DNL Target] per le persone con disabilità utilizzando i risultati di una verifica interna in termini di usabilità. I miglioramenti dell’accessibilità includono l’accesso a funzioni che in precedenza non erano raggiungibili tramite la tastiera, miglioramenti al testo alternativo, la possibilità di eseguire lo zoom di parti dell’interfaccia utente per renderle più utilizzabili, l’attivazione della tastiera migliorata e molto altro ancora.   (TGT-42759)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
