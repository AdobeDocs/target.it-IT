---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;Adobe Experience Platform debugger;reporting source;developer tools
description: Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).
title: Utilizzare un server di tracciamento di Analytics
feature: a4t general
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 08ad3291a1f981fbc3963ce403bf19849c358b97
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 27%

---


# Utilizzare un server di tracciamento di Analytics

If you are using an older version of at.js or mbox.js, you must specify an Analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].
>
>Il [!DNL Target] team supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l&#39;aggiornamento all&#39;aggiornamento più recente di una delle versioni principali di at.js per assicurarti che sia in esecuzione una versione supportata. For more information, see [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an Analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Platform Debugger] or your browser&#39;s Developer Tools to determine the correct tracking server for your activity.

## Ottenere il server di tracciamento di Analytics tramite Adobe Experience Platform Debugger

Il debugger deve essere visualizzato in una pagina in cui l&#39;attività verrà recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui state creando l&#39;attività, aprite la pagina [!DNL Adobe Experience Platform Debugger].

   Se il debugger non è installato, vedere [Introduzione a Adobe Experience Platform Debugger](https://docs.adobe.com/content/help/en/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Fate clic su **[!UICONTROL Analytics]** nel menu di navigazione a sinistra.

   The Analytics tracking server is found in the [!UICONTROL Hostname] section of the debugger.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio in uso, si tratta di un server di tracciamento di prime parti. Ad esempio, se utilizzi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di monitoraggio di terze parti è in genere `[company].sc.omtrdc.net` il luogo in cui la società corrisponde al nome della società, ma termina sempre `sc.omtrdc.net`.
   * **Implementazioni** CNAME: `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di richiesta di prima parte CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

## Ottenere il server di tracciamento di Analytics utilizzando gli strumenti per sviluppatori del browser in uso

Gli strumenti per sviluppatori devono essere visualizzati in una pagina in cui l&#39;attività verrà consegnata per essere certi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui state creando l&#39;attività, aprite gli strumenti per sviluppatori del browser (in Google Chrome, fate clic sulle tre ellissi verticali nell&#39;angolo in alto a destra > Altri strumenti > Strumenti per sviluppatori).

   ![Strumenti di sviluppo Chrome](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Click the **[!UICONTROL Network]** tab.

1. Filtrare per `/ss,` visualizzare le richieste di Analytics.

   ![Strumenti di sviluppo Chrome con ricerca /ss](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Il server di tracciamento è il nome host della richiesta.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio in uso, si tratta di un server di tracciamento di prime parti. Ad esempio, se utilizzi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di monitoraggio di terze parti è in genere `[company].sc.omtrdc.net` il luogo in cui la società corrisponde al nome della società, ma termina sempre `sc.omtrdc.net`.
   * **Implementazioni** CNAME: `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di richiesta di prima parte CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

