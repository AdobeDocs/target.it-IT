---
keywords: server di tracciamento di analytics;A4T;Adobe Experience Cloud debugger;Adobe Experience Platform debugger;origine per la generazione di rapporti;strumenti per sviluppatori
description: Scopri come specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for [!DNL Target] (A4T) se utilizzi una versione precedente di at.js.
title: Come si utilizza un server di tracciamento di Analytics?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 14%

---

# Usa un server di tracciamento [!DNL Analytics]

Se utilizzi una versione precedente di at.js, devi specificare un server di tracciamento [!DNL Analytics] per le attività che utilizzano [!DNL Adobe Analytics] per [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>Se utilizzi la versione 0.9.1 (o successiva) di at.js, non devi specificare un server di tracciamento durante la creazione dell’attività. La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione dell&#39;attività, è possibile lasciare vuoto il campo [!UICONTROL Tracking Server] nella pagina [!UICONTROL Goals & Settings].
>
>Il team [!DNL Target] supporta sia at.js 1.*x* che in at.js 2.*x*. Esegui l’aggiornamento alla versione più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata. Per ulteriori informazioni, consulta [Dettagli versione at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html?lang=it){target=_blank}.

Per garantire che i dati di [!DNL Target] vadano nella posizione corretta in [!DNL Analytics], A4T richiede che un server di tracciamento [!DNL Analytics] sia inviato in tutte le chiamate a Modstats da [!DNL Target]. Per le implementazioni che utilizzano più server di tracciamento, utilizzare [!DNL Adobe Experience Platform Debugger] o i Developer Tools del browser per determinare il server di tracciamento corretto per l&#39;attività.

## Ottieni il server di tracciamento [!DNL Analytics] utilizzando [!DNL Adobe Experience Platform Debugger]

Il debugger deve essere visualizzato in una pagina in cui l’attività viene consegnata per assicurarti di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui si sta creando l&#39;attività, aprire [!DNL Adobe Experience Platform Debugger].

   Se non hai installato il debugger, vedi [Panoramica Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. Fare clic su **[!UICONTROL Analytics]** nel menu di navigazione a sinistra.

   ![Immagine Screen_DebuggerTrackServ](assets/Screen_DebuggerTrackServ.png)

   Il server di tracciamento [!DNL Analytics] si trova nella sezione [!UICONTROL Hostname] del debugger.

   * **Server di tracciamento di prima parte**: se il nome host della richiesta corrisponde al dominio in cui ti trovi, è un server di tracciamento di prima parte. Ad esempio, se usi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server di monitoraggio di terze parti**: un server di monitoraggio di terze parti è in genere `[company].sc.omtrdc.net` dove società è il nome della società, ma termina sempre in `sc.omtrdc.net`.
   * **Implementazioni CNAME**: `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di una richiesta di prime parti CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Reporting Settings]** della schermata **[!UICONTROL Goal & Settings]** dell&#39;attività, incollare le informazioni sul server di tracciamento nel campo **[!UICONTROL Tracking Server]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics as the Reporting Source] per la tua attività affinché il campo [!UICONTROL Tracking Server] sia disponibile.

## Ottieni il server di monitoraggio [!DNL Analytics] utilizzando gli strumenti per sviluppatori del browser

Per essere certi di selezionare il server di tracciamento corretto, gli Strumenti per sviluppatori devono essere visualizzati in una pagina in cui l’attività viene consegnata. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui stai creando l’attività, apri gli Strumenti per sviluppatori del browser (in Google Chrome, fai clic sui tre puntini di sospensione verticali nell’angolo in alto a destra > Altri strumenti > Strumenti per sviluppatori).

   ![Strumenti per sviluppatori Chrome](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Fare clic sulla scheda **[!UICONTROL Network]**.

1. Filtra per `/ss,` per visualizzare le richieste [!DNL Analytics].

   ![Strumenti per sviluppatori Chrome con /ss search](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Il server di tracciamento è il nome host della richiesta.

   * **Server di tracciamento di prima parte**: se il nome host della richiesta corrisponde al dominio in cui ti trovi, è un server di tracciamento di prima parte. Ad esempio, se usi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server di monitoraggio di terze parti**: un server di monitoraggio di terze parti è in genere `[company].sc.omtrdc.net` dove società è il nome della società, ma termina sempre in `sc.omtrdc.net`.
   * **Implementazioni CNAME**: `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di una richiesta di prime parti CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Reporting Settings]** della schermata **[!UICONTROL Goal & Settings]** dell&#39;attività, incollare le informazioni sul server di tracciamento nel campo **[!UICONTROL Tracking Server]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics as the Reporting Source] per la tua attività affinché il campo [!UICONTROL Tracking Server] sia disponibile.
