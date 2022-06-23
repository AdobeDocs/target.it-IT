---
keywords: mbox globale;personalizzare mbox globale;modificare at.js;at.js;implementare at.js
description: Scopri come personalizzare una mbox globale per at.js nella pagina Amministrazione-implementazione di Adobe Target.
title: Come posso personalizzare una mbox globale?
feature: at.js
role: Developer
exl-id: 6d3eab89-818c-405c-81af-90dfbede7390
source-git-commit: b1e8ea2370fc15f4bfcd960ab2960cafe2db92b8
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 17%

---

# Personalizzare una mbox globale

Informazioni utili per personalizzare un [!DNL Adobe Target] mbox globale per at.js.

1. Fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Implementazione]**.

1. Disattiva **[!UICONTROL Caricamento pagina abilitato (Creazione automatica mbox globale)]**, quindi aggiungi il nome della mbox globale personalizzata da cui desideri distribuire le attività [!DNL Target].

   >[!IMPORTANT]
   >
   >La modifica viene salvata automaticamente quando selezioni una diversa mbox globale.

   Questa mbox globale personalizzata è utilizzata anche per il monitoraggio dei clic.

   ![custom-global-mbox](/help/main/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/c-understanding-global-mbox/assets/custom-global-mbox.png)

1. Implementare [!DNL at.js] sul sito.

   Vedi [Come distribuire at.js](https://developer.adobe.com/target/implement/client-side/atjs/how-to-deployatjs/how-to-deployatjs/) per ulteriori informazioni.

1. Sincronizza il passaggio con la pubblicazione.

   Quando sei pronto per [!DNL Target] per iniziare a utilizzare la mbox globale per tutte le attività future, puoi procedere con questo passaggio.

   Aggiorna il nome della mbox globale personalizzata in corrispondenza del nome utilizzato nel passaggio 2, sopra.

   >[!IMPORTANT]
   >
   >Tutte le attività nel tuo account si sincronizzano con questa mbox. Assicurati che la mbox globale sia presente sul tuo sito in modo che le attività continuino a funzionare. Assicurati di modificare e salvare nuovamente le attività interessate create con il Compositore esperienza visivo che si sincronizza con questa mbox. Non è necessario salvare nuovamente le attività create nel Compositore esperienza basato su moduli o tramite API.

