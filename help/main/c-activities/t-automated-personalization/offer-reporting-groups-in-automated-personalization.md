---
keywords: personalizzazione automatizzata;offerta;reporting;gruppo;gruppo di rapporti;app
description: Scopri come utilizzare i gruppi di reporting delle offerte in Adobe [!DNL Target] [!UICONTROL Automated Personalization] attività.
title: Posso utilizzare i gruppi di reporting delle offerte nelle attività di Automated Personalization?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="See what's included in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: bde5506033fbca1577fad1cda1af203702fc4bb3
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 30%

---

# Gruppi di reporting di offerte in [!UICONTROL Automated Personalization]

Informazioni sull’utilizzo dei gruppi di reporting in [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) attività.

I gruppi di reporting svolgono due funzioni chiave:

* I gruppi di reporting ti consentono di visualizzare le offerte raggruppate nel reporting delle attività di Personalizzazione automatizzata.
* I gruppi di reporting svolgono un ruolo chiave nel modo in cui [!DNL Target] funzione dei modelli di personalizzazione.

Quando si utilizzano gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni gruppo di reporting utilizzando i dati di tutte le offerte in quel gruppo. Senza gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni offerta nell&#39;attività di Personalizzazione automatizzata.

Se la configurazione dell’attività non dispone di dati sufficienti per creare un modello di personalizzazione per ogni offerta, i gruppi di reporting possono contribuire a ridurre i requisiti di dati da utilizzare [!UICONTROL Automated Personalization]. I gruppi di reporting consentono inoltre di risolvere il problema “Avvio a freddo” per le nuove offerte raggruppando offerte simili, in modo che ogni modello abbia più dati su cui basarsi. I gruppi di modeling possono essere utilizzati anche per attività in cui le nuove offerte vengono introdotte regolarmente nella tua attività di AP.

Questo approccio funziona bene se i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo. È consigliabile raggruppare offerte a cui gruppi simili di visitatori rispondono in modo simile. In altre parole, offerte per gruppi con tassi di conversione simili. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti. Raggruppare tutte le offerte o raggruppare le offerte con tassi di conversione diversi riduce probabilmente l’efficacia della [!DNL Target] modelli di personalizzazione.

>[!NOTE]
>
>Se un’offerta viene eliminata o sostituita da un particolare gruppo di modeling, viene rimosso dal gruppo anche il traffico storico relativo a quell’offerta specifica. In altre parole, le offerte eliminate non contribuiscono ai dati utilizzati per il [!DNL Target] modelli di personalizzazione da imparare.

## Imposta gruppi di reporting

1. Sulla **[!UICONTROL Esperienze]** pagina di un’attività di Personalizzazione automatizzata, fai clic sul pulsante **[!UICONTROL Gestire il contenuto]** icona.

   ![Icona Gestione contenuto](/help/main/c-reports/assets/ap_manage_content.png)

1. Fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore della finestra di dialogo [!UICONTROL Gestisci contenuto].
1. (Facoltativo) Aggiungi esperienze specifiche a un gruppo di reporting passando il mouse sull&#39;offerta desiderata e facendo clic sull&#39;icona della cartella **[!UICONTROL Gruppo di rapporti]**.

   ![Icona Gruppo di rapporti](/help/main/c-reports/assets/ap_manage_content_2.png)

1. (Facoltativo) Per raccogliere in batch le esperienze in un gruppo di reporting, seleziona la casella di controllo per le esperienze rilevanti e fai clic sul pulsante **[!UICONTROL Gruppo di reporting]** nell’angolo in alto a destra della finestra di dialogo.

   ![Icona Gruppo di rapporti](/help/main/c-reports/assets/ap_manage_content_3.png)

1. Per assegnare l&#39;offerta selezionata a un gruppo di reporting esistente, seleziona **[!UICONTROL Esistente]**, seleziona il gruppo di reporting desiderato dall&#39;elenco a discesa, quindi fai clic su **[!UICONTROL Applica]**.

   Oppure

   Per creare un gruppo di reporting a cui assegnare l&#39;offerta selezionata, seleziona **[!UICONTROL Nuovo]**, denomina il nuovo gruppo di reporting, quindi fai clic su **[!UICONTROL Applica]**.

   ![Nuova icona per creare un nuovo gruppo di rapporti](/help/main/c-reports/assets/ap_reporting_groups.png)

È possibile utilizzare [!UICONTROL Posizione] elenco per filtrare le offerte in base alla posizione. Utilizza l&#39;elenco [!UICONTROL Gruppo di rapporti] per filtrare le offerte in base ai gruppi di rapporti. È inoltre possibile utilizzare l&#39;elenco [!UICONTROL Gruppo di rapporti] per filtrare le [!UICONTROL Offerte non assegnate] così da poter assegnare un gruppo di rapporti a un&#39;offerta attualmente non assegnata ad alcun gruppo di rapporti.

Per informazioni su come indirizzare un’offerta a tipi di pubblico specifici, consulta [Offerte Personalizzazione automatizzata di Target](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Avvertenze

* È importante comprendere che i gruppi di reporting influiscono su come [!DNL Target] crea i suoi modelli. Di conseguenza, [!DNL Adobe] consiglia di utilizzare i gruppi di reporting solo se si prevede di sostituire o aggiungere nuove offerte mentre un&#39;attività è in esecuzione. Se viene introdotta una nuova offerta in un’attività live, inserirla in un gruppo con offerte simili esistenti consente al computer di utilizzare i dati già raccolti per le altre offerte del gruppo per conoscere la nuova offerta. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti.

* Le attività di Personalizzazione automatizzata hanno combinazioni di posizione+offerta (modelli). Quando [!DNL Target] i dati registrati nelle relazioni, [!DNL Target] considera tali combinazioni in modo che sia chiaro da quale evento (visualizzazione, clic e così via) è arrivata l&#39;offerta.

   Ad esempio, un’attività potrebbe avere diverse posizioni e diverse offerte, che potrebbero sovrapporsi. Se un visitatore visualizza più di una di queste offerte in posizioni diverse, [!DNL Target] registra i dati solo per tali offerte. Se lo stesso visitatore fa clic successivamente su un’offerta, [!DNL Target] registra un evento solo da tale combinazione (non per tutte le combinazioni).

   Allo stesso modo, se il clic proviene da una posizione diversa, presente in una metrica, ma che non visualizza un’offerta, questo evento viene registrato nell’attività, ma non per alcuna combinazione offerta+posizione. Di conseguenza, questa offerta non viene visualizzata nel gruppo di reporting delle offerte.

   Questo comportamento è dovuto al fatto che il clic potrebbe essere effettuato da una mbox diversa e non dalla mbox che ha servito l&#39;offerta. Per questo motivo, la metrica è associata all’attività , ma non all’offerta.

## Visualizzare le offerte in un gruppo di reporting

1. Fai clic su **[!UICONTROL Attività]**, fai clic sul [!UICONTROL Automated Personalization] dall’elenco, quindi fai clic sul pulsante **[!UICONTROL Rapporti]** per visualizzare la scheda [Livello di offerta](/help/main/c-reports/personalization-reports/reports-ap.md) rapporto.

   Se hai numerose attività, puoi filtrare l’elenco selezionando [!UICONTROL Personalizzazione automatizzata] dall’elenco a discesa [!UICONTROL Tipo].

1. Fai clic su **[!UICONTROL Controllo]** o **[!UICONTROL Target]** nella tabella per visualizzare le offerte e le offerte non raggruppate all’interno dei gruppi di reporting.

   ![Gruppi di offerte: Controllo e targeting](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Per informazioni sull&#39;utilizzo [!UICONTROL Automated Personalization] (compresi i [!UICONTROL Livello di offerta] rapporto), vedi [Report di riepilogo di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).


