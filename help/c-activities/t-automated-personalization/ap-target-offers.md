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
source-git-commit: 2baa75b6020b2f9229db68667c2e19a698954231

---


# ![PREMIUM](/help/assets/premium.png) Targeting delle offerte di Personalizzazione automatizzata{#target-automated-personalization-offers}

In un’attività di Personalizzazione automatizzata è possibile indirizzare le offerte a tipi di pubblico specifici.

Questa funzionalità riduce il numero di offerte che un visitatore specifico è qualificato per vedere. Ad esempio, considera un&#39;attività di personalizzazione automatica (AP) con tre offerte. L&#39;offerta 1 ha una regola di targeting che limita l&#39;esposizione solo al Pubblico A. Due visitatori hanno visto questa attività AP.

|  | Visitatore 1 | Visitatore 2 |
|--- |--- |--- |
| Qualifica per pubblico | Pubblico A | Pubblico B |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 1 | 90 | 90 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 2 | 50  | 70 |
| Punteggio del modello di personalizzazione di Target dell&#39;offerta 3 | 80 | 60 |

In questo scenario, il visitatore 1 vede l&#39;offerta 1 (perché ha diritto all&#39;ambito del pubblico A), che è il punteggio più elevato del visitatore. Tuttavia, il visitatore 2 vede l&#39;offerta 2 anche se il suo punteggio più elevato è per l&#39;offerta 1, perché il visitatore 2 non fa parte del pubblico A. Questo esempio dimostra perché le regole di targeting dovrebbero essere utilizzate con moderazione per soddisfare le esigenze aziendali. L&#39;aggiunta di queste regole può ridurre l&#39;efficacia dei modelli di personalizzazione di Target.

## Impostare le regole di targeting

1. Crea un’attività di Personalizzazione automatica contenente le offerte sulle quali desideri eseguire il targeting.
1. Dopo aver impostato le offerte per l’attività nel Compositore esperienza visivo, fai clic su **[!UICONTROL Contenuto]**.

   Viene visualizzata la finestra di dialogo Gestione contenuto.

   ![](assets/ap_content.png)

   >[!NOTE]
   >
   >È possibile impostare fino a 50 posizioni e 250 offerte per posizione.

1. Nella colonna **[!UICONTROL Contenuto]**, seleziona l’offerta, quindi fa clic su **[!UICONTROL Targeting]** e scegli il pubblico a cui desideri indirizzare l’offerta.

   Solo il pubblico selezionato riceverà tale offerta.

   >[!NOTE]
   >
   >Oltre a selezionare un pubblico esistente, puoi combinare più tipi di pubblico per creare un pubblico combinato ad hoc anziché crearne uno nuovo. Per ulteriori informazioni, consulta [Combinazione di più tipi di pubblico](../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

1. Fai clic su **[!UICONTROL Fine]**.
