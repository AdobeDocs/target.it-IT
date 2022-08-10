---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
description: Scopri come utilizzare [!DNL Adobe Experience Manager] frammenti di esperienza in [!DNL Adobe Target] attività.
title: Come si utilizza [!DNL Adobe Experience Manager] (AEM) Frammenti esperienza?
feature: Experiences and Offers
exl-id: 3dd811a4-c7be-443d-a5ad-5b9adcaf1a2c
source-git-commit: 470a56c6b1839902af963b1b28b8d56d2089c170
workflow-type: tm+mt
source-wordcount: '1371'
ht-degree: 52%

---

# Frammenti esperienza AEM

Utilizzare i frammenti esperienza creati in [!DNL Adobe Experience Manager] AEM [!DNL Target] attività per facilitare l’ottimizzazione o la personalizzazione.

>[!NOTE]
>
>Questa funzione richiede che [!DNL Adobe Experience Manager] (AEM) cliente. Per ulteriori informazioni, consulta [Requisiti](#section_AE6F0971E1574B3AA324003599B96E5A) sotto.

Utilizzo dei frammenti di esperienza creati in [!DNL AEM] in [!DNL Target] consente di combinare la facilità d&#39;uso e la potenza delle [!DNL AEM] con potenti capacità di intelligenza artificiale (AI) e apprendimento automatico (ML) in [!DNL Target] per testare e personalizzare le esperienze su larga scala.

[!DNL AEM] riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. [!DNL AEM] consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un&#39;unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo. [!DNL AEM] regola automaticamente ogni esperienza utilizzando i tuoi contenuti.

[!DNL Target] consente di fornire esperienze personalizzate in scala su una combinazione di approcci di apprendimento automatico basati sulle regole e guidati da intelligenze automatizzate che incorporano variabili comportamentali, contestuali e offline. Con [!DNL Target], è possibile configurare ed eseguire facilmente [Test A/B](/help/main/c-activities/t-test-ab/test-ab.md) e [Multivariato](/help/main/c-activities/c-multivariate-testing/multivariate-testing.md) Attività (MVT) per determinare le offerte, i contenuti e le esperienze migliori.

Frammenti di esperienza rappresentano un enorme passo avanti per collegare i creatori e i manager di contenuto/esperienza e professionisti di personalizzazione e ottimizzazione che stanno guidando i risultati di business tramite [!DNL Target].

## Requisiti {#section_AE6F0971E1574B3AA324003599B96E5A}

Devi essere provvisto della funzionalità frammenti di esperienza all&#39;interno di [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] as a Cloud Service o [!DNL AEM] 6.4 (o successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* [!DNL Adobe Experience Manager ] as a Cloud Service
* [!DNL Adobe Experience Manager] 6.5.
* [!DNL Adobe Experience Manager] 6.4.
* Account [!DNL Adobe Target Standard] o [!DNL Adobe Target Premium].

>[!NOTE]
>
>[!DNL Adobe Experience Manager] Le versioni 6.3 e 6.4 hanno raggiunto la fine del ciclo di vita e non sono più supportate (ad eccezione dei clienti che hanno acquistato un supporto esteso).

Per abilitare l’integrazione e ottenere i dettagli di autenticazione, contatta l’[Assistenza clienti per Adobe Target](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

## Creazione e configurazione di frammenti di esperienza in[!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare i frammenti di esperienza [!DNL AEM] in [!DNL Target], è necessario attenersi ai seguenti passaggi:

### Passaggio 1: Integrare [!DNL AEM] con [!DNL Target]

Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [Integrazione con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/integrating-adobe-target.html){target=_blank} nel *Experience Manager as a Cloud Service* guida.
* **Adobe I/O**: [Integrazione con Adobe Target tramite Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html?lang=it){target=_blank} nel *Guida utente all’amministrazione* documentazione.
* **[!DNL AEM]6,5**: [Accesso ad Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/opt-in.html?lang=it){target=_blank} nel *Adobe Experience Manager 6.5* documentazione.
* **[!DNL AEM]6.4**: [Accesso ad Adobe Analytics e Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=it){target=_blank} nel *Adobe Experience Manager 6.4* documentazione.

### Passaggio 2: creare il frammento di esperienza

I frammenti di esperienza sono creati in [!DNL AEM]. Per ulteriori informazioni, consulta:

* **AEM as a Cloud Service**: [Frammenti esperienza](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/authoring/fundamentals/experience-fragments.html?lang=en){target=_blank} nel *Experience Manager as a Cloud Service* guida.
* **[!DNL AEM]6,5**: [Frammenti esperienza](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nel *Adobe Experience Manager 6.5* documentazione.
* **[!DNL AEM]6.4**: [Frammenti esperienza](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/experience-fragments.html?lang=it){target=_blank} nel *Adobe Experience Manager 6.4* documentazione.

### Passaggio 3: configurare[!DNL AEM] per condividere il frammento di esperienza con [!DNL Target]

1. Dall’interno di [!DNL AEM], seleziona il frammento di esperienza desiderato o la cartella che lo contiene, quindi fai clic su **[!UICONTROL Proprietà]**.
2. Fa clic sulla scheda **[!UICONTROL Servizi cloud]**, poi, dall&#39;elenco a discesa **[!UICONTROL Configurazione del servizio cloud]**, seleziona **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >Il passaggio precedente presuppone che un utente dell’azienda abbia creato la configurazione di [!DNL Adobe Target].

3. Fai clic su **[!UICONTROL Salva e chiudi]**.

### Passaggio 4: pubblicare il frammento esperienza ed esportarlo in [!DNL Target]

A seconda della versione di [!DNL AEM], consulta i seguenti collegamenti per istruzioni dettagliate:

* **AEM as a Cloud Service**: [Esportazione di frammenti esperienza in Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/sites/integrations/experience-fragments-target.html?lang=en){target=_blank} nel *Experience Manager as a Cloud Service* guida.
* **[!DNL AEM]6,5**: [Esportazione di un frammento esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/experience-fragments-target.html?lang=en){target=_blank} nel *Adobe Experience Manager 6.5* documentazione.
* **[!DNL AEM]6.4**: [Esportazione di un frammento esperienza in Target](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html?lang=it){target=_blank} nel *Adobe Experience Manager 6.4* documentazione.

## Utilizzo di frammenti di esperienza nelle attività di [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il frammento di esperienza viene visualizzato nella pagina [!UICONTROL Offerte] di [!DNL Target].

>[!NOTE]
>
>* [!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. Il frammento di esperienza importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.
>
>* Il frammento di esperienza viene importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;principale&quot; del frammento di esperienza rimane in [!DNL AEM]. Non è possibile modificare il frammento di esperienza in [!DNL Target].


Passa il puntatore del mouse su un frammento di esperienza nell’elenco, quindi fai clic sull’icona [!UICONTROL Visualizza] ![Visualizza icona](assets/icon_info.png) per visualizzare ulteriori informazioni sul frammento di esperienza, compreso l’URL pubblico di consegna dell’offerta e il percorso [!DNL AEM].

Puoi utilizzare frammenti di esperienza nelle attività di [!DNL Target] tramite il [Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/visual-experience-composer.md) o il [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Per utilizzare completamente le [!DNL Target] Funzionalità AI e ML, puoi selezionare [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md) durante la creazione di un test A/B.
>
>I frammenti di esperienza non sono supportati in [!DNL Recommendations] attività. Tuttavia, per utilizzare i frammenti di esperienza per i consigli è possibile creare un [!UICONTROL Test A/B] attività [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico]) o un [!UICONTROL Targeting esperienza] (XT) e [includere consigli come offerta](/help/main/c-experiences/c-manage-content/aem-experience-fragments.md).

**Per utilizzare frammenti di esperienza utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza visivo](/help/main/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fai clic sul percorso nella pagina in cui desideri inserire il contenuto [!DNL AEM], quindi seleziona l’opzione desiderata per visualizzare l’elenco [!UICONTROL Scegli un frammento di esperienza].

   * [!UICONTROL Inserisci prima]
   * [!UICONTROL Inserisci dopo]
   * [!UICONTROL Scambia con frammento di esperienza]

   La [!UICONTROL Frammento esperienza] visualizza il contenuto creato in [!DNL AEM] che ora è disponibile in modo nativo da [!DNL Target].

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Scambia con frammento esperienza] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![](assets/experience_fragment_list.png)

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Fine]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Allocazione automatica:** [Allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](/help/main/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](/help/main/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Test multivariato (MVT):** [Creare un test multivariato](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendationfs:** [Creare un’attività di Recommendations](/help/main/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

>[!NOTE]
>
>Frammenti di esperienza esportati come JSON in [!DNL Target] non può essere utilizzato nelle attività create utilizzando il Compositore esperienza visivo; solo i frammenti di esperienza HTML sono supportati nelle attività basate su VEC. Se desideri utilizzare i frammenti di esperienza JSON, utilizzali nelle attività create utilizzando [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

**Per utilizzare frammenti di esperienza tramite il Compositore esperienza basato su moduli:**

1. In [!DNL Target], durante la creazione o la modifica di un’esperienza nel [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona il percorso nella pagina in cui desideri inserire il contenuto di [!DNL AEM], quindi seleziona **[!UICONTROL Cambia frammento esperienza]** per visualizzare l’elenco [!UICONTROL Scegli un frammento esperienza].

   ![](assets/experience_fragment_list.png)

   La [!UICONTROL Frammento esperienza] visualizza il contenuto creato in [!DNL AEM] che ora è disponibile in modo nativo da [!DNL Target].

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Considerazioni {#considerations}

* [!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. Il frammento di esperienza importato dovrebbe diventare disponibile in [!DNL Target] entro dieci minuti; tuttavia, in futuro dovrebbe richiedere meno tempo.
* Il frammento di esperienza viene importato in [!DNL Target] come offerta HTML o JSON. La versione &quot;principale&quot; del frammento di esperienza rimane in [!DNL AEM]. Non è possibile modificare il frammento di esperienza in [!DNL Target].
* Non puoi creare frammenti di esperienza utilizzando [!DNL Adobe I/O]. Crea frammenti di esperienza utilizzando AEM, come spiegato in precedenza.
* Se aggiorni il frammento esperienza in AEM, il frammento esperienza deve essere pubblicato ed esportato in [!DNL Target] di nuovo [!DNL Target] può utilizzare le modifiche più recenti.

## Rimozione di ClientLibs e HTML estranei dai frammenti di esperienza esportati in Target

Quando si utilizzano offerte di frammenti di esperienza con [!DNL Target] in una pagina consegnata da AEM, la pagina di destinazione contiene già tutte le librerie client necessarie. Inoltre, non sono necessari elementi HTML estranei nell’offerta.

A volte intere pagine di HTML avvolgono il frammento di esperienza e causano problemi. Assicurati che il frammento di esperienza sia un piccolo pezzo di HTML e non una pagina HTML completa con HTML, HEAD, BODY e così via.

Per ulteriori informazioni, consultare il seguente post di blog: [AEM 6.5: Rimozione delle librerie client dai frammenti esperienza esportati in Target](https://www.linkedin.com/pulse/aem-65-removing-clientlibs-from-experience-fragments-exported-haser){target=_blank}.

## Video di formazione: Utilizzo AEM frammenti di esperienza con [!DNL Adobe Target]

Il video seguente illustra come impostare e utilizzare i frammenti di esperienza:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>La funzione di deeplink [!DNL AEM] discussa in 4:54 è stata rimossa.

Per informazioni più dettagliate, consulta [Utilizzo di frammenti esperienza con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html?lang=it) sulla *Video e Tutorials di AEM Sites* pagina.
