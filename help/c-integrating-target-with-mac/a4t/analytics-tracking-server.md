---
keywords: server di tracciamento analisi;A4T;Adobe Experience Cloud Debugger;Adobe Experience Platform Debugger;reporting source;developer tools
description: 'Scoprite come specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics per Target (A4T) se utilizzate una versione precedente di at.js o mbox.js. '
title: Come si utilizza un server di tracciamento di Analytics?
feature: Analytics for Target (A4T)
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 22%

---


# Utilizzare un server di tracciamento di Analytics

Se utilizzi una versione precedente di at.js o mbox.js, devi specificare un server di tracciamento Analytics per le attività che utilizzano [!DNL Analytics] per [!DNL Target] (A4T).

>[!NOTE]
>
>Se utilizzate [!DNL Analytics] come origine di reporting dell&#39;attività, non è necessario specificare un server di tracciamento durante la creazione dell&#39;attività se utilizzate mbox.js versione 61 (o successiva) o at.js versione 0.9.1 (o successiva). La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].
>
>Il team [!DNL Target] supporta entrambi at.js 1.*x* e at.js 2.*x*. Esegui l&#39;aggiornamento all&#39;aggiornamento più recente di una delle versioni principali di at.js per assicurarti che sia in esecuzione una versione supportata. Per ulteriori informazioni, vedere [at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md).

Per garantire che i dati da [!DNL Target] vadano nella posizione corretta in [!DNL Analytics], A4T richiede l&#39;invio di un server di tracciamento di Analytics in tutte le chiamate a Modstats da [!DNL Target]. Per le implementazioni che utilizzano più server di tracciamento è possibile utilizzare gli [!DNL Adobe Experience Platform Debugger] o gli strumenti per sviluppatori del browser per determinare il server di tracciamento corretto per l&#39;attività.

## Ottenere il server di tracciamento di Analytics tramite Adobe Experience Platform Debugger

Il debugger deve essere visualizzato in una pagina in cui l&#39;attività verrà recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui state creando l&#39;attività, aprite la cartella [!DNL Adobe Experience Platform Debugger].

   Se il debugger non è installato, vedere [Introduzione a Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/tutorials/data-ingestion/web-sdk/introduction-to-the-experience-platform-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

1. Fate clic su **[!UICONTROL Analytics]** nel menu di navigazione a sinistra.

   Il server di tracciamento di Analytics si trova nella sezione [!UICONTROL Nome host] del debugger.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio in uso, si tratta di un server di tracciamento di prime parti. Ad esempio, se vi trovate su `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di monitoraggio di terze parti è in genere  `[company].sc.omtrdc.net` dove la società corrisponde al nome della società, ma termina sempre  `sc.omtrdc.net`.
   * **Implementazioni** CNAME:  `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di richiesta di prima parte CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >È necessario selezionare [!UICONTROL Analytics come origine di reporting] per l&#39;attività affinché il campo [!UICONTROL Server di tracciamento] sia disponibile.

## Ottenere il server di tracciamento di Analytics utilizzando gli strumenti per sviluppatori del browser in uso

Gli strumenti per sviluppatori devono essere visualizzati in una pagina in cui l&#39;attività verrà consegnata per essere certi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui state creando l&#39;attività, aprite gli strumenti per sviluppatori del browser (in Google Chrome, fate clic sulle tre ellissi verticali nell&#39;angolo in alto a destra > Altri strumenti > Strumenti per sviluppatori).

   ![Strumenti di sviluppo Chrome](/help/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Fare clic sulla scheda **[!UICONTROL Rete]**.

1. Filtro per `/ss,` per visualizzare le richieste di Analytics.

   ![Strumenti di sviluppo Chrome con ricerca /ss](/help/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Il server di tracciamento è il nome host della richiesta.

   * **Server** di tracciamento di prime parti: Se il nome host della richiesta corrisponde al dominio in uso, si tratta di un server di tracciamento di prime parti. Ad esempio, se vi trovate su `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server** di tracciamento di terze parti: Un server di monitoraggio di terze parti è in genere  `[company].sc.omtrdc.net` dove la società corrisponde al nome della società, ma termina sempre  `sc.omtrdc.net`.
   * **Implementazioni** CNAME:  `sstats.adobe.com` è un esempio di server di tracciamento di prime parti CNAME per una richiesta https (sicura). `stats.adobe.com` è un esempio di richiesta di prima parte CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >È necessario selezionare [!UICONTROL Analytics come origine di reporting] per l&#39;attività affinché il campo [!UICONTROL Server di tracciamento] sia disponibile.

