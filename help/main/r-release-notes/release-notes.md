---
keywords: note sulla versione;nuove funzioni;versioni;aggiornamenti;aggiornamento;versione;miglioramenti;correzioni;correzioni di bug;aggiornamenti,aggiornamenti correnti
description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target], compresi SDK, API e librerie JavaScript.
landing-page-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
short-description: Scopri le nuove funzioni, i miglioramenti e le correzioni inclusi nella versione corrente di  [!DNL Adobe Target].
title: Cosa è incluso nella versione corrente?
feature: Release Notes
exl-id: 3ffead4f-113c-4153-b0b1-fc2aff710063
source-git-commit: fe370f57978ace161ca2ba2b9f6b11ae8f9b4cfa
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 19%

---

# Note sulla versione (corrente) di [!DNL Target]

Queste note sulla versione forniscono informazioni su funzioni, miglioramenti e correzioni per ciascuna versione di [!DNL Adobe Target Standard] e [!DNL Target Premium]. Sono inoltre incluse, ove applicabili, le note sulla versione di API di [!DNL Target], SDK, [!DNL Adobe Experience Platform Web SDK], at.js e altre modifiche alla piattaforma.

I codici dei problemi tra parentesi sono per uso interno di [!DNL Adobe].

## [!DNL Target Standard/Premium] 25.3.1 (3 marzo 2025)

Questa versione include le correzioni e gli aggiornamenti seguenti:

* Un pubblico combinato può includere sottogruppi, ciascuno contenente più tipi di pubblico. Questa versione ha risolto un problema che impediva la visualizzazione dei tipi di pubblico dei sottogruppi nella finestra di dialogo [!UICONTROL Rules]. (TGT-51813)
* È stato risolto un problema che causava la sostituzione di alcuni tipi di pubblico di esperienza con [!UICONTROL All Visitors] durante l&#39;apertura di attività precedenti. (TGT-51812)
* È stato risolto un problema che impediva la modifica di attività con tipi di pubblico per sola attività. (TGT-51807)
* È stato risolto un problema che impediva la modifica delle modifiche dell&#39;intestazione della pagina nell&#39;interfaccia utente [!DNL Target] aggiornata. (TGT-51797)
* È stato risolto un errore Null che si verificava durante la duplicazione di un’esperienza, l’eliminazione di un’altra esperienza e il tentativo di salvare l’attività. (TGT-51796)
* È stato risolto un problema che impediva la visualizzazione delle regole di esclusione del pubblico nel pannello informazioni del pubblico durante il passaggio [!UICONTROL Targeting] della creazione delle attività. (TGT-51579)
* Aggiornati messaggi di errore localizzati in coreano. (TGT-51701 e TGT-51699)

## [!DNL Target Standard/Premium] 25.2.3 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stato risolto un problema che impediva aggiornamenti delle attività dopo la versione 25.2.1 di [!DNL Target] per alcune attività. (TGT-51781)
* È stato risolto un problema che causava la rimozione di tutte le modifiche apportate al pubblico nello stato in seguito all&#39;annullamento del processo di creazione attività (selezione di [!UICONTROL Cancel] invece di [!UICONTROL Add Audience]). (TGT-51769 e TGT-51770)
* È stato risolto un problema che impediva il caricamento di [!UICONTROL Visual Experience Composer] (VEC) per alcune attività, in particolare quando veniva utilizzato un codice personalizzato.  Il problema ha portato il Compositore esperienza visivo a visualizzare una schermata vuota o a ripristinare la versione precedente dell&#39;interfaccia utente [!DNL Target]. (TGT-51758)
* È stato risolto un problema a causa del quale le modifiche venivano eliminate dopo la modifica della distribuzione delle pagine per i tipi di pubblico. (TGT-51756)
* È stato risolto un problema che causava la rimozione dalle attività di tutti i tipi di pubblico non metrici (pubblico di pagina e pubblico di esperienza) in seguito alla modifica di un tipo di metrica nella pagina [!UICONTROL Goals & Settings]. (TGT-51753)
* È stato risolto un problema per cui facendo clic su [!UICONTROL Cancel] durante la modifica di un&#39;attività, l&#39;interfaccia utente di Target passava a [!UICONTROL Activities List] invece che alla pagina [!UICONTROL Activity Details]. (TGT-51731)
* È stato risolto un problema che impediva ai clienti di scaricare i report tramite l&#39;opzione [!UICONTROL Export Reports to CSV]. (TGT-51708)
* È stato risolto un problema nel Compositore esperienza basato su moduli a causa del quale [!DNL Target Standard] clienti venivano erroneamente visualizzati per l&#39;utilizzo di [!UICONTROL Properties], una funzionalità [!DNL Target Premium]. (TGT-51678)
* È stato risolto un problema che impediva la visualizzazione degli attributi [!DNL Adobe Experience Platform] durante la creazione di nuove offerte. (TGT-51665)
* Tutti i filtri attivi per l&#39;inventario [!DNL Recommendations] sono stati spostati nella ricerca rapida, allineando l&#39;interfaccia utente con [!UICONTROL Catalog Search] invece della barra [!UICONTROL Filter]. (TGT-50723)

## at.js versione 2.11.7 (26 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* È stata corretta la registrazione di telemetria quando `localStorage` non è disponibile. La telemetria causava problemi ad alcuni clienti che avevano disabilitato `localStorage` nei loro browser.

Per informazioni su questa versione e sulle versioni precedenti di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank}.

## Target Standard/Premium 25.2.1 (martedì 17 febbraio 2025)

Questa versione include i seguenti aggiornamenti:

* Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Activities]
* Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

### Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Activities]

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente [!DNL Adobe Target] continua, è possibile annunciare la disponibilità generale dell&#39;interfaccia utente [!UICONTROL Activities] aggiornata.

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Activities]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Activities]. Le fasi successive aggiorneranno i clienti rimanenti.

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* [Generazione rapporti riprogettata](/help/main/administrating-target/reporting.md) per ottenere informazioni più approfondite sui risultati delle attività.
* [[!UICONTROL Updated Change Log]](/help/main/c-activities/change-log.md) pagina, sta ottenendo le informazioni da [[!DNL Audit Query API]](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/audit-logs/audit-api/overview){target=_blank} per approfondimenti in tempo reale.
* [Visualizzazioni elenco personalizzabili](/help/main/c-activities/activities.md) per una maggiore flessibilità tra le diverse esigenze del team.
* [Sono state migliorate le schermate di informazioni rapide e dettagli](/help/main/c-activities/activities.md) per un accesso più semplice alle informazioni.
* [Opzioni di ricerca e filtro persistenti alla sessione](/help/main/c-activities/activities.md).
* Completamente [ ha ricostruito [!UICONTROL Visual Editing Composer]](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) con il supporto per gli ultimi aggiornamenti di sicurezza dai provider del browser e una moderna interfaccia utente.

  Per informazioni sulle differenze tra il Compositore esperienza visivo aggiornato e la versione precedente, vedi:

   * [Modifiche al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/vec-changes.md)
   * [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md)

* [Aggiornamento [!DNL Chrome] dell&#39;estensione](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) che supporta Manifest V3 per una maggiore sicurezza e un migliore supporto per i cookie di prime parti.

![Aggiornamento attività](/help/main/r-release-notes/assets/activities-refresh.png)

### Aggiornamento dell&#39;interfaccia utente di [!DNL Recommendations]

Mentre il tentativo di modernizzazione dell&#39;interfaccia utente [!DNL Adobe Target] continua, è possibile annunciare la disponibilità generale dell&#39;interfaccia utente [!DNL Recommendations] aggiornata.

>[!NOTE]
>
>A partire dal 17 febbraio, i clienti avranno gradualmente accesso alla nuova interfaccia utente [!UICONTROL Recommendations]. Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase aggiornerà il gruppo iniziale di [!DNL Target] clienti alla nuova interfaccia utente [!UICONTROL Activities]. Le fasi successive aggiorneranno i clienti rimanenti.

In base al sistema di progettazione [!DNL Adobe Spectrum] più recente, l&#39;aggiornamento standardizza i modelli di progettazione precedentemente incoerenti, aggiungendo nuovi miglioramenti, ad esempio:

* La [ricerca nel catalogo prodotti](/help/main/c-recommendations/c-products/catalog-search.md) ora include un database aggiornato che consente la sincronizzazione in tempo reale dei prodotti.
* [!UICONTROL Recommendations] oggetti ([!UICONTROL Criteria], [!UICONTROL Designs], [!UICONTROL Collections] e [!UICONTROL Exclusions]) [creati tramite API sono ora disponibili nell&#39;interfaccia utente](/help/main/c-recommendations/c-recommendations-faq/recommendations-faq.md).
* [Le impostazioni dei consigli](/help/main/administrating-target/recommendations-settings.md) sono state consolidate nella sezione [!UICONTROL Administration].
* Visualizzazioni elenco personalizzabili per una maggiore flessibilità tra le diverse esigenze del team.
* Aggiornati editor di codice HTML e JSON con [evidenziazione della sintassi e numerazione delle righe](/help/main/c-experiences/c-manage-content/create-json-offer.md).
* Sono state migliorate le schermate di informazioni rapide e dettagli per un accesso più semplice alle informazioni.
* Opzioni di ricerca e filtro persistenti nella sessione.

![Aggiornamento dell&#39;interfaccia utente Recommendations](/help/main/r-release-notes/assets/recs-ui-refresh.png)

## Target Standard/Premium 25.1.1 (venerdì 9 gennaio 2025)

Questa versione include i seguenti aggiornamenti:

### Aggiornamento dell&#39;interfaccia utente di [!UICONTROL Offers Library]

Per migliorare l&#39;esperienza utente per [!DNL Adobe Target] utenti, questa versione aggiorna l&#39;interfaccia utente di [!UICONTROL Offers Library].

>[!NOTE]
>
>Per garantire un rollout senza soluzione di continuità per tutti i clienti, questa versione verrà implementata in fasi controllate. La prima fase ha aggiornato il gruppo iniziale di clienti Target alla nuova interfaccia utente Offerte. Le fasi successive aggiorneranno i clienti rimanenti.

Utilizzando il più recente sistema di progettazione [!DNL Adobe Spectrum], questo aggiornamento standardizza i modelli di progettazione incoerenti e introduce nuovi miglioramenti, tra cui i seguenti:

* **Gestione delle offerte in blocco**: seleziona ed elimina o sposta più offerte contemporaneamente.

* **[!UICONTROL Code Editor]aggiornamenti**: gli editor HTML e JSON sono stati aggiornati con l&#39;evidenziazione della sintassi e la numerazione delle righe.

* **Schede offerte migliorate**: informazioni rapide e schede dettagli migliorate per un accesso più semplice alle informazioni.

* **Ricerca e filtri persistenti**: aggiunge opzioni di ricerca e filtro persistenti nella sessione.

Per ulteriori informazioni, vedere [Offerte](/help/main/c-experiences/c-manage-content/manage-content.md) e i sottoarticoli in questa sezione. Tutti gli articoli sulle offerte in questa sezione sono stati aggiornati per riflettere queste modifiche dell’interfaccia utente.

Di seguito un breve video che evidenzia le modifiche apportate a questa versione:

![Video di aggiornamento dell&#39;interfaccia utente delle offerte](/help/main/r-release-notes/assets/offers-video-v2.gif)

## Ottimizzazione dell&#39;ambito [!DNL Adobe Experience Platform Web SDK] `__view__` (22 ottobre 2024)

Tra il 22 luglio 2024 e il 15 agosto 2024, il team [!DNL Target] ha ottimizzato l&#39;ambito `__view__`, migliorando la precisione dei rapporti sulle impression delle attività, sulle visite e sui visitatori. Questa ottimizzazione mira a acquisire automaticamente i dati di reporting per le proposte con rendering automatico e dovrebbe essere trasparente per la maggior parte degli account.

Questa ottimizzazione verrà abilitata per tutti i nuovi clienti di [!DNL Adobe Experience Platform Web SDK]. Tuttavia, l’ottimizzazione è disabilitata per i clienti che hanno eseguito la migrazione da at.js e non hanno seguito i passaggi di implementazione indicati di seguito. Esortiamo questi clienti a rivedere le loro implementazioni entro il 3 febbraio 2025. Dopo questa data, abiliteremo l’ottimizzazione per tutti i clienti. Il mancato riesame e adeguamento delle implementazioni entro tale data potrebbe influire sui rapporti, come indicato di seguito. Contatta [!DNL Adobe Customer Care] se devi confermare se l&#39;implementazione è interessata o se hai bisogno di più tempo per regolarla.

>[!IMPORTANT]
>
>Se non riesci a completare la revisione dell’implementazione e risolvere eventuali problemi entro il 3 febbraio 2025, puoi richiedere una proroga una tantum di sei mesi. Assicurati di inviare la richiesta entro il 31 gennaio 2025. Adobe rivedrà e deciderà sulla tua richiesta.

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

## Note aggiuntive e dettagli sulla versione

| Risorsa | Dettagli |
|--- |--- |
| [Note sulla versione: Adobe Target Platform Experience Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/release-notes.html?lang=it) | Dettagli sulle modifiche apportate a ogni versione di Platform Web SDK. |
| [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank} | Dettagli sulle modifiche in ogni versione della libreria JavaScript at.js [!DNL Adobe Target]. |

## Modifiche alla documentazione, precedenti note sulla versione e note sulla versione di Experience Cloud

Per informazioni aggiuntive, oltre alle note di ciascuna versione, consulta le seguenti risorse:

| Risorsa | Dettagli |
|--- |--- |
| [Modifiche alla documentazione](/help/main/r-release-notes/doc-change.md) | Consulta le informazioni dettagliate sugli aggiornamenti di questa guida che non sono inclusi nelle presenti note sulla versione. |
| [Note sulla versione per le versioni precedenti](/help/main/r-release-notes/release-notes-for-previous-releases.md). | Informazioni su nuove funzionalità e miglioramenti introdotti nelle versioni precedenti di Target Standard e Target Premium. |
| [Note sulla versione di Adobe Experience Cloud](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=it){target=_blank} | Ultime note sulla versione per le soluzioni Adobe Experience Cloud. |

## Informazioni in anteprima {#section_5D588F0415A2435B851A4D0113ACA3A0}

Le risorse seguenti contengono informazioni sulle funzionalità in arrivo con la prossima versione di Target.

| Risorsa | Dettagli |
|--- |--- |
| [Adobe Priority Product Update](https://www.adobe.com/subscription/priority-product-update.html){target=_blank} | Notifiche anticipate sui miglioramenti dei prodotti in arrivo per [!DNL Target] e altre soluzioni [!DNL Adobe Experience Cloud]. |
| [Note sulla versione di Target: prerelease](/help/main/r-release-notes/target-release-notes.md){target=_blank} | Informazioni sulle versioni di Target del mese corrente, incluse le informazioni prerelease. |
