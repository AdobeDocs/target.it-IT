---
keywords: personalizzazione automatizzata;offerta;reporting;gruppo;gruppo di reporting;ap
description: Scopri come utilizzare i gruppi di reporting di offerte nelle attività di [!DNL Adobe Target] [!UICONTROL Automated Personalization].
title: Posso utilizzare i gruppi di reporting di offerte nelle attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 15%

---

# Gruppi di reporting di offerte in [!UICONTROL Automated Personalization]

Informazioni sull&#39;utilizzo dei gruppi di reporting nelle attività di [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP).

I gruppi di reporting svolgono due funzioni chiave:

* I gruppi di reporting consentono di visualizzare le offerte raggruppate nel reporting delle attività di AP.
* I gruppi di reporting svolgono un ruolo chiave nel funzionamento dei modelli di personalizzazione [!DNL Target].

Quando si utilizzano i gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni gruppo di reporting utilizzando i dati di tutte le offerte del gruppo. Senza gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni offerta nell&#39;attività di Personalizzazione automatizzata.

Se la configurazione dell&#39;attività non dispone di dati sufficienti per creare un modello di personalizzazione per offerta, i gruppi di reporting contribuiscono a ridurre i requisiti di dati per utilizzare [!UICONTROL Automated Personalization]. I gruppi di reporting consentono inoltre di risolvere il problema “Avvio a freddo” per le nuove offerte raggruppando offerte simili, in modo che ogni modello abbia più dati su cui basarsi. I gruppi di modeling possono essere utilizzati anche per attività in cui le nuove offerte vengono introdotte regolarmente nell’attività di AP.

Questo approccio funziona bene se i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo. È consigliabile raggruppare offerte a cui gruppi simili di visitatori rispondono in modo simile. In altre parole, offerte per gruppi con tassi di conversione simili. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti. Il raggruppamento di tutte le offerte o le offerte con tassi di conversione diversi riduce probabilmente l&#39;efficacia dei modelli di personalizzazione [!DNL Target].

>[!NOTE]
>
>Se un’offerta viene eliminata o sostituita da un particolare gruppo di modeling, viene rimosso dal gruppo anche il traffico storico relativo a quell’offerta specifica. In altre parole, le offerte eliminate non contribuiscono ai dati utilizzati per l&#39;apprendimento dei modelli di personalizzazione [!DNL Target].

## Configurare gruppi di reporting

1. Nella pagina **[!UICONTROL Experiences]** di un&#39;attività di Personalizzazione automatizzata, fare clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestione contenuto](/help/main/assets/icons/Experience.svg) )
1. Fare clic sulla scheda **[!UICONTROL Offers]** nella parte superiore della finestra di dialogo [!UICONTROL Manage Content].
1. (Condizionale) Aggiungi esperienze specifiche a un gruppo di reporting facendo clic sull&#39;icona [!UICONTROL More Actions] ( ![icona Altre azioni](/help/main/assets/icons/MoreSmall.svg) ) per l&#39;offerta desiderata e quindi facendo clic su **[!UICONTROL Reporting Group]**.

1. (Facoltativo) Si possono raccogliere le esperienze in gruppo di reporting selezionando le caselle di controllo relative alle esperienze desiderate e facendo clic su **[!UICONTROL Reporting Group]** nella parte inferiore della finestra di dialogo.

1. Per assegnare l&#39;offerta selezionata a un gruppo di reporting esistente, selezionare **[!UICONTROL Existing]**, selezionare il gruppo di reporting desiderato dall&#39;elenco a discesa, quindi fare clic su **[!UICONTROL Confirm]**.

   Oppure

   Per creare un gruppo di reporting a cui assegnare l&#39;offerta selezionata, selezionare **[!UICONTROL New]**, assegnare un nome al nuovo gruppo di reporting, quindi fare clic su **[!UICONTROL Confirm]**.

È possibile utilizzare l&#39;elenco [!UICONTROL Location] per filtrare le offerte in base alla posizione. Utilizzare l&#39;elenco [!UICONTROL Report Group] per filtrare le offerte in base ai gruppi di reporting. È inoltre possibile utilizzare l&#39;elenco [!UICONTROL Report Group] per filtrare [!UICONTROL Unassigned Offers] in modo da assegnare un gruppo di reporting a un&#39;offerta che non è attualmente assegnata ad alcun gruppo di reporting.

Per informazioni su come indirizzare un&#39;offerta a tipi di pubblico specifici, consulta [Offerte [!UICONTROL Automated Personalization] di Target](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#task_F207ED7A41B84FD39BB6FCBFABF4B23E).

## Avvertenze

* È importante comprendere che i gruppi di reporting influiscono sul modo in cui [!DNL Target] crea i propri modelli. Di conseguenza, [!DNL Adobe] consiglia di utilizzare i gruppi di reporting solo se si intende sostituire o aggiungere nuove offerte mentre un&#39;attività è in esecuzione. Se una nuova offerta viene introdotta in un’attività live, inserendo la nuova offerta in un gruppo con offerte simili esistenti, la macchina può utilizzare i dati già raccolti per le altre offerte del gruppo per scoprire la nuova offerta. È sconsigliabile mettere tutte le offerte in un unico gruppo di rapporti.

* Le attività di Personalizzazione automatizzata hanno combinazioni di posizione + offerta (modellabili). Quando [!DNL Target] registra i dati nei rapporti, [!DNL Target] considera tali combinazioni in modo che sia chiaro da quale evento (visualizzazione, clic e così via) è arrivata l&#39;offerta.

  Ad esempio, un’attività potrebbe avere più posizioni e diverse offerte, che potrebbero sovrapporsi. Se un visitatore vede più di una di queste offerte in posizioni diverse, [!DNL Target] registra i dati solo per tali offerte. Se lo stesso visitatore fa successivamente clic su un&#39;offerta, [!DNL Target] registra un evento solo da tale combinazione (non per tutte le combinazioni).

  Allo stesso modo, se il clic proviene da una posizione diversa, presente in una metrica, ma che non visualizza un’offerta, questo evento viene registrato nell’attività, ma non per qualsiasi combinazione di offerta e posizione. Di conseguenza, questa offerta non viene visualizzata nel gruppo di reporting delle offerte.

  Questo comportamento è dovuto al fatto che il clic potrebbe provenire da una mbox diversa e non dalla mbox che ha fornito l’offerta. Per questo motivo, la metrica è associata all’attività, ma non all’offerta.

## Visualizzare le offerte in un gruppo di reporting

1. Fai clic su **[!UICONTROL Activities]**, fai clic sull&#39;attività [!UICONTROL Automated Personalization] desiderata dall&#39;elenco, quindi fai clic sulla scheda **[!UICONTROL Reports]** per visualizzare il report [Livello di offerta](/help/main/c-reports/personalization-reports/reports-ap.md).

   Se hai numerose attività, fai clic sull&#39;icona [!UICONTROL Show Filters] (funnel), quindi seleziona la casella di controllo [!UICONTROL Automated Personalization] per filtrare l&#39;elenco in modo da visualizzare solo [!UICONTROL Automated Personalization] attività.

1. Fare clic su **[!UICONTROL Control]** o **[!UICONTROL Targeted]** nella tabella per visualizzare le offerte e le offerte non raggruppate all&#39;interno dei gruppi di reporting.

   ![Gruppi di offerte: controllo e destinazione](/help/main/c-reports/c-report-settings/assets/offer-groups.png)

Per informazioni sull&#39;utilizzo di [!UICONTROL Automated Personalization] report (incluso il report [!UICONTROL Offer Level]), vedere [Report di riepilogo di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).
