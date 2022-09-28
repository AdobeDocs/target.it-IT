---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 74531d6ca40d32c8e794d463ed211164342240cd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 29%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 28 settembre 2022**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 22.10.1 (versione scaglionata dal 4 al 6 ottobre 2022)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **4 ottobre**: Area Europa, Medio Oriente e Africa (EMEA)
* **5 ottobre**: regione Asia-Pacifico (APAC)
* **6 ottobre**: Regione delle Americhe

Questa versione contiene le seguenti nuove funzioni, miglioramenti e correzioni:

| Funzione | Dettagli |
| --- | --- |
| Nuovo [!UICONTROL Compositore esperienza visivo] estensione per Google Chrome | Nuovo [!DNL Adobe Target] [!UICONTROL Compositore esperienza visivo] L’estensione (VEC) per Chrome è disponibile in Chrome Web Store.<br>A partire da gennaio 2023, la [!DNL Target] L’estensione VEC Helper smetterà di funzionare in Google Chrome perché Google non consente le estensioni che utilizzano Manifest V2. Scarica la nuova estensione per continuare a creare visivamente i tuoi siti web in [!DNL Target] a partire dal nuovo anno.<br>I seguenti collegamenti mostrano le due estensioni in Chrome Web Store:<ul><li>[Nuova estensione](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=_blank}</li><li>[Vecchia estensione](https://chrome.google.com/webstore/detail/adobe-target-vec-helper/ggjpideecfnbipkacplkhhaflkdjagak){target=_blank}</li></ul> |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]<br>(Data esatta di rilascio da determinare.) | Tieni presente le seguenti modifiche:<ul><li>È stato aggiunto il supporto per le metriche binarie e di ottimizzazione in [!UICONTROL Analytics for Target] Generazione di rapporti per A4T per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico] attività</li><li>È stato rimosso il messaggio di avviso sulle metriche binarie per [!UICONTROL Targeting automatico] attività</li><li>Comportamento mantenuto per le attività esistenti fino al 20 febbraio 2023. Dopo questa data, le attività verranno interrotte per forzare la migrazione delle attività esistenti a nuovi comportamenti</li><li>A partire dal 20 febbraio 2023, supporto per `averagetimespentonsite`, `bouncerate`e `entries` metriche in [!DNL Target] le attività diventeranno obsolete.</li></ul> |

* È stato risolto un problema che impediva la corretta visualizzazione delle informazioni sulla regola del pubblico in [!UICONTROL Perfezionamenti dei tipi di pubblico] finestra delle informazioni. (TGT-43917)
* Miglioramento delle prestazioni della [!DNL Target] Interfaccia utente per il caricamento di tipi di pubblico che si avvicinano alla [limite consigliato per le regole di targeting](/help/main/r-troubleshooting-target/target-limits.md#targeting-rules). (TGT-43675)
* È stato risolto un problema che impediva la corretta visualizzazione di alcuni componenti nel [!UICONTROL Modifiche] sul pannello [!UICONTROL Esperienze] quando crei o modifichi attività nel Compositore esperienza visivo dopo il passaggio da [!UICONTROL Componi] a [!UICONTROL Sfoglia] modalità. (TGT-43300)
* È stato risolto un problema che impediva ad alcuni clienti di archiviare [!UICONTROL Test A/B] attività che utilizzano [!UICONTROL Targeting automatico]. (TGT-40978)
* Aggiunta la possibilità di utilizzare automaticamente una singola offerta in più posizioni all&#39;interno di un singolo gruppo di reporting. (TGT-43974)
* Aggiunta la possibilità di filtrare [!DNL Adobe Experience Manager] (AEM) [frammenti esperienza](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md) per tipo (HTML o JSON) nel [!UICONTROL Offerte] elenco. (TGT-43121)
* È stato risolto un problema che consentiva ai clienti di inserire JSON [!UICONTROL Frammento esperienza] offerte quando si utilizza il Compositore esperienza visivo, che non è supportato. Le offerte JSON possono essere inserite solo quando si utilizza il [!UICONTROL Esperienza basata su moduli] compositore. (TGT-43846)

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
