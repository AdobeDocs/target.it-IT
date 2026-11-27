---
keywords: multipagina;test di viaggio;attività multipagina
description: Scopri come creare un'attività multipagina in Adobe [!DNL Target] per creare una storia su più pagine, con una progettazione specifica per ogni pagina.
title: Come si crea un’attività multipagina?
feature: Visual Experience Composer (VEC)
exl-id: d000cc73-4729-4ce0-ab30-756dd3ca8545
TQID: 'https://experienceleague.adobe.com/ZFqgbNp-sLF-ahG-uXKvWY0XPcxO0oZScGkpNX8hDHY'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f7501c88-b36a-590b-9cc4-dea607bda94b
    internal-label: Visual Experience Composer (VEC)
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c18d9e03-ac7d-4811-9c92-3e92ddc70ade
    internal-label: Mobile experience
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 13%
---
# Attività multipagina {#multipage-activity}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come utilizzare un&#39;attività multipagina per creare una storia su più pagine, con una progettazione specifica per ogni pagina.

>[!ENDSHADEBOX]

Un&#39;attività multipagina in [!DNL Adobe Target] crea una storia su più pagine, con una struttura specifica per ogni pagina.

Ad esempio, è possibile testare un’offerta di spedizione gratuita con acquisti superiori a un determinato importo. L’offerta può apparire nella pagina di destinazione, in una pagina di categoria e in alcune pagine di prodotto, con dimensioni e posizione diverse su ciascun tipo di pagina. Un’offerta importante può essere visualizzata nella home page, quindi rafforzata con offerte più piccole su altre pagine pertinenti.

Un’attività multipagina può anche definire layout diversi per i siti desktop e mobili non reattivi. Se il sito dispone di un sito mobile separato come [!DNL m.mysite.com] invece di [!DNL `www.mysite.com`], crea un&#39;attività multipagina, aggiungi [!DNL m.mysite.com] come pagine separate, quindi applica le modifiche mobile per apportare le modifiche appropriate alla versione desktop e alla versione mobile nella stessa esperienza. Per i siti per dispositivi mobili adattivi, utilizza le [modifiche delle esperienze mobile](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md).

>[!NOTE]
>
>Le attività multipagina sono progettate per le attività in cui la stessa offerta ha un aspetto diverso su più pagine. Se l’offerta appare nello stesso modo su tutte le pagine, un [test modello](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages) risulta più efficiente.

È possibile specificare le regole del modello per ogni pagina nel test multipagina. Ad esempio, un test multipagina può essere eseguito in tutta la home page e in tutte le pagine delle categorie applicando regole di modello alla pagina delle categorie nel test multipagina. Vedi [Includere la stessa esperienza in pagine simili](/help/main/c-experiences/c-visual-experience-composer/temtest.md#similar-pages).

## Aggiungere pagine a un’attività {#add-pages}

Ogni pagina aggiunta all’attività può avere una propria progettazione dell’offerta.

1. Fai clic sull&#39;icona **[!UICONTROL Configura]** ( ![Configura icona](/help/main/assets/icons/Setting.svg) ).

1. Fai clic su **[!UICONTROL Aggiungi pagine supplementari]**.

   Nella parte sinistra dello schermo viene visualizzato un riquadro di **[!UICONTROL Pagine]**.

   ![Icona Configura](assets/vec_edit_4.png)

1. Specificare le pagine e impostare la pagina predefinita.

   Fai clic su **[!UICONTROL Aggiungi pagina]** ( ![Aggiungi icona](/help/main/assets/icons/Add.svg) ) per aggiungere una pagina, specifica il nome e l&#39;URL della pagina, quindi fai clic su **[!UICONTROL Salva]**.

1. Utilizza il [!UICONTROL Compositore esperienza visivo] per progettare l&#39;aspetto dell&#39;offerta in ogni pagina.
