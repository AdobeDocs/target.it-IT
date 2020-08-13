---
keywords: Analytics as reporting source;a4t;A4T
description: I requisiti dell’account utente per creare un’attività basata su Adobe Analytics in Adobe Target (A4T).
title: Requisiti delle autorizzazioni utente
feature: a4t implementation
solution: Target,Analytics
topic: Reports and analytics
uuid: cf359bcd-547e-4f8f-bcf6-e646245bb9ce
translation-type: tm+mt
source-git-commit: e203dc94e9bb34c4090f5795cbf73869808ada88
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 63%

---


# Requisiti delle autorizzazioni utente {#user-permission-requirements}

Informazioni sui requisiti dell’account utente per creare un’attività basata su [!DNL Adobe Analytics] in [!DNL Adobe Target] (A4T).

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di [!DNL Analytics], devi disporre di un account utente sia per [!DNL Analytics] che per [!DNL Target].

Gli account utente devono essere configurati come descritto nelle sezioni seguenti:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Completa le seguenti attività in [!DNL Adobe Experience Cloud][Admin Console](https://adminconsole.adobe.com):

### Collegare gli account di soluzioni all’Adobe ID

Gli account utente [!DNL Analytics] e [!DNL Target] devono essere collegati al tuo Adobe ID.

For more information, see [Organizations and account linking](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Configurare l’iscrizione al gruppo Experience Cloud

Devi essere membro di uno o più gruppi di [!DNL Experience Cloud] che hanno accesso a [!DNL Analytics] e a [!DNL Target].

For more information, see [Manage Experience Cloud users and products](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Completa le seguenti attività in [!DNL Adobe Analytics]:

### Configurare l’accesso alla suite di rapporti di Analytics

Before creating or viewing reports for an [!DNL Analytics]-powered activity, you must be a member of the **[!UICONTROL All Report Access]** group, or a member of a group that has access to at least one report in the report suite that you want to use. Se non riesci a visualizzare i rapporti, assicurati di essere un membro di uno di questi gruppi.

Per ulteriori informazioni, consulta Profili [di prodotto e gruppi](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/admin-getting-started.html#section_AB50558124D541CF80A0D3D76D35A4BF).

### Configurare l’accesso al gruppo con accesso ai servizi Web

Devi appartenere al gruppo con accesso ai servizi Web in [!DNL Analytics] per poter utilizzare [!DNL Analytics] come origine di generazione di rapporti per [!DNL Target].

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Non sono necessari privilegi aggiuntivi.
