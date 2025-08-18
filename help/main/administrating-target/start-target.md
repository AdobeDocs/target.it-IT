---
keywords: Amministrazione;ruolo approvatore;approvatore
description: Esegui le prime attività [!DNL Adobe Target] che gli amministratori devono eseguire dopo aver ricevuto l'invito via e-mail a [!DNL Adobe Experience Cloud].
title: Dove Si Inizia Ad Amministrare  [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
source-git-commit: 614fd89c9746ce55f502debd5b689c34de400ae5
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 32%

---

# Primi passaggi per l&#39;amministratore

Questo articolo contiene i primi passi che gli amministratori di [!DNL Adobe Target] devono compiere dopo aver ricevuto l&#39;invito a [!DNL Adobe Experience Cloud].

## Ricevi invito per [!DNL Target] {#task_3E0817630774431983FAA3D2CB2E75BD}

Un amministratore di sistema in [!DNL Adobe Admin Console] deve aggiungerti come utente in [!DNL Target] invitandoti a partecipare. L’amministratore di sistema deve quindi aggiungerti a uno o più profili di prodotto (gruppi di utenti) specifici per il tuo ruolo. Entrambe queste attività vengono eseguite in [Adobe Admin Console](https://adminconsole.adobe.com).

Per ulteriori informazioni, vedere [Gestione dei gruppi di utenti](https://helpx.adobe.com/enterprise/using/users.html).

Dopo che l’amministratore di sistema avrà eseguito questi passaggi, riceverai un’e-mail di invito.

## Accettare l&#39;invito {#task_24FE66659E634B24AB61DB8497772E17}

Dopo aver ricevuto l&#39;invito a partecipare a [!DNL Adobe Experience Cloud], accettare l&#39;invito, accedere e accettare il [!UICONTROL End User License Agreement] (EULA).

1. Accetta l’invito per [!DNL Adobe Experience Cloud].
1. Se non disponi già di un Adobe ID, viene richiesto di crearne uno.

   Se disponi di un Adobe ID, il tuo Adobe ID viene riconosciuto e ti viene richiesto di accedere.
1. Accetta [!UICONTROL Terms of Use].
1. Rivedi il riepilogo delle operazioni eseguite finora, quindi fai clic su **[!UICONTROL Continue to Experience Cloud]**.
1. Accedere a [!DNL Adobe Experience Cloud] e fare clic su **[!UICONTROL Link Account]**.

   >[!NOTE]
   >
   >Se non colleghi l’account, non potrai accedere ad [!DNL Target].

   Tutti i prodotti [!UICONTROL Experience Cloud] vengono visualizzati nella pagina di collegamento. Fai clic su `Link Target` e immetti il nome utente e la password di [!DNL Target] per accedere a [!DNL Target].
1. Fare clic su **[!UICONTROL Continue to Experience Cloud]**.

   A questo punto, non disponi ancora di gruppi configurati con diritti per effettuare collegamenti.
1. Puoi guardare il video con l’introduzione ad [!DNL Adobe Experience Cloud].
1. Per visualizzare i nuovi privilegi e accedere al prodotto, disconnettiti da [!DNL Adobe Experience Cloud], quindi accedi nuovamente.
1. Procedi al passaggio successivo, [Assegnarsi il ruolo Approvatore](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Assegnarsi il ruolo Approvatore {#task_15CAA437A71444E2932B333D5E66A3C7}

Dopo aver accettato l&#39;invito ad aderire a [!DNL Adobe Experience Cloud] e aver effettuato l&#39;accesso, confermare che [!DNL Target] è stato aggiunto al tuo account [!DNL Experience Cloud], quindi assegnare te stesso la mansione [!UICONTROL Approver] per [!DNL Target].

Se la tua organizzazione dispone di una licenza di [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905), consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.

Se la tua organizzazione dispone di una licenza di [Target Premium](/help/main/c-intro/intro.md#premium), consulta il [Passaggio 6: specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configurare le autorizzazioni Enterprise*.

Il passaggio successivo deve essere la configurazione degli utenti in [!DNL Target Standard] e [!DNL Target Premium]. Per ulteriori informazioni, consulta [Gestione utenti](/help/main/administrating-target/c-user-management/user-management.md).

## Autorizzazioni necessarie per modificare le impostazioni di [!UICONTROL Administration] {#admin-permissions}

**Prima del 22 aprile 2025**: gli utenti con i diritti [!UICONTROL Approvers] in [!DNL Adobe Admin Console] possono modificare o modificare tutte le impostazioni nella pagina [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md) di [!DNL Target], indipendentemente dal ruolo [!DNL Target].

**In vigore dal 22 aprile 2025**: solo gli amministratori [!UICONTROL Product] e [!UICONTROL Solutions] potranno aggiornare le impostazioni nelle sezioni [[!UICONTROL Administration]](/help/main/administrating-target/administrating-target.md), indipendentemente dai ruoli che ricoprono nelle aree di lavoro [!DNL Target]. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Administration].

Questo aggiornamento migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.
