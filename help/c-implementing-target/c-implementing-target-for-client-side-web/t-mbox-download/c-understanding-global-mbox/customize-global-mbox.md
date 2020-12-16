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

