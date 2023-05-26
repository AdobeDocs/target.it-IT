---
keywords: Targeting esperienza;xt;URL attività;url
description: Scopri come specificare l’URL attività che determina la pagina utilizzata nel test e che viene visualizzata quando l’attività Targeting esperienza viene progettata utilizzando Adobe Target.
title: Qual è l’URL attività in un’attività Targeting esperienza?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 63%

---

# URL attività nelle attività Targeting esperienza

Il [!UICONTROL URL attività] determina la pagina utilizzata in [!DNL Adobe Target] [!UICONTROL Targeting esperienza] (XT) e che si apre nel [!UICONTROL Compositore esperienza visivo] (VEC) oppure [!UICONTROL Compositore esperienza basato su moduli] quando l’attività è progettata.

1. Quando viene richiesto durante la [creazione di un’attività Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), specifica l’URL dell’attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.
   >
   >Per impostazione predefinita, nel Compositore esperienza visivo e in quello basato su moduli viene aperta la pagina specificata nel [Impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se hai specificato un URL per un sito che non include il codice JavaScript di Target Standard, non puoi selezionare elementi di pagina.

1. (Condizionale) Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic su **[!UICONTROL Configura]**, seleziona **[!UICONTROL Consegna pagine]** e specifica l’URL nel campo [!UICONTROL URL].

   ![Finestra di dialogo Consegna pagine](/help/main/c-activities/t-experience-target/t-xt-create/assets/url-config-new.png)

   >[!NOTE]
   >
   >Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

1. (Condizionale) Fai clic su **[!UICONTROL Aggiungi regola modello]** per aggiungere più pagine o sezioni all’attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox

   È possibile aggiungere altre regole all’URL attività mediante l’operatore E oppure O. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fai clic su **[!UICONTROL Salva]**.
