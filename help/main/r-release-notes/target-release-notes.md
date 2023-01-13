---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: c12df34c9c7392a0ea50e8d1dea32147e8b7b165
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 52%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 12 gennaio 2023**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.13.3 (25-26 gennaio 2023)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

* È stato aggiunto il supporto per le offerte JSON nelle attività di [!UICONTROL Automated Personalization] (AP) utilizzando il Compositore esperienza basato su moduli. (TGT-41460)
* Implementato [Modalità QA](/help/main/c-activities/c-activity-qa/activity-qa.md) per le attività di Personalizzazione automatizzata. (TGT-44341)
* Nomi di esperienza in [!DNL Recommendations] le attività ora vengono visualizzate con nomi descrittivi in modo che i clienti possano correlare meglio i dati in [!DNL Adobe Analytics] con quello [!DNL Target] Interfaccia utente. (TGT-41853)
* È stato risolto un problema che causava un &quot;errore 500&quot; in [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) attività che contengono consigli. Questo problema è stato causato quando [!DNL Target] impossibile eliminare correttamente gli oggetti criteri dal [!DNL Target] Interfaccia utente e [!DNL Recommendations] backend non più in uso. (TGT-44383)
* È stata rimossa la posizione dal nome dell’offerta visualizzato nel [!UICONTROL Livello di offerta] rapporto [!UICONTROL Automated Personalization] attività. Questa modifica rende il rapporto più leggibile. (TGT-44294)
* &quot; rinominato[!UICONTROL Frammento esperienza]&quot; nella [!UICONTROL Compositore esperienza visivo] Flusso di lavoro (VEC). L&#39;opzione è ora “[!UICONTROL HTML XF]”. (TGT-44132)
* È stata ggiunta la possibilità di visualizzare i metadati dell’offerta del frammento esperienza nella descrizione dei comandi per le informazioni sull’offerta. (TGT-43838)
* Sono state rimosse le opzioni del calendario di 45 giorni e 90 giorni da AP e [!UICONTROL Targeting automatico] [!UICONTROL Approfondimenti personalizzazione] e rapporti [!UICONTROL Attributi importanti] nell’[!DNL Target] Interfaccia utente. A causa dei pattern di utilizzo e nel tentativo di migliorare le prestazioni, questi intervalli di date sono stati dichiarati obsoleti. L’interfaccia utente è stata aggiornata per riflettere gli intervalli attualmente consentiti: 15, 30 e 60 giorni. (TGT-39357)
* Possibilità di modificare la [!UICONTROL Come obiettivo di ottimizzazione] l&#39;impostazione [!UICONTROL Obiettivi e impostazioni] dopo che l’attività è stata pubblicata. (TGT-43923)
* È stato risolto un problema che causava problemi con la posizione di lavoro predefinita nel [!DNL Target] backend per l’aggiornamento da [!DNL Target Standard] a [!DNL Target Premium]. (TGT-44081 e TGT-44306)
* Il collegamento sul [!UICONTROL Implementazione] page ([!UICONTROL Amministrazione] > [!UICONTROL Implementazione]) per &quot;Metodi di implementazione con On-Device Decisioning&quot;, indica la pagina che spiega come utilizzare le decisioni sui dispositivi per tutti gli SDK supportati: Node.js, Java, .NET e Python. Per ulteriori informazioni, consulta [Guida introduttiva agli SDK di Target](https://developer.adobe.com/target/implement/server-side/sdk-guides/getting-started/){target=_blank} in the [Adobe Target Developer Guide](https://developer.adobe.com/target/){target=_blank}.
* È stato risolto un problema che causava problemi di caricamento dei file durante l&#39;utilizzo di [!DNL Scene7] e [!DNL Target].
* Miglioramento dell’accessibilità dei [!DNL Target] Interfaccia utente per le persone con disabilità tramite i risultati di un controllo interno dell’usabilità. Questi miglioramenti dell’accessibilità includono l’accesso a funzioni che in precedenza non erano accessibili tramite la tastiera, miglioramenti al testo alt, la possibilità di eseguire lo zoom di parti dell’interfaccia utente per renderle più utilizzabili, una migliore messa a fuoco da tastiera e altro ancora.   (TGT-42759)
* Sono state apportate diverse correzioni di localizzazione in tutto il [!DNL Target] Interfaccia utente.

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
