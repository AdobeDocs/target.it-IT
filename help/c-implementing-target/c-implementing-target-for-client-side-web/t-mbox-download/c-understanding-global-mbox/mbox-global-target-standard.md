---
keywords: mbox globale;target classic;utilizzare mbox globale da target classic
description: Scoprite come utilizzare una mbox globale legacy per le attività Adobe Target  se avete già creato una mbox globale sulle pagine per le implementazioni precedenti.
title: Posso utilizzare una mbox globale da un'implementazione legacy?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 41%

---


# Utilizzate una mbox globale da un&#39;implementazione legacy

Per impostazione predefinita, [!DNL Target] crea una mbox globale denominata target-global-mbox, utilizzata per eseguire le attività create in [!DNL Target]. Tuttavia, se hai già creato una mbox globale sulle tue pagine per le implementazioni legacy, puoi utilizzarla anche per le attività di [!DNL Target].

>[!NOTE]
>
>Puoi avere una sola mbox globale per ogni account.

Per utilizzare la mbox globale esistente sia per [!DNL Target] che per l&#39;implementazione precedente, è necessario impostare alcuni parametri.

1. Vai a [!DNL Target], quindi fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

   Per impostazione predefinita, **[!UICONTROL Caricamento pagina abilitato (Creazione automatica di mbox globale]** è abilitata, e la mbox globale personalizzata è denominata `target-global-mbox`.

1. Se desiderate utilizzare una mbox esistente, disattivate il caricamento di **[!UICONTROL pagina abilitato (create automaticamente mbox globale]**) e specificate il nome di una mbox globale creata in precedenza nel campo **[!UICONTROL Mbox globale]**.

   L&#39;elenco a discesa [!UICONTROL Mbox globale] elenca tutte le mbox nell&#39;account. Per utilizzare una mbox non esistente, creala.

1. Fai clic su **[!UICONTROL Salva]**.

   Le impostazioni di mbox.js per l&#39;account vengono aggiornate.

1. Scaricate il nuovo file at.js e farvi riferimento sul sito.

   Tutte le attività esistenti vengono aggiornate in modo da utilizzare la mbox globale specificata, comprese quelle create e implementate in precedenza.

## Risoluzione dei problemi di implementazione mbox globale

Le seguenti domande frequenti possono essere utilizzate per risolvere eventuali problemi di implementazione della mbox globale:

### Perché la mbox globale non viene caricata o perché c&#39;è latenza nel caricamento della mbox globale quando la pagina viene caricata?

Assicuratevi che il riferimento at.js sia la prima chiamata JavaScript sulla pagina. Per altre soluzioni a questo problema, consultate [Global mbox Frequently Asked Questions](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-target-atjs-faq/global-mbox-frequently-asked-questions.md) (Domande frequenti globali sulla mbox).
