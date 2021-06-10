---
keywords: esperienza;json;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
description: Scopri come utilizzare AEM frammenti di esperienza nelle attività Adobe [!DNL Target] . Combina la facilità d'uso e la potenza di AEM con le potenti funzionalità AI e ML in [!DNL Target].
title: Come Si Utilizzano I Frammenti Esperienza Di Adobe Experience Manager (AEM)?
feature: Esperienze e offerte
exl-id: 3dd811a4-c7be-443d-a5ad-5b9adcaf1a2c
source-git-commit: 603d98a972d1b421dae2047b70d65d0037b7a068
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 30%

---

# Frammenti esperienza AEM

Informazioni sull’utilizzo dei frammenti di esperienza creati in [!DNL Adobe Experience Manager] (AEM) nelle attività [!DNL Target] per facilitare l’ottimizzazione o la personalizzazione.

>[!NOTE]
>
>Questa funzione richiede di essere un cliente [!DNL Adobe Experience Manager] ([!DNL AEM]). Per ulteriori informazioni, consulta [“Risoluzione dei problemi”](/help/c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A).

## Panoramica {#section_95A91830530F493B81C5C9CDB9B783EA}

L’utilizzo di frammenti di esperienza creati in [!DNL AEM] nelle attività [!DNL Target] consente di combinare la facilità d’uso e la potenza di [!DNL AEM] con le potenti funzionalità di intelligenza automatizzata (AI) e apprendimento automatico (ML) in [!DNL Target] per testare e personalizzare le esperienze su larga scala.

[!DNL AEM] riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. [!DNL AEM] consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un&#39;unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo. [!DNL AEM] regola automaticamente ogni esperienza utilizzando il contenuto.

[!DNL Target] consente di fornire esperienze personalizzate in scala su una combinazione di approcci di apprendimento automatico basati sulle regole e guidati da intelligenze automatizzate che incorporano variabili comportamentali, contestuali e offline. Con [!DNL Target] puoi facilmente impostare ed eseguire attività [Test A/B](/help/c-activities/t-test-ab/test-ab.md) e [Multivariate](/help/c-activities/c-multivariate-testing/multivariate-testing.md) (MVT) per determinare le offerte, i contenuti e le esperienze migliori.

Frammenti di esperienza rappresentano un enorme passo avanti per collegare i creatori e i manager di contenuto/esperienza e professionisti di personalizzazione e ottimizzazione che stanno guidando i risultati di business tramite [!DNL Target].

## Requisiti {#section_AE6F0971E1574B3AA324003599B96E5A}

Devi essere provvisto della funzionalità frammenti di esperienza all&#39;interno di [!DNL Target]. Inoltre, devi utilizzare [!DNL AEM] 6.3 con il service pack appropriato o [!DNL AEM] 6.4 (o successivo). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* [!DNL Adobe Experience Manager] 6.4 (o successiva).
* [!DNL Adobe Experience Manager] 6.3 SP2 (o successivo).
* [!DNL Adobe Target Standard] o  [!DNL Adobe Target Premium] account.
* Contatta l’ [Assistenza clienti Adobe Target](/help/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) per abilitare l’integrazione e per ottenere i dettagli di autenticazione.

## Creazione e configurazione di frammenti di esperienza in [!DNL AEM] {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare i frammenti di esperienza [!DNL AEM] in [!DNL Target], esegui le seguenti operazioni:

### Passaggio 1: Integrare [!DNL AEM] con [!DNL Target]

Per ulteriori informazioni, consulta:

* **Adobe I/O**:  [Integrazione con Adobe Target tramite Adobe I/0](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/integration-ims-adobe-io.html) nella documentazione  _sulla_ guida utente per l’amministrazione.
* **[!DNL AEM]6.3**:  [Scelta di Adobe Analytics e ](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) targeting di Adobe nella documentazione di  _Adobe Experience Manager 6.3_ .
* **[!DNL AEM]6.4**:  [Scelta di Adobe Analytics e ](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) targeting di Adobe nella documentazione di  _Adobe Experience Manager 6.4_ .
* **[!DNL AEM]6.5**:  [Scelta di Adobe Analytics e ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/opt-in.html) targeting di Adobe nella documentazione di  *Adobe Experience Manager 6.5* .

### Passaggio 2: creare il frammento di esperienza

I frammenti di esperienza sono creati in [!DNL AEM]. Per ulteriori informazioni, consulta:

* **[!DNL AEM]6.3**:  [Frammenti esperienza ](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) nella documentazione di  *Adobe Experience Manager 6.3* .
* **[!DNL AEM]6.4**:  [Frammenti esperienza ](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) nella documentazione di  *Adobe Experience Manager 6.4* .
* **[!DNL AEM]6.5**:  [Frammenti esperienza ](https://helpx.adobe.com/experience-manager/6-5/sites/authoring/using/experience-fragments.html) nella documentazione di  *Adobe Experience Manager 6.5* .

### Passaggio 3: Configura [!DNL AEM] per condividere il frammento di esperienza con [!DNL Target]

1. Dall&#39;interno di [!DNL AEM], seleziona il frammento di esperienza desiderato o la cartella che lo contiene, quindi fai clic su **[!UICONTROL Proprietà]**.
2. Fa clic sulla scheda **[!UICONTROL Servizi cloud]**, poi, dall&#39;elenco a discesa **[!UICONTROL Configurazione del servizio cloud]**, seleziona **[!UICONTROL Adobe Target]**.

   >[!NOTE]
   >
   >Il passaggio precedente presuppone che un utente dell&#39;organizzazione abbia creato la configurazione [!DNL Adobe Target].

3. Fai clic su **[!UICONTROL Salva e chiudi]**.

### Passaggio 4: pubblicare il frammento esperienza ed esportarlo in [!DNL Target]

A seconda della versione [!DNL AEM], consulta i seguenti collegamenti per istruzioni dettagliate:

* **[!DNL AEM]6.3**:  [Esportazione di un frammento esperienza in ](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/experience-fragments-target.html) Target nella documentazione di  *Adobe Experience Manager 6.3* .
* **[!DNL AEM]6.4**:  [Esportazione di un frammento esperienza in ](https://experienceleague.adobe.com/docs/experience-manager-64/administering/integration/experience-fragments-target.html) Target nella documentazione di  *Adobe Experience Manager 6.4* .
* **[!DNL AEM]6.5**:  [Esportazione di un frammento esperienza in ](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/experience-fragments-target.html) Target nella documentazione di  *Adobe Experience Manager 6.5* .

## Utilizzo di frammenti di esperienza nelle attività [!DNL Target] {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il frammento di esperienza viene visualizzato nella pagina [!UICONTROL Offerte] di [!DNL Target].

>[!NOTE]
>
>[!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. Il frammento di esperienza importato dovrebbe essere disponibile in [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi andando avanti.

>[!IMPORTANT]
>
>Il frammento di esperienza è attualmente importato in [!DNL Target] come offerta HTML. Il frammento di esperienza nella versione &quot;principale&quot; rimane in [!DNL AEM]. Non è possibile modificare il frammento di esperienza in [!DNL Target].

Passa il puntatore del mouse su un frammento di esperienza nell’elenco, quindi fai clic sull’icona [!UICONTROL Visualizza] ![Visualizza icona](assets/icon_info.png) per visualizzare ulteriori informazioni sul frammento di esperienza, compreso l’URL pubblico di consegna dell’offerta e il relativo percorso [!DNL AEM].

Puoi utilizzare frammenti di esperienza nelle attività [!DNL Target] utilizzando il [Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) o il [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

>[!NOTE]
>
>Per utilizzare appieno le funzionalità di AI e ML [!DNL Target], seleziona [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md) durante la creazione di un test A/B.

**Per utilizzare frammenti di esperienza utilizzando il Compositore esperienza visivo:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza visivo](/help/c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fai clic sul percorso nella pagina in cui desideri inserire il contenuto [!DNL AEM], quindi seleziona l&#39;opzione desiderata per visualizzare l&#39;elenco [!UICONTROL Scegli un frammento esperienza].

   * [!UICONTROL Inserisci prima]
   * [!UICONTROL Inserisci dopo]
   * [!UICONTROL Scambio con frammento esperienza]

   L’elenco [!UICONTROL Frammenti esperienza][!DNL AEM] presenta tutti i contenuti creati in che ora sono disponibili in modo nativo in [!DNL Target].

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Scambia con frammento esperienza] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   ![](assets/experience_fragment_list.png)

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Fine]**.
1. Termina la configurazione dell’attività.

   Per ulteriori informazioni sulla configurazione dei vari tipi di attività, consulta i seguenti argomenti:

   * **Test A/B:** [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md)
   * **Allocazione automatica:** [Allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4)
   * **Targeting automatico:** [Targeting automatico](/help/c-activities/auto-target/auto-target-to-optimize.md)
   * **Personalizzazione automatizzata (AP):** [Creazione di un’attività di personalizzazione automatica](/help/c-activities/t-automated-personalization/create-ap-activity.md#task_8AAF837796D74CF893CA2F88BA1491C9)
   * **Targeting delle esperienze (XT):** [Creare un’attività di targeting delle esperienze](/help/c-activities/t-experience-target/t-xt-create/xt-create.md#task_D6B3429AC31549E1A70EDF04B3DDC765)
   * **Test multivariato (MVT):** [Creare un test multivariato](/help/c-activities/c-multivariate-testing/t-create-multivariate-test/create-multivariate-test.md#task_BF870FA60A8245AB8F0B775BE32EA710)
   * **Recommendationfs:** [Creare un’attività di Recommendations](/help/c-recommendations/t-create-recs-activity/create-recs-activity.md#task_6874328773C64C44A73F0A130AD3F96F)

**Per utilizzare frammenti di esperienza utilizzando il Compositore esperienza basato su moduli:**

1. In [!DNL Target], durante la creazione o la modifica di un&#39;esperienza nel [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona il percorso nella pagina in cui desideri inserire il contenuto [!DNL AEM], quindi seleziona **[!UICONTROL Cambia frammento esperienza]** per visualizzare l&#39;elenco [!UICONTROL Scegli un frammento esperienza].

   ![](assets/experience_fragment_list.png)

   L’elenco [!UICONTROL Frammenti esperienza][!DNL AEM] presenta tutti i contenuti creati in che ora sono disponibili in modo nativo in [!DNL Target].

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Considerazioni {#considerations}

* [!DNL Target] cerca attualmente frammenti di esperienza per importare ogni dieci minuti. Il frammento di esperienza importato dovrebbe essere disponibile in [!DNL Target] entro dieci minuti, ma questo intervallo di tempo dovrebbe accorciarsi andando avanti.
* Il frammento di esperienza è attualmente importato in [!DNL Target] come offerta HTML. Il frammento di esperienza nella versione &quot;principale&quot; rimane in [!DNL AEM]. Non è possibile modificare il frammento di esperienza in [!DNL Target].
* Puoi importare le offerte JSON come frammenti di esperienza in [!DNL Target]. Tuttavia, queste offerte vengono importate come offerte HTML. Le offerte JSON (frammenti di esperienza) non sono attualmente completamente supportate nell’ interfaccia utente di [!DNL Target] .
* Non è possibile creare frammenti di esperienza utilizzando Adobe IO. È necessario creare frammenti di esperienza utilizzando AEM, come spiegato in precedenza.

## Video di formazione: Utilizzo di frammenti di esperienza AEM con Adobe Target ![Badge tutorial](/help/assets/overview.png) {#section_C0EDC54063464F41A182492D2045BC64}

Il video seguente illustra come impostare e utilizzare i frammenti di esperienza:

>[!VIDEO](https://video.tv.adobe.com/v/22383)

>[!NOTE]
>
>La funzione di collegamento profondo [!DNL AEM] discussa in 4:54 è stata rimossa.

Per ulteriori informazioni, consulta [Utilizzo di frammenti di esperienza con Adobe Target](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/personalization/experience-fragment-target-offer-feature-video-use.html) nella pagina *Video e Tutorials AEM Sites* .
