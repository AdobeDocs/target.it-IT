---
keywords: multipagina;test di viaggio;attività multipagina
description: Scopri come creare un'attività multipagina in Adobe [!DNL Target] consente di creare una storia su più pagine, con una progettazione specifica per ogni pagina.
title: Come si crea un’attività multipagina?
feature: Visual Experience Composer (VEC)
exl-id: d000cc73-4729-4ce0-ab30-756dd3ca8545
source-git-commit: 293b2869957c2781be8272cfd0cc9f82d8e4f0f0
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 68%

---

# Attività multipagina

Un&#39;attività multipagina in [!DNL Adobe Target] consente di creare una storia su più pagine, con una progettazione specifica per ogni pagina.

Ad esempio, ti può essere utile per testare un’offerta di spedizione gratuita per acquisti superiori a un determinato importo. Vorresti che questa offerta venga visualizzata nella pagina di destinazione, in una pagina di categoria e in alcune pagine di prodotto, ma con dimensioni e posizione diverse in ciascun tipo di pagina. L’offerta dovrà essere prominente sulla home page, quindi proposta di nuovo ma più piccola su altre pagine correlate.

Puoi anche utilizzare un’attività multipagina per definire layout diversi per i siti desktop e mobile non reattivi. Se il sito dispone di un sito per dispositivi mobili separato come [!DNL m.mysite.com] invece di [!DNL `www.mysite.com`], è preferibile creare un&#39;[attività multipagina](/help/main/c-experiences/c-visual-experience-composer/multipage-activity.md#concept_277E096063E14813AC5D8EDFA1D2ED48), aggiungere [!DNL m.mysite.com] come pagine separate e quindi applicare le modifiche per dispositivi mobili per apportare le modifiche appropriate alla versione desktop e alla versione mobile nella stessa esperienza. Per i siti per dispositivi mobili adattivi, utilizza le [modifiche delle esperienze mobile](/help/main/c-experiences/c-visual-experience-composer/mobile-viewports.md#concept_8E45527C4ABC41D59AA3553BEDC76FA5).

>[!NOTE]
>
>Le attività multipagina sono progettate per le attività in cui la stessa offerta ha un aspetto diverso su più pagine. Se l’offerta appare nello stesso modo su tutte le pagine, un [test modello](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781) risulta più efficiente.

È possibile specificare regole modello per ogni pagina del test multipagina. Ad esempio, è possibile eseguire un test multipagina nella home page e in tutte le pagine delle categorie applicando delle regole modello alla pagina categoria del test multipagina. Vedi [Includere la stessa esperienza in pagine simili](/help/main/c-experiences/c-visual-experience-composer/temtest.md#task_2539D51A18044F82B0D9895636546781).

Per aggiungere delle pagine a un test:

1. Fare clic sull&#39;icona ingranaggio **[!UICONTROL Configure]**.
1. Fare clic su **[!UICONTROL Add Additional Pages]**.

   Sulla sinistra dello schermo appare una barra di navigazione.

   ![immagine multipagina](assets/multipage_nav.png)

1. Questa barra di navigazione permette di specificare le pagine e impostare la pagina predefinita.

   Fare clic su **[!UICONTROL Add Page]** per aggiungere una pagina.

   Fai clic sull&#39;icona dei tre puntini di sospensione verticali per visualizzare un menu di azione:

   ![immagine menu_multipagina](assets/multipage_menu.png)

   Questo menu permette di rinominare le pagine, eseguire un test di reindirizzamento dall&#39;interno dell&#39;attività multipagina ed eliminare la pagina.

1. Il compositore di esperienza visivo permette di progettare il modo in cui l&#39;offerta appare in ogni pagina.
