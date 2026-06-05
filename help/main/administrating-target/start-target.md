---
keywords: Amministrazione;ruolo approvatore;approvatore
description: Esegui le prime attività [!DNL Adobe Target] che gli amministratori devono eseguire dopo aver ricevuto l'invito via e-mail a [!DNL Adobe Experience Cloud].
title: Dove Si Inizia Ad Amministrare  [!DNL Target]?
feature: Administration & Configuration
role: Admin
exl-id: b60236da-20ae-4bab-b261-6a33d2f70e23
TQID: https://experienceleague.adobe.com/GfadY-knTwzXCB-n1AZ9u3PtoAyJokn1OXu3elRhgXk
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 473
ht-degree: 30%

---

# Primi passaggi per l&#39;amministratore

Questo articolo contiene i primi passi che gli amministratori di [!DNL Adobe Target] devono compiere dopo aver ricevuto l&#39;invito a [!DNL Adobe Experience Cloud].

## Ricevi invito per [!DNL Target] {#task_3E0817630774431983FAA3D2CB2E75BD}

Un amministratore di sistema in [!DNL Adobe Admin Console] deve aggiungerti come utente in [!DNL Target] invitandoti a partecipare. L’amministratore di sistema deve quindi aggiungerti a uno o più profili di prodotto (gruppi di utenti) specifici per il tuo ruolo. Entrambe queste attività vengono eseguite in [Adobe Admin Console](https://adminconsole.adobe.com).

Per ulteriori informazioni, vedere [Gestione dei gruppi di utenti](https://helpx.adobe.com/enterprise/using/users.html).

Dopo che l’amministratore di sistema avrà eseguito questi passaggi, riceverai un’e-mail di invito.

## Accettare l&#39;invito {#task_24FE66659E634B24AB61DB8497772E17}

Dopo aver ricevuto l&#39;invito ad aderire a [!DNL Adobe Experience Cloud], accettare l&#39;invito, accedere e accettare il [!UICONTROL Contratto di licenza con l&#39;utente finale] (EULA).

1. Accetta l’invito per [!DNL Adobe Experience Cloud].
1. Se non disponi già di un Adobe ID, viene richiesto di crearne uno.

   Se disponi di un Adobe ID, il tuo Adobe ID viene riconosciuto e ti viene richiesto di accedere.
1. Accetta le [!UICONTROL Condizioni per l&#39;utilizzo].
1. Rivedi il riepilogo di quello che hai fatto finora, quindi fai clic su **[!UICONTROL Continua per Experience Cloud]**.
1. Accedi a [!DNL Adobe Experience Cloud] e fai clic su **[!UICONTROL Collega account]**.

   >[!NOTE]
   >
   >Se non colleghi l’account, non potrai accedere ad [!DNL Target].

   Tutti i prodotti [!UICONTROL Experience Cloud] vengono visualizzati nella pagina di collegamento. Fai clic su `Link Target` e immetti il nome utente e la password di [!DNL Target] per accedere a [!DNL Target].
1. Fai clic su **[!UICONTROL Continua su Experience Cloud]**.

   A questo punto, non disponi ancora di gruppi configurati con diritti per effettuare collegamenti.
1. Puoi guardare il video con l’introduzione ad [!DNL Adobe Experience Cloud].
1. Per visualizzare i nuovi privilegi e accedere al prodotto, disconnettiti da [!DNL Adobe Experience Cloud], quindi accedi nuovamente.
1. Procedi al passaggio successivo, [Assegnarsi il ruolo Approvatore](/help/main/administrating-target/start-target.md#task_15CAA437A71444E2932B333D5E66A3C7).

## Assegnarsi il ruolo Approvatore {#task_15CAA437A71444E2932B333D5E66A3C7}

Dopo aver accettato l&#39;invito ad aderire a [!DNL Adobe Experience Cloud] e aver effettuato l&#39;accesso, verificare che [!DNL Target] sia stato aggiunto al tuo account [!DNL Experience Cloud], quindi assegnarti il ruolo [!UICONTROL Approvatore] per [!DNL Target].

Se la tua organizzazione dispone di una licenza di [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905), consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.

Se la tua organizzazione dispone di una licenza di [Target Premium](/help/main/c-intro/intro.md#premium), consulta il [Passaggio 6: specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/properties-overview.md#section_8C425E43E5DD4111BBFC734A2B7ABC80) in *Configurare le autorizzazioni Enterprise*.

Il passaggio successivo deve essere la configurazione degli utenti in [!DNL Target Standard] e [!DNL Target Premium]. Per ulteriori informazioni, consulta [Gestione utenti](/help/main/administrating-target/c-user-management/user-management.md).

## Autorizzazioni necessarie per modificare le impostazioni di [!UICONTROL Amministrazione] {#admin-permissions}

**Prima del 22 aprile 2025**: gli utenti con i diritti [!UICONTROL Approvatori] in [!DNL Adobe Admin Console] possono modificare o modificare tutte le impostazioni nella pagina [[!UICONTROL Amministrazione]](/help/main/administrating-target/administrating-target.md) di [!DNL Target], indipendentemente dal ruolo [!DNL Target].

**In vigore dal 22 aprile 2025**: solo gli amministratori di [!UICONTROL Prodotto] e [!UICONTROL Soluzioni] potranno aggiornare le impostazioni nelle sezioni [[!UICONTROL Amministrazione]](/help/main/administrating-target/administrating-target.md), indipendentemente dai ruoli che ricoprono nelle [!DNL Target] aree di lavoro. Gli utenti senza questa autorizzazione avranno accesso in sola lettura alle sezioni [!UICONTROL Amministrazione].

Questo aggiornamento migliora il controllo dell&#39;organizzazione sulle configurazioni delle istanze [!DNL Target], impedendo aggiornamenti accidentali che potrebbero influire sulla distribuzione delle attività tra i vari team di test e personalizzazione.
