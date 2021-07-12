---
keywords: mbox globale;personalizzare mbox globale;modificare at.js;at.js;implementare at.js
description: Scopri come personalizzare una mbox globale per at.js nella pagina Amministrazione-implementazione di Adobe Target.
title: Come posso personalizzare una mbox globale?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: fb0a62ecc5609e7b8ef5f6a4fb5a94f8ba025fec
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 22%

---

# Personalizzare una mbox globale

Informazioni su come personalizzare una mbox globale per at.js.

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

1. Disabilita **[!UICONTROL Caricamento pagina abilitato (Creazione automatica mbox globale)]**, quindi aggiungi il nome della mbox globale personalizzata che desideri utilizzare per fornire attività da [!DNL Target].

   >[!IMPORTANT]
   >
   >La modifica viene salvata automaticamente quando selezioni una diversa mbox globale.

   Questa mbox globale personalizzata è utilizzata anche per il monitoraggio dei clic.

   ![custom-global-mbox](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementa la libreria [!DNL at.js] sul tuo sito.

   Per ulteriori informazioni, consulta [Come distribuire at.js](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/how-to-deployatjs.md) .

1. Sincronizza il passaggio con la pubblicazione.

   Quando sei pronto per [!DNL Target] iniziare a utilizzare la tua mbox globale per tutte le attività future, puoi procedere con questo passaggio.

   Aggiorna il nome della mbox globale personalizzata in corrispondenza del nome utilizzato nel passaggio 2, sopra.

   >[!IMPORTANT]
   >
   >Tutte le attività nel tuo account si sincronizzano con questa mbox. Se questa mbox non è presente sul sito, tutte le attività smettono di funzionare.
