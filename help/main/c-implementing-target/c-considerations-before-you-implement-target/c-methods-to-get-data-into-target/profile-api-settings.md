---
keywords: implementazione;api;profilo;impostazioni API profilo;token di autenticazione
description: Scopri come configurare l’autenticazione per gli aggiornamenti batch tramite Adobe [!DNL Target] API e genera un token di autenticazione profilo.
title: Come si utilizzano le impostazioni API del profilo per attivare o disattivare gli aggiornamenti in batch?
feature: APIs/SDKs
role: Developer
exl-id: 6346e11b-0853-47f1-9706-69e8635a6f25
source-git-commit: c196b7e41101978ee029f93d5cd71c9b2d5b99f1
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 61%

---

# Impostazioni API del profilo

Abilita o disabilita l’autenticazione per gli aggiornamenti batch tramite [!DNL Adobe Target] API e genera un token di autenticazione profilo.

[!DNL Adobe Target] crea e conserva un profilo per ogni singolo utente. Questo profilo è memorizzato nel [!DNL Target] cluster edge ed è aggiornato in tempo reale dopo ogni visita; tuttavia, puoi aggiornare un profilo singolarmente o in blocco tramite API.

Per una maggiore sicurezza, puoi scegliere che l’intestazione della richiesta di aggiornamento collettivo dell’API debba contenere un token di accesso valido.

**Per richiedere l’autenticazione e generare un token di accesso utilizzando l’interfaccia utente di Target:**

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.
1. Sotto **[!UICONTROL API del profilo]** far scorrere **[!UICONTROL Richiedi autenticazione]** passa alla posizione abilitata o disabilitata.

   ![](assets/profile_api_settings.png)

1. (Condizionale) Se hai abilitato i requisiti di autenticazione, fai clic su **[!UICONTROL Genera nuovo token di autenticazione del profilo]**.

   ![](assets/profile_api_settings_2.png)

   La scadenza del token è indicata nella casella [!UICONTROL Scade tra].

   Per generare un token di autenticazione, è necessario disporre di una delle seguenti autorizzazioni utente:

   * Almeno il livello di autorizzazione [!UICONTROL Editor] (o [!UICONTROL Approvatore])

      Per ulteriori informazioni per i clienti [!DNL Target Standard], consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*. Per ulteriori informazioni per i clienti [!DNL Target Premium], consulta [Configurare le autorizzazioni aziendali](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Ruolo amministratore a livello di area di lavoro/profilo di prodotto

      Le aree di lavoro sono disponibili solo per i clienti [!DNL Target Premium]. Per ulteriori informazioni, consulta [Configurare le autorizzazioni aziendali](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md).

   * Diritti di amministrazione (autorizzazione Sysadmin) a livello di prodotto [!DNL Adobe Target]
   >[!NOTE]
   >
   >Puoi anche generare un token di autenticazione profilo tramite API. Per ulteriori informazioni, vedi [Profili](https://developers.adobetarget.com/api/#profiles) sul [sito web per sviluppatori di Adobe Target](https://developers.adobetarget.com/).

1. Copia il token e includilo nell’intestazione della richiesta nel formato: &quot;Authorization&quot; : &quot;Bearer&quot;.

Fai clic su [!UICONTROL Genera nuovo token di autenticazione del profilo] per generare il token in base alle esigenze.

>[!IMPORTANT]
>
>Se si reimposta il token, le chiamate API che utilizzano il token attuale non riusciranno. Sarà necessario aggiornare tutti gli script o le applicazioni che utilizzano tale token.
