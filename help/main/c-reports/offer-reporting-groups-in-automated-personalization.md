---
keywords: personalizzazione automatizzata;offerta;reporting;gruppo;gruppo di rapporti
description: Scopri come utilizzare i gruppi di reporting delle offerte in Adobe [!DNL Target] Attività Automated Personalization. Utilizzo dei gruppi di reporting, [!DNL Target] crea un solo modello di personalizzazione per ogni gruppo di reporting.
title: Posso utilizzare i gruppi di reporting delle offerte nelle attività di Automated Personalization?
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 152257a52d836a88ffcd76cd9af5b3fbfbdc0839
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 62%

---

# ![PREMIUM](/help/main/assets/premium.png) Gruppi di creazione di rapporti di offerte in Personalizzazione automatizzata

Informazioni sull’utilizzo dei gruppi di reporting in [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) attività.

I gruppi di reporting svolgono due funzioni chiave:

* Consentono di vedere le offerte raggruppate nel reporting delle attività di AP.
* Giocano un ruolo chiave nel modo in cui [!DNL Target] funzione dei modelli di personalizzazione.

Quando si utilizzano gruppi di reporting, [!DNL Target] crea un solo modello di personalizzazione per ogni gruppo di reporting, invece di ogni offerta nella tua attività di AP, utilizzando i dati di tutte le offerte in quel gruppo.

Se la configurazione dell&#39;attività non dispone di dati sufficienti per creare un modello di personalizzazione per ciascuna offerta, i gruppi di reporting possono contribuire a ridurre i requisiti di dati per utilizzare la Personalizzazione automatizzata. I gruppi di reporting consentono inoltre di risolvere il problema “Avvio a freddo” per le nuove offerte raggruppando offerte simili, in modo che ogni modello abbia più dati su cui basarsi. I gruppi di modeling possono essere utilizzati anche per attività in cui le nuove offerte vengono introdotte regolarmente nella tua attività di AP.

Questo approccio funziona bene se i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo. È consigliabile raggruppare offerte a cui gruppi simili di visitatori rispondono in modo simile. In altre parole, offerte per gruppi con tassi di conversione simili. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti. Raggruppare tutte le offerte o raggruppare le offerte con tassi di conversione molto diversi riduce probabilmente l’efficacia della [!DNL Target] modelli di personalizzazione.

>[!NOTE]
>
>Se un’offerta viene eliminata o sostituita da un particolare gruppo di modeling, viene rimosso dal gruppo anche il traffico storico relativo a quell’offerta specifica. In altre parole, le offerte eliminate non contribuiscono ai dati utilizzati per il [!DNL Target] modelli di personalizzazione da imparare.

**Per impostare i gruppi di reporting:**

1. Sulla [!UICONTROL Esperienze] pagina di un’attività di Personalizzazione automatizzata, fai clic sul pulsante **[!UICONTROL Gestire il contenuto]** icona.

   ![](assets/ap_manage_content.png)

1. Fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore della finestra di dialogo [!UICONTROL Gestisci contenuto].
1. (Facoltativo) Aggiungi esperienze specifiche a un gruppo di reporting passando il mouse sull&#39;offerta desiderata e facendo clic sull&#39;icona della cartella **[!UICONTROL Gruppo di rapporti]**.

   ![](assets/ap_manage_content_2.png)

1. (Facoltativo) Si possono raccogliere le esperienze in gruppo di reporting selezionando la casella di spunta relativa alle esperienze desiderate e facendo clic sull&#39;icona della cartella **[!UICONTROL Gruppo di rapporti]** nell&#39;angolo in alto a destra della finestra di dialogo.

   ![](assets/ap_manage_content_3.png)

1. (Condizionale) Per assegnare l&#39;offerta selezionata a un gruppo di reporting esistente, seleziona **[!UICONTROL Esistente]**, seleziona il gruppo di reporting desiderato dall’elenco a discesa, quindi fai clic su **[!UICONTROL Applica]**.

   Oppure

   Per creare un nuovo gruppo di reporting a cui assegnare l&#39;offerta selezionata, seleziona **[!UICONTROL Nuovo]**, dai un nome al nuovo gruppo di reporting, quindi fai clic su **[!UICONTROL Applica]**.

   ![](assets/ap_reporting_groups.png)
