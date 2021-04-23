---
keywords: server di tracciamento di analytics;A4T;debugger di Adobe Experience Cloud;debugger di Adobe Experience Platform;origine per la generazione rapporti;strumenti per sviluppatori
description: 'Scopri come specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for [!DNL Target] (A4T) se utilizzi una versione precedente di at.js o mbox.js. '
title: Come si utilizza un server di tracciamento di Analytics?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 20%

---

# Utilizzare un server di tracciamento di Analytics

Se utilizzi una versione precedente di at.js o mbox.js, devi specificare un server di tracciamento di Analytics per le attività che utilizzano [!DNL Adobe Analytics] per [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>Non è necessario specificare un server di tracciamento durante la creazione dell’attività se si utilizza mbox.js versione 61 (o successiva) o at.js versione 0.9.1 (o successiva). La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].
>
>Il team [!DNL Target] supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata. Per ulteriori informazioni, consulta [Dettagli sulle versioni di at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Per garantire che i dati da [!DNL Target] vadano nella posizione corretta in [!DNL Analytics], A4T richiede l’invio di un server di tracciamento Analytics in tutte le chiamate a Modstats da [!DNL Target]. Per le implementazioni che utilizzano più server di tracciamento, utilizza [!DNL Adobe Experience Platform Debugger] o gli strumenti per sviluppatori del browser per determinare il server di tracciamento corretto per l&#39;attività.

## Ottenere il server di tracciamento di Analytics utilizzando il debugger di Adobe Experience Platform

Il debugger deve essere visualizzato in una pagina in cui l&#39;attività viene distribuita per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui stai creando l&#39;attività, apri la cartella [!DNL Adobe Experience Platform Debugger].

   Se non hai installato il debugger, consulta [Introduzione al debugger Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Fai clic su **[!UICONTROL Analytics]** nel menu di navigazione a sinistra.

   Il server di tracciamento di Analytics si trova nella sezione [!UICONTROL Hostname] del debugger.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio su cui ti trovi, si tratta di un server di tracciamento di prime parti. Ad esempio, se utilizzi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di tracciamento di terze parti è in genere  `[company].sc.omtrdc.net` dove l&#39;azienda corrisponde al nome della tua azienda, ma termina sempre con  `sc.omtrdc.net`.
   * **Implementazioni** CNAME:  `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (secure). `stats.adobe.com` è un esempio di richiesta di prime parti CNAME per una pagina http (non protetta).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics come origine per la generazione di rapporti] per l&#39;attività affinché il campo [!UICONTROL Server di tracciamento] sia disponibile.

## Ottenere il server di tracciamento di Analytics utilizzando gli strumenti per sviluppatori del browser in uso

Gli Strumenti per sviluppatori devono essere visualizzati in una pagina in cui l’attività viene recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui stai creando l’attività, apri gli Strumenti per sviluppatori del browser (in Google Chrome, fai clic sui tre puntini di sospensione verticali nell’angolo in alto a destra > Altri strumenti > Strumenti per sviluppatori).

   ![Strumenti per sviluppatori Chrome](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Fare clic sulla scheda **[!UICONTROL Rete]**.

1. Filtra per `/ss,` per visualizzare le richieste di Analytics.

   ![Strumenti per sviluppatori Chrome con ricerca /ss](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Il server di tracciamento è il nome host della richiesta.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio su cui ti trovi, si tratta di un server di tracciamento di prime parti. Ad esempio, se utilizzi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di tracciamento di terze parti è in genere  `[company].sc.omtrdc.net` dove l&#39;azienda corrisponde al nome della tua azienda, ma termina sempre con  `sc.omtrdc.net`.
   * **Implementazioni** CNAME:  `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (secure). `stats.adobe.com` è un esempio di richiesta di prime parti CNAME per una pagina http (non protetta).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics come origine per la generazione di rapporti] per l&#39;attività affinché il campo [!UICONTROL Server di tracciamento] sia disponibile.
