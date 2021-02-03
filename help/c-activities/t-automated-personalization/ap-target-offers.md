---
keywords: personalizzazione automatizzata;offerte;target;audience;regole di targeting;targeting
description: In un’attività di Personalizzazione automatizzata è possibile indirizzare le offerte a tipi di pubblico specifici.
title: ' offerte Automated Personalization '
feature: Automated Personalization
solution: Target,Analytics
translation-type: tm+mt
source-git-commit: 48b94f967252f5ddb009597456edf0a43bc54ba6
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 93%

---


# ![PREMIUM](/help/assets/premium.png) Targeting delle offerte di Personalizzazione automatizzata{#target-automated-personalization-offers}

In un&#39;attività [!DNL Adobe Target] [!DNL Automated Personalization] (AP), potete eseguire il targeting delle offerte per audience specifiche.

Questa funzionalità riduce il numero di offerte per le quali un dato visitatore risulta idoneo (qualificato). Ad esempio, considera un’attività di Personalizzazione automatizzata con tre offerte. L’offerta 1 ha una regola di targeting che ne limita l’esposizione al solo Pubblico A. Due visitatori hanno visto questa attività.

|  | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualifica per pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50 | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché ha diritto all&#39;ambito del pubblico A), che è il punteggio più elevato del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il suo punteggio più elevato è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia dei modelli di personalizzazione di Target.

## Impostare le regole di targeting

1. Creare un’[attività di Personalizzazione automatizzata](/help/c-activities/t-automated-personalization/create-ap-activity.md) contenente le offerte sulle quali desideri eseguire il targeting.
1. Dopo aver impostato le offerte per l’attività nel Compositore esperienza visivo, fai clic su **[!UICONTROL Gestione contenuto]**.

   ![Gestione contenuto](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata la finestra di dialogo Gestione contenuto.

1. Fai clic sulla scheda Offerte.

   ![Pagina Offerte](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Seleziona le offerte desiderate e scegli i tipi di pubblico che dovranno visualizzare l’offerta.

   Per impostare il targeting per una singola offerta, passa il cursore sull’offerta desiderata e fai clic sull’icona **[!UICONTROL Targeting]**.

   Per impostare il targeting per più offerte, seleziona la casella di controllo di ciascuna offerta e fai clic sull’icona **[!UICONTROL Targeting] che viene visualizzata in alto a destra dell’elenco.

1. Nella finestra di dialogo [!UICONTROL Scegli il pubblico], seleziona il pubblico desiderato per le offerte, quindi fai clic su **[!UICONTROL Fine]** per tornare alla finestra di dialogo [!UICONTROL Gestione contenuto].

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.

>[!NOTE]
>
>È possibile impostare fino a 50 posizioni e 250 offerte per posizione.
