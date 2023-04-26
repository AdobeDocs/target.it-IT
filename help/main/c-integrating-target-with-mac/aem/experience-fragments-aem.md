---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
description: Scopri come utilizzare i  [!DNL Adobe Experience Manager] [!UICONTROL frammenti di esperienza] nelle attività di  [!DNL Adobe Target] .
title: Come posso utilizzare i [!UICONTROL frammenti di esperienza] di  [!DNL Adobe Experience Manager] (AEM)?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: 7c81362a82ca6692bb8c183b8e8fc50c6329e2e8
workflow-type: ht
source-wordcount: '1352'
ht-degree: 100%

---

# [!UICONTROL Frammenti di esperienza] AEM

Puoi utilizzare i [!UICONTROL frammenti di esperienza] (XF) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare l’ottimizzazione e la personalizzazione.

## Considerazioni

Quando utilizzi i [!UICONTROL frammenti di esperienza] di AEM in [!DNL Target], considera quanto segue:

* Questa funzionalità è disponibile solo per chi è cliente [!DNL Adobe Experience Manager] (AEM). Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Frammenti di esperienza] e [!UICONTROL frammenti di contenuto] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Personalizzazione automatizzata] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Targeting dell’esperienza] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Frammenti di esperienza] e [!UICONTROL frammenti di contenuto] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test multivariato] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Raccomandazioni]](/help/main/c-recommendations/recommendations.md)

* È possibile sfruttare i [!UICONTROL frammenti di esperienza] nelle attività di [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

Per ulteriori informazioni sui [!UICONTROL frammenti di esperienza] e sui [!UICONTROL frammenti di contenuto] di AEM, consulta [[!UICONTROL frammenti di esperienza] e la Panoramica dei frammenti di contenuto di AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

Devi disporre della funzionalità [!UICONTROL frammenti di esperienza] all’interno di [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] as a Cloud Service o [!DNL AEM] versione 6.4 (o successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* Account [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium].

Le versioni 6.3 e 6.4 di [!DNL Adobe Experience Manager] hanno raggiunto la fine del ciclo di vita e non sono più supportate (ad eccezione dei clienti che hanno acquistato un’estensione del supporto).

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Creazione e configurazione di [!UICONTROL frammenti di esperienza] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare i [!UICONTROL frammenti di esperienza] [!DNL AEM] in [!DNL Target], devi eseguire i seguenti passaggi:

### Passaggio 1: Integrare [!DNL AEM] con [!DNL Target]

Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [Integrazione con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html?lang=it){target=_blank} nella guida di *Experience Manager as a Cloud Service*.
* **Adobe I/O**: [Integrazione con Adobe Target tramite Adobe I/O](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=it){target=_blank} nella documentazione della *Guida per la gestione degli utenti*.
* **[!DNL AEM]6.5**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 2: creare il frammento di esperienza

I [!UICONTROL frammenti di esperienza] sono creati in [!DNL AEM]. Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [[!UICONTROL frammenti di esperienza]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=it){target=_blank} nella guida di *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [[!UICONTROL Frammenti di esperienza]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [[!UICONTROL Frammenti di esperienza]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 3: configurare [!DNL AEM]per condividere il [!UICONTROL frammento di esperienza] con [!DNL Target]

1. Dall’interno di [!DNL AEM], seleziona il [!UICONTROL frammento di esperienza] desiderato o la cartella che lo contiene, quindi fai clic su **[!UICONTROL Proprietà]**.
2. Fa clic sulla scheda **[!UICONTROL Servizi cloud]**, poi, dall&#39;elenco a discesa **[!UICONTROL Configurazione del servizio cloud]**, seleziona **[!UICONTROL Adobe Target]**.

   Il passaggio precedente presuppone che un utente dell’azienda abbia creato la configurazione di [!DNL Adobe Target].

3. Fai clic su **[!UICONTROL Salva e chiudi]**.

### Passaggio 4: pubblicare il [!UICONTROL frammento di esperienza] ed esportarlo in [!DNL Target]

A seconda della versione di [!DNL AEM], consulta i seguenti collegamenti per istruzioni dettagliate:

* **AEM as a Cloud Service**: [Esportazione di [!UICONTROL frammenti di esperienza] in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=it){target=_blank} nella guida di *Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

## Utilizzo dei [!UICONTROL frammenti di esperienza] nelle attività di [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il [!UICONTROL Frammento di esperienza] viene visualizzato nella pagina [!UICONTROL Offerte] di [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL frammenti di esperienza] da importare ogni dieci minuti. Il [!UICONTROL frammento di esperienza] importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.

Il [!UICONTROL frammento di esperienza] è importato in [!DNL Target] come offerta HTML o JSON. La versione “primaria” del [!UICONTROL frammento di esperienza] rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL frammento di esperienza] in [!DNL Target].

Puoi filtrare ed eseguire ricerche per [!UICONTROL XF HTML] e [!UICONTROL XF JSON] per distinguere meglio i tipi di [!UICONTROL frammenti di esperienza] esportati in [!DNL Target].

![Filtrare per tipi di frammento di esperienza: HTML o JSON nell’interfaccia utente di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Puoi passare il cursore sopra un [!UICONTROL frammento di esperienza] nell’elenco, quindi fai clic sull’icona [!UICONTROL Visualizza] ![icona Info](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) per visualizzare ulteriori informazioni sul [!UICONTROL frammento di esperienza], tra cui [!UICONTROL Nome], [!UICONTROL Tipo], [!UICONTROL ID offerta], [!UICONTROL Percorso offerta] e informazioni sulle ultime modifiche. Fai clic sulla scheda [!UICONTROL Utilizzo offerta] per visualizzare le attività che fanno riferimento a questa offerta.

![Finestra a comparsa con informazioni sul frammento di esperienza](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

È possibile sfruttare i [!UICONTROL frammenti di esperienza] nelle attività di [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).


>[!TIP]
>
>Utilizza funzioni di intelligenza artificiale, apprendimento automatico e consigli con i [!UICONTROL frammenti di esperienza]:
>
>* Per sfruttare appieno le funzionalità basate su IA e ML di [!DNL Target], seleziona [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un’attività.
>
>* I [!UICONTROL frammenti di esperienza] non sono supportati nelle attività di [!DNL Recommendations]. Tuttavia, per utilizzare i [!UICONTROL frammenti di esperienza] per i consigli è possibile creare un’attività [!UICONTROL Test A/B] (che comprende [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un [!UICONTROL Targeting dell’esperienza] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).


**Per sfruttare i [!UICONTROL frammenti di esperienza] utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza visivo](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fai clic sul percorso nella pagina in cui desideri inserire il contenuto [!DNL AEM], quindi seleziona l’opzione desiderata per visualizzare l’elenco [!UICONTROL Scegli un frammento di esperienza].

   * [!UICONTROL Inserisci prima]
   * [!UICONTROL Inserisci dopo]
   * [!UICONTROL Scambia con frammento di esperienza]

   L’elenco dei [!UICONTROL frammenti di esperienza] presenta tutti i contenuti creati in [!DNL AEM] che ora sono disponibili in modo nativo in [!DNL Target].

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Scambia con frammento esperienza] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Seleziona il [!UICONTROL frammento di esperienza] desiderato, quindi fai clic su **[!UICONTROL Fine]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Allocazione automatica:** [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Consigli in un’attività Test A/B o XT:** [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md)

   I [!UICONTROL frammenti di esperienza] esportati come JSON in [!DNL Target] non possono essere utilizzati nelle attività create utilizzando il Compositore esperienza visivo; nelle attività basate sul Compositore esperienza visivo sono supportati solo i [!UICONTROL frammenti di esperienza] HTML. Se desideri utilizzare i [!UICONTROL frammenti di esperienza] JSON, utilizzali nelle attività create tramite il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

**Per sfruttare i [!UICONTROL frammenti di esperienza] utilizzando il [!UICONTROL Compositore esperienza basato su moduli]:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona il percorso nella pagina in cui desideri inserire il contenuto di [!DNL AEM], quindi seleziona **[!UICONTROL Cambia frammento di esperienza]** per visualizzare l’elenco [!UICONTROL Scegli un frammento di esperienza].

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   L’elenco dei [!UICONTROL frammenti di esperienza] presenta tutti i contenuti creati in [!DNL AEM] che ora sono disponibili in modo nativo in [!DNL Target].

1. Seleziona il [!UICONTROL frammento di esperienza] desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] cerca attualmente [!UICONTROL frammenti di esperienza] da importare ogni dieci minuti. Il [!UICONTROL frammento di esperienza] importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.
* Il [!UICONTROL frammento di esperienza] è importato in [!DNL Target] come offerta HTML o JSON. La versione “primaria” del [!UICONTROL frammento di esperienza] rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL frammento di esperienza] in [!DNL Target].
* Non è possibile creare [!UICONTROL frammenti di esperienza] utilizzando [!DNL Adobe I/O]. Crea [!UICONTROL frammenti di esperienza] utilizzando AEM, come spiegato in precedenza.
* Se aggiorni il [!UICONTROL frammento di esperienza] in AEM, il [!UICONTROL frammento di esperienza] deve essere pubblicato ed esportato nuovamente in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.

## Rimozione di ClientLibs e HTML estranei dai [!UICONTROL frammenti di esperienza] esportati in [!UICONTROL Target]

Quando si utilizzano le offerte del [!UICONTROL frammento di esperienza] con [!DNL Target] in una pagina distribuita da AEM, la pagina di destinazione contiene già tutte le librerie client necessarie. Inoltre, non sono necessari nemmeno gli elementi HTML estranei nell’offerta.

A volte intere pagine HTML mandano a testo il [!UICONTROL frammento di esperienza] e causano problemi. Assicurati che il [!UICONTROL frammento di esperienza] sia un piccolo frammento HTML e non una pagina HTML completa con HTML, HEAD, BODY e così via.

Per ulteriori informazioni, consulta il seguente articolo di blog: [AEM 6.5: Rimozione di ClientLibs dai [!UICONTROL frammenti di esperienza] esportati in Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Video di formazione: utilizzo dei [!UICONTROL frammenti di esperienza] di AEM con [!DNL Adobe Target]

Il video seguente illustra come impostare e utilizzare i [!UICONTROL frammenti di esperienza]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>La funzione di deeplink di [!DNL AEM] discussa in 4:54 è stata rimossa.

Per ulteriori informazioni dettagliate, consulta [Utilizzo dei [!UICONTROL frammenti di esperienza] con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=it) nella pagina *Video e tutorial di AEM Sites*.
