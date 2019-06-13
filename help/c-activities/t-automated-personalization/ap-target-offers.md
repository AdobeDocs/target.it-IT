---
description: In un’attività di Personalizzazione automatizzata è possibile indirizzare le offerte a tipi di pubblico specifici.
seo-description: In un’attività di Personalizzazione automatizzata è possibile indirizzare le offerte a tipi di pubblico specifici.
seo-title: Targeting delle offerte di Personalizzazione automatizzata
solution: Target,Analytics
title: Targeting delle offerte di Personalizzazione automatizzata
title-outputclass: premium
uuid: 4ee30e1a-bfda-4b20-9313-99e32dcf60ac
badge: premium
translation-type: tm+mt
source-git-commit: 7b7f61efde2c72e6054dd8f08fbde2a395b6447c

---


# ![PREMIUM](/help/assets/premium.png) Targeting delle offerte di Personalizzazione automatizzata{#target-automated-personalization-offers}

In un&#39;attività di Automated Personalization (Personalizzazione automatizzata), potete eseguire il targeting delle offerte per audience specifiche.

Questa funzionalità riduce il numero di offerte che un visitatore specifico è qualificato per vedere. Ad esempio, considerate un&#39;attività AP con tre offerte. Offerta 1 ha una regola di targeting che limita l&#39;esposizione all&#39;Audience A. Due visitatori hanno visto questa attività AP.

|  | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualifica per pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50 | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché ha diritto all&#39;ambito del pubblico A), che è il punteggio più elevato del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il suo punteggio più elevato è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia dei modelli di personalizzazione di Target.

## Configurare le regole di targeting

1. Create un [&#39;attività di Automated Personalization](/help/c-activities/t-automated-personalization/create-ap-activity.md) (Personalizzazione automatizzata) contenente le offerte desiderate.
1. Dopo aver configurato le offerte per l&#39;attività in Visual Experience Composer (Compositore esperienza visivo), fate clic su **[!UICONTROL Manage Content (Gestisci contenuto]**).

   ![Gestire il contenuto](/help/c-activities/t-automated-personalization/assets/manage-content.png)

   Viene visualizzata la finestra di dialogo Gestione contenuto.

1. Fate clic sulla scheda Offerte.

   ![Offerte, pagina](/help/c-activities/t-automated-personalization/assets/manage-content-offers.png)

1. Selezionate le offerte desiderate e scegliete le audience da qualificare per visualizzare l&#39;offerta.

   Per impostare il targeting per una singola offerta, posizionate il puntatore sull&#39;offerta desiderata, quindi fate clic sull&#39;icona **[!UICONTORL Targeting]** .

   Per impostare il targeting per più offerte, selezionate le caselle di controllo delle offerte desiderate, quindi fate clic sull&#39;icona**[!UICONTROL Targeting] che viene visualizzata in alto a destra nell&#39;elenco.

1. Nella [!UICONTROL finestra di] dialogo Scegliete Audience, selezionate il pubblico desiderato per le offerte, quindi fate clic su **[!UICONTROL Fine]** per tornare alla finestra [!UICONTROL di] dialogo Gestisci contenuto.

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.

>[!NOTE]
>
>È possibile impostare fino a 50 posizioni e 250 offerte per posizione.
