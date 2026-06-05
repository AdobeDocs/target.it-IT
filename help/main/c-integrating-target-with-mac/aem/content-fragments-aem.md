---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di contenuto;frammenti;CF;cf;headless;personalizzazione;sperimentazione
description: Scopri come utilizzare  [!DNL Adobe Experience Manager] [!UICONTROL Frammenti di contenuto] in [!DNL Adobe Target] attività.
title: Come Si Utilizza  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Frammenti Di Contenuto]?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
TQID: https://experienceleague.adobe.com/tb500kFSZoR3czs10Gs3EIOWEX2ybnd7tSWwDmWSMWQ
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 775
ht-degree: 20%

---

# AEM [!UICONTROL Frammenti di contenuto]

Utilizza [!UICONTROL Frammenti di contenuto] (FC) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare la personalizzazione e la sperimentazione headless.

## Considerazioni

Considera quanto segue mentre lavori con AEM [!UICONTROL Frammenti di contenuto] in [!DNL Target]:

* Questa funzione richiede una licenza come cliente di [!DNL Adobe Experience Manager as a Cloud Service]. Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Targeting dell’esperienza] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test multivariato] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Funzione Consigli]](/help/main/c-recommendations/recommendations.md)

* Puoi utilizzare [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività utilizzando solo il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *impossibile* utilizzare [!UICONTROL Frammenti di contenuto] nelle attività [!DNL Target] utilizzando il [!UICONTROL Compositore esperienza visivo].

Per ulteriori informazioni su [!UICONTROL Frammenti di contenuto] e [!UICONTROL Frammenti di esperienza] di AEM, consulta la [panoramica su [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] di AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

Devi usare [[!DNL AEM] as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=it){target=_blank}. Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Configurazione e utilizzo di [!UICONTROL Frammenti di contenuto] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per esportare [!UICONTROL Frammenti di contenuto] da utilizzare nelle attività [!DNL Target], è necessario eseguire alcuni passaggi preliminari in AEM. Per ulteriori informazioni, vedere [Esportazione di frammenti di contenuto in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=it){target=_blank} nella *documentazione di Experience Manager as a Cloud Service*.

Per informazioni sulla progettazione, la creazione, la cura e la pubblicazione di [!UICONTROL frammenti di contenuto], vedere [[!UICONTROL Frammenti di contenuto]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=it){target=_blank} e [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=it){target=_blank} nella [documentazione di Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=it){target=_blank}.

## Utilizzo di [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il [!UICONTROL frammento di contenuto] viene visualizzato nella pagina [!UICONTROL Offerte] in [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL Frammenti di contenuto] da importare ogni dieci minuti. Il [!UICONTROL frammento di contenuto] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.

Il [!UICONTROL frammento di contenuto] è importato in [!DNL Target] come offerta JSON. La versione &quot;primaria&quot; del [!UICONTROL frammento di contenuto] rimane in [!DNL AEM]. Impossibile modificare il [!UICONTROL frammento di contenuto] in [!DNL Target].

Puoi filtrare ed eseguire ricerche per [!UICONTROL XFs], [!UICONTROL XFs] JSON e [!UICONTROL Frammenti di contenuto] per distinguere tra diversi tipi di offerte esportati in [!DNL Target].

![Filtrare per tipi di frammento di contenuto: HTML o JSON nell’interfaccia di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Puoi passare il cursore del mouse su un [!UICONTROL frammento di esperienza] nell&#39;elenco, quindi fare clic sull&#39;icona [!UICONTROL Visualizza] ![Informazioni](/help/main/assets/icons/InfoOutline.svg) per visualizzare ulteriori informazioni sul [!UICONTROL frammento di contenuto], incluso il relativo [!UICONTROL Nome], [!UICONTROL Tipo], [!UICONTROL ID offerta], [!UICONTROL Percorso offerta] e informazioni sulle ultime modifiche. Fai clic su [!UICONTROL [!UICONTROL Visualizza dettagli completi]] per visualizzare le attività che fanno riferimento a questa offerta.

Puoi utilizzare [!UICONTROL Frammenti di contenuto] in [!DNL Target] attività utilizzando solo il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *impossibile* utilizzare [!UICONTROL Frammenti di contenuto] nelle attività [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md). [!UICONTROL I frammenti di contenuto] sono esportati come JSON in [!DNL Target] e non possono essere utilizzati nelle attività create utilizzando il Compositore esperienza visivo.

>[!TIP]
>
>Utilizza l&#39;intelligenza artificiale, l&#39;apprendimento automatico e i consigli con [!UICONTROL frammenti di contenuto]:
>
>* Per utilizzare completamente la funzionalità di IA e ML [!DNL Target], è possibile selezionare [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un&#39;attività [!UICONTROL Test A/B].
>
>* [!UICONTROL I frammenti di contenuto] non sono supportati nelle attività [!DNL Recommendations]. Tuttavia, per utilizzare [!UICONTROL Frammenti di contenuto] per i consigli, puoi creare un&#39;attività [!UICONTROL Test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un&#39;attività [!UICONTROL Targeting esperienza] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Per utilizzare [!UICONTROL Frammenti di contenuto] tramite il [!UICONTROL Compositore esperienza basato su moduli]:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), selezionare il percorso nella pagina in cui si desidera inserire il contenuto [!DNL AEM], quindi selezionare **[!UICONTROL Cambia frammento di contenuto]** per visualizzare l&#39;elenco [!UICONTROL Scegli un frammento di contenuto].

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   Nell&#39;elenco [!UICONTROL Frammento di contenuto] è visualizzato il contenuto creato in [!DNL AEM] che è ora disponibile in modo nativo in [!DNL Target].

1. Seleziona il [!UICONTROL frammento di contenuto] desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] cerca attualmente [!UICONTROL Frammenti di contenuto] da importare ogni dieci minuti. Il [!UICONTROL frammento di contenuto] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.
* Il [!UICONTROL frammento di contenuto] è importato in [!DNL Target] come offerta JSON. La versione &quot;primaria&quot; del [!UICONTROL frammento di contenuto] rimane in [!DNL AEM]. Impossibile modificare il [!UICONTROL frammento di contenuto] in [!DNL Target].
* Impossibile creare [!UICONTROL frammenti di contenuto] utilizzando [!DNL Adobe I/O]. Crea [!UICONTROL frammenti di contenuto] con AEM, come descritto in precedenza.
* Se aggiorni il [!UICONTROL frammento di contenuto] in AEM, il [!UICONTROL frammento di contenuto] deve essere pubblicato ed esportato di nuovo in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.
