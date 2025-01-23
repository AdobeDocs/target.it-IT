---
keywords: personalizzazione automatizzata;offerte;target;pubblico;regole targeting;targeting;automated personalization;offers;target;audience;targeting rules;targeting rules;targeting rules;targeting
description: Scopri come indirizzare singole offerte a tipi di pubblico specifici utilizzando le attività di [!UICONTROL Automated Personalization] (AP).
title: Come Posso Eseguire Il Targeting Di [!UICONTROL Automated Personalization] Offerte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
hide: true
hidefromtoc: true
exl-id: 2897c4d1-116d-483c-8fc0-64857b9cbdaf
source-git-commit: 2c10ec521ceed1901ef8c3f95eb11654a7182590
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 19%

---

# Targeting delle offerte [!UICONTROL Automated Personalization]

In un&#39;attività [!DNL Adobe Target] [!DNL Automated Personalization] (AP) è possibile indirizzare le offerte a tipi di pubblico specifici.

Questa funzionalità riduce il numero di offerte per le quali un dato visitatore risulta idoneo (qualificato). Consideriamo ad esempio un&#39;attività [!UICONTROL Automated Personalization] con tre offerte. L&#39;offerta 1 ha una regola di targeting che ne limita l&#39;esposizione al Pubblico A. Due visitatori hanno visto questa attività.

| | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualificazione del pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50 | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché il visitatore si qualifica come parte del pubblico A), che è il punteggio più alto del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il punteggio più alto è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia dei modelli di personalizzazione [!DNL Target].

## Impostare le regole di targeting

1. Crea o modifica un&#39;attività di [Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) contenente le offerte sulle quali desideri eseguire il targeting.
1. Dopo aver impostato le offerte per l&#39;attività in [!UICONTROL Visual Experience Composer], fare clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ).

   Viene visualizzata la finestra di dialogo [!UICONTROL Manage Content].

1. Fare clic sulla scheda **[!UICONTROL Offers]**.

1. Seleziona le offerte desiderate, quindi scegli il pubblico a cui desideri indirizzare l’offerta.

   Per impostare il targeting per una singola offerta, fai clic sull&#39;icona Ulteriori informazioni ( ![Icona Ulteriori informazioni](/help/main/assets/icons/MoreSmallList.svg) ) accanto all&#39;offerta desiderata, quindi fai clic su **[!UICONTROL Target Audience]** per visualizzare la finestra di dialogo [!UICONTROL Add Audiences].

   Per impostare il targeting per più offerte, seleziona le caselle di controllo per le offerte desiderate, quindi fai clic sul collegamento **[!UICONTROL Target Audience]** che viene visualizzato in fondo all&#39;elenco.

1. Nella finestra di dialogo [!UICONTROL Add Audiences], seleziona il pubblico desiderato per le offerte, quindi fai clic su **[!UICONTROL Assign Audience]** per tornare alla finestra di dialogo [!UICONTROL Manage Content].

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato su richiesta anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fare clic su **[!UICONTROL Done]**.

>[!NOTE]
>
>È possibile impostare fino a 50 posizioni e 250 offerte per posizione.
