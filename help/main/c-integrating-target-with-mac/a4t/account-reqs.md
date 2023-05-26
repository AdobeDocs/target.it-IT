---
keywords: Analytics come origine per la generazione di rapporti;a4t;A4T;requirements
description: Scopri come configurare i requisiti dell’account utente necessari per creare un’attività basata su Adobe Analytics in Adobe [!DNL Target] utilizzo di Analytics per [!DNL Target] (A4T).
title: Quali requisiti di autorizzazione utente sono necessari per A4T?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 34%

---

# Requisiti delle autorizzazioni utente

Informazioni sui requisiti dell’account utente per creare un’attività basata su [!DNL Adobe Analytics] in [!DNL Adobe Target] (A4T).

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di [!DNL Analytics], devi disporre di un account utente sia per [!DNL Analytics] che per [!DNL Target].

Gli account utente devono essere configurati come descritto nelle sezioni seguenti:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Completa le seguenti attività in [!DNL Adobe Experience Cloud][Admin Console](https://adminconsole.adobe.com):

### Collegare gli account di soluzioni all’Adobe ID

Gli account utente [!DNL Analytics] e [!DNL Target] devono essere collegati al tuo Adobe ID.

Per ulteriori informazioni, consulta [Organizzazioni e collegamento di account](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=en).

### Configurare l’iscrizione al gruppo Experience Cloud

Devi essere membro di uno o più gruppi di [!DNL Experience Cloud] che hanno accesso a [!DNL Analytics] e a [!DNL Target].

Per ulteriori informazioni, consulta [Gestione di utenti e prodotti Experienci Cloud](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Per utilizzare A4T in una determinata suite di rapporti, devi avere accesso a tale suite di rapporti e concedere l’accesso a [!DNL Web Services Access] gruppo.

1. In entrata **[!UICONTROL Admin Console]**, fare clic su un [!DNL Analytics] profilo di prodotto, quindi fai clic su **[!UICONTROL Autorizzazioni]** scheda.

   Puoi quindi vedere a quali suite di rapporti il profilo ha accesso.

1. Assicurati che la suite di rapporti a cui desideri avere accesso in [!DNL Target] è uno di quelli elencati nel profilo di prodotto di cui fai parte.

   L’illustrazione seguente è un esempio di un profilo di prodotto che ha accesso a tutte le suite di rapporti:

   ![Scheda Autorizzazione Admin Console](/help/main/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Configurare l’accesso a [!UICONTROL Accesso ai servizi Web] gruppo.

   Accesso al [!UICONTROL Accesso ai servizi Web] raggruppare in [!DNL Analytics] deve essere in grado di utilizzare [!DNL Analytics] come origine di reporting per [!DNL Target].


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Non sono necessari privilegi aggiuntivi.
