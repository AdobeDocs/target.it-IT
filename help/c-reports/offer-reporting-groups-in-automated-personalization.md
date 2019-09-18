---
description: Informazioni sull'uso dei gruppi di reporting nelle attività di Personalizzazione automatizzata (AP).
keywords: personalizzazione automatizzata;offerta;rapporto;gruppo;gruppo di rapporti
seo-description: Informazioni sull'utilizzo dei gruppi di reporting nelle attività di Automated Personalization (AP) in Adobe Target.
seo-title: Offrire gruppi di reporting nelle attività di Automated Personalization (AP) in Adobe Target
solution: Target
title: Gruppi di reporting di offerte in Personalizzazione automatizzata
title-outputclass: premium
topic: Advanced
uuid: 5b111a68-bd05-4ef1-8156-d064f2c7e257
badge: premium
translation-type: tm+mt
source-git-commit: 1df7fbf78f9e20d8a907809b228ed591036c1a24

---


# ![PREMIUM](/help/assets/premium.png) Gruppi di creazione di rapporti di offerte in Personalizzazione automatizzata{#offer-reporting-groups-in-automated-personalization}

Information about using reporting groups in [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) activities.

I gruppi di reporting svolgono due funzioni chiave:

* Consentono di vedere le offerte raggruppate nel reporting delle attività di AP.
* They play a key role with how the [!DNL Target] personalization models function.

When you use reporting groups, [!DNL Target] creates only one personalization model for each reporting group instead of each offer in your AP activity using the data from all offers in that group.

Se la configurazione dell'attività non dispone di dati sufficienti per creare un modello di personalizzazione per ciascuna offerta, i gruppi di reporting possono contribuire a ridurre i requisiti di dati per utilizzare la Personalizzazione automatizzata. I gruppi di reporting consentono inoltre di risolvere il problema “Avvio a freddo” per le nuove offerte raggruppando offerte simili, in modo che ogni modello abbia più dati su cui basarsi. I gruppi di modeling possono essere utilizzati anche per attività in cui le nuove offerte vengono introdotte regolarmente nella tua attività di AP.

Questo approccio funziona bene se i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo. È consigliabile raggruppare offerte a cui gruppi simili di visitatori rispondono in modo simile. In altre parole, offerte per gruppi con tassi di conversione simili. È sconsigliabile mettere tutte le offerte in un unico gruppo di reporting. Grouping all offers or grouping offers with very different conversion rates likely reduces the effectiveness of the [!DNL Target] personalization models.

>[!NOTE]
>
>Se un’offerta viene eliminata o sostituita da un particolare gruppo di modeling, viene rimosso dal gruppo anche il traffico storico relativo a quell’offerta specifica. In other words, deleted offers do not contribute to what data is used for the [!DNL Target] personalization models to learn.

**Per impostare i gruppi di reporting:**

1. On the [!UICONTROL Experiences] page of an AP activity, click the **[!UICONTROL Manage Content]** icon.

   ![](assets/ap_manage_content.png)

1. Fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore della finestra di dialogo [!UICONTROL Gestisci contenuto].
1. (Facoltativo) Aggiungi esperienze specifiche a un gruppo di reporting passando il mouse sull'offerta desiderata e facendo clic sull'icona della cartella **[!UICONTROL Gruppo di rapporti]**.

   ![](assets/ap_manage_content_2.png)

1. (Facoltativo) Si possono raccogliere le esperienze in gruppo di reporting selezionando la casella di spunta relativa alle esperienze desiderate e facendo clic sull'icona della cartella **[!UICONTROL Gruppo di rapporti]** nell'angolo in alto a destra della finestra di dialogo.

   ![](assets/ap_manage_content_3.png)

1. (Conditional) To assign the selected offer to an existing reporting group, select **[!UICONTROL Existing]**, select the desired reporting group from the drop-down list, then click **[!UICONTROL Apply]**.

   Oppure

   Per creare un nuovo gruppo di reporting a cui assegnare l'offerta selezionata, seleziona **[!UICONTROL Nuovo]**, dai un nome al nuovo gruppo di reporting, quindi fai clic su **[!UICONTROL Applica]**.

   ![](assets/ap_reporting_groups.png)

