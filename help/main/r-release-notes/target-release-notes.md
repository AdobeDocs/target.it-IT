---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 4baa78ac1119e86002c415f09b9481ad351fdcfc
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 24%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 4 ottobre 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.10.1 (versione scaglionata dal 5 al 7 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **5 ottobre**: regione Asia-Pacifico (APAC)
* **6 ottobre**: Regione delle Americhe
* **7 ottobre**: Area Europa, Medio Oriente e Africa (EMEA)

Questa versione contiene le seguenti nuove funzioni, miglioramenti e correzioni:

| Funzione | Dettagli |
| --- | --- |
| [!DNL Adobe Experience Manager] (AEM) frammenti di esperienza | Gli aggiornamenti alla funzionalità frammenti di esperienza AEM includono:<ul><li>È stata aggiunta la possibilità di filtrare AEM frammenti di esperienza per tipo (HTML o JSON) in [!UICONTROL Offerte] elenco. (TGT-43121)</li><li>È stato risolto un problema che consentiva ai clienti di inserire JSON [!UICONTROL Frammento esperienza] offerte quando si utilizza il Compositore esperienza visivo, che non è supportato. Le offerte JSON possono essere inserite solo quando si utilizza il [!UICONTROL Esperienza basata su moduli] compositore. (TGT-43846)</li></ul>Per ulteriori informazioni, consulta AEM [frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md). |
| Nuovo [!UICONTROL Compositore esperienza visivo] estensione per Google Chrome | Nuovo [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] L’estensione (VEC) per Chrome è disponibile in Chrome Web Store.<br>A partire da gennaio 2023, la [!DNL Target] L’estensione VEC Helper smetterà di funzionare in Google Chrome perché Google non consente le estensioni che utilizzano Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni in Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Vecchia estensione](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul>Per ulteriori informazioni, consulta [Estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]<br>(Data esatta di rilascio da determinare.) | Tieni presente le seguenti modifiche:<ul><li>È stato aggiunto il supporto per le metriche binarie e di ottimizzazione in [!UICONTROL Analytics for Target] Generazione di rapporti per A4T per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività</li><li>Comportamento mantenuto per le attività esistenti fino al 20 febbraio 2023. Dopo questa data, le attività verranno interrotte per forzare la migrazione delle attività esistenti a nuovi comportamenti</li><li>A partire dal 20 febbraio 2023, supporto per `averagetimespentonsite`, `bouncerate`e `entries` metriche in [!DNL Target] le attività diventeranno obsolete.</li></ul> |
| Aggiornamenti alla documentazione | Gli aggiornamenti principali della documentazione includono:<ul><li>Novità e aggiornamento [Documentazione dell’API per l’amministrazione di Adobe Target e la creazione di rapporti](https://developer.adobe.com/target/administer/admin-api/){target=_blank} include una copertura completa degli endpoint API di amministrazione e reporting, tra cui proprietà, offerte, host, ambienti, client, pubblico, attività e altro ancora.<br>Vedi questo e altri contenuti per sviluppatori nella sezione [[!DNL Adobe Target] [!UICONTROL Guida per gli sviluppatori]](https://developer.adobe.com/target/){target=_blank}.</li><li>[Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md)<br>Questo articolo documenta i calcoli statistici dettagliati utilizzati nei test A/Bn manuali in [!DNL Adobe Target].<br>Le informazioni contenute in questo articolo sostituiscono le *Calcoli di Adobe Target per test A/B* file pdf precedentemente disponibile per il download su questo sito.</li></ul> |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulla regola del pubblico in [!UICONTROL Perfezionamenti dei tipi di pubblico] finestra delle informazioni. (TGT-43917)
* Miglioramento delle prestazioni della [!DNL Target] Interfaccia utente per il caricamento di tipi di pubblico che si avvicinano alla [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti nel [!UICONTROL Modifiche] sul pannello [!UICONTROL Esperienze] quando crei o modifichi attività nel Compositore esperienza visivo dopo il passaggio da [!UICONTROL Componi] a [!UICONTROL Sfoglia] modalità. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare [!UICONTROL Test A/B] attività che utilizzano [!UICONTROL Targeting automatico]. (TGT-40978)
* Aggiunta la possibilità di utilizzare automaticamente una singola offerta in più posizioni all&#39;interno di un singolo gruppo di reporting. (TGT-40689)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
