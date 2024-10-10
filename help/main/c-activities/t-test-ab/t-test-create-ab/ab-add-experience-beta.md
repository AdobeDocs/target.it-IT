---
keywords: Targeting;esperienza;aggiungere un’esperienza;aggiunta esperienza
description: Padroneggiare utilizzando [!UICONTROL Visual Experience Composer] (VEC) per aggiungere esperienze alle attività.
title: Come si aggiungono esperienze in un’attività A/B?
feature: A/B Tests
hide: true
hidefromtoc: true
source-git-commit: 6e9d18b8347d8ae68be699640c4cde91bdec762c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 28%

---

# Aggiungi esperienza

Il [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) fornisce un&#39;interfaccia visiva per l&#39;aggiunta e la modifica delle esperienze sulla pagina.

Per ulteriori dettagli sulle esperienze, vedi [Esperienze](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

1. Dalla pagina **[!UICONTROL Experiences]** nel Compositore esperienza visivo, fai clic sull&#39;icona [!UICONTROL Add] ( ![icona Aggiungi](/help/main/assets/icons/Add.svg) ) nella parte superiore del riquadro [!UICONTROL Experiences].

   Dopo aver creato una nuova attività, il Compositore esperienza visivo visualizza due schede a sinistra: Esperienza A e Esperienza B. L’esperienza A è l’esperienza di controllo. Puoi aggiungere più esperienze al test.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Quando passi il cursore del mouse sugli elementi nella pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo.

   Se hai creato una richiesta [!DNL Target] sulla pagina utilizzando [!DNL Target Classic] (precedentemente [!DNL Test&Target]), tale richiesta [!DNL Target] viene visualizzata come un elemento che mostra il nome della richiesta e può essere modificata come qualsiasi altro elemento.

   Per un elenco delle azioni che possono essere eseguite su un elemento nella pagina visualizzata per modificare l&#39;esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Se distribuisci un’immagine da un’origine che non corrisponde alla pagina principale (ad esempio un’immagine in hosting su `akamai.net` e distribuita su `example.com`), l’immagine non viene visualizzata nella miniatura della pagina mostrata nel diagramma di flusso.

1. Fare clic su **[!UICONTROL Next]** al termine della progettazione dell&#39;esperienza.

## Rinominare un’esperienza

1. Fai clic sull&#39;icona **[!UICONTROL Rename Experience]** ( ![Icona Rinomina](/help/main/assets/icons/Rename.svg) ) accanto a un&#39;esperienza per assegnarle un nuovo nome.

2. Specificare un nuovo nome, quindi fare clic su **[!UICONTROL Save]**.

   Quando denomini o rinomini un’esperienza, i seguenti caratteri non sono consentiti:

   | Carattere | Descrizione |
   |--- |--- |
   | / | Barra |
   | ? | Punto interrogativo |
   | # | Cancelletto |
   | : | Due punti |
   | = | Uguale |
   | + | Più |
   | - | Meno |
   | @ | Chiocciola |

## Reindirizzare verso un URL

1. Nel riquadro **[!UICONTROL Experiences]** fare clic sull&#39;icona **[!UICONTROL More]** ( ![Icona Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto a un&#39;esperienza, quindi fare clic su **[!UICONTROL Redirect to URL]**.

   Per ulteriori informazioni, consulta [Reindirizzare verso un URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

1. Specifica l&#39;URL a cui reindirizzare l&#39;esperienza.

1. (Condizionale) Selezionare la casella di controllo **[!UICONTROL Include Current Query Parameters]**.

1. Fare clic su **[!UICONTROL Save]**.

## Duplicare un’esperienza

È possibile copiare un&#39;esperienza in un [!UICONTROL A/B Test] in modo da poter apportare modifiche minori senza dover ricreare l&#39;esperienza.

1. Nel riquadro **[!UICONTROL Experiences]** fare clic sull&#39;icona **[!UICONTROL More]** ( ![Icona Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto a un&#39;esperienza, quindi fare clic su **[!UICONTROL Duplicate]**.

## Eliminare un’esperienza

1. Nel riquadro **[!UICONTROL Experiences]** fare clic sull&#39;icona **[!UICONTROL More]** ( ![Icona Altro](/help/main/assets/icons/MoreSmall.svg) ) accanto a un&#39;esperienza, fare clic su **[!UICONTROL Delete]**, quindi fare clic su **[!UICONTROL Delete]** per confermare l&#39;azione.