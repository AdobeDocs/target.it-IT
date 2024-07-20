---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di contenuto;frammenti;CF;cf;headless;personalizzazione;sperimentazione
description: Scopri come utilizzare  [!DNL Adobe Experience Manager] [!UICONTROL Content Fragments] in [!DNL Adobe Target] attività.
title: Come si utilizza  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Content Fragments]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: fe1e97710e7692ba7724103853ed7438c3f361b1
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 21%

---

# AEM [!UICONTROL Content Fragments]

Utilizza [!UICONTROL Content Fragments] (FC) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare la personalizzazione e la sperimentazione headless.

## Considerazioni

Durante l&#39;utilizzo dell&#39;AEM [!UICONTROL Content Fragments] in [!DNL Target], considerare quanto segue:

* Questa funzione richiede una licenza come cliente di [!DNL Adobe Experience Manager as a Cloud Service]. Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL A/B Test]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Auto-Allocate]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Auto-Target]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Experience Targeting] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Multivariate Test] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Recommendations]](/help/main/c-recommendations/recommendations.md)

* È possibile utilizzare [!UICONTROL Content Fragments] in [!DNL Target] attività utilizzando solo il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *impossibile* utilizzare [!UICONTROL Content Fragments] in [!DNL Target] attività utilizzando [!UICONTROL Visual Experience Composer] (VEC).

Per ulteriori informazioni su AEM [!UICONTROL Content Fragments] e [!UICONTROL Experience Fragments], vedere [Panoramica su AEM [!UICONTROL Experience Fragments] e [!UICONTROL Content Fragments]](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

Devi utilizzare [[!DNL AEM] as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it){target=_blank}. Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Configurazione e utilizzo di [!UICONTROL Content Fragments] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per esportare [!UICONTROL Content Fragments] da utilizzare nelle attività [!DNL Target], è necessario eseguire alcuni passaggi preliminari in AEM. Per ulteriori informazioni, consulta [Esportazione di frammenti di contenuto in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=it){target=_blank} nella *documentazione di Experience Manager as a Cloud Service*.

Experience Manager Per informazioni sulla progettazione, la creazione, la cura e la pubblicazione di [!UICONTROL Content Fragments], vedere [[!UICONTROL Content Fragments]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=it){target=_blank} e [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=it){target=_blank} nella [documentazione dell&#39;as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=it){target=_blank}.

## Utilizzo di [!UICONTROL Content Fragments] nelle attività [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, [!UICONTROL Content Fragment] viene visualizzato nella pagina [!UICONTROL Offers] in [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL Content Fragments] per importare ogni dieci minuti. Il [!UICONTROL Content Fragment] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.

[!UICONTROL Content Fragment] è importato in [!DNL Target] come offerta JSON. La versione &quot;primaria&quot; di [!UICONTROL Content Fragment] rimane in [!DNL AEM]. Impossibile modificare [!UICONTROL Content Fragment] in [!DNL Target].

È possibile filtrare ed eseguire ricerche in base a [!UICONTROL HTML XFs], [!UICONTROL JSON XFs] e [!UICONTROL Content Fragments] per distinguere tra i diversi tipi di offerte esportati in [!DNL Target].

![Filtrare per tipi di frammento di contenuto: HTML o JSON nell’interfaccia di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Passa il puntatore del mouse su un [!UICONTROL Content Fragment] nell&#39;elenco, quindi fai clic sull&#39;icona [!UICONTROL View] ![Info](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) per visualizzare ulteriori informazioni su [!UICONTROL Content Fragment], inclusi [!UICONTROL AEM path] e [!UICONTROL AEM deep link]. Fare clic sulla scheda [!UICONTROL Offer Usage] per visualizzare le attività che fanno riferimento a questa offerta.

![Finestra a comparsa con informazioni sul frammento di contenuto](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

È possibile utilizzare [!UICONTROL Content Fragments] in [!DNL Target] attività utilizzando solo il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *impossibile* utilizzare [!UICONTROL Content Fragments] in [!DNL Target] attività tramite il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md). [!UICONTROL Content Fragments] sono esportati come JSON in [!DNL Target] e non possono essere utilizzati nelle attività create utilizzando il Compositore esperienza visivo.

>[!TIP]
>
>Utilizzare l&#39;intelligenza artificiale, l&#39;apprendimento automatico e i consigli con [!UICONTROL Content Fragments]:
>
>* Per utilizzare completamente la funzionalità di IA e ML [!DNL Target], è possibile selezionare [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un&#39;attività [!UICONTROL A/B Test].
>
>* [!UICONTROL Content Fragments] non sono supportati nelle attività [!DNL Recommendations]. Tuttavia, per utilizzare [!UICONTROL Content Fragments] per i consigli è possibile creare un&#39;attività [!UICONTROL A/B Test] (inclusi [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target]) o un&#39;attività [!UICONTROL Experience Targeting] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Per utilizzare [!UICONTROL Content Fragments] utilizzando [!UICONTROL Form-based Experience Composer]:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), selezionare il percorso nella pagina in cui si desidera inserire il contenuto [!DNL AEM], quindi selezionare **[!UICONTROL Change Content Fragment]** per visualizzare l&#39;elenco [!UICONTROL Choose a Content Fragment].

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   Nell&#39;elenco [!UICONTROL Content Fragment] sono visualizzati i contenuti creati in [!DNL AEM] che ora sono disponibili in modo nativo in [!DNL Target].

1. Selezionare il [!UICONTROL Content Fragment] desiderato, quindi fare clic su **[!UICONTROL Save]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] cerca attualmente [!UICONTROL Content Fragments] per importare ogni dieci minuti. Il [!UICONTROL Content Fragment] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.
* [!UICONTROL Content Fragment] è importato in [!DNL Target] come offerta JSON. La versione &quot;primaria&quot; di [!UICONTROL Content Fragment] rimane in [!DNL AEM]. Impossibile modificare [!UICONTROL Content Fragment] in [!DNL Target].
* Impossibile creare [!UICONTROL Content Fragments] con [!DNL Adobe I/O]. Creare [!UICONTROL Content Fragments] utilizzando AEM, come spiegato in precedenza.
* Se aggiorni [!UICONTROL Content Fragment] in AEM, [!UICONTROL Content Fragment] deve essere pubblicato ed esportato di nuovo in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.
