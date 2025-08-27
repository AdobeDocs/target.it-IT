---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
description: Scopri come utilizzare  [!DNL Adobe Experience Manager] [!UICONTROL Experience Fragments] in [!DNL Adobe Target] attività.
title: Come Si Utilizza  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Experience Fragments]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
source-git-commit: 51e484d54f4d318ea59fdfdb16d1ed7014abdfdb
workflow-type: tm+mt
source-wordcount: '1084'
ht-degree: 31%

---

# AEM [!UICONTROL Experience Fragments]

Utilizza [!UICONTROL Experience Fragments] (XF) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per aiutare l&#39;ottimizzazione e la personalizzazione.

## Considerazioni

Considera quanto segue mentre lavori con AEM [!UICONTROL Experience Fragments] in [!DNL Target]:

* Questa funzionalità è disponibile solo per chi è cliente [!DNL Adobe Experience Manager] (AEM). Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* È possibile utilizzare [!UICONTROL Experience Fragments] nelle attività [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) e il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

Per ulteriori informazioni su AEM [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments], vedere [AEM [!UICONTROL Experience Fragments] e Panoramica sui frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

È necessario disporre della funzionalità [!UICONTROL Experience Fragments] in [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] as a Cloud Service o [!DNL AEM] versione 6.4 (o successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* Account [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium].

Le versioni 6.3 e 6.4 di [!DNL Adobe Experience Manager] hanno raggiunto la fine del ciclo di vita e non sono più supportate (ad eccezione dei clienti che hanno acquistato un’estensione del supporto).

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Creazione e configurazione di [!UICONTROL Experience Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare [!DNL AEM] [!UICONTROL Experience Fragments] in [!DNL Target], è necessario effettuare le seguenti operazioni:

### Passaggio 1: Integrare [!DNL AEM] con [!DNL Target]

Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [Integrazione con Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **Adobe Developer**: [Integrazione con Adobe Target tramite Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html){target=_blank} nella *Guida utente per l&#39;amministrazione*.
* **[!DNL AEM]6.5**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 2: creare il frammento di esperienza

[!UICONTROL Experience Fragments] creati in [!DNL AEM]. Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=it){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [[!UICONTROL Experience Fragments]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 3: configurare [!DNL AEM] per condividere [!UICONTROL Experience Fragment] con [!DNL Target]

1. Dall&#39;interno di [!DNL AEM], selezionare il [!UICONTROL Experience Fragment] desiderato o la cartella che lo contiene, quindi fare clic su **[!UICONTROL Properties]**.
2. Fai clic sulla scheda **[!UICONTROL Cloud Services]**, quindi seleziona **[!UICONTROL Cloud Service Configuration]** dall&#39;elenco a discesa **[!UICONTROL Adobe Target]**.

   Il passaggio precedente presuppone che un utente dell’azienda abbia creato la configurazione di [!DNL Adobe Target].

3. Fare clic su **[!UICONTROL Save & Close]**.

### Passaggio 4: pubblicare [!UICONTROL Experience Fragment] ed esportarlo in [!DNL Target]

A seconda della versione di [!DNL AEM], consulta i seguenti collegamenti per istruzioni dettagliate:

* **AEM as a Cloud Service**: [Esportazione di [!UICONTROL Experience Fragments] in Adobe Target](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

## Utilizzo di [!UICONTROL Experience Fragments] nelle attività [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, [!UICONTROL Experience Fragment] viene visualizzato nella pagina [!UICONTROL Offers] in [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL Experience Fragments] per importare ogni dieci minuti. Il [!UICONTROL Experience Fragment] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.

[!UICONTROL Experience Fragment] è importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;primaria&quot; di [!UICONTROL Experience Fragment] rimane in [!DNL AEM]. Impossibile modificare [!UICONTROL Experience Fragment] in [!DNL Target].

È possibile filtrare ed eseguire ricerche per [!UICONTROL HTML XFs] e [!UICONTROL JSON XFs] per distinguere tra [!UICONTROL Experience Fragment] tipi esportati in [!DNL Target].

![Filtrare per tipi di frammento di esperienza: HTML o JSON nell’interfaccia utente di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Passa il cursore del mouse su un [!UICONTROL Experience Fragment] nell&#39;elenco, quindi fai clic sull&#39;icona [!UICONTROL View] ![Info](/help/main/assets/icons/InfoOutline.svg) per visualizzare ulteriori informazioni su [!UICONTROL Experience Fragment], inclusi [!UICONTROL Name], [!UICONTROL Type], [!UICONTROL Offer ID], [!UICONTROL Offer path] e le ultime modifiche. Fare clic su [!UICONTROL [!UICONTROL View Full Details]] per visualizzare le attività che fanno riferimento a questa offerta.

![Finestra a comparsa con informazioni sul frammento di esperienza](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

È possibile utilizzare [!UICONTROL Experience Fragments] nelle attività [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) e il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

>[!TIP]
>
>Utilizzare l&#39;intelligenza artificiale, l&#39;apprendimento automatico e i consigli con [!UICONTROL Experience Fragments]:
>
>* Per sfruttare appieno le funzionalità basate su IA e ML di [!DNL Target], seleziona [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un’attività.
>
>* [!UICONTROL Experience Fragments] non sono supportati nelle attività [!DNL Recommendations]. Tuttavia, per utilizzare [!UICONTROL Experience Fragments] per i consigli è possibile creare un&#39;attività [!UICONTROL A/B Test] (inclusi [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]) o un&#39;attività [!UICONTROL Experience Targeting] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Per utilizzare [!UICONTROL Experience Fragments] utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza visivo](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fare clic sul percorso nella pagina in cui si desidera inserire il contenuto di [!DNL AEM], quindi fare clic su **[!UICONTROL Replace Content]** > **[!UICONTROL Experience Fragment]** per visualizzare la finestra di dialogo [!UICONTROL Experience Fragment].

   Nella finestra di dialogo [!UICONTROL Experience Fragment] viene visualizzato il contenuto creato in [!DNL AEM] che è ora disponibile in modo nativo in [!DNL Target].

   >[!NOTE]
   >
   >Opzione [!UICONTROL Replace Content] non disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Selezionare il [!UICONTROL Experience Fragment] desiderato, quindi fare clic su **[!UICONTROL Add]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Allocazione automatica:** [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Consigli in un’attività Test A/B o XT:** [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md)

   [!UICONTROL Experience Fragments] esportato come JSON in [!DNL Target] non può essere utilizzato nelle attività create utilizzando il Compositore esperienza visivo; solo HTML [!UICONTROL Experience Fragments] sono supportati nelle attività basate sul Compositore esperienza visivo. Se si desidera utilizzare il JSON [!UICONTROL Experience Fragments], utilizzarlo nelle attività create utilizzando il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

**Per utilizzare [!UICONTROL Experience Fragments] utilizzando [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), selezionare il percorso nella pagina in cui si desidera inserire il contenuto di [!DNL AEM], fare clic sull&#39;icona **[!UICONTROL More Details]** ( ![icona Ulteriori dettagli](/help/main/assets/icons/MoreSmall.svg) ), quindi selezionare **[!UICONTROL Change Experience Fragment]** per visualizzare la finestra di dialogo [!UICONTROL Change Experience Fragment].

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   Nella finestra di dialogo [!UICONTROL Experience Fragment] viene visualizzato il contenuto creato in [!DNL AEM] che è ora disponibile in modo nativo in [!DNL Target].

1. Selezionare il [!UICONTROL Experience Fragment] desiderato, quindi fare clic su **[!UICONTROL Add]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] cerca attualmente [!UICONTROL Experience Fragments] per importare ogni dieci minuti. Il [!UICONTROL Experience Fragment] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.
* [!UICONTROL Experience Fragment] è importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;primaria&quot; di [!UICONTROL Experience Fragment] rimane in [!DNL AEM]. Impossibile modificare [!UICONTROL Experience Fragment] in [!DNL Target].
* Impossibile creare [!UICONTROL Experience Fragments] con [!DNL Adobe Developer]. Creare [!UICONTROL Experience Fragments] con AEM, come descritto in precedenza.
* Se aggiorni [!UICONTROL Experience Fragment] in AEM, [!UICONTROL Experience Fragment] deve essere pubblicato ed esportato di nuovo in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.

## Rimozione di clientlibs e HTML estranei da [!UICONTROL Experience Fragments] esportati in [!UICONTROL Target]

Quando si utilizzano offerte [!UICONTROL Experience Fragment] con [!DNL Target] in una pagina distribuita da AEM, la pagina di destinazione contiene già le librerie client necessarie. Inoltre, non sono necessari nemmeno gli elementi HTML estranei nell’offerta.

A volte intere pagine di HTML racchiudono [!UICONTROL Experience Fragment] e causano problemi. Assicurarsi che [!UICONTROL Experience Fragment] sia una piccola parte di HTML e non una pagina HTML completa con HTML, HEAD, BODY e così via.

Per ulteriori informazioni, vedere il seguente post di blog: [AEM 6.5: Removing clientlibs from [!UICONTROL Experience Fragments] export to Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser/){target=_blank}.

## Video di formazione: Utilizzo di AEM [!UICONTROL Experience Fragments] con [!DNL Adobe Target]

Nel video seguente viene illustrato come impostare e utilizzare [!UICONTROL Experience Fragments]:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>La funzionalità di collegamento diretto di [!DNL AEM] discussa in 4:54 è stata rimossa.

Per informazioni più dettagliate, vedere [Utilizzo di [!UICONTROL Experience Fragments] con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=it) nella pagina *Video e tutorial su AEM Sites*.
