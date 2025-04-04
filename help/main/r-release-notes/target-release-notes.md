---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: 0618d39fc5966c64cceea8f5bcccb625fc243ebb
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 38%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: giovedì 2 aprile 2025**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamento delle autorizzazioni di Target (22 aprile 2025)

Questo aggiornamento futuro migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.

A decorrere dal 22 aprile 2025, solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [!UICONTROL Administration], indipendentemente dai loro ruoli nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Per ulteriori informazioni, vedere [Amministrare Target](/help/main/administrating-target/start-target.md).

## [!DNL Target Standard/Premium] 25.4.1 (2 aprile 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* È stato risolto un problema che causava la scomparsa dei tipi di pubblico dell’esperienza dalle attività di. (TGT-52003)
* È stato risolto un problema che causava elementi imprevisti durante la consegna. (TGT-52011)
* È stato risolto un problema che impediva ai clienti di visualizzare il pubblico nel grafico di targeting nella pagina Ove[!UICONTROL r]view e durante la modifica dell&#39;attività. (TGT-52050)
* È stato risolto un problema che impediva ai clienti di riordinare le esperienze in ordine di priorità nelle attività [!UICONTROL Experience Targeting] (XT). (TGT-52054)
* È stato risolto un problema che causava un rendering errato quando si annullavano le modifiche allo stile del testo. (TGT-51876)
* È stato risolto un problema a causa del quale durante la modifica di un&#39;offerta di reindirizzamento, [!DNL Target] rimuove anche i selettori [!UICONTROL ClickTrack] associati a tale offerta. (TGT-51936)
* È stato risolto un problema che causava il salvataggio errato del selettore da parte di [!DNL Target] durante l&#39;annullamento di [!UICONTROL ClickTrack]. (TGT-51937)
* È stato risolto un problema che causava un errore di nome non valido dopo l&#39;apertura e la chiusura del selettore mbox sulla pagina [!UICONTROL Goals & Settings] senza apportare modifiche. (TGT-51983)
* È stato risolto un problema che impediva la modifica delle offerte ad hoc create nell&#39;interfaccia utente legacy di [!DNL Target]. (TGT-51984)
* È stato risolto un problema che bloccava le attività di modifica con offerte ad hoc contenenti codice personalizzato. (TGT-51995)
* È stato risolto un problema che causava la visualizzazione delle regole di esclusione come regole di inclusione durante la modifica delle definizioni di pubblico combinato. (TGT-51999)
* È stato risolto un problema che impediva la corretta visualizzazione del codice personalizzato durante la modifica dell’esperienza. (TGT-52005)
* È stato risolto un problema che rendeva l&#39;opzione [!UICONTROL Insert Before] non disponibile per l&#39;inserimento di contenuto prima della barra di navigazione. (TGT-52031)
* È stato risolto un problema che impediva la corretta evidenziazione dell’esperienza predefinita nel reporting. (TGT-51716)
* È stato risolto un problema che attivava un messaggio `default message [Invalid optionLocalIds: xx]]` durante la creazione di un&#39;attività. (TGT-52038)

<!-- 
## [!DNL Target Standard/Premium] 24.10.2 (October 21, 2024)

This release contains the following fixes:

* Fixed an issue that prevented [!UICONTROL Recommendations] activities from loading in [!UICONTROL Compose] and [!UICONTROL Browse] modes. (TGT-50709)
* Fixed an issue with the new [[!DNL Google Chrome] [!UICONTROL Visual Editing Helper] extension](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) that caused a redirect from the [!UICONTROL Visual Experience Composer] (VEC) to the [!UICONTROL Activities Library] after clicking Cancel. Before this fix, customers needed to refresh the [!UICONTROL Activities Library] before being able to create new activities. (TGT-49980)-->

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js di [!DNL Adobe Target]. |

## Informazioni in anteprima {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

Per ricevere notifiche prioritarie sui prossimi miglioramenti per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud], iscriviti ad [!DNL Adobe Priority Product Update]:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)
