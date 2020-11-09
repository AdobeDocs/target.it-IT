---
keywords: global mbox;customize global mbox;edit at.js;at.js;implement at.js
description: Informazioni utili per personalizzare una mbox globale per at.js.
title: Personalizzare una mbox globale
feature: null
translation-type: tm+mt
source-git-commit: 968d36d65016e51290f6bf754f69c91fd8f68405
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---


# Personalizzare una mbox globale{#customize-a-global-mbox}

Informazioni utili per personalizzare una mbox globale per at.js.

1. Fate clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

1. Disable **[!UICONTROL Page load enabled (Auto create global mbox)]**, then add the name of the custom global mbox that you would like to use to deliver activities from [!DNL Target].

   Questa mbox globale personalizzata è utilizzata anche per il monitoraggio dei clic.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Al termine, fai clic su **[!UICONTROL Salva]**.

1. Implement the [!DNL at.js] library on your site.

   Per ulteriori informazioni, consulta [Come distribuire at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) .

1. Sincronizza il passaggio con la pubblicazione.

   Non appena sei pronto a utilizzare la tua mbox globale in [!DNL Target] per tutte le attività che stai portando avanti, puoi procedere con questo passaggio.

   Aggiorna il nome della mbox globale personalizzata in corrispondenza del nome utilizzato nel passaggio 2, sopra.

   >[!IMPORTANT]
   >
   >Quando si salva, tutte le attività nel tuo account si sincronizzano con questa mbox. Se il sito non contiene questa mbox, tutte le attività smetteranno di funzionare.

