---
keywords: personalizzazione automatizzata;offerte;target;pubblico;regole targeting;targeting;automated personalization;offers;target;audience;targeting rules;targeting rules;targeting rules;targeting
description: Scopri come indirizzare le singole offerte a tipi di pubblico specifici utilizzando un’ [!UICONTROL Automated Personalization] Attività di (AP) in [!DNL Adobe Target].
title: Come posso eseguire il targeting [!UICONTROL Automated Personalization] Offerte?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Automated Personalization
solution: Target,Analytics
exl-id: 633308dd-437b-4525-a7f8-69656c7d89be
source-git-commit: eacee6f353aa685d17b781ac82d3f79574384dfe
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 29%

---

# Target [!UICONTROL Automated Personalization] offerte

In un [!DNL Adobe Target] [!DNL Automated Personalization] (AP), puoi indirizzare le offerte a tipi di pubblico specifici.

Questa funzionalità riduce il numero di offerte per le quali un dato visitatore risulta idoneo (qualificato). Ad esempio, considera un’ [!UICONTROL Automated Personalization] attività con tre offerte. L&#39;offerta 1 ha una regola di targeting che ne limita l&#39;esposizione al Pubblico A. Due visitatori hanno visto questa attività.

| | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualificazione del pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50 | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché il visitatore si qualifica come parte del pubblico A), che è il punteggio più alto del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il punteggio più alto è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia di [!DNL Target] modelli di personalizzazione.

## Impostare le regole di targeting

1. Creare un [Attività Automated Personalization](/help/main/c-activities/t-automated-personalization/create-ap-activity.md) contenente le offerte sulle quali desideri eseguire il targeting.
1. Dopo aver impostato le offerte per l’attività in [!UICONTROL Compositore esperienza visivo], fai clic su **[!UICONTROL Gestione contenuto]**.

   ![Gestione contenuto](/help/main/c-activities/t-automated-personalization/assets/manage-content.png)

   Il [!UICONTROL Gestione contenuto] viene visualizzata.

1. Fai clic su **[!UICONTROL Offerte]** scheda.

   ![Pagina Offerte](/help/main/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Seleziona le offerte desiderate, quindi scegli il pubblico a cui desideri indirizzare l’offerta.

   Per impostare il targeting per una singola offerta, passa il cursore sull’offerta desiderata e fai clic sull’icona **[!UICONTROL Targeting]**.

   Per impostare il targeting per più offerte, seleziona la casella di controllo di ciascuna offerta e fai clic su **[!UICONTROL Targeting]** che viene visualizzata in alto a destra nell’elenco.

1. In [!UICONTROL Scegli pubblico] , seleziona il pubblico desiderato per le offerte, quindi fai clic su **[!UICONTROL Fine]** per tornare al [!UICONTROL Gestione contenuto] .

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.

>[!NOTE]
>
>È possibile impostare fino a 50 posizioni e 250 offerte per posizione.
