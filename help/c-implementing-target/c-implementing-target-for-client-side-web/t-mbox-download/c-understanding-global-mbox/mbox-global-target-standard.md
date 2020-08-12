---
keywords: global mbox;target classic;use global mbox from target classic
description: Per impostazione predefinita, in Target Standard viene creata una mbox globale denominata target-global-mbox, utilizzata per eseguire le attività create in Target Standard. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di Target Standard.
title: Utilizzare una mbox globale da unʼimplementazione legacy
feature: null
subtopic: Getting Started
topic: Standard
uuid: 31b03dab-99da-4040-bab6-4f5cb452ffdc
translation-type: tm+mt
source-git-commit: a51addc6155f2681f01f2329b25d72327de36701
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 96%

---


# Utilizzare una mbox globale da unʼimplementazione legacy{#use-a-global-mbox-from-a-legacy-implementation}

Per impostazione predefinita, in Target Standard viene creata una mbox globale denominata target-global-mbox, utilizzata per eseguire le attività create in Target Standard. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di Target Standard.

>[!NOTE]
>
>Puoi avere una sola mbox globale per ogni account.

Per utilizzare la mbox globale esistente sia per [!DNL Target Standard] che per l&#39;implementazione precedente, è necessario impostare alcuni parametri.

1. Go to [!DNL Target Standard], then click **[!UICONTROL Administration]** > **[!UICONTROL Implementation]**.

   Per impostazione predefinita, l&#39;opzione [!UICONTROL Crea automaticamente mbox globale] è abilitata e la mbox globale personalizzata è denominata `target-global-mbox`.
1. Per utilizzare una mbox esistente, disattiva [!UICONTROL Crea automaticamente mbox globale] e specifica il nome di una mbox globale creata in precedenza nel campo [!UICONTROL Mbox globale personalizzata].

   L&#39;elenco a discesa della [!UICONTROL mbox globale personalizzata] mostra tutti gli elementi mbox nel tuo account. Per utilizzare una mbox non esistente, creala in Target Classic.
1. Fai clic su **[!UICONTROL Salva]**.

   Le impostazioni di mbox.js per l&#39;account vengono aggiornate.
1. Scarica il nuovo file mbox.js e crea un riferimento a esso sul sito.

   Dopo aver aggiornato il sito di produzione con il nuovo file mbox.js, sei pronto per impostare le preferenze.
1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Visual Experience Composer (Compositore esperienza visivo)]**.
1. Nel campo [!UICONTROL  Global Mbox (Mbox globale personalizzata)] specificate il nome della mbox globale selezionata nella pagina Implementazione.
1. Fai clic su **[!UICONTROL Invia]**.

   Tutte le attività esistenti vengono aggiornate in modo da utilizzare la mbox globale specificata, comprese quelle create e implementate in precedenza.
   **Risoluzione dei problemi di implementazione della mbox globale** *Perché la mbox globale non viene caricata o perché c&#39;è latenza nel caricamento della mbox globale quando la pagina viene caricata?*

Assicurati che il riferimento mbox.js sia la prima chiamata JavaScript sulla pagina. Per altre soluzioni a questo problema, vedi [Implementazione di mbox.js](../../../../c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mbox-download.md#task_4EAE26BB84FD4E1D858F411AEDF4B420).
