---
keywords: Targeting;esperienza;aggiungere un’esperienza;aggiunta esperienza
description: Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) per aggiungere esperienze alle attività.
title: Come si aggiungono esperienze in un’attività A/B?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
TQID: 'https://experienceleague.adobe.com/7qEiUXkfMbPmtB2eMio0LztOYM3naHxG-WRQZOyMmlU'
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
source-git-commit: 9f1aaf5c0b172b4bbe89266800708881306e4592
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 25%
---
# Aggiungi esperienza {#ab-add-experience}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come aggiungere e progettare un&#39;esperienza in un&#39;attività A/B e come rinominarla, reindirizzarla, duplicarla o eliminarla.

>[!ENDSHADEBOX]

Il [!DNL Adobe Target] **[!UICONTROL Compositore esperienza visivo]** (VEC) fornisce un&#39;interfaccia visiva per l&#39;aggiunta e la modifica delle esperienze sulla pagina. Per ulteriori dettagli sulle esperienze, vedi [Esperienze](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

## Aggiungere e progettare un’esperienza {#add-experience}

Per aggiungere un’esperienza e modificarne la pagina:

1. Dalla pagina **[!UICONTROL Esperienze]** nel Compositore esperienza visivo, fai clic sull&#39;icona **[!UICONTROL Aggiungi]** ( ![Aggiungi icona](/help/main/assets/icons/Add.svg) ) nella parte superiore del riquadro **[!UICONTROL Esperienze]**.

   Dopo aver creato una nuova attività, nel Compositore esperienza visivo vengono visualizzate due schede sul lato sinistro: Esperienza A e Esperienza B. L’Esperienza A è l’esperienza di controllo. È possibile aggiungere più esperienze al test.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Quando passi il cursore del mouse sugli elementi nella pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo. Se hai creato una richiesta [!DNL Target] sulla pagina utilizzando [!DNL Target Classic] (precedentemente [!DNL Test&Target]), tale richiesta [!DNL Target] viene visualizzata come un elemento che mostra il nome della richiesta e può essere modificata come qualsiasi altro elemento.

   Per un elenco delle azioni che possono essere eseguite su un elemento nella pagina visualizzata per modificare l&#39;esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

1. Fai clic su **[!UICONTROL Avanti]** al termine della progettazione dell&#39;esperienza.

>[!NOTE]
>
>Se distribuisci un’immagine da un’origine che non corrisponde alla pagina principale (ad esempio un’immagine in hosting su `akamai.net` e distribuita su `example.com`), l’immagine non viene visualizzata nella miniatura della pagina mostrata nel diagramma di flusso.

## Rinominare un’esperienza {#rename-experience}

Per assegnare un nuovo nome a un&#39;esperienza:

1. Fai clic sull&#39;icona **[!UICONTROL Rinomina esperienza]** ( ![Rinomina icona](/help/main/assets/icons/Rename.svg) ) accanto all&#39;esperienza.

1. Specifica un nuovo nome, quindi fai clic su **[!UICONTROL Salva]**.

Quando denomini o rinomini un’esperienza, i seguenti caratteri non sono consentiti:

| Carattere | Descrizione |
|--- |--- |
| `/` | Barra |
| `?` | Punto interrogativo |
| `#` | Cancelletto |
| `:` | Due punti |
| `=` | Uguale |
| `+` | Più |
| `-` | Meno |
| `@` | Chiocciola |

## Reindirizzare un’esperienza a un URL {#redirect-to-url}

Per inviare i visitatori di un&#39;esperienza a un altro URL, vedi anche [Reindirizza all&#39;URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md):

1. Nel riquadro **[!UICONTROL Esperienze]** fare clic sull&#39;icona **[!UICONTROL Altro]** ( ![Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto all&#39;esperienza, quindi fare clic su **[!UICONTROL Reindirizza all&#39;URL]**.

1. Specifica l&#39;URL a cui reindirizzare l&#39;esperienza.

1. (Condizionale) Selezionare la casella di controllo **[!UICONTROL Includi parametri query correnti]**.

1. Fai clic su **[!UICONTROL Salva]**.

## Duplicare un’esperienza {#duplicate-experience}

È possibile copiare un’esperienza in un test A/B in modo da poter apportare modifiche minori senza dover ricreare l’esperienza. Nel riquadro **[!UICONTROL Esperienze]**, fai clic sull&#39;icona **[!UICONTROL Altro]** ( ![Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto all&#39;esperienza, quindi fai clic su **[!UICONTROL Duplica]**.

## Eliminare un’esperienza {#delete-experience}

Nel riquadro **[!UICONTROL Esperienze]**, fai clic sull&#39;icona **[!UICONTROL Altro]** ( ![Icona Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto all&#39;esperienza, fai clic su **[!UICONTROL Elimina]**, quindi su **[!UICONTROL Elimina]** per confermare l&#39;azione.
