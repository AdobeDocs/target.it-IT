---
keywords: server di tracciamento di Analytics;A4T;debugger di Adobe Experience Cloud;fonte di reportistica
description: Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).
title: Utilizzare un server di tracciamento di Analytics
uuid: ad700b90-f409-496a-bc26-0f0367410a85
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Utilizzare un server di tracciamento di Analytics{#use-an-analytics-tracking-server}

Se utilizzi una versione precedente di at.js o mbox.js, è necessario specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics for Target (A4T).

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione di rapporti dell’attività e la versione 61 (o successiva) di mbox.js o la versione 0.9.1 (o successiva) di at.js, non è necessario specificare un server di tracciamento durante la creazione di attività. La libreria mbox.js o at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di tracciamento] nella pagina [!UICONTROL Obiettivi e impostazioni].

Per garantire che i dati di Target vadano nella posizione corretta in Analytics, A4T richiede che un server di tracciamento Analytics venga inviato in tutte le chiamate a Modstats da Target. Per le implementazioni che utilizzano più server di tracciamento è possibile utilizzare il debugger di Adobe Experience Cloud per determinare il server di tracciamento corretto per l'attività.

Il debugger deve essere visualizzato in una pagina in cui l'attività verrà recapitata per assicurarsi di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l'assistenza clienti per specificare o modificare l'impostazione predefinita.

1. Dalla pagina in cui si sta creando l'attività, apri il debugger di Adobe Experience Cloud.

   Se non hai installato il debugger, consulta [Installare Experience Cloud Debugger](https://docs.adobe.com/content/help/en/debugger/using/install-debugger.html).

   ![](assets/Screen_DebuggerTrackServ.png)

   Il server di tracciamento Analytics si trova nella sezione immagine SiteCatalyst del debugger. Il campo è chiamato *Cookie proprietari* o *Cookie di terze parti* a seconda dell'implementazione e il valore del server di tracciamento Analytics sarà in uno di questi formati:

   * (per le implementazioni CNAME)
   * (per le implementazioni non RDC)
   * (per l’implementazione RDC)
   *Società* rappresenta il nome della società di Analytics, *metriche* è un esempio di un valore CNAME, e *d1* è un esempio di un centro dati Analytics.
1. Copiare l'intero contenuto del campo.
1. Nella sezione [!UICONTROL Impostazioni reporting] della schermata [!UICONTROL Obiettivo e impostazioni] dell'attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >È necessario selezionare Adobe Analytics come origine dei rapporti dell’attività perché il campo server di tracciamento risulti disponibile.

