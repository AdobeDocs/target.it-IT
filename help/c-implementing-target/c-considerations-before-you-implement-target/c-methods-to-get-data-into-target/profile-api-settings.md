---
keywords: implementation;api;profile;profile api settings;authentication token
description: Abilitare o disabilitare l'autenticazione per gli aggiornamenti batch tramite  API Adobe Target e generare un token di autenticazione del profilo.
title: Impostazioni API profilo in  Adobe Target
feature: APIs/SDKs
translation-type: tm+mt
source-git-commit: 6bb75e3b818a71af323614d9150e50e3e9f611b7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 40%

---


# Impostazioni API del profilo

Abilitare o disabilitare l&#39;autenticazione per gli aggiornamenti batch tramite le API [!DNL Adobe Target] e generare un token di autenticazione del profilo.

[!DNL Adobe Target] crea e conserva un profilo per ogni singolo utente. Questo profilo viene memorizzato nel cluster periferico [!DNL Target] e aggiornato in tempo reale dopo ogni visita; tuttavia, potete aggiornare un profilo singolarmente o in blocco tramite API.

Per una maggiore sicurezza, puoi scegliere che l’intestazione della richiesta di aggiornamento collettivo dell’API debba contenere un token di accesso valido.

**Per richiedere l’autenticazione e generare un token di accesso utilizzando l’interfaccia utente di Target:**

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. In **[!UICONTROL Profile API]** (API profilo), fate scorrere il cursore **[!UICONTROL Richiedi autenticazione]** per passare alla posizione abilitata o disabilitata.

   ![](assets/profile_api_settings.png)

1. (Condizionale) Se avete attivato i requisiti di autenticazione, fate clic su **[!UICONTROL Genera nuovo token di autenticazione profilo]**.

   ![](assets/profile_api_settings_2.png)

   La scadenza del token è indicata nella casella [!UICONTROL Scade tra].

   Per generare un token di autenticazione è necessario disporre di una delle seguenti autorizzazioni utente:

   * Autorizzazione di almeno [!UICONTROL Editor] (o [!UICONTROL Approver])

      Per ulteriori informazioni per i clienti [!DNL Target Standard], vedere [Specificare ruoli e autorizzazioni](/help/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*. Per ulteriori informazioni per i clienti [!DNL Target Premium], vedere [Configurare le autorizzazioni aziendali](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Ruolo amministratore nell’area di lavoro/a livello di profilo di prodotto

      Le aree di lavoro sono disponibili solo per i clienti [!DNL Target Premium]. Per ulteriori informazioni, vedere [Configurare le autorizzazioni aziendali](/help/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Diritti di amministratore (autorizzazione Sysadmin) a livello di prodotto [!DNL Adobe Target]
   >[!NOTE]
   >
   >Puoi anche generare un token di autenticazione profilo tramite API. Per ulteriori informazioni, vedi [Profili](https://developers.adobetarget.com/api/#profiles) sul [sito web per sviluppatori di Adobe Target](https://developers.adobetarget.com/).

1. Copia il token e includilo nell’intestazione della richiesta nel formato: &quot;Authorization&quot; : &quot;Bearer&quot;.

Fare clic su [!UICONTROL Genera nuovo token di autenticazione profilo] per rigenerare il token in base alle esigenze.

>[!IMPORTANT]
>
>Se si reimposta il token, le chiamate API che utilizzano il token attuale non riusciranno. Sarà necessario aggiornare tutti gli script o le applicazioni che utilizzano tale token.
