---
keywords: mbox globale;target classic;utilizzare mbox globale da target classic
description: Scopri come utilizzare una mbox globale legacy per le attività di Adobe [!DNL Target] se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy.
title: Posso utilizzare una mbox globale da un'implementazione legacy?
feature: at.js
role: Developer
exl-id: 1eb6836b-6b3c-4494-af67-cd72a4f357e2
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 41%

---

# Utilizzare una mbox globale da un’implementazione legacy

Per impostazione predefinita, [!DNL Target] crea una mbox globale denominata target-global-mbox, utilizzata per eseguire le attività create in [!DNL Target]. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di [!DNL Target].

>[!NOTE]
>
>Puoi avere una sola mbox globale per ogni account.

Per utilizzare la mbox globale esistente sia per [!DNL Target] che per l&#39;implementazione precedente, è necessario impostare alcuni parametri.

1. Vai a [!DNL Target], quindi fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

   Per impostazione predefinita, il **[!UICONTROL Caricamento pagina abilitato (Creazione automatica mbox globale]** è abilitato e la mbox globale personalizzata è denominata `target-global-mbox`.

1. Se desideri utilizzare una mbox esistente, disattiva **[!UICONTROL Caricamento pagina abilitato (Creazione automatica mbox globale]** e specifica il nome di una mbox globale creata in precedenza nel campo **[!UICONTROL Mbox globale]** .

   Il menu a discesa [!UICONTROL Mbox globale] elenca tutte le mbox nel tuo account. Per utilizzare una mbox non esistente, creala.

1. Fai clic su **[!UICONTROL Salva]**.

   Le impostazioni di mbox.js per l&#39;account vengono aggiornate.

1. Scarica il nuovo file at.js e fai riferimento a esso sul tuo sito.

   Tutte le attività esistenti vengono aggiornate in modo da utilizzare la mbox globale specificata, comprese quelle create e implementate in precedenza.

## Risoluzione dei problemi di implementazione della mbox globale

Le seguenti domande frequenti possono essere utilizzate per risolvere i problemi di implementazione della mbox globale:

### Perché la mbox globale non viene caricata o perché c&#39;è latenza nel caricamento della mbox globale quando la pagina viene caricata?

Assicurati che il riferimento at.js sia la prima chiamata JavaScript sulla pagina. Per altre soluzioni a questo problema, consulta [Domande frequenti sulla mbox globale](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md).
