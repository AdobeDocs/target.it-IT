---
keywords: Targeting esperienza;xt;URL attività;url
description: Scopri come specificare [!UICONTROL URL attività] che determina la pagina utilizzata nel test e che viene visualizzata quando [!UICONTROL Targeting esperienza] l’attività è progettata utilizzando [!DNL Adobe Target].
title: Cos'è [!UICONTROL URL attività] In un [!UICONTROL Targeting esperienza] (XT) Attività?
feature: Experience Targeting
exl-id: 8e3be814-6ad6-4ffa-be8d-68f0cb7857b5
source-git-commit: 24513d8cb39d38dcfbc74bf40961d5517cc90a4b
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 48%

---

# URL attività in [!UICONTROL Targeting esperienza] Attività (XT)

Il [!UICONTROL URL attività] determina la pagina utilizzata in un [!DNL Adobe Target] [!UICONTROL Targeting esperienza] (XT) attività. Questa è la pagina che si apre in [!UICONTROL Compositore esperienza visivo] (VEC) oppure [!UICONTROL Compositore esperienza basato su moduli] quando l’attività è progettata.

1. Quando viene richiesto durante la [creazione di un’attività Targeting esperienza](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md), specifica l’URL dell’attività. Digita l’URL completo (comprensivo di `https://`), quindi fai clic su **[!UICONTROL Crea attività]**.

   >[!NOTE]
   >
   >[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `https://www.adobe.com`] e [!DNL `http://www.adobe.com`] sono entrambi validi.
   >
   >Per impostazione predefinita, il Compositore esperienza visivo o [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) apre la pagina specificata nel [Impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.
   >
   >Se si specifica un URL per un sito che non include [[!DNL Target] Libreria JavaScript at.js o [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=it){target=_blank}, non è possibile selezionare elementi di pagina.

1. (Condizionale) Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo, fai clic su **[!UICONTROL Configura]**, seleziona **[!UICONTROL Consegna pagine]**, quindi specifica l’URL in [!UICONTROL URL] campo.

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
