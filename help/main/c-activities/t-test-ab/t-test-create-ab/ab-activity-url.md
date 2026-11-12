---
keywords: url attività;url;url diverso
description: Scopri come impostare l’[!UICONTROL URL attività] in un’attività A/B, Targeting esperienza o Test multivariato per definire le pagine di test e garantire una progettazione accurata dei test.
title: Qual è l’URL attività in un’attività A/B, Targeting esperienza o Test multivariato?
feature: A/B Tests
exl-id: 7f1b8364-790d-4767-bff3-4217ced1a77b
reason: republish
TQID: 'https://experienceleague.adobe.com/arQWsSfBKYtrayq9AI8ejU1T-Uor-oL5j2Sp2JKKXZE'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: aad553690f1f399177214c94a2276d038f46d9cb
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 25%
---
# URL attività {#ab-activity-url}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come specificare l&#39;URL attività di un&#39;attività A/B, Targeting esperienza o Test multivariato (MVT), come visualizzare una pagina diversa e come aggiungere regole per più pagine o sezioni.

>[!ENDSHADEBOX]

L&#39;[!UICONTROL URL attività] determina la pagina utilizzata nell&#39;attività. Questa è la pagina che si apre nel [!UICONTROL Compositore esperienza visivo] o nel [!UICONTROL Compositore esperienza basato su moduli] quando l&#39;attività è progettata in [!DNL Adobe Target].

## Specifica l’URL dell’attività {#specify-url}

Quando viene richiesto durante la creazione dell’attività, specifica l’URL attività. Digita l&#39;URL completo (incluso `https://`), quindi fai clic su **[!UICONTROL Crea]**.

>[!NOTE]
>
>[!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com/it`] e [!DNL `https://www.adobe.com/it`] corrispondono entrambi.

Se si specifica un URL per un sito che non include la libreria JavaScript di [!DNL Target] [at.js o  [!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html?lang=it){target=_blank}, non è possibile selezionare elementi di pagina.

## Visualizza una pagina diversa {#different-page}

Per impostazione predefinita, il Compositore esperienza visivo o il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md) apre la pagina specificata nelle [impostazioni del Compositore esperienza visivo](/help/main/administrating-target/visual-experience-composer-set-up.md). È possibile specificare una pagina diversa durante la creazione dell’attività.

Per visualizzare una pagina diversa dopo l’apertura del Compositore esperienza visivo:

1. Nella pagina **[!UICONTROL Esperienze]**, fai clic su **[!UICONTROL Configura]** nella parte superiore della pagina, quindi seleziona **[!UICONTROL Consegna pagine]**.

1. Specifica l&#39;URL nel campo **[!UICONTROL URL]**.

1. Al termine, fai clic su **[!UICONTROL Salva]**.

Per impostazione predefinita, il Compositore esperienza visivo non consente di modificare gli elementi contenenti JavaScript, ad esempio i banner rotanti. Puoi disattivare **[!UICONTROL Esegui rendering con JavaScript]** se desideri modificare tali elementi utilizzando il Compositore esperienza visivo.

>[!NOTE]
>
>Se modifichi l’URL dopo aver apportato modifiche a una pagina per una o più esperienze, l’esperienza viene reimpostata utilizzando la nuova pagina e le modifiche apportate andranno perse.

## Aggiungere regole per più pagine o sezioni {#add-rules}

Per aggiungere altre pagine o sezioni all&#39;attività, fai clic su **[!UICONTROL Aggiungi regola]** nelle impostazioni **[!UICONTROL Consegna pagine]**, quindi fai clic su **[!UICONTROL Salva]** al termine.

Le regole aggiuntive possono essere basate su uno dei seguenti elementi:

* URL
* Dominio
* Percorso
* Frammento hash (#)
* Query
* Parametro mbox
* Personalizzato

È possibile unire ulteriori regole all’URL attività con AND o OR. Tutte le regole aggiunte vengono valutate tra loro con E.
