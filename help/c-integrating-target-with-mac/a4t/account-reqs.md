---
keywords: Analytics come origine per la generazione di rapporti;a4t;A4T;requisiti
description: Scopri come configurare i requisiti dell’account utente necessari per creare un’attività basata su Adobe Analytics in Adobe [!DNL Target] using Analytics for [!DNL Target] (A4T).
title: Quali requisiti di autorizzazione utente sono necessari per A4T?
feature: Analytics for Target (A4T)
solution: Target,Analytics
exl-id: f56fc525-92da-4814-86c1-18b3a2765f37
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 36%

---

# Requisiti delle autorizzazioni utente

Informazioni sui requisiti dell’account utente per creare un’attività basata su [!DNL Adobe Analytics] in [!DNL Adobe Target] (A4T).

Prima di poter selezionare una suite di rapporti durante la definizione di un’attività di [!DNL Analytics], devi disporre di un account utente sia per [!DNL Analytics] che per [!DNL Target].

Gli account utente devono essere configurati come descritto nelle sezioni seguenti:

## Adobe Experience Cloud {#section_3931A2FAD38F4A4FA92CC77B92AF3F0D}

Completa le seguenti attività in [!DNL Adobe Experience Cloud][Admin Console](https://adminconsole.adobe.com):

### Collegare gli account di soluzioni all’Adobe ID

Gli account utente [!DNL Analytics] e [!DNL Target] devono essere collegati al tuo Adobe ID.

Per ulteriori informazioni, consulta [Collegamento di organizzazioni e account](https://docs.adobe.com/help/en/core-services/interface/manage-users-and-products/organizations.html).

### Configurare l’iscrizione al gruppo Experience Cloud

Devi essere membro di uno o più gruppi di [!DNL Experience Cloud] che hanno accesso a [!DNL Analytics] e a [!DNL Target].

Per ulteriori informazioni, consulta [Gestione di utenti e prodotti Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

## Adobe Analytics {#section_8F404FDE9A634534AB0AA4CB3075582B}

Per utilizzare A4T in una determinata suite di rapporti, devi disporre dell’accesso a tale suite di rapporti e concedere l’accesso al gruppo [!DNL Web Services Access] .

1. In **[!UICONTROL Admin Console]**, fai clic su un profilo di prodotto [!DNL Analytics], quindi fai clic sulla scheda **[!UICONTROL Autorizzazioni]** .

   Puoi quindi vedere a quali suite di rapporti ha accesso il profilo.

1. Assicurati che la suite di rapporti a cui desideri accedere in [!DNL Target] sia una delle suite elencate nel profilo di prodotto di cui fai parte.

   L’illustrazione seguente è un esempio di un profilo di prodotto con accesso a tutte le suite di rapporti:

   ![Scheda Autorizzazione Admin Console](/help/c-integrating-target-with-mac/a4t/assets/permissions-tab.png)

1. Configura l&#39;accesso al gruppo [!UICONTROL Accesso ai servizi Web].

   Per poter utilizzare [!DNL Analytics] come origine per la generazione di rapporti, è necessario accedere al gruppo [!UICONTROL Accesso ai servizi Web] in [!DNL Analytics].[!DNL Target]


## Adobe [!DNL Target] {#section_26BA212D8D40443E9EE2AB327091425C}

Non sono necessari privilegi aggiuntivi.
