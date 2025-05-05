---
keywords: Targeting;esperienza;aggiungere un’esperienza;aggiunta esperienza
description: Scopri come utilizzare il [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target].
title: Come si aggiungono esperienze in un'attività A/B di  [!DNL Target] ?
feature: A/B Tests
exl-id: c0f1b5a7-07b0-46c2-97f3-95dcc0fcbe3d
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 43%

---

# Aggiungi esperienza

Il [!DNL Adobe Target] [!UICONTROL Visual Experience Composer] (VEC) fornisce un&#39;interfaccia visiva per l&#39;aggiunta e la modifica delle esperienze sulla pagina.

Per ulteriori dettagli sulle esperienze, vedi [Esperienze](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D).

1. Dalla pagina **[!UICONTROL Experiences]** nel Compositore esperienza visivo, fai clic su **[!UICONTROL Add Experience]**.

   ![Opzione Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/add-experience.png)

   >[!NOTE]
   >
   >Se stai eseguendo il targeting di un&#39;esperienza per un pubblico, è necessario selezionare il pubblico prima di poter aggiungere un’esperienza. Viene visualizzato un messaggio per ricordarti di scegliere il pubblico.

1. Seleziona gli elementi da modificare e apporta le modifiche desiderate.

   Quando passi il cursore del mouse sugli elementi nella pagina, gli elementi vengono evidenziati. Qualsiasi elemento evidenziato può essere modificato utilizzando il Compositore esperienza visivo.

   Se hai creato una richiesta [!DNL Target] sulla pagina utilizzando [!DNL Target Classic] (precedentemente [!DNL Test&Target]), tale richiesta [!DNL Target] viene visualizzata come un elemento che mostra il nome della richiesta e può essere modificata come qualsiasi altro elemento.

   Per un elenco delle azioni che possono essere eseguite su un elemento nella pagina visualizzata per modificare l&#39;esperienza, consulta [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   >[!NOTE]
   >
   >Se distribuisci un’immagine da un’origine che non corrisponde alla pagina principale (ad esempio un’immagine in hosting su `akamai.net` e distribuita su `example.com`), l’immagine non viene visualizzata nella miniatura della pagina mostrata nel diagramma di flusso.

1. Fare clic su **[!UICONTROL Save]** al termine della progettazione dell&#39;esperienza.

## Rinominare un’esperienza

1. Fare clic sull&#39;icona **[!UICONTROL Rename Experience]** in un&#39;esperienza in un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] (XT) per assegnare un nuovo nome all&#39;esperienza.

   ![Rinomina esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/rename-experience.png)

2. Specifica un nuovo nome.

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

1. Fai clic sull&#39;icona **[!UICONTROL More]** (puntini di sospensione verticali) in un&#39;esperienza in un&#39;attività [!UICONTROL A/B Test] o [!UICONTROL Experience Targeting] (XT), quindi fai clic su **[!UICONTROL Redirect to URL]**.

   Per ulteriori informazioni, consulta [Reindirizzare verso un URL](/help/main/c-experiences/c-visual-experience-composer/redirect-offer.md).

   **NOTA**: quando denomini o rinomini un’esperienza, i seguenti caratteri non sono consentiti:

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

1. Specifica l&#39;URL a cui reindirizzare l&#39;esperienza.

1. (Condizionale) Selezionare la casella di controllo **[!UICONTROL Include Current Query Parameters]**.

## Duplicare un’esperienza

È possibile copiare un&#39;esperienza in un [!UICONTROL A/B Test] in modo da poter apportare modifiche minori senza dover ricreare l&#39;esperienza da zero.

1. Nella pagina **[!UICONTROL Experiences]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sull&#39;icona con puntini di sospensione verticali > **[!UICONTROL Duplicate]**.

   ![Opzione Duplica esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/duplicate-experience.png)

## Eliminare un’esperienza

1. Nella pagina **[!UICONTROL Experiences]** (il primo passaggio del flusso di lavoro guidato in tre passaggi), fai clic sull&#39;icona con puntini di sospensione verticali > **[!UICONTROL Duplicate]**.

   ![Opzione Elimina esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/delete-experience.png)

## Video di formazione: Utilizzo di [!UICONTROL Visual Experience Composer]

Il video seguente fornisce informazioni sull&#39;utilizzo delle opzioni [!UICONTROL Visual Experience Composer]. (7:17)

* Modificare il contenuto di una pagina
* Modificare il layout di una pagina

>[!VIDEO](https://video.tv.adobe.com/v/36326?captions=ita)
