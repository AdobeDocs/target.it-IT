---
keywords: personalizzazione automatizzata;offerta;reporting;gruppo;gruppo di reporting;ap
description: Scopri come utilizzare i gruppi di reporting di offerte nelle attività [!DNL Adobe Target] [!UICONTROL Automated Personalization].
title: Posso utilizzare i gruppi di reporting di offerte nelle [!UICONTROL attività Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Reports
exl-id: 9058a6c5-c651-480f-9b23-d0782a13b042
TQID: 'https://experienceleague.adobe.com/VW3zVGXb3IuQMDaRyidbkjsbUrojvwFsvwP3yRVeHp4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: e8a43148-398f-56c7-9433-6564f96999c2
    internal-label: Reports
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 44c6bdd4ab818226e76477782d7e4238b49d5cdc
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 3%
---
# Gruppi di reporting di offerte in [!UICONTROL Automated Personalization] {#offer-reporting-groups}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come funzionano i gruppi di reporting delle offerte nelle attività di **[!UICONTROL Automated Personalization]**, come configurarli e come visualizzarli nei rapporti.

>[!ENDSHADEBOX]

I gruppi di reporting consentono di organizzare le offerte di un&#39;attività [!DNL Adobe Target] [Automated Personalization](/help/main/c-activities/t-automated-personalization/automated-personalization.md) (AP) in gruppi. I gruppi di reporting svolgono due funzioni chiave:

* Consentono di vedere le offerte raggruppate nel reporting delle attività di PA.
* Hanno un ruolo chiave nel funzionamento dei modelli di personalizzazione [!DNL Target].

Quando si utilizzano i gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni gruppo di reporting, utilizzando i dati di tutte le offerte del gruppo. Senza gruppi di reporting, [!DNL Target] crea un modello di personalizzazione per ogni offerta nell&#39;attività di Personalizzazione automatizzata.

I gruppi di reporting riducono inoltre i requisiti di dati per utilizzare **[!UICONTROL Automated Personalization]** quando la configurazione dell&#39;attività non dispone di dati sufficienti per creare un modello di personalizzazione per offerta. Sono utili per risolvere il problema dell’avvio a freddo delle nuove offerte, che sono raggruppate con offerte simili, in modo che ogni modello abbia più dati su cui formarsi.

Questo approccio funziona bene quando i visitatori rispondono allo stesso modo a tutte le offerte di un gruppo, pertanto le offerte di gruppo con tassi di conversione simili. Non mettere mai tutte le offerte in un unico gruppo di reporting e non raggruppare le offerte con tassi di conversione diversi, perché entrambe le scelte probabilmente ridurranno l&#39;efficacia dei modelli di personalizzazione [!DNL Target].

>[!NOTE]
>
>Se un&#39;offerta viene rimossa o sostituita in un gruppo di reporting, anche il traffico storico relativo a tale offerta viene eliminato dal gruppo, pertanto le offerte eliminate non contribuiscono ai dati utilizzati dai modelli di personalizzazione [!DNL Target] per apprendere.


## Considerazioni

### Utilizzare i gruppi di reporting per le attività live

I gruppi di reporting influiscono sul modo in cui [!DNL Target] crea i propri modelli. Di conseguenza, [!DNL Adobe] consiglia di utilizzare i gruppi di reporting solo se si intende sostituire o aggiungere offerte mentre un&#39;attività è in esecuzione. Se una nuova offerta viene introdotta in un&#39;attività live, inserendo la nuova offerta in un gruppo con offerte simili esistenti, [!DNL Target] potrà utilizzare i dati già raccolti per le altre offerte del gruppo per conoscere la nuova offerta.

### Registrazione dei dati per offerte e posizioni

Le attività di Personalizzazione automatizzata hanno combinazioni di posizione e offerta (modellabili). Quando [!DNL Target] registra i dati nei rapporti, considera queste combinazioni, quindi è chiaro da quale evento (visualizzazione, clic e così via) è arrivata l&#39;offerta.

Ad esempio, un’attività potrebbe avere più posizioni e diverse offerte, che potrebbero sovrapporsi. Se un visitatore vede più di una di queste offerte in posizioni diverse, [!DNL Target] registra i dati solo per tali offerte. Se lo stesso visitatore fa successivamente clic su un&#39;offerta, [!DNL Target] registra un evento solo da tale combinazione (non per tutte le combinazioni).

Allo stesso modo, se il clic proviene da una posizione diversa presente in una metrica ma che non visualizza un’offerta, l’evento viene registrato nell’attività, ma non per qualsiasi combinazione di offerta e posizione. Di conseguenza, questa offerta non viene visualizzata nel gruppo di reporting delle offerte. Questo comportamento si verifica perché il clic potrebbe essere stato fatto da una mbox diversa da quella che ha servito l’offerta. In tal caso, la metrica è associata all’attività, ma non all’offerta.

## Configurare gruppi di reporting

L&#39;assegnazione delle offerte ai gruppi di reporting determina il modo in cui [!DNL Target] crea i modelli di personalizzazione e il modo in cui le offerte vengono visualizzate nei rapporti attività. Imposta i gruppi durante la creazione dell’attività o in un secondo momento, se aggiungi nuove offerte a un’attività live.

1. Nella pagina **[!UICONTROL Esperienze]** di un&#39;attività di Personalizzazione automatizzata, fare clic sull&#39;icona **[!UICONTROL Gestisci contenuto]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ).

1. Fai clic sulla scheda **[!UICONTROL Offerte]** nella parte superiore della finestra di dialogo **[!UICONTROL Gestisci contenuto]**.

   ![Icona Configura](../assets/ap-offers-2.png)

1. (Condizionale) Scegli le offerte da aggiungere a un gruppo di reporting.

   * Per aggiungere una singola offerta, fai clic sull&#39;icona **[!UICONTROL Altre azioni]** ( ![Altre azioni](/help/main/assets/icons/MoreSmall.svg) ) per l&#39;offerta, quindi fai clic su **[!UICONTROL Gruppo di reporting]**.
   * Per aggiungere più offerte contemporaneamente, seleziona le caselle di controllo relative alle offerte, quindi fai clic su **[!UICONTROL Gruppo di reporting]** nella parte inferiore della finestra di dialogo.

1. Assegna le offerte selezionate a un gruppo di reporting.

   * Per assegnare le offerte a un gruppo di reporting esistente, seleziona **[!UICONTROL Esistente]**, seleziona il gruppo di reporting dall&#39;elenco a discesa, quindi fai clic su **[!UICONTROL Conferma]**.
   * Per creare un gruppo di reporting per le offerte, seleziona **[!UICONTROL Nuovo]**, assegna un nome al nuovo gruppo di reporting, quindi fai clic su **[!UICONTROL Conferma]**.

Per limitare l&#39;elenco delle offerte, filtrarlo in base alla posizione con l&#39;elenco **[!UICONTROL Posizione]** o in base al gruppo di reporting con l&#39;elenco **[!UICONTROL Gruppo di rapporti]**. L&#39;elenco **[!UICONTROL Gruppo di rapporti]** offre anche l&#39;opzione **[!UICONTROL Offerte non assegnate]**, che visualizza le offerte che non appartengono ancora ad alcun gruppo di reporting, in modo da poterle assegnare a uno.

Per informazioni su come indirizzare un&#39;offerta a tipi di pubblico specifici, consulta [Offerte di Target **[!UICONTROL Automated Personalization]**](/help/main/c-activities/t-automated-personalization/ap-target-offers.md#set-up-targeting-rules).

## Visualizzare le offerte in un gruppo di reporting

Il report **[!UICONTROL Livello offerta]** mostra le prestazioni delle offerte di un&#39;attività, raggruppate per gruppo di reporting, in modo da poter confrontare i gruppi e le singole offerte.

1. Fai clic su **[!UICONTROL Attività]**, fai clic sull&#39;attività **[!UICONTROL Automated Personalization]** nell&#39;elenco, quindi fai clic sulla scheda **[!UICONTROL Rapporti]** per visualizzare il rapporto [Livello offerta](/help/main/c-reports/personalization-reports/reports-ap.md).

   Se hai numerose attività, fai clic sull&#39;icona **[!UICONTROL Mostra filtri]** (funnel), quindi seleziona la casella di controllo **[!UICONTROL Automated Personalization]** per visualizzare solo **[!UICONTROL Automated Personalization]** attività.

1. Fai clic su **[!UICONTROL Controllo]** o **[!UICONTROL Destinato]** nella tabella per visualizzare le offerte non raggruppate e le offerte all&#39;interno dei gruppi di reporting.

   ![Gruppi di offerte: controllo e destinazione](/help/main/c-reports/assets/offer-groups.png)

Per informazioni sull&#39;utilizzo dei report **[!UICONTROL Automated Personalization]** (incluso il report **[!UICONTROL Livello di offerta]**), vedi [Report di riepilogo di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).
