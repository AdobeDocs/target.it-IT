---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di contenuto;frammenti;CF;cf;headless;personalizzazione;sperimentazione
description: Scopri come utilizzare la funzione di [!DNL Adobe Experience Manager] [!UICONTROL Frammenti di contenuto] nelle attività di  [!DNL Adobe Target] .
title: Come posso utilizzare i [!UICONTROL frammenti di contenuto] di [!DNL Adobe Experience Manager] (AEM)?
feature: Integrations
exl-id: 2057d9fe-c0f9-41d5-82e1-529db9ef7ca5
source-git-commit: 593cbcc1ff8ccae7afa6098524e95659aa6890f3
workflow-type: ht
source-wordcount: '736'
ht-degree: 100%

---

# [!UICONTROL Frammenti di contenuto] di AEM

Puoi utilizzare i [!UICONTROL frammenti di contenuto] (FC) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare la personalizzazione e la sperimentazione.

## Considerazioni

Quando utilizzi i [!UICONTROL frammenti di contenuto] di AEM in [!DNL Target], considera quanto segue:

* Questa funzione richiede una licenza come cliente di [!DNL Adobe Experience Manager as a Cloud Service]. Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Frammenti di esperienza] e [!UICONTROL frammenti di contenuto] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Targeting dell’esperienza] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Frammenti di esperienza] e [!UICONTROL frammenti di contenuto] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test multivariato] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Raccomandazioni]](/help/main/c-recommendations/recommendations.md)

* Puoi sfruttare i [!UICONTROL frammenti di contenuto] solo nelle attività di [!DNL Target] che utilizzano il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *Non* puoi sfruttare i [!UICONTROL frammenti di contenuto] nelle attività di [!DNL Target] che utilizzano il [!UICONTROL Compositore esperienza visivo].

Per ulteriori informazioni sui [!UICONTROL frammenti di contenuto] e [!UICONTROL frammenti di esperienza] di AEM, consulta [Panoramica dei [!UICONTROL frammenti di esperienza] e [!UICONTROL frammenti di contenuto] di AEM](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

Devi utilizzare [[!DNL AEM] as a Cloud Service](https://experienceleague.corp.adobe.com/docs/experience-manager-cloud-service.html?lang=it){target=_blank}. Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Configurazione e utilizzo dei [!UICONTROL frammenti di contenuto] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per esportare [!UICONTROL frammenti di contenuto] da utilizzare nelle attività di [!DNL Target], devi eseguire alcuni passaggi preliminari in AEM. Per ulteriori informazioni, consulta [Esportazione di frammenti di contenuto in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/content-fragments-target.html?lang=it){target=_blank} nella *documentazione di Experience Manager as a Cloud Service*.

Per informazioni sulla progettazione, la creazione, la cura e la pubblicazione di [!UICONTROL frammenti di contenuto], consulta [[!UICONTROL Frammenti di contenuto]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/content-fragments.html?lang=it){target=_blank} and [Working with Content Fragments](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments.html?lang=it){target=_blank} in the [Experience Manager as a Cloud Service documentation](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/home.html?lang=it){target=_blank}.

## Utilizzo dei [!UICONTROL frammenti di contenuto] nelle attività di [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il [!UICONTROL frammento di contenuto] viene visualizzato nella pagina [!UICONTROL Offerte] di [!DNL Target].

[!DNL Target] attualmente cerca [!UICONTROL frammenti di contenuto] da importare ogni dieci minuti. Il [!UICONTROL frammento di contenuto] importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.

Il [!UICONTROL frammento di contenuto] viene importato in [!DNL Target] come offerta JSON. La versione “primaria” del [!UICONTROL frammento di contenuto] rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL frammento di contenuto] in [!DNL Target].

Puoi filtrare ed eseguire ricerche per [!UICONTROL XF HTML], [!UICONTROL XF JSON] e [!UICONTROL Frammenti di contenuto] per distinguere tra i diversi tipi di offerta esportati in [!DNL Target].

![Filtrare per tipi di frammento di contenuto: HTML o JSON nell’interfaccia di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Puoi passare il cursore sopra un [!UICONTROL frammento di contenuto] nell’elenco, quindi fare clic sull’icona [!UICONTROL Visualizza] ![Icona Info](/help/main/c-integrating-target-with-mac/aem/assets/icon-info.png) per visualizzare informazioni aggiuntive sul [!UICONTROL frammento di contenuto], tra cui [!UICONTROL Percorso AEM] e [!UICONTROL Collegamento profondo AEM]. Fai clic sulla scheda [!UICONTROL Utilizzo offerta] per visualizzare le attività che fanno riferimento a questa offerta.

![Finestra a comparsa con informazioni sul frammento di contenuto](/help/main/c-integrating-target-with-mac/aem/assets/cf-info-popup.png)

Puoi sfruttare i [!UICONTROL frammenti di contenuto] solo nelle attività di [!DNL Target] che utilizzano il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md). *Non* puoi sfruttare i [!UICONTROL frammenti di contenuto] nelle attività di [!DNL Target] che utilizzano il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md). I [!UICONTROL frammenti di contenuto] vengono esportati come codice JSON in [!DNL Target] e non possono essere utilizzati nelle attività create mediante il Compositore esperienza visivo.

>[!TIP]
>
>Utilizza funzioni di intelligenza artificiale, apprendimento automatico e consigli con i [!UICONTROL frammenti di contenuto]:
>
>* Per sfruttare appieno le funzionalità basate su IA e ML di [!DNL Target], seleziona [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un’attività [!UICONTROL Test A/B].
>
>* I [!UICONTROL frammenti di contenuto] non sono supportati nelle attività di [!DNL Recommendations]. Tuttavia, per utilizzare [!UICONTROL frammenti di contenuto] per i consigli è possibile creare un’attività [!UICONTROL Test A/B] (che comprende [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un’attività di [!UICONTROL Targeting dell’esperienza] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Per utilizzare i [!UICONTROL rrammenti di contenuto] tramite il [!UICONTROL Compositore esperienza basato su moduli]:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona la posizione della pagina in cui desideri inserire il contenuto di [!DNL AEM], quindi seleziona **[!UICONTROL Cambia frammento di contenuto]** per visualizzare l’elenco [!UICONTROL Scegli un frammento di contenuto].

   ![content_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/choose-content-fragment.png)

   L’elenco [!UICONTROL Frammenti di contenuto] presenta tutti i contenuti creati in [!DNL AEM] che ora sono disponibili in modo nativo in [!DNL Target].

1. Seleziona il [!UICONTROL frammento di contenuto] desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] attualmente cerca [!UICONTROL frammenti di contenuto] da importare ogni dieci minuti. Il [!UICONTROL frammento di contenuto] importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.
* Il [!UICONTROL frammento di contenuto] viene importato in [!DNL Target] come offerta JSON. La versione “primaria” del [!UICONTROL frammento di contenuto] rimane in [!DNL AEM]. Non è possibile modificare il [!UICONTROL frammento di contenuto] in [!DNL Target].
* Non è possibile creare [!UICONTROL frammenti di contenuto] utilizzando [!DNL Adobe I/O]. Crea [!UICONTROL frammenti di contenuto] utilizzando AEM, come spiegato in precedenza.
* Se aggiorni il [!UICONTROL frammento di contenuto] in AEM, il [!UICONTROL frammento di contenuto] deve essere pubblicato ed esportato nuovamente in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.
