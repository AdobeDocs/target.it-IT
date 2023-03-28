---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di Adobe Target.
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 1cc630f12f4b9dc1d9c5700bc6174b40d4f0dae2
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 48%

---

# Note sulla versione di Target (prerelease)

Questo articolo contiene informazioni di pre-release. Date di rilascio, funzioni e altre informazioni sono soggette a cambiamenti senza preavviso.

**Ultimo aggiornamento: 27 marzo 2023**

Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle versioni. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target] Standard/Premium 23.3.1 (28-30 marzo 2023)

Questa versione sarà disponibile in base al seguente programma scaglionato:

* **28 marzo**: area geografica Europa, Medio Oriente e Africa (EMEA)
* **29 marzo**: area geografica Asia Pacifico (APAC)
* **30 marzo**: area geografica delle Americhe

Questa versione include le nuove funzioni, i miglioramenti e le correzioni seguenti:

| Funzione | Dettagli |
|--- |--- |
| Frammenti di contenuto AEM per personalizzazione e sperimentazione headless | Utilizzo [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività. Combina la facilità d&#39;uso e la potenza delle AEM con le potenti funzionalità di intelligenza artificiale (AI) e apprendimento automatico (ML) in [!DNL Target] per testare e personalizzare le esperienze su larga scala. |
| Metriche A4T ottimizzate per [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]<p>(Data di rilascio: 30 marzo 2023) | [!DNL Target] consente di scegliere le metriche basate su eventi binomiali o le metriche basate su eventi continui quando si utilizza [!UICONTROL A4T] per attività di [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].<P>In particolare, tieni conto delle seguenti modifiche nelle metriche supportate:<ul><li>[!DNL Target] ha mantenuto il comportamento precedente per le attività esistenti fino al 9 settembre 2023. Dopo tale data, le attività che utilizzando le metriche non supportate verranno interrotte e sarà necessario effettuarne la migrazione ai nuovi comportamenti.</li></ul> |
| [!UICONTROL Allocazione automatica] utilizzando [!UICONTROL Analytics for Target] (A4T) | Esercitazione aggiornata:<ul><li>[Configurazione dei rapporti A4T in  [!DNL Analysis Workspace]  per le attività di [!UICONTROL Allocazione automatica] ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-allocate-activities.html?lang=it){target=_blank}</li></ul> |
| [!UICONTROL Targeting automatico] utilizzando [!UICONTROL Analytics for Target] (A4T) | Esercitazione aggiornata:<ul><li>[Configurazione dei rapporti A4T in  [!DNL Analysis Workspace]  per le attività di [!UICONTROL Targeting automatico] ](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/set-up-a4t-reports-in-analysis-workspace-for-auto-target-activities.html?lang=it){target=_blank}</li></ul> |

* Miglioramento della sincronizzazione di pubblico e attività in modo che gli elementi creati in [!DNL Adobe Experience Platform] e [!DNL Adobe Audience Manager] sono disponibili in [!DNL Target] Interfaccia più rapida. (TGT-44568)
* È stata apportata una modifica per consentire agli utenti di rimuovere la [!UICONTROL URL predefinito] sotto [!UICONTROL Amministrazione] > [!UICONTROL Compositore esperienza visivo] > [!UICONTROL URL predefinito]. Questa modifica consente ai clienti di ripristinare l’URL predefinito a una stringa vuota, che in precedenza non era possibile dopo la configurazione iniziale. (TGT-44577)
* Sono state rimosse le restrizioni che impedivano ai clienti di modificare o eliminare i tipi di pubblico predefiniti (tipi di pubblico con nomi riservati). (TGT-44655)
* Disabilitato &quot;[!UICONTROL Fine]&quot; durante il caricamento degli spinaroli erano visibili nella [!DNL Target] Interfaccia utente durante la creazione [pubblico combinato](/help/main/c-target/combining-multiple-audiences.md). (TGT-44079)
* È stato corretto il [!UICONTROL Lingua] link nella parte inferiore del [!UICONTROL Tipi di pubblico] in modo che si colleghi correttamente a &quot;[!UICONTROL Preferenze di comunicazione dell&#39;account]&quot; pagina. (TGT-43562)
* È stato risolto un problema che a volte impediva ai clienti di creare [!UICONTROL Test A/B] dopo aver selezionato [!UICONTROL Adobe Analytics] opzione sotto [!UICONTROL Amministrazione] > [!UICONTROL Reporting] > [!UICONTROL Soluzione Experience Cloud di reporting]. (TGT-44844)
* È stato risolto un problema che impediva ai clienti di visualizzare l’ultima esperienza in un [!UICONTROL Test multivariato] attività con molte esperienze dall’interno di [!UICONTROL Compositore esperienza visivo] (Compositore esperienza visivo). La [Percorso DOM](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md#dom-path) nella parte inferiore del Compositore esperienza visivo a volte impediva ai clienti di visualizzare l’ultima esperienza. (TGT-44578)
* È stato risolto un problema a causa del quale l’URL di navigazione nel Compositore esperienza visivo non rispecchiava la pagina corrente visibile in una normale sessione del browser se la pagina richiede l’autorizzazione o richiama reindirizzamenti. (TGT-44350)
* È stato risolto un problema che impediva ai clienti di modificare il [!UICONTROL Filtra criteri incompatibili] impostazione [!UICONTROL Recommendations] > [!UICONTROL Impostazioni]. (TGT-44398)
* È stato risolto un problema che causava la creazione di nuove richieste POST [!DNL Recommendations] feed con errore durante l’utilizzo di [!UICONTROL Classificazioni di Analytics] con suite di rapporti con punti nel loro nome. (TGT-44598)
* Collegamenti aggiornati nella [!DNL Target] Interfaccia utente per puntare al nuovo [Estensione Visual Editing Helper](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md). (TGT-44459)
* Protezione avanzata per impedire tentativi di falsificazione delle richieste lato server (SSRF) in [!DNL Recommendations] feed. (TGT-43769)
* È stato risolto un problema che impediva ai clienti di visualizzare in anteprima le immagini in [!DNL Recommendations] progetta se il nome dell&#39;immagine contiene [GB18030 caratteri](https://en.wikipedia.org/wiki/GB_18030){target=_blank}. (TGT-44614)
* È stato risolto un problema che causava [GB18030 caratteri](https://en.wikipedia.org/wiki/GB_18030){target=_blank} da evitare nel [!UICONTROL Modifiche] pannello durante la modifica [!UICONTROL Testo/HTML] di un’attività [!UICONTROL Esperienze] pagina. (TGT-44600)
* Sono state apportate diverse correzioni di localizzazione in tutta l’interfaccia utente di [!DNL Target].


## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://developer.adobe.com/target/implement/client-side/atjs/target-atjs-versions/){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |


## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
