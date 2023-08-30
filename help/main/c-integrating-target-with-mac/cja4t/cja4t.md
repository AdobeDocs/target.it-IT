---
keywords: cja4t;customer percorsi analytics;customer percorsi analytics for target;customer percorsi analytics origine per la generazione di rapporti;customer percorsi analytics come origine per la generazione di rapporti per target
description: Utilizza  [!DNL Adobe Customer Journey Analytics]  for  [!DNL Target]  (A4T) per creare attività basate su metriche di conversione di  [!DNL Customer Journey Analytics]  e segmenti di pubblico e utilizza i rapporti di  [!DNL Customer Journey Analytics]  per esaminare i risultati.
title: Cos’è [!DNL Adobe Customer Journey Analytics] per [!DNL Target] (CJA4T)
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 79d4bfa7bbdaea6b779ab548b80fbcf732635ba5
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 16%

---

# [!DNL Adobe Customer Journey Analytics] come origine di reporting per [!DNL Adobe Target] (CJA4T)

[!DNL Customer Journey Analytics for Target] (CJA4T) è un’integrazione tra soluzioni che consente di creare attività basate su [Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html){target=_blank} metriche di conversione. L’integrazione di CJA4T consente di utilizzare [!DNL Customer Journey Analytics] report per esaminare i risultati. Se usa [!DNL Customer Journey Analytics] come origine per la generazione di rapporti per un’attività, tutti i rapporti per tale attività si basano su [!DNL Customer Journey Analytics] raccolta dati.

## Panoramica

L’integrazione [!DNL Customer Journey Analytics for Target] tra [!DNL Customer Journey Analytics] e [!DNL Target] fornisce potenti strumenti di analisi per il programma di ottimizzazione, che consentono di risparmiare tempo prezioso.

L’utilizzo dei dati di [!DNL Customer Journey Analytics] in [!DNL Target] offre i tre vantaggi principali seguenti:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] o i segmenti di reporting ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Una singola origine di dati riduce al minimo la varianza che si verifica durante la raccolta dei dati in due sistemi separati.
* Il tuo esistente [!DNL Customer Journey Analytics] l’implementazione raccoglie tutti i dati richiesti. Non è necessario implementare mbox sulle pagine al solo scopo di raccogliere dati per i rapporti.

Quando prendi in considerazione l’utilizzo di CJA4T, considera gli aspetti seguenti:

* Per utilizzare [!DNL Customer Journey Analytics] come origine per la generazione di rapporti per [!DNL Target], sia tu che la tua società dovete avere accesso ad [!DNL Customer Journey Analytics] e a [!DNL Target]. Se hai bisogno di accedere a una delle soluzioni, contatta l’amministratore della tua organizzazione o il rappresentante del tuo account.
* Per creare [!DNL Target] attività con [!DNL Customer Journey Analytics] nel reporting, devi disporre di un’&quot;[!UICONTROL Approvatore]&quot; o &quot;[!UICONTROL Editor]&quot; ruolo in [!DNL Target].
   * Se si dispone di [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905) account, consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.
   * Se si dispone di [Target Premium](/help/main/c-intro/intro.md#premium) account, consulta [Ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Autorizzazioni per gli utenti Enterprise*.

* A seconda delle impostazioni, il reporting può essere modificato per attività o a livello di organizzazione. Consulta [Soluzione Reporting Cloud](/help/main/administrating-target/reporting.md#solution) in *Configurare la generazione di rapporti in Target*.
* Per la generazione dei rapporti, utilizza un’origine o l’altra. Non è possibile raccogliere dati per una singola attività per più origini di reporting.
* Quando si imposta [!DNL Customer Journey Analytics] come origine per la generazione di rapporti, viene richiesto di specificare la sandbox per la generazione dei rapporti. Durante la configurazione, vengono visualizzate solo le sandbox a cui hai accesso.
* Qualsiasi esistente [!DNL Target] le attività continuano a utilizzare [!DNL Target] e non sono influenzati dall’abilitazione di CJA4T.
* CJA4T è disponibile solo se [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank}. Il supporto per il connettore dati di Analytics è pianificato per il futuro.
* Per eventuali domande sulla tempistica, consulta [Considerazioni sulla latenza](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=en#latency){target=_blank} in *Domande frequenti* nel *Guida di Adobe Customer Analytics*.

## Tipi di attività supportati

I seguenti tipi di attività sono supportati quando si utilizza [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html){target=_blank} or [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html){target=_blank}:

| Tipi di attività | CJA4T compatibile? |
|--- |--- |
| [Attività A/B con suddivisione manuale del traffico](/help/main/c-activities/t-test-ab/test-ab.md) | Sì |
| [Attività A/B con allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Attività A/B con targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | No |
| [Targeting delle esperienze (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Sì |
| [Test multivariato (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Sì |
| [Attività di Automated Personalization (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | No |
| [Attività di Consigli](/help/main/c-recommendations/recommendations.md) | Sì |

## Creare un’attività che utilizza [!DNL Customer Journey Analytics] come origine per la generazione di rapporti

Creazione di un [!DNL Target] attività che utilizza [!DNL Customer Journey Analytics] poiché l’origine per la generazione di rapporti è simile alla configurazione di un’ [!DNL Target] attività.

1. Dalla sezione **[!UICONTROL Attività]** , fare clic su **[!UICONTROL Crea attività]**, quindi seleziona il tipo di attività (in base al grafico delle attività supportato riportato sopra) e inizia a impostare l’attività.
1. Quando si arriva al **[!UICONTROL Obiettivi e impostazioni]** pagina del flusso di lavoro di creazione attività in tre parti, seleziona **[!DNL Customer Journey Analytics]** come origine per la generazione di rapporti.

   ![Customer Journey Analytics come opzione origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Impossibile modificare l’origine per la generazione di rapporti dopo un [!DNL Target] l’attività diventa live.

1. Seleziona una sandbox.

   In questo elenco a discesa puoi visualizzare solo le sandbox a cui hai accesso. Se una o più sandbox a cui hai accesso non sono presenti nell’elenco, verifica di avere accesso alla sandbox. Contatto [Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) se continui a visualizzare i problemi.

   ![Seleziona opzione sandbox](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Specifica l&#39;obiettivo dell&#39;attività.

   È necessario selezionare una metrica di successo da utilizzare come obiettivo per ogni attività. Puoi scegliere uno dei [!DNL Target] metriche di conversione o utilizzare un [!DNL Customer Journey Analytics] metrica.

   ![Utilizza un’opzione di metrica Customer Journey Analytics in Metrica per obiettivo](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Fai clic su **[!UICONTROL Salva e chiudi]**.

## Configurare un [!DNL Customer Journey Analytics] connessione

Dopo un [!DNL Target] è stata creata, è necessario creare una connessione in [!DNL Customer Journey Analytics]. Se disponi già di una connessione, puoi utilizzarla e passare al passaggio 4 seguente. La connessione consente [!DNL Customer Journey Analytics] per iniziare a estrarre dati dal set di dati per il reporting.

1. In entrata [!DNL Customer Journey Analytics], sulla **[!UICONTROL Connessioni]** pagina, fai clic su **[!UICONTROL Crea una nuova connessione]**.

   ![Crea nuovo collegamento di connessione nel Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Configurare [impostazioni di connessione e dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html){target=_blank} informazioni corrette.
1. Aggiungi il set di dati evento utilizzato durante la configurazione dello stream di dati.
1. Aggiungi il **[!UICONTROL Eventi di classificazione Adobe Target]** cerca set di dati, quindi fai clic su **[!UICONTROL Successivo]**.

   ![Finestra di dialogo Aggiungi set di dati nel Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Configura il set di dati evento.

   Per ulteriori informazioni, consulta [Aggiungere e configurare i set di dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=en#add-dataset){target=_blank} in *Creare una connessione* nel *Guida di Adobe Customer Journey Analytics*.

1. Configura il set di dati di ricerca con il campo Chiave come &quot;chiave&quot; e il campo Chiave corrispondente con il seguente percorso:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Finestra di dialogo dell’evento Classificazioni di Adobe Target nel Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Clic **[!UICONTROL Aggiungere set di dati]**, quindi fai clic su **[!UICONTROL Salva]** nella schermata successiva per terminare la connessione.

## Impostare le visualizzazioni dati

Configurare una visualizzazione dati in [!DNL Customer Journey Analytics]. Una visualizzazione dati garantisce che i dati della connessione possano essere utilizzati correttamente.

1. Configura la visualizzazione dati e accertati che punti alla connessione creata in precedenza.

   Per ulteriori informazioni, consulta [Creare o modificare una visualizzazione dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html){target=_blank} nel *Guida di Adobe Customer Journey Analytics*.

1. Per visualizzare correttamente [!DNL Target] dati in [!DNL Customer Journey Analytics], è necessario aggiungere i campi seguenti dal set di dati di ricerca come dimensioni:

   * Nome esperienza
   * ID esperienza
   * Nome attività
   * ID attività

   ![Opzioni per nomi e ID nel Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Completa l’impostazione di altri campi, quindi fai clic su **[!UICONTROL Salva e continua]** al termine.
