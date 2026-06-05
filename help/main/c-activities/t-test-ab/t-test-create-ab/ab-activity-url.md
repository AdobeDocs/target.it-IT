---
keywords: url attività;url;url diverso
description: Scopri come impostare l’[!UICONTROL URL attività] per definire le pagine di test e garantire una progettazione accurata dei test.
title: Qual è l’URL attività in un’attività A/B?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
reason: republish
TQID: https://experienceleague.adobe.com/arQWsSfBKYtrayq9AI8ejU1T-Uor-oL5j2Sp2JKKXZE
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 38%

---

# URL attività

L&#39;URL attività determina la pagina utilizzata nel test e che viene aperta quando il test viene progettato utilizzando [!DNL Adobe Target].

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l&#39;URL completo (incluso `https://`), quindi fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://www.adobe.com`] corrispondono entrambi.

## Specificare un URL diverso

Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

1. (Condizionale) Per visualizzare una pagina diversa dopo l&#39;apertura del [!UICONTROL Compositore esperienza visivo], nella pagina **[!UICONTROL Esperienze]** fai clic su **[!UICONTROL Configura]** nella parte superiore della pagina, quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Specifica l&#39;URL nel campo **[!UICONTROL URL]**.

1. (Condizionale) Fai clic su **[!UICONTROL Aggiungi regola]** per aggiungere più pagine o sezioni all&#39;attività.

   Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

   * URL
   * Dominio
   * Percorso
   * Frammento hash (#)
   * Query
   * Parametro mbox
   * Personalizzato

   È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate tra loro con E.

1. Al termine, fai clic su **[!UICONTROL Salva]**.

   Se hai inserito un URL per un sito che non include il codice JavaScript di [!DNL Target], non puoi selezionare elementi di pagina.

   Per impostazione predefinita, il [!UICONTROL Compositore esperienza visivo] non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando [!UICONTROL Compositore esperienza visivo].—>

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.
