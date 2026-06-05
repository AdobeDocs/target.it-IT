---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
description: Scopri come utilizzare  [!DNL Adobe Experience Manager] [!UICONTROL Frammenti di esperienza] in [!DNL Adobe Target] attività.
title: Come Si Utilizza  [!DNL Adobe Experience Manager] (AEM) [!UICONTROL Frammenti Esperienza]?
feature: Integrations
exl-id: 400d0cde-e435-4cac-9bf0-64a6cad98995
TQID: https://experienceleague.adobe.com/-W1ELJx0ajes6BPEVIiS8q6ebmRLTTgIrxvGMUEWEaM
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: f7c7de77-382f-4f48-8b36-61a170f06d3d
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1446
ht-degree: 32%

---

# [!UICONTROL Frammenti esperienza] di AEM

Utilizza [!UICONTROL Frammenti esperienza] (XF) creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare l&#39;ottimizzazione e la personalizzazione.

## Considerazioni

Considera quanto segue mentre lavori con i [!UICONTROL Frammenti esperienza] di AEM in [!DNL Target]:

* Questa funzionalità è disponibile solo per chi è cliente [!DNL Adobe Experience Manager] (AEM). Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A), di seguito.
* [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test A/B]](/help/main/c-activities/t-test-ab/test-ab.md)
   * [[!UICONTROL Allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md)
   * [[!UICONTROL Targeting automatico]](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * [[!UICONTROL Automated Personalization] (AP)](/help/main/c-activities/t-automated-personalization/automated-personalization.md)
   * [[!UICONTROL Targeting dell’esperienza] (XT)](/help/main/c-activities/t-experience-target/experience-target.md)

* [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] non sono disponibili per i seguenti tipi di attività:

   * [[!UICONTROL Test multivariato] (MVT)](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md)
   * [[!UICONTROL Funzione Consigli]](/help/main/c-recommendations/recommendations.md)

* È possibile utilizzare [!UICONTROL Frammenti di esperienza] in [!DNL Target] attività utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) e il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

Per ulteriori informazioni su [!UICONTROL Frammenti di esperienza] e [!UICONTROL Frammenti di contenuto] di AEM, consulta [AEM [!UICONTROL Frammenti di esperienza] e Panoramica sui frammenti di contenuto](/help/main/c-integrating-target-with-mac/aem/aem-experience-and-content-fragments.md).

## Requisiti {#requirements}

Devi essere provvisto della funzionalità [!UICONTROL Frammenti esperienza] in [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] as a Cloud Service o [!DNL AEM] versione 6.4 (o successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* [!DNL Adobe Experience Manager] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5
* [!DNL Adobe Experience Manager] 6.4
* Account [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium].

Le versioni 6.3 e 6.4 di [!DNL Adobe Experience Manager] hanno raggiunto la fine del ciclo di vita e non sono più supportate (ad eccezione dei clienti che hanno acquistato un’estensione del supporto).

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Creazione e configurazione di [!UICONTROL Frammenti esperienza] in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare [!DNL AEM] [!UICONTROL Frammenti esperienza] in [!DNL Target], è necessario eseguire i passaggi seguenti:

### Passaggio 1: Integrare [!DNL AEM] con [!DNL Target]

Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [Integrazione con Adobe Target](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **Adobe Developer**: [Integrazione con Adobe Target tramite Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-target-ims-adobe-io.html?lang=it){target=_blank} nella *Guida utente per l&#39;amministrazione*.
* **[!DNL AEM]6.5**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Scelta di Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 2: creare il frammento di esperienza

[!UICONTROL Frammenti esperienza] creati in [!DNL AEM]. Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [[!UICONTROL Frammenti esperienza]](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=it){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [[!UICONTROL Frammenti esperienza]](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [[!UICONTROL Frammenti esperienza]](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 3: configurare [!DNL AEM] per condividere il [!UICONTROL frammento di esperienza] con [!DNL Target]

1. Dall&#39;interno di [!DNL AEM], seleziona il [!UICONTROL frammento di esperienza] desiderato o la cartella che lo contiene, quindi fai clic su **[!UICONTROL Proprietà]**.
2. Fai clic sulla scheda **[!UICONTROL Servizi cloud]**, quindi seleziona **[!UICONTROL Adobe Target]** dall&#39;elenco a discesa **[!UICONTROL Configurazione Cloud Service]**.

   Il passaggio precedente presuppone che un utente dell’azienda abbia creato la configurazione di [!DNL Adobe Target].

3. Fai clic su **[!UICONTROL Salva e chiudi]**.

### Passaggio 4: pubblicare il [!UICONTROL frammento esperienza] ed esportarlo in [!DNL Target]

A seconda della versione di [!DNL AEM], consulta i seguenti collegamenti per istruzioni dettagliate:

* **AEM as a Cloud Service**: [Esportazione di [!UICONTROL Frammenti esperienza] in Adobe Target](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target?lang=en){target=_blank} nella *guida di Experience Manager as a Cloud Service*.
* **[!DNL AEM]6.5**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.5*.
* **[!DNL AEM]6.4**: [Esportazione di un frammento di esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nella documentazione di *Adobe Experience Manager 6.4*.

## Utilizzo di [!UICONTROL Frammenti esperienza] in [!DNL Target] attività {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il [!UICONTROL Frammento esperienza] viene visualizzato nella pagina [!UICONTROL Offerte] in [!DNL Target].

[!DNL Target] cerca attualmente [!UICONTROL Frammenti esperienza] per importare ogni dieci minuti. Il [!UICONTROL frammento di esperienza] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.

Il [!UICONTROL frammento di esperienza] è importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;primaria&quot; di [!UICONTROL Frammento esperienza] rimane in [!DNL AEM]. Impossibile modificare il [!UICONTROL frammento esperienza] in [!DNL Target].

È possibile filtrare ed eseguire ricerche in base a [!UICONTROL XFs] di HTML e [!UICONTROL XFs JSON] per distinguere tra i tipi di [!UICONTROL Frammenti esperienza] esportati in [!DNL Target].

![Filtrare per tipi di frammento di esperienza: HTML o JSON nell’interfaccia utente di Target](/help/main/c-integrating-target-with-mac/aem/assets/fragment-types.png)

Puoi passare il cursore del mouse su un [!UICONTROL frammento di esperienza] nell&#39;elenco, quindi fare clic sull&#39;icona [!UICONTROL Visualizza] ![Informazioni](/help/main/assets/icons/InfoOutline.svg) per visualizzare ulteriori informazioni sul [!UICONTROL frammento di esperienza], incluso il relativo [!UICONTROL Nome], [!UICONTROL Tipo], [!UICONTROL ID offerta], [!UICONTROL Percorso offerta] e informazioni sulle ultime modifiche. Fai clic su [!UICONTROL [!UICONTROL Visualizza dettagli completi]] per visualizzare le attività che fanno riferimento a questa offerta.

![Finestra a comparsa con informazioni sul frammento di esperienza](/help/main/c-integrating-target-with-mac/aem/assets/xf-info-popup.png)

È possibile utilizzare [!UICONTROL Frammenti di esperienza] in [!DNL Target] attività utilizzando il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) e il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

>[!TIP]
>
>Utilizza l&#39;intelligenza artificiale, l&#39;apprendimento automatico e i consigli con [!UICONTROL Frammenti esperienza]:
>
>* Per sfruttare appieno le funzionalità basate su IA e ML di [!DNL Target], seleziona [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un’attività.
>
>* [!UICONTROL I frammenti di esperienza] non sono supportati nelle attività [!DNL Recommendations]. Tuttavia, per utilizzare [!UICONTROL Frammenti esperienza] per i consigli, puoi creare un&#39;attività [!UICONTROL Test A/B] (tra cui [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un&#39;attività [!UICONTROL Targeting esperienza] (XT) e [includere i consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md).

**Per utilizzare [!UICONTROL Frammenti esperienza] utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza visivo](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fare clic sul percorso nella pagina in cui si desidera inserire il contenuto [!DNL AEM], quindi fare clic su **[!UICONTROL Sostituisci contenuto]** > **[!UICONTROL Frammento esperienza]** per visualizzare la finestra di dialogo [!UICONTROL Frammento esperienza].

   La finestra di dialogo [!UICONTROL Frammento esperienza] visualizza il contenuto creato in [!DNL AEM] che è ora disponibile in modalità nativa in [!DNL Target].

   >[!NOTE]
   >
   >L&#39;opzione [!UICONTROL Sostituisci contenuto] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

1. Seleziona il [!UICONTROL frammento di esperienza] desiderato, quindi fai clic su **[!UICONTROL Aggiungi]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Allocazione automatica:** [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Consigli in un’attività Test A/B o XT:** [consigli come offerta](/help/main/c-recommendations/recommendations-as-an-offer.md)

   I [!UICONTROL Frammenti esperienza] esportati come JSON in [!DNL Target] non possono essere utilizzati nelle attività create utilizzando il Compositore esperienza visivo. Nelle attività basate sul Compositore esperienza visivo sono supportati solo i [!UICONTROL Frammenti esperienza] HTML. Se desideri utilizzare [!UICONTROL Frammenti esperienza] JSON, utilizzali nelle attività create utilizzando il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

**Per utilizzare [!UICONTROL Frammenti di esperienza] tramite il [!UICONTROL Compositore esperienza basato su moduli]:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona il percorso nella pagina in cui desideri inserire il contenuto di [!DNL AEM], fai clic sull&#39;icona **[!UICONTROL Ulteriori dettagli]** ( ![Icona Altri dettagli](/help/main/assets/icons/MoreSmall.svg) ), quindi seleziona **[!UICONTROL Cambia frammento esperienza]** per visualizzare la finestra di dialogo [!UICONTROL Cambia frammento esperienza].

   ![experience_fragment_list image](/help/main/c-integrating-target-with-mac/aem/assets/experience_fragment_list.png)

   La finestra di dialogo [!UICONTROL Frammento esperienza] visualizza il contenuto creato in [!DNL AEM] che è ora disponibile in modalità nativa in [!DNL Target].

1. Seleziona il [!UICONTROL frammento di esperienza] desiderato, quindi fai clic su **[!UICONTROL Aggiungi]**.
1. Termina la configurazione dell’attività.

## Informazioni aggiuntive

* [!DNL Target] cerca attualmente [!UICONTROL Frammenti esperienza] per importare ogni dieci minuti. Il [!UICONTROL frammento di esperienza] importato dovrebbe essere disponibile tra [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi in futuro.
* Il [!UICONTROL frammento di esperienza] è importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;primaria&quot; di [!UICONTROL Frammento esperienza] rimane in [!DNL AEM]. Impossibile modificare il [!UICONTROL frammento esperienza] in [!DNL Target].
* Impossibile creare [!UICONTROL Frammenti esperienza] utilizzando [!DNL Adobe Developer]. Crea [!UICONTROL Frammenti esperienza] con AEM, come descritto in precedenza.
* Se aggiorni il [!UICONTROL frammento di esperienza] in AEM, il [!UICONTROL frammento di esperienza] deve essere pubblicato ed esportato di nuovo in [!DNL Target] in modo che [!DNL Target] possa utilizzare le modifiche più recenti.

## Rimozione di clientlibs e HTML estranei da [!UICONTROL Frammenti esperienza] esportati in [!UICONTROL Target]

Quando si utilizzano le offerte [!UICONTROL Frammento di esperienza] con [!DNL Target] in una pagina distribuita da AEM, la pagina di destinazione contiene già le librerie client necessarie. Inoltre, non sono necessari nemmeno gli elementi HTML estranei nell’offerta.

A volte intere pagine di HTML racchiudono il [!UICONTROL frammento di esperienza] e causano problemi. Assicurati che il [!UICONTROL frammento di esperienza] sia un piccolo pezzo di HTML e non una pagina HTML completa con HTML, HEAD, BODY e così via.

Per ulteriori informazioni, consulta il seguente post sul blog: [AEM 6.5: Removing clientlibs from [!UICONTROL Experience Fragments] export to Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser/){target=_blank}.

## Video di formazione: Utilizzo di [!UICONTROL Frammenti esperienza] in AEM con [!DNL Adobe Target]

Il video seguente illustra come impostare e utilizzare [!UICONTROL Frammenti esperienza]:

>[!VIDEO](https://video.tv.adobe.com/v/326989?captions=ita)

>[!NOTE]
>
>La funzionalità di collegamento diretto di [!DNL AEM] discussa in 4:54 è stata rimossa.

Per informazioni più dettagliate, consulta [Utilizzo di [!UICONTROL Frammenti di esperienza] con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=it) nella pagina *Video e tutorial su AEM Sites*.
