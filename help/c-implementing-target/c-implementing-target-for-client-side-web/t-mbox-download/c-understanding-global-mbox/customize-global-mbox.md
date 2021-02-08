---
keywords: mbox globale;personalizzare mbox globale;modificare at.js;at.js;implementare at.js
description: Scoprite come personalizzare una mbox globale per at.js nella pagina Amministrazione-implementazione di  Adobe Target.
title: Come posso personalizzare una mbox globale?
feature: at.js
role: Developer
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 50%

---


# Personalizzare una mbox globale

Informazioni utili per personalizzare una mbox globale per at.js.

1. Fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

1. Disattivate **[!UICONTROL Caricamento pagina abilitato (Creazione automatica di mbox globale)]**, quindi aggiungete il nome della mbox globale personalizzata che desiderate utilizzare per distribuire le attività da [!DNL Target].

   Questa mbox globale personalizzata è utilizzata anche per il monitoraggio dei clic.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Al termine, fai clic su **[!UICONTROL Salva]**.

1. Implementate la [!DNL at.js] libreria sul sito.

   Per ulteriori informazioni, vedere [Come distribuire at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md).

1. Sincronizza il passaggio con la pubblicazione.

   Non appena sei pronto a utilizzare la tua mbox globale in [!DNL Target] per tutte le attività che stai portando avanti, puoi procedere con questo passaggio.

   Aggiorna il nome della mbox globale personalizzata in corrispondenza del nome utilizzato nel passaggio 2, sopra.

   >[!IMPORTANT]
   >
   >Quando si salva, tutte le attività nel tuo account si sincronizzano con questa mbox. Se il sito non contiene questa mbox, tutte le attività smetteranno di funzionare.

