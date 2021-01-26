---
keywords: Analytics as reporting source;a4t;A4T;requirements
description: I requisiti dell’account utente per creare un’attività basata su Adobe Analytics in Adobe Target (A4T).
title: Requisiti delle autorizzazioni utente
feature: Analytics for Target (A4T)
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: cf47b7f3625bb1c3430b9fba00c573f489efc448
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 49%

---


# Requisiti delle autorizzazioni utente

Informazioni sui requisiti dell’account utente per creare un’attività basata su [!DNL Adobe Analytics] in [!DNL Adobe Target] (A4T).

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di [!DNL Analytics], devi disporre di un account utente sia per [!DNL Analytics] che per [!DNL Target].

Gli account utente devono essere configurati come descritto nelle sezioni seguenti:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Completa le seguenti attività in [!DNL Adobe Experience Cloud][Admin Console](https://adminconsole.adobe.com):

### Collegare gli account di soluzioni all’Adobe ID

Gli account utente [!DNL Analytics] e [!DNL Target] devono essere collegati al tuo Adobe ID.

Per ulteriori informazioni, vedere [Organizzazioni e collegamento dell&#39;account](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Configurare l’iscrizione al gruppo Experience Cloud

Devi essere membro di uno o più gruppi di [!DNL Experience Cloud] che hanno accesso a [!DNL Analytics] e a [!DNL Target].

Per ulteriori informazioni, vedere [Gestione di utenti  Experienci Cloud e prodotti](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Configurare l&#39;accesso alla suite di rapporti [!DNL Analytics]:

Per utilizzare A4T in una determinata suite di rapporti, è necessario avere accesso a tale suite di rapporti.

1. In **[!UICONTROL Admin Console]**, fare clic su un profilo di prodotto [!DNL Analytics], quindi fare clic sulla scheda **[!UICONTROL Autorizzazioni]**.

   Potete quindi vedere a quali suite di rapporti ha accesso il profilo.

1. Assicurati che la suite di rapporti a cui vuoi accedere in [!DNL Target] sia una delle suite elencate nel profilo di prodotto di cui fai parte.

   L&#39;illustrazione seguente è un esempio di un profilo di prodotto che ha accesso a tutte le suite di rapporti:

   ![, scheda Autorizzazioni Admin Console](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

## Adobe Target {#section_26BA212D8D40443E9EE2AB327091425C}

Non sono necessari privilegi aggiuntivi.
