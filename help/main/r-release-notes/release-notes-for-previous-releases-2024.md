---
keywords: Note sulla versione;note sulla versione prerelease;miglioramenti futuri;correzioni future;funzioni future;prossima versione
description: Visualizza un elenco di funzioni, miglioramenti e correzioni inclusi nelle versioni precedenti di Adobe Target.
title: Quali funzioni sono incluse nelle versioni precedenti?
feature: Release Notes
source-git-commit: 53cd01d2406b8a2f8560fe380ebb5044872e6711
workflow-type: tm+mt
source-wordcount: '1232'
ht-degree: 15%
---
# Note sulla versione per le versioni precedenti

Note sulle versioni precedenti di [!DNL Adobe Target], incluse le note di rilascio per [!DNL Target Standard/Premium], la piattaforma [!DNL Target] e le librerie JavaScript (at.js) di [!DNL Target].

Le note sulla versione sono elencate in ordine decrescente per mese e anno di rilascio.

>[!NOTE]
>
>Consulta [Note sulla versione di Target (corrente)](/help/main/r-release-notes/release-notes.md#reference_8FE40B43A5A34DDF8F26A53D55EE036A) per informazioni sulle versioni di Target del mese corrente (piattaforma e Target Standard/Premium).

## Note sulla versione - 2024

### Ottimizzazione dell&#39;ambito [!DNL Adobe Experience Platform Web SDK] `__view__` (22 ottobre 2024)

Tra il 22 luglio 2024 e il 15 agosto 2024, il team [!DNL Target] ha ottimizzato l&#39;ambito `__view__`, migliorando la precisione dei rapporti sulle impression delle attività, sulle visite e sui visitatori. Questa ottimizzazione mira a acquisire automaticamente i dati di reporting per le proposte con rendering automatico e dovrebbe essere trasparente per la maggior parte degli account.

Questa ottimizzazione verrà abilitata per tutti i nuovi clienti di [!DNL Adobe Experience Platform Web SDK]. Tuttavia, l’ottimizzazione è disabilitata per i clienti che hanno eseguito la migrazione da at.js e non hanno seguito i passaggi di implementazione indicati di seguito. Esortiamo questi clienti a rivedere le loro implementazioni entro il 3 febbraio 2025. Dopo questa data, abiliteremo l’ottimizzazione per tutti i clienti. Il mancato riesame e adeguamento delle implementazioni entro tale data potrebbe influire sui rapporti, come indicato di seguito. Contatta [!DNL Adobe Customer Care] se devi confermare se l&#39;implementazione è interessata o se hai bisogno di più tempo per regolarla.

>[!IMPORTANT]
>
>Se non riesci a completare la revisione dell’implementazione e risolvere eventuali problemi entro il 3 febbraio 2025, puoi richiedere una proroga una tantum di sei mesi. Assicurati di inviare la richiesta entro il 31 gennaio 2025. Adobe rivedrà e deciderà sulla tua richiesta.

Per beneficiare di questa ottimizzazione in caso di rendering manuale della proposta, controlla [[!DNL Platform Web SDK implementation]](https://experienceleague.adobe.com/it/docs/target-dev/developer/client-side/aep/aep-web-sdk-overview){target=_blank} per assicurarti di inviare le notifiche dopo il rendering manuale delle esperienze o quando utilizzi il metodo `applyPropositions` (o l&#39;azione [!DNL Launch] corrispondente come helper) per eseguire il rendering delle esperienze.

Gli scenari più comuni in cui viene eseguito manualmente il rendering delle esperienze includono:

* Utilizzo delle offerte JSON
* Utilizzo di un ambito di decisione personalizzato in un&#39;attività creata nel [[!UICONTROL Compositore esperienza basato su moduli]](/help/main/c-experiences/form-experience-composer.md)
* Non utilizzare `renderDecisions: true` durante il recupero di un&#39;attività creata con il Compositore esperienza basato su moduli  che utilizza l&#39;ambito `__view__` globale

Se le notifiche non sono implementate come documentato in [Rendering del contenuto personalizzato](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/personalization/rendering-personalization-content){target=_blank} nella guida *Raccolta dati*, i dati di reporting potrebbero essere mancanti in [!DNL Target] e in [Analytics for Target reporting](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). In alcuni scenari, potresti notare una suddivisione del traffico errata perché i dati di reporting non vengono acquisiti. Oppure, in altri scenari, riportare ripetutamente lo stesso evento.

A seconda dell&#39;implementazione, verifica la presenza di [!DNL Analytics] e l&#39;impatto dei rapporti A4T.

[!DNL Platform Web SDK] supporta due tipi di implementazione per il rendering di esperienze e personalizzazioni:

* **Chiamata singola per la personalizzazione e la misurazione.**

  Inizialmente consigliato, l&#39;approccio a chiamata singola per [!DNL Platform Web SDK] verrà dichiarato obsoleto a favore dell&#39;approccio a chiamata divisa. Adobe consiglia a tutte le nuove implementazioni di utilizzare il nuovo approccio di split-call e consiglia ai clienti esistenti di passare anche loro al metodo di split-call.

  Se si continua a utilizzare l&#39;approccio a chiamata singola, è possibile che nei report [!DNL Analytics] vengano rilevate le seguenti modifiche impreviste:

  * Un tuffo nei mancati recapiti.
  * Gli hit A4T e [!UICONTROL Visualizzazione pagina] non sono uniti tra loro, rendendo difficile eseguire determinati raggruppamenti e correlazioni dei rapporti A4T utilizzando [!DNL Analytics] eVar ed eventi.

* **Chiamate divise (note anche come eventi di inizio e fine pagina).**

  Questo tipo di implementazione è il nuovo [approccio di implementazione con chiamata divisa](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/use-cases/top-bottom-page-events){target=_blank} consigliato da [!DNL Adobe]. Con questo approccio, la nuova ottimizzazione non influisce sui rapporti [!DNL Analytics] o A4T.

In caso di domande, contatta l&#39;[Assistenza clienti Adobe](/help/main/cmp-resources-and-contact-information.md##reference_ACA3391A00EF467B87930A450050077C). (KB-2179)

### at.js versione 2.11.6 (29 settembre 2024)

* È stato risolto un problema che impediva a [!DNL Target] di funzionare correttamente con le offerte di reindirizzamento all&#39;interno del [!UICONTROL Compositore esperienza visivo] (VEC) o del [!UICONTROL Compositore esperienza basato su moduli].

Per ulteriori informazioni sulle versioni di at.js, consulta [Dettagli sulla versione di at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions){target=_blank} nella *Guida per gli sviluppatori di Adobe Target*.

### Generazione rapporti [!DNL Target] in [!DNL Adobe Customer Journey Analytics] (8 maggio 2024)

L&#39;integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/customer-journey-analytics){target=_blank} e [!DNL Target] offre potenti strumenti di analisi che consentono di risparmiare tempo per il programma di ottimizzazione.

I vantaggi principali dell’utilizzo di [!DNL Customer Journey Analytics] come origine di reporting per [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Gli addetti al marketing possono sfruttare le funzionalità di [!DNL Customer Journey Analytics], ad esempio il [pannello Sperimentazione](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, per analizzare ulteriormente la personalizzazione del sito Web.

Per ulteriori informazioni, consulta [Generazione rapporti di Target in Adobe Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).

### [!UICONTROL Estensione helper per Compositore esperienza visivo] (23 aprile 2024)

L&#39;estensione legacy [!DNL Target] Helper per il Compositore esperienza visivo è stata creata con Manifest V2. [!DNL Google] ha annunciato che non consentirà più le estensioni create utilizzando Manifest V2 a partire da giugno 2024. Per ulteriori informazioni, vedere [[!UICONTROL Estensione helper del Compositore esperienza visivo]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/vec-helper-browser-extension.md).

[!DNL Adobe] consiglia ai clienti di passare al più recente [estensione Helper per editing video](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) non appena possibile.

### Aggiornamenti per `Browser:iPad` e `Browser:iPhone` in [!UICONTROL Browser] attributi pubblico (30 aprile 2024)

| Aggiornamenti | Dettagli |
|--- |--- |
| [!UICONTROL Browser:iPad] e [!UICONTROL Browser:iPhone] aggiornati in [Attributi browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) utilizzati per la creazione di tipi di pubblico. | [!DNL Adobe Target] consente di [eseguire il targeting per uno qualsiasi degli attributi di categoria](/help/main/c-target/c-audiences/c-target-rules/target-rules.md), inclusi i visitatori che visitano la pagina utilizzando [opzioni browser o browser](/help/main/c-target/c-audiences/c-target-rules/browser.md) specifiche.<P>A partire da [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024), i tipi di pubblico incorporati creati utilizzando l&#39;interfaccia utente di Target, come `Browser:iPad` e `Browser:iPhone`, verranno aggiornati per eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] utilizzando `profile.mobile.deviceVendor`, `profile.mobile.isMobilePhone` e `profile.mobile.isTablet`.<P>Questo aggiornamento non richiede alcuna azione da parte dei clienti.<p><B>Importante</b>: per consentire ai clienti di eseguire il targeting corretto per [!DNL iPad] e [!DNL iPhone] negli script di profilo (e nei segmenti JavaScript), il cliente deve apportare modifiche manuali entro il **30 aprile 2024**. Per esempi di impostazioni alternative che devono essere modificate manualmente, vedere [Aggiornamenti per [!DNL iPad] e [!DNL iPhone] in [!UICONTROL Browser] attributi di pubblico](/help/main/c-target/c-audiences/c-target-rules/browser.md#updates). |

### [!UICONTROL Estensione Helper per editing video] (14 marzo 2024)

Questa versione contiene i miglioramenti e le correzioni seguenti per l&#39;estensione [[!DNL Adobe Experience Cloud Editing Helper]](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/visual-editing-helper-extension.md) per [!DNL Google Chrome]:

* È stato migliorato il meccanismo di caricamento dell’iFrame durante l’authoring nei siti web dei clienti.
* È stato risolto un problema che causava la duplicazione dei cookie da parte dell&#39;estensione durante l&#39;esecuzione dell&#39;authoring nel [!UICONTROL Compositore esperienza visivo].

### [!DNL Target] Standard/Premium 24.3.1 (4-6 marzo 2024)

Questa versione include i miglioramenti e le correzioni seguenti:

* È stata corretta la logica che calcola il numero di selettori univoci in un’attività. (TGT-47878)
* È stato risolto un problema che impediva la corretta visualizzazione delle attività [!UICONTROL Multivariate] (MVT) configurate con il reporting [!UICONTROL Analytics for Target] (A4T). (TGT-47490)
* È stato migliorato il messaggio di avviso visualizzato nel reporting quando un’esperienza senza traffico viene utilizzata come esperienza di controllo. (TGT-47537)
* Sono state aggiunte numerose correzioni di back-end e localizzazione.

### [!DNL Target] Standard/Premium 24.1.1 (22, 23 e 25 gennaio 2024)

Questa versione include i miglioramenti e le correzioni seguenti:

* [!UICONTROL Le attività di Analytics for Target] (A4T) con metriche dell&#39;obiettivo di ricavo non mostravano &quot;Ricavi&quot; come nome della colonna e la metrica Ricavi non veniva visualizzata nel formato ($) nei rapporti. Si trattava di un problema estetico che è stato risolto. (TGT-46995)
* È stato risolto un problema che impediva il corretto funzionamento della reportistica degli intervalli di date. (TGT-47396)
* È stato risolto un problema che causava la visualizzazione dello stato errato nella pagina [!UICONTROL Tutte le attività] dopo che i clienti avevano attivato o disattivato un&#39;attività utilizzando l&#39;icona [!UICONTROL Altre azioni]. (TGT-47367)
* È stato risolto un problema che impediva la visualizzazione del report [!UICONTROL Attributi importanti] per un singolo cliente. (TGT-47272)
* È stato risolto un problema che causava la visualizzazione di un messaggio di “payload non valido” quando un singolo cliente tentava di abilitare “Richiedi autenticazione”. (TGT-47195)
* Sono state aggiornate diverse stringhe localizzate nell’interfaccia utente di [!DNL Target].
