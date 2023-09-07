---
keywords: cja4t;customer journey analytics;customer journey analytics per target;customer journey analytics origine di reporting;customer journey analytics come origine di reporting per target
description: Utilizza  [!DNL Adobe Customer Journey Analytics]  for  [!DNL Target]  (A4T) per creare attività basate su metriche di conversione di  [!DNL Customer Journey Analytics]  e segmenti di pubblico e utilizza i rapporti di  [!DNL Customer Journey Analytics]  per esaminare i risultati.
title: Cos’è  [!DNL Adobe Customer Journey Analytics]  for  [!DNL Target]  (CJA4T)?
feature: Integrations
hide: true
hidefromtoc: true
source-git-commit: 13c899b656d9f15e7368d981ac25540c46caccb2
workflow-type: ht
source-wordcount: '919'
ht-degree: 100%

---

# [!DNL Adobe Customer Journey Analytics] come origine di reporting per [!DNL Adobe Target] (CJA4T)

L’integrazione di [!DNL Customer Journey Analytics for Target] (CJA4T) tra [Adobe Customer Journey Analytics (CJA)](https://experienceleague.adobe.com/docs/customer-journey-analytics.html?lang=it){target=_blank} e [!DNL Target] fornisce potenti strumenti di analisi per il programma di ottimizzazione, che consentono di risparmiare tempo prezioso.

I vantaggi principali dell’utilizzo dei dati di [!DNL Customer Journey Analytics] in [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Un’unica origine dati elimina la varianza che si verifica quando si raccolgono dati in due sistemi distinti.

## Considerazioni

Valuta le seguenti informazioni prima di utilizzare l’integrazione CJA4T:

* Per utilizzare [!DNL Customer Journey Analytics] come origine per la generazione di rapporti per [!DNL Target], sia tu che la tua società dovete avere accesso ad [!DNL Customer Journey Analytics] e a [!DNL Target]. Se hai bisogno di accedere a una delle soluzioni, contatta l’amministratore della tua organizzazione o il rappresentante del tuo account.
* Per creare attività [!DNL Target] con il reporting di [!DNL Customer Journey Analytics], è necessario avere un ruolo di “[!UICONTROL Approvatore]” o “[!UICONTROL Editor]” in [!DNL Target].
   * Se la tua organizzazione dispone di un account [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905), consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.
   * Se si dispone di un account [Target Premium](/help/main/c-intro/intro.md#premium), consulta [Ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Autorizzazioni per gli utenti Enterprise*.

* A seconda delle impostazioni, il reporting può essere modificato per attività o a livello di organizzazione. Consulta [Soluzione Reporting Cloud](/help/main/administrating-target/reporting.md#solution) in *Configurare il reporting in Target*.
* Per la generazione dei rapporti, utilizza un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da diverse origini di reporting.
* Quando imposti [!DNL Customer Journey Analytics] come origine di reporting, ti viene richiesto di specificare la sandbox per la generazione dei rapporti. Durante la configurazione, vengono visualizzate solo le sandbox a cui hai accesso.
* Tutte le attività di [!DNL Target] esistenti continuano a utilizzare la raccolta dati di [!DNL Target] e non sono influenzate dall’abilitazione di CJA4T.
* CJA4T è disponibile solo se hai [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform.html?lang=it){target=_blank} and [!DNL Target] implemented through the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank}. Il supporto per [!DNL Analytics Data Connector] è pianificato per il futuro.
* Per domande sulla tempistica, consulta [Considerazioni sulla latenza](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-faq.html?lang=it#latency){target=_blank} in *Domande frequenti* nella *Guida di Adobe Customer Analytics*.

## Tipi di attività supportati {#supported-activities}

I seguenti tipi di attività sono supportati quando si utilizza la libreria JavaScript di [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/aep-web-sdk.html?lang=it){target=_blank} or the [at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/overview.html?lang=it){target=_blank}:

| Tipi di attività | Compatibilità CJA4T? |
|--- |--- |
| [Attività A/B con suddivisione manuale del traffico](/help/main/c-activities/t-test-ab/test-ab.md) | Sì |
| [Attività A/B con allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) | No |
| [Attività A/B con targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) | No |
| [Targeting delle esperienze (XT)](/help/main/c-activities/t-experience-target/experience-target.md) | Sì |
| [Test multivariato (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) | Sì |
| [Attività di Automated Personalization (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md) | No |
| [Attività di Consigli](/help/main/c-recommendations/recommendations.md) | Sì |

## Creare un’attività che utilizza [!DNL Customer Journey Analytics] come origine di reporting

La creazione di un’attività [!DNL Target] che utilizza [!DNL Customer Journey Analytics] come origine di reporting è simile alla configurazione di una normale attività [!DNL Target].

1. Dall’elenco **[!UICONTROL Attività]**, fai clic su **[!UICONTROL Crea attività]**, quindi seleziona il tipo di attività (in base al [grafico attività supportato qui sopra](#supported-activities)) e inizia a configurare l’attività.
1. Quando si arriva alla pagina **[!UICONTROL Obiettivi e impostazioni]** del flusso di lavoro di creazione attività in tre parti, seleziona **[!DNL Customer Journey Analytics]** come origine di reporting.

   ![Customer Journey Analytics come opzione di origine di reporting](/help/main/c-integrating-target-with-mac/cja4t/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Impossibile modificare l’origine di reporting quando l’attività [!DNL Target] è già live.

1. Seleziona una sandbox.

   In questo elenco a discesa puoi visualizzare solo le sandbox a cui hai accesso. Se una o più delle sandbox a cui hai accesso non è presente nell’elenco, verifica di avere l’accesso. Contatta l’[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) se i problemi persistono.

   ![Seleziona opzione sandbox](/help/main/c-integrating-target-with-mac/cja4t/assets/sandbox.png)

1. Specifica l’obiettivo dell’attività.

   Seleziona una metrica di successo da utilizzare come obiettivo per ogni attività. Puoi scegliere una delle metriche di conversione di [!DNL Target] o utilizzare una metrica di [!DNL Customer Journey Analytics].

   ![Utilizza un’opzione di metrica di Customer Journey Analytics in Metrica per obiettivo](/help/main/c-integrating-target-with-mac/cja4t/assets/goal-metric.png)

1. Fai clic su **[!UICONTROL Salva e chiudi]**.

## Configurare una connessione a [!DNL Customer Journey Analytics]

Dopo la creazione di un’attività [!DNL Target], è necessario creare una connessione in [!DNL Customer Journey Analytics]. Se hai già impostato una connessione, puoi utilizzarla e saltare al passaggio 4 seguente. La connessione consente a [!DNL Customer Journey Analytics] di iniziare a estrarre dati dal set di dati per il reporting.

1. In [!DNL Customer Journey Analytics], dalla pagina **[!UICONTROL Connessioni]**, fai clic su **[!UICONTROL Crea una nuova connessione]**.

   ![Crea nuovo collegamento di connessione in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/create-connection.png)

1. Configura le [impostazioni di connessione e dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/overview.html?lang=it){target=_blank} con le informazioni corrette.
1. Aggiungi il set di dati evento utilizzato durante la configurazione dello stream di dati.
1. Aggiungi il set di dati di ricerca **[!UICONTROL Eventi di classificazione Adobe Target]**, quindi fai clic su **[!UICONTROL Successivo]**.

   ![Finestra di dialogo Aggiungi set di dati in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/add-datasets.png)

1. Configura il set di dati evento.

   Per ulteriori informazioni, consulta [Aggiungere e configurare i set di dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-connections/create-connection.html?lang=it#add-dataset){target=_blank} in *Creare una connessione* nella *Guida di Adobe Customer Journey Analytics*.

1. Configura il set di dati di ricerca con il campo [!UICONTROL Chiave] come “chiave” e il campo Chiave corrispondente con il seguente percorso:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Finestra di dialogo dell’evento Classificazioni di Adobe Target in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/classifications-events.png)

1. Fai clic su **[!UICONTROL Aggiungi set di dati]**, quindi su **[!UICONTROL Salva]** nella schermata successiva per concludere la connessione.

## Impostare le visualizzazioni dati

Configurare una visualizzazione dati in [!DNL Customer Journey Analytics]. Una visualizzazione dati garantisce che i dati della connessione possano essere utilizzati correttamente.

1. Configura la visualizzazione dati e accertati che punti alla connessione creata in precedenza.

   Per ulteriori informazioni, consulta [Creare o modificare una visualizzazione dati](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/create-dataview.html?lang=it){target=_blank} nella *Guida di Adobe Customer Journey Analytics*.

1. Per visualizzare correttamente i dati [!DNL Target] in [!DNL Customer Journey Analytics], è necessario aggiungere come dimensioni i campi seguenti dal set di dati di ricerca:

   * Nome esperienza
   * ID esperienza
   * Nome attività
   * ID attività

   ![Opzioni per nomi e ID in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja4t/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Completa l’impostazione di eventuali altri campi, quindi fai clic su **[!UICONTROL Salva e continua]** al termine.
