---
keywords: app mobile;sdk app mobile;target app mobile;sdk target mobile;sdk app mobile;target in sdk
description: Scopri come aggiungere l’SDK di Mobile Services  Adobe alla tua app mobile.
title: Come si attiva Target nell'SDK Mobile  Adobe?
feature: Implement Mobile
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 81%

---


# Attivare Target nell’SDK{#enable-target-in-the-sdk}

Aggiungi l’SDK di Adobe Mobile Services all’app.

1. Se non hai installato l’SDK di Adobe Mobile Services nell’app, utilizza le credenziali di Google Analytics o di Experience Cloud e scarica l’SDK dal sito web di [Adobe Mobile Services](https://mobilemarketing.adobe.com).

1. Aggiungi l’SDK di Adobe Mobile Services all’app.

   È possibile trovare le istruzioni alla voce [Implementazione principale e Ciclo di durata](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/dev-qs.html).

1. Aggiungere il codice client, timeout e abilitare SSL.

   In Experience Cloud, apri Mobile Services, quindi vai su **[!UICONTROL Gestisci impostazioni app]** > **[!UICONTROL Opzioni Target SDK]**.

   Aggiungi il tuo codice client di Target e timeout. Il codice client è univoco per il tuo account o azienda. Il timeout è il lasso di tempo, per numero di secondi, in cui Target attenderà una risposta prima di mostrare il contenuto predefinito. Assicurati che l&#39;opzione **[!UICONTROL Usa HTTPS]** sia selezionata nella pagina Gestisci impostazioni app di Adobe Mobile Services. Se HTTPS non è abilitato, tutte le chiamate in iOS9+ saranno bloccate a meno che non inserire nell&#39;elenco Consentiti   il server di Target.

   ![](assets/mobile-clientcode.png)

1. Dopo aver creato/individuato l&#39;app, trova le impostazioni dell&#39;app e scarica l&#39;SDK desiderato.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Se non hai accesso all’interfaccia di mobile marketing, puoi apportare modifiche direttamente nel file di configurazione nel codice dell’app. Tuttavia, non sarà sincronizzato con la pagina delle impostazioni nell’interfaccia utente.

