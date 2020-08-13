---
keywords: implementation;api;profile;profile api settings;authentication token
description: Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.
title: Impostazioni API del profilo
feature: api
subtopic: Getting Started
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 64%

---


# Impostazioni API del profilo{#profile-api-settings}

Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.

[!DNL Adobe Target] crea e conserva un profilo per ogni singolo utente. This profile is stored on the [!DNL Target] edge cluster and is updated in real time after every visit, however, you can update a profile individually or in bulk via API.

Per una maggiore sicurezza, puoi scegliere che l’intestazione della richiesta di aggiornamento collettivo dell’API debba contenere un token di accesso valido. Users with [!UICONTROL Approver] permissions can generate and enable profile API authentication tokens.

**Per richiedere l’autenticazione e generare un token di accesso utilizzando l’interfaccia utente di Target:**

1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. In API **** profilo (Profile API **[!UICONTROL ) fate scorrere l’opzione]** Richiedi autenticazioneper passare alla posizione abilitata o disabilitata.

   ![](assets/profile_api_settings.png)

1. (Conditional) If you enabled authentication requirements, click **[!UICONTROL Generate New Pfofile Authentication Token]**.

   ![](assets/profile_api_settings_2.png)

   La scadenza del token è indicata nella casella [!UICONTROL Scade tra].

   >[!NOTE]
   >
   >Puoi anche generare un token di autenticazione profilo tramite API. Per ulteriori informazioni, vedi [Profili](https://developers.adobetarget.com/api/#profiles) sul [sito web per sviluppatori di Adobe Target](https://developers.adobetarget.com/).

1. Copia il token e includilo nell’intestazione della richiesta nel formato: &quot;Authorization&quot; : &quot;Bearer&quot;.

Click [!UICONTROL Generate New Profile Authentication Token] to regenerate the token as needed.

>[!IMPORTANT]
>
>Se si reimposta il token, le chiamate API che utilizzano il token attuale non riusciranno. Sarà necessario aggiornare tutti gli script o le applicazioni che utilizzano tale token.
