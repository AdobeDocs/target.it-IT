---
description: Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).
keywords: server di tracciamento di Analytics;A4T;debugger di Adobe Experience Cloud;fonte di reportistica
seo-description: Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).
seo-title: Utilizzare un server di tracciamento di Analytics
title: Utilizzare un server di tracciamento di Analytics
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Utilizzare un server di tracciamento di Analytics{#use-an-analytics-tracking-server}

Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

Per garantire che i dati di Target vadano nella posizione corretta in Analytics, A4T richiede che un server di tracciamento Analytics venga inviato in tutte le chiamate a Modstats da Target. Per le implementazioni che utilizzano più server di tracciamento è possibile utilizzare il debugger di Adobe Experience Cloud per determinare il server di tracciamento corretto per l&#39;attività.

Il debugger deve essere visualizzato in una pagina in cui l&#39;attività verrà recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui si sta creando l&#39;attività, apri il debugger di Adobe Experience Cloud. 

   Se il debugger non è stato installato, attenersi alle [istruzioni di installazione del debugger di Adobe](https://marketing.adobe.com/resources/help/en_US/sc/implement/debugger_install.html).

   ![](assets/Screen_DebuggerTrackServ.png)

   Il server di tracciamento Analytics si trova nella sezione immagine SiteCatalyst del debugger. Il campo è chiamato *Cookie proprietari* o *Cookie di terze parti* a seconda dell&#39;implementazione e il valore del server di tracciamento Analytics sarà in uno di questi formati:

   * (per le implementazioni CNAME)
   * (per le implementazioni non RDC)
   * (per l’implementazione RDC)
   *Società* rappresenta il nome della società di Analytics, *metriche* è un esempio di un valore CNAME, e *d1* è un esempio di un centro dati Analytics.
1. Copiare l&#39;intero contenuto del campo.
1. Nella sezione [!UICONTROL Impostazioni reporting] della schermata [!UICONTROL Obiettivo e impostazioni] dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >È necessario selezionare Adobe Analytics come origine dei rapporti dell’attività perché il campo server di tracciamento risulti disponibile.

