---
keywords: esperienza;json;aem;adobe experience manager;export to adobe target;experience fragments;fragments;XF
description: Informazioni sull’utilizzo di frammenti esperienza creati in Adobe Experience Manager (AEM) nelle attività di Adobe Target per facilitare l’ottimizzazione o la personalizzazione.
title: Frammenti esperienza Adobe Experience Manager (AEM) in Adobe Target
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: 217ca811521e67dcd1b063d77a644ba3ae94a72c

---


# Frammenti di esperienza AEM{#aem-experience-fragments}

Information about using experience fragments created in [!DNL Adobe Experience Manager] (AEM) in [!DNL Target] activities to aid optimization or personalization.

>[!NOTE]
>
>This feature requires that you are an [!DNL Adobe Experience Manager] (AEM) customer. Per ulteriori informazioni, consulta [“Risoluzione dei problemi”](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A).

## Panoramica {#section_95A91830530F493B81C5C9CDB9B783EA}

Using experience fragments created in AEM in [!DNL Target] activities lets you combine the ease-of-use and power of AEM with powerful Automated Intelligence (AI) and Machine Learning (ML) capabilities in [!DNL Target] to test and personalize experiences at scale.

AEM riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. AEM consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un'unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo. AEM regola automaticamente ogni esperienza utilizzando il contenuto.

[!DNL Target] consente di fornire esperienze personalizzate in scala su una combinazione di approcci di apprendimento automatico basati sulle regole e guidati da intelligenze automatizzate che incorporano variabili comportamentali, contestuali e offline. With [!DNL Target] you can easily set up and run [A/B Test](/help/c-activities/t-test-ab/test-ab.md) and [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) activities to determine the best offers, content, and experiences.

Frammenti di esperienza rappresentano un enorme passo avanti per collegare i creatori e i manager di contenuto/esperienza e professionisti di personalizzazione e ottimizzazione che stanno guidando i risultati di business tramite [!DNL Target].

## Requisiti {#section_AE6F0971E1574B3AA324003599B96E5A}

You must be provisioned with the experience fragments functionality within [!DNl Target]. Inoltre, devi utilizzare AEM 6.3 con il service pack appropriato o AEM 6.4 (o versione successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* Adobe Experience Manager 6.4 (o successive).
* Adobe Experience Manager 6.3 SP2 (o successive).
* Account Adobe Target Standard o Adobe Target Premium.
* Contact [Adobe Target Customer Care](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) to enable the integration and to provide you with authentication details.

## Creazione e configurazione di frammenti di esperienza in AEM {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

In order to use AEM experience fragments in [!DNL Target], you must perform the following steps:

### Passaggio 1: integrare AEM con Target

Per ulteriori informazioni, consulta:

* **AEM 6.3**: [Scegliere Adobe Analytics e Adobe Target](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) nella documentazione di _Adobe Experience Manager 6.3_ .
* **AEM 6.4**: [Scegliere Adobe Analytics e Adobe Target](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) nella documentazione di _Adobe Experience Manager 6.4_ .
* **AEM 6.5**: [Scegliere Adobe Analytics e Adobe Target](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) nella documentazione di *Adobe Experience Manager 6.5* .

### Passaggio 2: creare il frammento di esperienza

I frammenti di esperienza sono creati in AEM. Per ulteriori informazioni, consulta:

* **AEM 6.3**: Frammenti [](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) esperienza nella documentazione di *Adobe Experience Manager 6.3* .
* **AEM 6.4**: Frammenti [](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) esperienza nella documentazione di *Adobe Experience Manager 6.4* .
* **AEM 6.5**: Frammenti [](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) esperienza nella documentazione di *Adobe Experience Manager 6.5* .

### Passaggio 3: configurare AEM per condividere il frammento di esperienza con Target

1. Dall’interno di AEM, seleziona il frammento di esperienza desiderato o la cartella che lo contiene, quindi fai clic su **[!UICONTROL Proprietà]**.
2. Click the **[!UICONTROL Cloud Services]** tab, then from the **[!UICONTROL Cloud Service Configuration]** drop-down list, select **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >The previous step assumes that someone in your organization has created the [!DNL Adobe Target] configuration.

3. Fai clic su **[!UICONTROL Salva e chiudi]**.

### Passaggio 4: pubblicare il frammento esperienza ed esportarlo in Target

A seconda della versione di AEM in uso, consultate i seguenti collegamenti per istruzioni dettagliate:

* **AEM 6.3**: Esportazione [di un frammento esperienza in Target](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) nella documentazione di *Adobe Experience Manager 6.3* .
* **AEM 6.4**: Esportazione [di un frammento esperienza in Target](https://docs.adobe.com/content/help/en/experience-manager-64/administering/integration/experience-fragments-target.html) nella documentazione di *Adobe Experience Manager 6.4* .
* **AEM 6.5**: Esportazione [di un frammento esperienza in Target](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) nella documentazione di *Adobe Experience Manager 6.5* .

## Utilizzo di frammenti di esperienza nelle attività di Target {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il frammento di esperienza viene visualizzato nella pagina [!UICONTROL Offerte] di Target.

>[!NOTE]
>
>[!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.

>[!IMPORTANT]
>
>The experience fragment is currently imported into [!DNL Target] as an HTML offer. Nota che il frammento di esperienza nella versione “master” rimane in AEM. Non è possibile modificare il frammento di esperienza in Target.

You can hover over an experience fragment in the list, then click the View icon ![View icon](assets/icon_info.png) to see additional information about the experience fragment, including its public offer delivery URL, its AEM path, and a deep link to open the experience fragment inside of AEM.

You can consume Experience Fragments in [!DNL Target] activities using the [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) or the [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>To fully utilize the [!DNL Target] AI and ML functionality, you can select [Auto-Allocate](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) or [Auto-Allocate](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) while creating an A/B Test.

**Per utilizzare frammenti di esperienza utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target]quando create o modificate un'esperienza in [Visual Experience Composer (Compositore esperienza visivo](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D)), fate clic sul percorso nella pagina in cui desiderate inserire il contenuto AEM, quindi selezionate l'opzione desiderata per visualizzare l'elenco [!UICONTROL Choose an Experience Fragment (Scegli un frammento] esperienza).

   * [!UICONTROL Inserisci prima]
   * [!UICONTROL Inserisci dopo]
   * [!UICONTROL Sostituire con un frammento esperienza]
   L’elenco [!UICONTROL Frammenti esperienza] presenta tutti i contenuti creati in AEM che ora sono disponibili in modo nativo in [!DNL Target].

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Scambia con frammento esperienza] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![](assets/experience_fragment_list.png)

1. Select the desired experience fragment, then click **[!UICONTROL Done]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](../../c-activities/t-test-ab/t-test-create-ab/test-create-ab.md#task_68C8079BF9FF4625A3BD6680D554BB72)
   * **Allocazione automatica:** [Allocazione automatica](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico per esperienze personalizzate](../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](../../c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](../../c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Test multivariato (MVT):** [Creare un test multivariato](../../c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendationfs:** [Creare un’attività di Recommendations](../../c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**Per utilizzare frammenti di esperienza tramite il Compositore esperienza basato su moduli:**

1. In [!DNTarget], durante la creazione o la modifica di un'esperienza in Experience Composer (Compositore esperienza basato su [moduli](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E)), selezionate il percorso nella pagina in cui desiderate inserire il contenuto AEM, quindi selezionate **[!UICONTROL Modifica frammento]** esperienza per visualizzare l'elenco [!UICONTROL Scegli un frammento] esperienza.

   ![](assets/experience_fragment_list.png)

   L’elenco [!UICONTROL Frammenti esperienza] presenta tutti i contenuti creati in AEM che ora sono disponibili in modo nativo in [!DNL Target].

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Considerazioni {#considerations}

* [!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. The imported experience fragment should be available in [!DNL Target] within ten minutes, but this time frame should shorten going forward.
* The experience fragment is currently imported into [!DNL Target] as an HTML offer. Nota che il frammento di esperienza nella versione “master” rimane in AEM. Non è possibile modificare il frammento di esperienza in [!DNL Target].
* Potete importare offerte JSON come frammenti esperienza in [!DNL Target]. Tuttavia, queste offerte vengono importate come offerte HTML. Le offerte JSON (frammenti esperienza) non sono attualmente completamente supportate nell' [!DNL Target] interfaccia utente.

## Video di formazione: Utilizzo dei frammenti esperienza AEM con Adobe Target {#section_C0EDC54063464F41A182492D2045BC64}

Il seguente video illustra come impostare e utilizzare i frammenti di esperienza: [Uso dei frammenti di esperienza AEM con Adobe Target](https://helpx.adobe.com/experience-manager/kt/sites/using/experience-fragment-target-feature-video-use.html).
