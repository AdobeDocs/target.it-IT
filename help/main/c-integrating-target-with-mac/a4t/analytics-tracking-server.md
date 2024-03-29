---
keywords: server di tracciamento di analytics;A4T;Adobe Experience Cloud debugger;Adobe Experience Platform debugger;origine per la generazione di rapporti;strumenti per sviluppatori
description: Scopri come specificare un server di tracciamento di Analytics per le attività che utilizzano Analytics per [!DNL Target] (A4T) se utilizzi una versione precedente di at.js.
title: Come si utilizza un server di tracciamento di Analytics?
feature: Analytics for Target (A4T)
exl-id: 8066d6a6-661e-428b-9d5c-18537a80fb43
source-git-commit: 2fc704a1779414a370ffd00ef5442fce36e7a5dd
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 21%

---

# Utilizza un [!DNL Analytics] server di monitoraggio

Se utilizzi una versione precedente di at.js, devi specificare un [!DNL Analytics] server di tracciamento per le attività che utilizzano [!DNL Adobe Analytics] per [!DNL Adobe Target] (A4T).

>[!NOTE]
>
>Se utilizzi la versione 0.9.1 (o successiva) di at.js, non devi specificare un server di tracciamento durante la creazione dell’attività. La libreria at.js invia automaticamente i valori del server di tracciamento a [!DNL Target]. Durante la creazione di attività, puoi lasciare vuoto il campo [!UICONTROL Server di monitoraggio] nella pagina [!UICONTROL Obiettivi e impostazioni].
>
>Il [!DNL Target] il team supporta sia at.js 1.*x* e at.js 2.*x*. Esegui l’aggiornamento alla versione più recente di una delle versioni principali di at.js per assicurarti di eseguire una versione supportata. Per ulteriori informazioni, consulta [Dettagli sulle versioni di at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/target-atjs-versions.html){target=_blank}.

Per garantire che i dati [!DNL Target] passa alla posizione corretta in [!DNL Analytics], A4T richiede un [!DNL Analytics] server di tracciamento da inviare in tutte le chiamate a Modstats da [!DNL Target]. Per le implementazioni che utilizzano più server di tracciamento, utilizza [!DNL Adobe Experience Platform Debugger] o i Developer Tools del browser per determinare il server di tracciamento corretto per l’attività.

## Ottieni [!DNL Analytics] server di tracciamento che utilizza [!DNL Adobe Experience Platform Debugger]

Il debugger deve essere visualizzato in una pagina in cui l’attività viene consegnata per assicurarti di selezionare il server di tracciamento corretto. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui stai creando l’attività, apri la sezione [!DNL Adobe Experience Platform Debugger].

   Se non hai installato il debugger, consulta [Panoramica di Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/platform-learn/data-collection/debugger/overview.html).

1. Clic **[!UICONTROL Analytics]** nel menu di navigazione sinistro.

   ![Immagine Screen_DebuggerTrackServ](assets/Screen_DebuggerTrackServ.png)

   Il [!DNL Analytics] il server di tracciamento si trova in [!UICONTROL Nome host] sezione del debugger.

   * **Server di tracciamento di prime parti**: se il nome host della richiesta corrisponde al dominio in cui ti trovi, si tratta di un server di tracciamento di prima parte. Ad esempio, se usi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server di tracciamento di terze parti**: un server di tracciamento di terze parti è in genere `[company].sc.omtrdc.net` dove l&#39;azienda è il nome dell&#39;azienda, ma termina sempre con `sc.omtrdc.net`.
   * **Implementazioni CNAME**: `sstats.adobe.com` è un esempio di server di tracciamento di prima parte CNAME per una richiesta https (secure). `stats.adobe.com` è un esempio di richiesta di prime parti CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics come origine per la generazione di rapporti] per la tua attività per [!UICONTROL Server di tracciamento] campo disponibile.

## Ottieni [!DNL Analytics] server di tracciamento utilizzando gli strumenti per sviluppatori del browser

Per essere certi di selezionare il server di tracciamento corretto, gli Strumenti per sviluppatori devono essere visualizzati in una pagina in cui l’attività viene consegnata. È inoltre possibile specificare un server di tracciamento predefinito per ogni account. Contatta l&#39;assistenza clienti per specificare o modificare l&#39;impostazione predefinita.

1. Dalla pagina in cui stai creando l’attività, apri gli Strumenti per sviluppatori del browser (in Google Chrome, fai clic sui tre puntini di sospensione verticali nell’angolo in alto a destra > Altri strumenti > Strumenti per sviluppatori).

   ![Strumenti per sviluppatori di Chrome](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-dev-tools.png)

1. Fai clic su **[!UICONTROL Rete]** scheda.

1. Filtra per `/ss,` per visualizzare [!DNL Analytics] richieste.

   ![Strumenti per sviluppatori di Chrome con /ss search](/help/main/c-integrating-target-with-mac/a4t/assets/chrome-search.png)

   Il server di tracciamento è il nome host della richiesta.

   * **Server di tracciamento di prime parti**: se il nome host della richiesta corrisponde al dominio in cui ti trovi, si tratta di un server di tracciamento di prima parte. Ad esempio, se usi `adobe.com`, `adobe.com` è il server di tracciamento di prime parti.
   * **Server di tracciamento di terze parti**: un server di tracciamento di terze parti è in genere `[company].sc.omtrdc.net` dove l&#39;azienda è il nome dell&#39;azienda, ma termina sempre con `sc.omtrdc.net`.
   * **Implementazioni CNAME**: `sstats.adobe.com` è un esempio di server di tracciamento di prima parte CNAME per una richiesta https (secure). `stats.adobe.com` è un esempio di richiesta di prime parti CNAME per una pagina http (non sicura).

1. Copiare l&#39;intero contenuto del campo.

1. Nella sezione **[!UICONTROL Impostazioni reporting]** della schermata **[!UICONTROL Obiettivo e impostazioni]** dell&#39;attività, incollare le informazioni del server di tracciamento nel campo **[!UICONTROL server di tracciamento]**.

   >[!NOTE]
   >
   >Seleziona [!UICONTROL Analytics come origine per la generazione di rapporti] per la tua attività per [!UICONTROL Server di tracciamento] campo disponibile.
