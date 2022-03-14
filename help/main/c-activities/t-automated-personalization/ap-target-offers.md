---
keywords: personalizzazione automatizzata;offerte;target;pubblico;regole di targeting;targeting
description: Scopri come eseguire il targeting di singole offerte per tipi di pubblico specifici utilizzando un’attività Automated Personalization (AP) in Adobe Target.
title: Come posso [!DNL Target] Offerte Automated Personalization?
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 87%

---

# ![PREMIUM](/help/main/assets/premium.png) [!DNL Target] Offerte Automated Personalization

In un [!DNL Adobe Target] [!DNL Automated Personalization] (AP) puoi eseguire il targeting delle offerte per tipi di pubblico specifici.

Questa funzionalità riduce il numero di offerte per le quali un dato visitatore risulta idoneo (qualificato). Ad esempio, considera un’attività di Personalizzazione automatizzata con tre offerte. L’offerta 1 ha una regola di targeting che ne limita l’esposizione al solo Pubblico A. Due visitatori hanno visto questa attività.

|  | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualifica per pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50 | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché ha diritto all&#39;ambito del pubblico A), che è il punteggio più elevato del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il suo punteggio più elevato è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia dei modelli di personalizzazione di Target.

## Impostare le regole di targeting

1. Creare un’[attività di Personalizzazione automatizzata](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) contenente le offerte sulle quali desideri eseguire il targeting.
1. Dopo aver impostato le offerte per l’attività nel Compositore esperienza visivo, fai clic su **[!UICONTROL Gestione contenuto]**.

   ![Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata la finestra di dialogo Gestione contenuto.

1. Fai clic sulla scheda Offerte.

   ![Pagina Offerte](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Seleziona le offerte desiderate e scegli i tipi di pubblico che dovranno visualizzare l’offerta.

   Per impostare il targeting per una singola offerta, passa il cursore sull’offerta desiderata e fai clic sull’icona **[!UICONTROL Targeting]**.

   Per impostare il targeting per più offerte, seleziona la casella di controllo di ciascuna offerta e fai clic sull’icona **[!UICONTROL Targeting] che viene visualizzata in alto a destra dell’elenco.

1. Nella finestra di dialogo [!UICONTROL Scegli il pubblico], seleziona il pubblico desiderato per le offerte, quindi fai clic su **[!UICONTROL Fine]** per tornare alla finestra di dialogo [!UICONTROL Gestione contenuto].

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.

>[!NOTE]
>
>È possibile impostare fino a 50 posizioni e 250 offerte per posizione.
