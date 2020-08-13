---
keywords: analytics tracking server;A4T;Adobe Experience Cloud debugger;reporting source
description: Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).
title: Utilizzare un server di tracciamento di Analytics
feature: a4t general
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 53%

---


# Utilizzare un server di tracciamento di Analytics{#use-an-analytics-tracking-server}

If you are using an older version of at.js or mbox.js, you must specify an analytics tracking server for activities that use [!DNL Analytics] for [!DNL Target] (A4T).

>[!NOTE]
>
>If you use [!DNL Analytics] as your activity&#39;s reporting source, you do not need to specify a tracking server during activity creation if you are using mbox.js version 61 (or later) or at.js version 0.9.1 (or later). La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

To ensure that data from [!DNL Target] goes to the correct location in [!DNL Analytics], A4T requires an analytics tracking server to be sent in all calls to Modstats from [!DNL Target]. For implementations using multiple tracking servers you can use the [!DNL Adobe Experience Cloud Debugger] to determine the correct tracking server for your activity.

Il debugger deve essere visualizzato in una pagina in cui l&#39;attività verrà recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui state creando l&#39;attività, aprite la pagina [!DNL Adobe Experience Cloud Debugger].

   Se non avete installato il debugger, consultate [Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/install-debugger.html)di installazione.

   ![](assets/Screen_DebuggerTrackServ.png)

   The analytics tracking server is found in the [!UICONTROL SiteCatalyst Image] section of the debugger. Il campo è chiamato *Cookie proprietari* o *Cookie di terze parti* a seconda dell&#39;implementazione e il valore del server di tracciamento sarà in uno di questi formati:[!DNL Analytics]

   * (per le implementazioni CNAME)
   * (per le implementazioni non RDC)
   * (per l’implementazione RDC)

   *Società*[!DNL Analytics] rappresenta il nome della società di , *metriche* è un esempio di un valore CNAME, e *d1* è un esempio di un centro dati [!DNL Analytics]
1. Copiare l&#39;intero contenuto del campo.
1. Nella sezione [!UICONTROL Impostazioni reporting] della schermata [!UICONTROL Obiettivo e impostazioni] dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >You must select [!UICONTROL Analytics as the Reporting Source] for your activity for the [!UICONTROL Tracking Server] field to be available.

