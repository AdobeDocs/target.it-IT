---
keywords: global mbox;target classic;use global mbox from target classic
description: Per impostazione predefinita, in Target Standard viene creata una mbox globale denominata target-global-mbox, utilizzata per eseguire le attività create in Target Standard. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di Target Standard.
title: Utilizzare una mbox globale da unʼimplementazione legacy
feature: null
subtopic: Getting Started
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: 6922b80c88cbd2947c3bfd0cc9d8409ff5dcdcd0
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 57%

---


# Utilizzare una mbox globale da unʼimplementazione legacy{#use-a-global-mbox-from-a-legacy-implementation}

By default, [!DNL Target] creates a global mbox called target-global-mbox, which is used to run activities created in [!DNL Target]. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di [!DNL Target].

>[!NOTE]
>
>Puoi avere una sola mbox globale per ogni account.

Per utilizzare la mbox globale esistente sia per [!DNL Target] che per l&#39;implementazione precedente, è necessario impostare alcuni parametri.

1. Go to [!DNL Target], then click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   By default, **[!UICONTROL Page load enabled (Auto-create global mbox]** is enabled, and the custom global mbox is named `target-global-mbox`.

1. If you want to use an existing mbox, disable **[!UICONTROL Page load enabled (Auto-create global mbox]**, and specify the name of a previously created global mbox in the **[!UICONTROL Global Mbox]** field.

   The [!UICONTROL Global Mbox] drop-down lists all mboxes in your account. Per utilizzare una mbox non esistente, creala.

1. Fai clic su **[!UICONTROL Salva]**.

   Le impostazioni di mbox.js per l&#39;account vengono aggiornate.

1. Scaricate il nuovo file at.js e farvi riferimento sul sito.

   Tutte le attività esistenti vengono aggiornate in modo da utilizzare la mbox globale specificata, comprese quelle create e implementate in precedenza.

## Risoluzione dei problemi di implementazione mbox globale

Le seguenti domande frequenti possono essere utilizzate per risolvere eventuali problemi di implementazione della mbox globale:

### Perché la mbox globale non viene caricata o perché c&#39;è latenza nel caricamento della mbox globale quando la pagina viene caricata?

Assicuratevi che il riferimento at.js sia la prima chiamata JavaScript sulla pagina. Per altre soluzioni a questo problema, consultate [Global mbox Frequently Asked Questions (Domande](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md)globali più frequenti).
