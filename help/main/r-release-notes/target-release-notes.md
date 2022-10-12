---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 36c05ee2531009ea74ef9085404d12e389cef743
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 100%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 5 ottobre 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.10.1 (rilascio scaglionato dal 10 al 13 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **10 ottobre**: area geografica Asia-Pacifico (APAC)
* **12 ottobre**: area geografica delle Americhe
* **13 ottobre**: area geografica Europa, Medio Oriente e Africa (EMEA)

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Adobe Experience Manager] Frammenti esperienza (AEM) | Gli aggiornamenti relativi alla funzionalità dei frammenti di esperienza AEM includono:<ul><li>È stata aggiunta la possibilità di filtrare i Frammenti di esperienza di (AEM) per tipo (HTML o JSON) nell’elenco delle [!UICONTROL Offerte]. (TGT-43121)</li><li>È stato risolto un problema che consentiva ai clienti di inserire offerte di [!UICONTROL Frammenti di esperienza] JSON utilizzando il Compositore esperienza visivo (VEC), azione che non è supportata. Le offerte JSON possono essere inserite esclusivamente utilizzando il [!UICONTROL Compositore esperienza basato su moduli]. (TGT-43846)</li></ul>Per ulteriori informazioni, consulta i [Frammenti esperienza AEM](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nuova estensione [!UICONTROL Compositore esperienza visivo] per Google Chrome | Nel Chrome Web Store, è disponibile una nuova estensione per il [!UICONTROL Compositore esperienza visivo] (VEC) di [!DNL Adobe Target] per Chrome.<br>A partire dal mese di gennaio 2023, l’attuale estensione [!DNL Target] VEC Helper cesserà di funzionare in Google Chrome perché Google non consentirà l’utilizzo di estensioni basate su Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni nel Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Estensione precedente](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Per ulteriori informazioni, consulta [Estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Aggiornamenti della documentazione | Gli aggiornamenti principali della documentazione includono:<ul><li>La [Documentazione delle API per l’amministrazione e il reporting di Adobe Target](https://developer.adobe.com/target/administer/admin-api/){target=_blank} nuova e aggiornata include una copertura completa degli endpoint API di amministrazione e reporting, tra cui proprietà, offerte, host, ambienti, client, tipi di pubblico, attività e molto altro ancora.<br>Consulta la documentazione e altri contenuti per sviluppatori nella sezione Guida per gli sviluppatori di [[!DNL Adobe Target] ](https://developer.adobe.com/target/){target=_blank}.</li><li>[Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>Questo articolo documenta i calcoli statistici dettagliati utilizzati nei test A/Bn manuali in [!DNL Adobe Target].<br>Le informazioni contenute in questo articolo sostituiscono il file pdf dei *Calcoli di Adobe Target per test A/B* precedentemente disponibile per il download su questo sito.</li></ul> |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulle regole del pubblico nella finestra [!UICONTROL Perfezionamenti dei tipi di pubblico]. (TGT-43917)
* Sono state migliorate le prestazioni dell’interfaccia utente di [!DNL Target] durante il caricamento dei tipi di pubblico che si avvicinano al [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti sul pannello [!UICONTROL Modifiche] nella pagina [!UICONTROL Esperienze] durante la creazione o la modifica delle attività nel Compositore esperienza visivo dopo il passaggio dalla modalità [!UICONTROL Componi] alla modalità [!UICONTROL Sfoglia]. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare le attività di [!UICONTROL Test A/B] che utilizzano il [!UICONTROL Targeting automatico]. (TGT-40978)
* È stata aggiunta la possibilità di utilizzare automaticamente un’unica offerta in più posizioni all’interno di un singolo gruppo di reporting. (TGT-40689)

## Note aggiuntive sulla versione e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
