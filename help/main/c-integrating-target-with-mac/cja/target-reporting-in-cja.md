---
keywords: analisi del percorso di clienti;analisi del percorso di clienti per target;origine per la generazione di rapporti analisi del percorso di clienti;analisi del percorso di clienti come origine per la generazione di rapporti per target;generazione di rapporti target in cja; generazione di rapporti target in Customer Journey Analytics
description: Utilizza  [!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics] per creare attività basate su [!DNL Customer Journey Analytics] metriche di conversione e segmenti di pubblico e utilizza [!DNL Customer Journey Analytics] rapporti per esaminare i risultati.
title: Cos'è il reporting di  [!DNL Target]  in [!DNL Adobe Customer Journey Analytics]?
feature: Integrations
exl-id: 67b20bf6-ffbe-4220-9455-cb3886bb9227
source-git-commit: 52f11998149cddeb4245a0f07280562d79332a04
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 54%

---

# Generazione rapporti per [!DNL Target] in [!DNL Adobe Customer Journey Analytics]

L&#39;integrazione tra [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/customer-journey-analytics){target=_blank} e [!DNL Target] fornisce potenti strumenti di analisi che consentono di risparmiare tempo per il programma di ottimizzazione.

I vantaggi principali dell’utilizzo di [!DNL Customer Journey Analytics] come origine di reporting per [!DNL Target] sono:

* Gli addetti al marketing possono applicare dinamicamente le metriche di successo di [!DNL Customer Journey Analytics] ai rapporti delle attività di [!DNL Target] in qualsiasi momento. Non è necessario specificare tutte le impostazioni prima di eseguire l’attività.
* Gli addetti al marketing possono sfruttare le funzionalità di [!DNL Customer Journey Analytics], ad esempio il [pannello Sperimentazione](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/panels/experimentation){target=_blank}, per analizzare ulteriormente la personalizzazione del sito Web.
* Gli addetti al marketing possono avere un&#39;unica origine per la generazione di rapporti per [!DNL Adobe Journey Optimizer] e [!DNL Target]. Entrambi i prodotti di personalizzazione possono essere collegati a [!DNL Customer Journey Analytics] per una visione più olistica della personalizzazione web.

## Considerazioni

Prima di utilizzare l&#39;integrazione di [!DNL Customer Journey Analytics] e [!DNL Target], considera le seguenti informazioni:

>[!IMPORTANT]
>
>Questa integrazione non è la stessa di [[!UICONTROL Adobe Analytics for Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T). I tipi di implementazione e attività supportate sono diversi. Assicurati di aver letto attentamente questo articolo prima di utilizzare questa integrazione per le attività di [!DNL Target].

* Per utilizzare [!DNL Customer Journey Analytics] come origine per la generazione di rapporti per [!DNL Target], sia tu che la tua società dovete avere accesso ad [!DNL Customer Journey Analytics] e a [!DNL Target]. Se hai bisogno di accedere a una delle soluzioni, contatta l’amministratore della tua organizzazione o il rappresentante del tuo account.
* Per creare attività [!DNL Target] con reporting [!DNL Customer Journey Analytics], è necessario avere il ruolo &quot;[!UICONTROL Approver]&quot; o &quot;[!UICONTROL Editor]&quot; in [!DNL Target].
   * Se la tua organizzazione dispone di un account [Target Standard](/help/main/c-intro/intro.md#section_ACD5EFF17AAB4E979CBEFA0145CCD905), consulta [Specificare ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/c-user-management/user-management.md#roles-permissions) in *Utenti*.
   * Se si dispone di un account [Target Premium](/help/main/c-intro/intro.md#premium), consulta [Ruoli e autorizzazioni](/help/main/administrating-target/c-user-management/property-channel/property-channel.md#roles-permissions) in *Autorizzazioni per gli utenti Enterprise*.

* Devi far parte di un ruolo in [!DNL Adobe Experience Platform] per impostare un’attività [!DNL Target] con [!DNL Customer Journey Analytics] come origine di reporting. Per ulteriori informazioni, consulta [Aggiungere un ruolo in [!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/platform-learn/getting-started-for-data-architects-and-data-engineers/configure-permissions#add-a-role-in-adobe-experience-platform-requires-a-system-administrator-or-product-admin){target=_blank} nella sezione *Configurare le autorizzazioni* del *tutorial per Data Architect e Data Engineer.*
* A seconda delle impostazioni, il reporting può essere modificato per attività o a livello di organizzazione. Consulta [Soluzione Reporting Cloud](/help/main/administrating-target/reporting.md#solution) in *Configurare il reporting in Target*.
* Per la generazione dei rapporti, utilizza un’origine o l’altra. Non è possibile raccogliere dati per una singola attività da diverse origini di reporting.
* Quando imposti [!DNL Customer Journey Analytics] come origine di reporting, ti viene richiesto di specificare la sandbox per la generazione dei rapporti. Durante la configurazione, vengono visualizzate solo le sandbox a cui hai accesso.
* Tutte le attività [!DNL Target] esistenti continuano a utilizzare la raccolta dati [!DNL Target] e non sono interessate dall&#39;abilitazione di questa integrazione.
* Per utilizzare questa integrazione, il metodo di implementazione preferito ha [[!DNL Adobe Experience Platform]](https://experienceleague.adobe.com/en/docs/experience-platform){target=_blank} e [!DNL Target] implementati tramite [[!DNL Adobe Experience Platform Web SDK]](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank}.

  Se al momento non hai implementato [!DNL Adobe Experience Platform Web SDK], puoi anche creare una [[!DNL Adobe Analytics] connessione di origine](https://experienceleague.adobe.com/en/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics) per inserire i dati in [!DNL Adobe Experience Platform]. Se prevedi di utilizzare questo metodo, devi selezionare una suite di rapporti [!DNL Analytics] insieme alla sandbox [!DNL Adobe Experience Platform] utilizzata con [!DNL Customer Journey Analytics].

  ![Opzione Sandbox nella finestra di dialogo Impostazioni reporting](/help/main/c-integrating-target-with-mac/cja/assets/aep-sandbox.png)

  >[!NOTE]
  >
  >Se si utilizza una connessione di origine [!DNL Adobe Analytics], si disporranno di report sia in [!DNL Adobe Analytics] che in [!DNL Customer Journey Analytics]. Tuttavia, a causa di diversi algoritmi tra queste due soluzioni, è improbabile che i risultati corrispondano.

* Per domande sulla tempistica, consulta [Considerazioni sulla latenza](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-faq#latency){target=_blank} in *Domande frequenti* nella Guida di *[!DNL Adobe Customer Analytics]*.

## Tipi di attività supportati {#supported-activities}

I seguenti tipi di attività sono supportati quando si utilizza la libreria JavaScript [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/aep-web-sdk){target=_blank} o [at.js](https://experienceleague.adobe.com/en/docs/target-dev/developer/client-side/at-js-implementation/overview){target=_blank}:

| Tipi di attività | Supportate? |
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

>[!TIP]
>
>È inoltre possibile specificare che [!DNL Target] utilizza la creazione di rapporti in [!DNL Customer Journey Analytics] per tutte le attività create nel tuo account (**[!UICONTROL Administration]** > **[!UICONTROL Reporting]** > **[!UICONTROL Reporting Experience Cloud Solution]**). Per ulteriori informazioni, consulta *Soluzione Reporting Cloud* in [Configurare la generazione di rapporti in [!DNL Target]](/help/main/administrating-target/reporting.md#solution).

1. Dall&#39;elenco **[!UICONTROL Activities]**, fai clic su **[!UICONTROL Create Activity]**, quindi seleziona il tipo di attività (in base al [grafico attività supportato sopra](#supported-activities)) e inizia a configurare l&#39;attività.
1. Quando si arriva alla pagina **[!UICONTROL Goals & Settings]** del flusso di lavoro di creazione attività in tre parti, selezionare **[!DNL Customer Journey Analytics]** come origine per la generazione di rapporti.

   ![Customer Journey Analytics come opzione di origine di reporting](/help/main/c-integrating-target-with-mac/cja/assets/cja-as-reporting-source.png)

   >[!NOTE]
   >
   >Impossibile modificare l’origine di reporting quando l’attività [!DNL Target] è già live.

1. Seleziona una sandbox.

   In questo elenco a discesa sono visualizzate solo le sandbox a cui hai accesso. Se una o più delle sandbox a cui hai accesso non è presente nell’elenco, verifica di avere l’accesso. Contatta l’[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) se i problemi persistono.

   ![Seleziona opzione sandbox](/help/main/c-integrating-target-with-mac/cja/assets/sandbox.png)

1. Specifica l’obiettivo dell’attività.

   Seleziona una metrica di successo da utilizzare come obiettivo per ogni attività. Puoi scegliere una delle metriche di conversione di [!DNL Target] o utilizzare una metrica di [!DNL Customer Journey Analytics].

   ![Utilizza un’opzione di metrica di Customer Journey Analytics in Metrica per obiettivo](/help/main/c-integrating-target-with-mac/cja/assets/goal-metric.png)

1. Fare clic su **[!UICONTROL Save & Close]**.

## Configurare una connessione a [!DNL Customer Journey Analytics]

Dopo la creazione di un’attività [!DNL Target], è necessario creare una connessione in [!DNL Customer Journey Analytics]. Se hai già impostato una connessione, puoi utilizzarla e saltare al passaggio 4 seguente. La connessione consente a [!DNL Customer Journey Analytics] di iniziare a estrarre dati dal set di dati per il reporting.

1. In [!DNL Customer Journey Analytics] nella pagina **[!UICONTROL Connections]** fare clic su **[!UICONTROL Create a new connection]**.

   ![Crea nuovo collegamento connessione in [!DNL Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/assets/create-connection.png)

1. Configura le [impostazioni di connessione e dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/overview){target=_blank} con le informazioni corrette.
1. Aggiungi il set di dati evento utilizzato durante la configurazione dello stream di dati.
1. Aggiungi il set di dati di ricerca **[!UICONTROL Adobe Target Classification Events]**, quindi fai clic su **[!UICONTROL Next]**.

   ![Finestra di dialogo Aggiungi set di dati in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/add-datasets.png)

1. Configura il set di dati evento.

   Per ulteriori informazioni, vedere [Aggiungere e configurare i set di dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection#add-dataset){target=_blank} in *Creare una connessione* nella Guida di *[!DNL Adobe Customer Journey Analytics]*.

1. Configura il set di dati di ricerca con il campo [!UICONTROL Key] come &quot;chiave&quot; e il campo chiave [!UICONTROL Matching] con il seguente percorso:

   ```
   _experience.decisioning.propositions.scopeDetails.correlationID
   ```

   ![Finestra di dialogo dell’evento Classificazioni di Adobe Target in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/classifications-events.png)

1. Fai clic su **[!UICONTROL Add datasets]**, quindi su **[!UICONTROL Save]** nella schermata successiva per terminare la connessione.

## Impostare le visualizzazioni dati

Configurare una visualizzazione dati in [!DNL Customer Journey Analytics]. Una visualizzazione dati garantisce che i dati della connessione possano essere utilizzati correttamente.

1. Configura la visualizzazione dati e accertati che punti alla connessione creata in precedenza.

   Per ulteriori informazioni, vedere [Creare o modificare una visualizzazione dati](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview){target=_blank} nella Guida di *[!DNL Adobe Customer Journey Analytics]*.

1. Per visualizzare correttamente i dati [!DNL Target] in [!DNL Customer Journey Analytics], è necessario aggiungere come dimensioni i campi seguenti dal set di dati di ricerca:

   * [!UICONTROL Experience Name]
   * [!UICONTROL Experience ID]
   * [!UICONTROL Activity Name]
   * [!UICONTROL Activity ID]

   ![Opzioni per nomi e ID in Customer Journey Analytics](/help/main/c-integrating-target-with-mac/cja/assets/names-and-ids.png){width="600" zoomable="yes"}

1. Per utilizzare le dimensioni [!DNL Target] nel pannello [!UICONTROL Experimentation], imposta le seguenti etichette di contesto:

   * Per [!UICONTROL Activity Name], utilizzare &quot;Sperimentazione&quot;.
   * [!UICONTROL Experience Name], utilizzare &quot;Variante esperimento&quot;.

   ![Etichette di contesto nel pannello Sperimentazione](/help/main/c-integrating-target-with-mac/cja/assets/context-labels.png){width="600" zoomable="yes"}

1. Terminare la configurazione di altri campi, quindi al termine fare clic su **[!UICONTROL Save and continue]**.
