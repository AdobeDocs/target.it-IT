---
description: Informazioni sull'uso dei gruppi di reporting nelle attività di Personalizzazione automatizzata (AP).
keywords: personalizzazione automatizzata;offerta;rapporto;gruppo
seo-description: Informazioni sull'uso dei gruppi di reporting nelle attività di Personalizzazione automatizzata (AP).
seo-title: Gruppi di reporting di offerte in Personalizzazione automatizzata
solution: Target
title: Gruppi di reporting di offerte in Personalizzazione automatizzata
title-outputclass: premium
topic: Advanced
uuid: 5b111a68-bd05-4ef1-8156-d064f2c7e257
badge: premium
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# ![PREMIUM](/help/assets/premium.png) Gruppi di creazione di rapporti di offerte in Personalizzazione automatizzata{#offer-reporting-groups-in-automated-personalization}

Informazioni sull'uso dei gruppi di reporting nelle attività di Personalizzazione automatizzata (AP).

I gruppi di reporting svolgono due funzioni chiave:

* Consentono di vedere le offerte raggruppate nel reporting delle attività di AP.
* Hanno un ruolo fondamentale nel funzionamento dei modelli di personalizzazione di Target.

Quando utilizzi i gruppi di reporting, Target crea un solo modello di personalizzazione per ciascun gruppo di reporting, anziché ogni offerta presente nella tua attività di AP, utilizzando i dati di tutte le offerte del gruppo.

Se la configurazione dell'attività non dispone di dati sufficienti per creare un modello di personalizzazione per ciascuna offerta, i gruppi di reporting possono contribuire a ridurre i requisiti di dati per utilizzare la Personalizzazione automatizzata. I gruppi di reporting consentono inoltre di risolvere il problema “Avvio a freddo” per le nuove offerte raggruppando offerte simili, in modo che ogni modello abbia più dati su cui basarsi. I gruppi di modeling possono essere utilizzati anche per attività in cui le nuove offerte vengono introdotte regolarmente nella tua attività di AP.

Questo approccio funziona bene se i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo. È consigliabile raggruppare offerte a cui gruppi simili di visitatori rispondono in modo simile. In altre parole, offerte per gruppi con tassi di conversione simili. È sconsigliabile mettere tutte le offerte in un unico gruppo di reporting. Raggruppare tutte le offerte o raggruppare offerte con tassi di conversione molto diversi riduce notevolmente l'efficacia dei modelli di personalizzazione di Target.

>[!NOTE]
>
>Se un’offerta viene eliminata o sostituita da un particolare gruppo di modeling, viene rimosso dal gruppo anche il traffico storico relativo a quell’offerta specifica. In altre parole, le offerte eliminate non contribuiscono ai dati utilizzati per l'apprendimento dei modelli di personalizzazione di Target.

**Per impostare i gruppi di reporting:**

1. Nella pagina Esperienze di un'attività di Personalizzazione automatizzata, fai clic sull'icona **[!UICONTROL Gestisci contenuto]**.

   ![](assets/ap_manage_content.png)

1. Fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore della finestra di dialogo [!UICONTROL Gestisci contenuto].
1. (Facoltativo) Aggiungi esperienze specifiche a un gruppo di reporting passando il mouse sull'offerta desiderata e facendo clic sull'icona della cartella **[!UICONTROL Gruppo di rapporti]**.

   ![](assets/ap_manage_content_2.png)

1. (Facoltativo) Si possono raccogliere le esperienze in gruppo di reporting selezionando la casella di spunta relativa alle esperienze desiderate e facendo clic sull'icona della cartella **[!UICONTROL Gruppo di rapporti]** nell'angolo in alto a destra della finestra di dialogo.

   ![](assets/ap_reporting_groups.png)

1. Per assegnare l'offerta selezionata a un gruppo di reporting esistente, seleziona **[!UICONTROL Esistente]**, seleziona il gruppo di reporting desiderato dall'elenco a discesa, quindi fai clic su **[!UICONTROL Applica]**.

   Oppure

   Per creare un nuovo gruppo di reporting a cui assegnare l'offerta selezionata, seleziona **[!UICONTROL Nuovo]**, dai un nome al nuovo gruppo di reporting, quindi fai clic su **[!UICONTROL Applica]**.

   ![](assets/ap_manage_content_3.png)

