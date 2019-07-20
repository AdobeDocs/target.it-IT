---
description: Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.
keywords: implementazione;api;profilo;impostazioni API profilo
seo-description: Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.
seo-title: Impostazioni API del profilo
solution: Target
subtopic: Introduzione
title: Impostazioni API del profilo
topic: Standard
uuid: 481b4a14-f10f-47cd-988d-9e6b8c4d5c00
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Impostazioni API del profilo{#profile-api-settings}

Puoi abilitare o disabilitare l’autenticazione per gli aggiornamenti collettivi tramite API e generare un token di autenticazione del profilo.

Adobe Target crea e conserva un profilo per ogni singolo utente. Questo profilo è memorizzato sul cluster Edge di Target e viene aggiornato in tempo reale dopo ogni visita. Tuttavia tramite le API puoi aggiornare i profili singolarmente o in modalità collettiva.

Per una maggiore sicurezza, puoi scegliere che l’intestazione della richiesta di aggiornamento collettivo dell’API debba contenere un token di accesso valido. Gli utenti con ruolo di approvatore possono generare e attivare i token di autenticazione dell’API per i profili.

**Per richiedere l’autenticazione e generare un token di accesso utilizzando l’interfaccia utente di Target:**

1. Fai clic su **[!UICONTROL Configurazione]** &gt; **[!UICONTROL Implementazione]**.
1. In **[!UICONTROL Impostazioni API profilo]**, utilizza l’elenco a discesa **[!UICONTROL Richiedi autenticazione]** per abilitare o disabilitare i requisiti di autenticazione.

   ![](assets/profile_api_settings.png)

1. (Condizionale) Se hai abilitato i requisiti di autenticazione, fai clic su **[!UICONTROL Genera token di autenticazione profilo]**.

   ![](assets/profile_api_settings_2.png)

   La scadenza del token è indicata nella casella [!UICONTROL Scade tra].

   >[!NOTE]
   >
   >Puoi anche generare un token di autenticazione profilo tramite API. Per ulteriori informazioni, vedi [Profili](https://developers.adobetarget.com/api/#profiles) sul [sito web per sviluppatori di Adobe Target](https://developers.adobetarget.com/).

1. Copia il token e includilo nell’intestazione della richiesta nel formato: "Authorization" : "Bearer".

Fai clic su [!UICONTROL Rigenera token di autorizzazione profilo] per rigenerare il token quando necessario.

>[!IMPORTANT]
>
>Se si reimposta il token, le chiamate API che utilizzano il token attuale non riusciranno. Sarà necessario aggiornare tutti gli script o le applicazioni che utilizzano tale token.

