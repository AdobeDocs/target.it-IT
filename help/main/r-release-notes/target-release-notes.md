---
keywords: note sulla versione;versioni;aggiornamenti;versione futura;miglioramenti;nuove funzioni;correzioni;aggiornamenti;prerelease;early access
description: Scopri le nuove funzioni, i miglioramenti e le correzioni, compresi SDK, API e librerie JavaScript, inclusi nella prossima versione di [!DNL Adobe Target].
title: Quali nuove funzioni e miglioramenti saranno inclusi nella prossima versione [!DNL Target] ?
feature: Release Notes
exl-id: f2783042-f6ee-4f73-b487-ede11d55d530
source-git-commit: cf00d2e43b0d0746e4369fcc7933a79f465c9549
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 21%

---

# Note sulla versione (prerelease) di [!DNL Target]

Questo articolo contiene informazioni prerelease per le prossime versioni di [!DNL Adobe Target], incluse SDK, API e librerie JavaScript.

**Ultimo aggiornamento: giovedì 11 dicembre 2024**

>[!NOTE]
>
>Date di rilascio, funzioni e altre informazioni sono soggette a modifica senza preavviso.
>
>Per visualizzare informazioni sulla versione corrente, consulta [Note sulla versione di Target](release-notes.md). Le informazioni su queste pagine potrebbero essere uguali, a seconda della tempistica delle release. I codici tra parentesi sono per uso interno di [!DNL Adobe].

## Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Offers Library] (9 gennaio 2025)

Per migliorare l&#39;esperienza utente per [!DNL Adobe Target] utenti, questa versione aggiorna l&#39;interfaccia utente di [!UICONTROL Offers Library]. Utilizzando il più recente sistema di progettazione [!DNL Adobe Spectrum], questo aggiornamento standardizza i modelli di progettazione incoerenti e introduce nuovi miglioramenti, tra cui i seguenti:

* **Gestione delle offerte in blocco**: seleziona ed elimina più offerte contemporaneamente.

* **[!UICONTROL Code Editor]aggiornamenti**: gli editor HTML e JSON sono stati aggiornati con l&#39;evidenziazione della sintassi e la numerazione delle righe.

* **Schede offerte migliorate**: informazioni rapide e schede dettagli migliorate per un accesso più semplice alle informazioni.

* **Ricerca e filtri persistenti**: aggiunge opzioni di ricerca e filtro persistenti nella sessione.

A partire dal 9 gennaio 2025, tutti i clienti [!DNL Target] avranno accesso alla nuova interfaccia utente, con la possibilità di tornare alla versione corrente dell&#39;interfaccia utente, se necessario.

Di seguito un breve video che evidenzia le modifiche apportate a questa versione:

![Video di aggiornamento dell&#39;interfaccia utente delle offerte](/help/main/r-release-notes/assets/offers-video-v2.gif)

## Ottimizzazione dell&#39;ambito [!DNL Adobe Experience Platform Web SDK] `__view__` (22 ottobre 2024)

Tra il 22 luglio 2024 e il 15 agosto 2024, il team [!DNL Target] ha ottimizzato l&#39;ambito `__view__`, migliorando la precisione dei rapporti sulle impression delle attività, sulle visite e sui visitatori. Questa ottimizzazione mira a acquisire automaticamente i dati di reporting per le proposte con rendering automatico e dovrebbe essere trasparente per la maggior parte degli account.

Questa ottimizzazione verrà abilitata per tutti i nuovi clienti di [!DNL Adobe Experience Platform Web SDK]. Tuttavia, l’ottimizzazione è disabilitata per i clienti che hanno eseguito la migrazione da at.js e non hanno seguito i passaggi di implementazione indicati di seguito. Esortiamo questi clienti a rivedere le loro implementazioni entro il 3 febbraio 2025. Dopo questa data, abiliteremo l’ottimizzazione per tutti i clienti. Il mancato riesame e adeguamento delle implementazioni entro tale data potrebbe influire sui rapporti, come indicato di seguito. Contatta [!DNL Adobe Customer Care] se devi confermare se l&#39;implementazione è interessata o se hai bisogno di più tempo per regolarla.

>[!IMPORTANT]
>
>Se non riesci a completare la revisione dell’implementazione e risolvere eventuali problemi entro il 3 febbraio 2025, puoi richiedere una proroga una tantum di sei mesi. Assicurati di inviare la richiesta entro il 31 gennaio 2025. Adobe esaminerà e deciderà in merito alla tua richiesta.

Per beneficiare di questa ottimizzazione in caso di rendering manuale della proposta, controlla [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} per assicurarti di inviare le notifiche dopo il rendering manuale delle esperienze o quando utilizzi il metodo `applyPropositions` (o l&#39;azione [!DNL Launch] corrispondente come helper) per eseguire il rendering delle esperienze.

Gli scenari più comuni in cui viene eseguito manualmente il rendering delle esperienze includono:

* Utilizzo delle offerte JSON
* Utilizzo di un ambito di decisione personalizzato in un&#39;attività creata in [[!UICONTROL Form-Based Experience Composer]](/help/main/c-experiences/form-experience-composer.md)
* Non utilizzare `renderDecisions: true` durante il recupero di un&#39;attività creata utilizzando [!UICONTROL Form-Based Experience Composer] che utilizza l&#39;ambito `__view__` globale

Se le notifiche non sono implementate come documentato in [Rendering del contenuto personalizzato](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} nella guida *Raccolta dati*, i dati di reporting potrebbero essere mancanti in [!DNL Target] e in [Analytics for Target reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In alcuni scenari, potresti notare una suddivisione del traffico errata perché i dati di reporting non vengono acquisiti. Oppure, in altri scenari, riportare ripetutamente lo stesso evento.

A seconda dell&#39;implementazione, verifica la presenza di [!DNL Analytics] e l&#39;impatto dei rapporti A4T.

[!DNL Platform Web SDK] supporta due tipi di implementazione per il rendering di esperienze e personalizzazioni:

* **Chiamata singola per la personalizzazione e la misurazione.**

  Inizialmente consigliato, l&#39;approccio a chiamata singola per [!DNL Platform Web SDK] verrà dichiarato obsoleto a favore dell&#39;approccio a chiamata divisa. Adobe consiglia a tutte le nuove implementazioni di utilizzare il nuovo approccio di split-call e consiglia ai clienti esistenti di passare anche loro al metodo di split-call.

  Se si continua a utilizzare l&#39;approccio a chiamata singola, è possibile che nei report [!DNL Analytics] vengano rilevate le seguenti modifiche impreviste:

   * Un tuffo nei mancati recapiti.
   * Gli hit A4T e [!UICONTROL Page View] non sono uniti tra loro, rendendo difficile eseguire determinati raggruppamenti e correlazioni dei rapporti A4T utilizzando [!DNL Analytics] eVar ed eventi.

* **Chiamate divise (note anche come eventi di inizio e fine pagina).**

  Questo tipo di implementazione è il nuovo [approccio di implementazione con chiamata divisa](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} consigliato da [!DNL Adobe]. Con questo approccio, la nuova ottimizzazione non influisce sui rapporti [!DNL Analytics] o A4T.

In caso di domande, contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

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
