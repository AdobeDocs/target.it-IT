---
keywords: app mobile;sdk app mobile;target app mobile;sdk target mobile;sdk app mobile;target in sdk
description: Scopri come aggiungere Adobe Mobile Services SDK alla tua app mobile.
title: Come si attivano [!DNL Target] nell’SDK di Adobe Mobile?
feature: Implement Mobile
role: Developer
exl-id: c34bd50c-e17f-4dfb-8470-8f4c8639ee9f
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 80%

---

# Abilita [!DNL Target] nell’SDK

Aggiungi l’SDK di Adobe Mobile Services all’app.

1. Se non hai installato l’SDK di Adobe Mobile Services nell’app, utilizza le credenziali di Google Analytics o di Experience Cloud e scarica l’SDK dal sito web di [Adobe Mobile Services](https://mobilemarketing.adobe.com/).

1. Aggiungi l’SDK di Adobe Mobile Services all’app.

   È possibile trovare le istruzioni alla voce [Implementazione principale e Ciclo di durata](https://experienceleague.adobe.com/docs/mobile-services/ios/getting-started-ios/dev-qs.html).

1. Aggiungere il codice client, timeout e abilitare SSL.

   In Experience Cloud, apri Mobile Services, quindi vai su **[!UICONTROL Gestisci impostazioni app]** > **[!UICONTROL Opzioni Target SDK]**.

   Aggiungi il tuo codice client di Target e timeout. Il codice client è univoco per il tuo account o azienda. Il timeout è il lasso di tempo, per numero di secondi, in cui Target attenderà una risposta prima di mostrare il contenuto predefinito. Assicurati che l&#39;opzione **[!UICONTROL Usa HTTPS]** sia selezionata nella pagina Gestisci impostazioni app di Adobe Mobile Services. Se HTTPS non è abilitato, tutte le chiamate in iOS9+ verranno bloccate a meno che non si inserire nell&#39;elenco Consentiti il server di Target.

   ![](assets/mobile-clientcode.png)

1. Dopo aver creato/individuato l&#39;app, trova le impostazioni dell&#39;app e scarica l&#39;SDK desiderato.

   ![](assets/download-sdk.png)

>[!IMPORTANT]
>
> Se non hai accesso all’interfaccia di mobile marketing, puoi apportare modifiche direttamente nel file di configurazione nel codice dell’app. Tuttavia, non sarà sincronizzato con la pagina delle impostazioni nell’interfaccia utente.