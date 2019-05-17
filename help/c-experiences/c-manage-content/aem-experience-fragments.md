---
description: Informazioni sull’utilizzo dei frammenti di esperienza creati in Adobe Experience Manager (AEM) nelle attività di Target per aiutare l’ottimizzazione o la personalizzazione.
keywords: esperienza;aem;adobe experience manager;esportare in adobe target;frammenti di esperienza;frammenti;XF
seo-description: Informazioni sull’utilizzo dei frammenti di esperienza creati in Adobe Experience Manager (AEM) nelle attività di Target per aiutare l’ottimizzazione o la personalizzazione.
seo-title: Frammenti esperienza AEM
solution: Target
title: Frammenti esperienza AEM
topic: Standard
uuid: 4dc2b5da-524f-4d6a-8ffc-8c3ac78cb39e
translation-type: tm+mt
source-git-commit: 9b8f39240cbbd7a494d74dc0016ed666a58fd870

---


# Frammenti di esperienza AEM{#aem-experience-fragments}

Informazioni sull’utilizzo dei frammenti di esperienza creati in Adobe Experience Manager (AEM) nelle attività di Target per aiutare l’ottimizzazione o la personalizzazione.

## Frammenti di esperienza AEM {#topic_1E1E4EA01F074349B2CF8785387B5FE8}

Informazioni sull’utilizzo dei frammenti di esperienza creati in Adobe Experience Manager (AEM) nelle attività di Target per aiutare l’ottimizzazione o la personalizzazione.

>[!NOTE]
>
>Questa funzione richiede di essere cliente di Adobe Experience Manager (AEM). Per ulteriori informazioni, consulta [“Risoluzione dei problemi”](../../c-experiences/c-manage-content/aem-experience-fragments.md#section_AE6F0971E1574B3AA324003599B96E5A).

## Panoramica {#section_95A91830530F493B81C5C9CDB9B783EA}

I frammenti di esperienza creati in AEM possono essere utilizzati nelle attività di Target per combinare la facilità d&#39;uso e la potenza di AEM con le potenti capacità di intelligenza automatizzata (AI) ed apprendimento automatico (ML) di Target per testare e personalizzare le esperienze su grande scala.

AEM riunisce tutti i contenuti e le risorse in una posizione centrale per alimentare la tua strategia di personalizzazione. AEM consente di creare facilmente contenuti per desktop, tablet e dispositivi mobili in un&#39;unica posizione senza scrivere codice. Non è necessario creare pagine per ogni dispositivo: AEM regola automaticamente ogni esperienza utilizzando il contenuto.

Target consente di fornire esperienze personalizzate in scala su una combinazione di approcci di apprendimento automatico basati sulle regole e guidati da intelligenze automatizzate che incorporano variabili comportamentali, contestuali e offline.  Con Target puoi facilmente impostare ed eseguire attività di test A/B e multivariati (MVT) per determinare le offerte, i contenuti e le esperienze migliori.

La funzione Frammenti esperienza rappresenta un enorme passo avanti per la collaborazione tra i creatori e i manager di contenuti ed esperienze, e i professionisti di personalizzazione e ottimizzazione che usano Target per conseguire risultati di business.

## Requisiti {#section_AE6F0971E1574B3AA324003599B96E5A}

Devi essere provvisto della funzionalità frammenti di esperienza all&#39;interno di Target. Inoltre, devi utilizzare AEM 6.3 con il service pack appropriato o AEM 6.4 (o versione successiva). Il rappresentante del tuo account può aiutarti a rispettare i requisiti per utilizzare questa funzione:

* Adobe Experience Manager 6.4 (o successive).
* Adobe Experience Manager 6.3 SP2 (o successive).
* Account Adobe Target Standard o Premium.
* Contatta il Servizio clienti Adobe Target per abilitare l&#39;integrazione e per ottenere i dettagli di autenticazione.

## Creazione e configurazione di frammenti di esperienza in AEM {#section_745C8EFE29F547A2958FDBF61A5ADF7B}

Per utilizzare i frammenti di esperienza AEM in Target, è necessario attenersi ai seguenti passaggi:

### Passaggio 1: integrare AEM con Target

Per ulteriori informazioni, consulta:

* **AEM 6.3:**[scelta di Adobe Analytics e Adobe Target](https://docs.adobe.com/docs/en/aem/6-3/administer/integration/marketing-cloud/opt-in.html) nella documentazione di _Adobe Experience Manager 6.3_.
* **AEM 6.4:**[scelta di Adobe Analytics e Adobe Target](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/opt-in.html) nella documentazione di _Adobe Experience Manager 6.4_.

### Passaggio 2: creare il frammento di esperienza

I frammenti di esperienza sono creati in AEM. Per ulteriori informazioni, consulta:

* **AEM 6.3:**[Frammenti di esperienza](https://docs.adobe.com/docs/en/aem/6-3/author/experience-fragments.html) nella documentazione di *Adobe Experience Manager 6.3*.
* **** AEM 6.4: [Frammenti di esperienza](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/experience-fragments.html) nella documentazione di *Adobe Experience Manager 6.4*.

### Passaggio 3: configurare AEM per condividere il frammento di esperienza con Target

1. Dall’interno di AEM, seleziona il frammento di esperienza desiderato o la cartella che lo contiene, quindi fai clic su [!UICONTROL Proprietà].
2. Fa clic sulla scheda [!UICONTROL Servizi cloud], poi, dall&#39;elenco a discesa [!UICONTROL Configurazione del servizio cloud], seleziona [!UICONTROL Adobe Target].

   >[!NOTE]
   >
   >Il passaggio precedente presuppone che un utente dell’azienda abbia creato la configurazione di Adobe Target.

3. Fai clic su [!UICONTROL Salva e chiudi].

### Passaggio 4: pubblicare il frammento esperienza ed esportarlo in Target

**AEM 6.3:**

1. dall&#39;interno di AEM, seleziona il frammento di esperienza desiderato, fai clic sulla scheda [!UICONTROL Pubblica], quindi fai clic sul pulsante [!UICONTROL Pubblica].
2. Dall&#39;interno di AEM, seleziona il frammento di esperienza desiderato, fai clic su [!UICONTROL Esporta in Adobe Target], quindi fai clic su [!UICONTROL OK].

   ![](assets/experience_fragment_export_to_target.png)

**AEM 6.4:**

1. dall&#39;interno di AEM, seleziona il frammento di esperienza desiderato e fai clic su [!UICONTROL Esporta in Adobe Target].

   ![](assets/experience_fragment_export_to_target.png)

2. Nella finestra di dialogo che appare, seleziona [!UICONTROL Pubblica] per pubblicare su [!DNL Target] tutte le risorse all’interno del frammento di esperienza.

## Utilizzo di frammenti di esperienza nelle attività di Target {#section_17CE4BE6B2B74CCEBAE0C68DEB84ABB9}

Dopo aver eseguito le attività precedenti, il frammento di esperienza viene visualizzato nella pagina [!UICONTROL Offerte] di Target.

>[!NOTE]
>
>Target cerca attualmente frammenti di esperienza per importare ogni dieci minuti. Il frammento di esperienza importato dovrebbe diventare disponibile in Target entro dieci minuti; tuttavia, questo intervallo di tempo dovrebbe accorciarsi andando avanti.

>[!IMPORTANT]
>
>Il frammento esperienza è attualmente importato in Target come offerta HTML. Nota che il frammento di esperienza nella versione “master” rimane in AEM. Non è possibile modificare il frammento di esperienza in Target.

Passa il puntatore del mouse su un frammento esperienza nell’elenco, quindi fai clic sull’icona Visualizza ( ![](assets/icon_info.png)

) per visualizzare ulteriori informazioni sul frammento esperienza, tra cui l’URL pubblico di consegna dell’offerta, il percorso AEM e un collegamento diretto per aprire il frammento esperienza all’interno di AEM.

È possibile utilizzare frammenti di esperienza nelle attività di Target utilizzando il Compositore esperienza visivo il Compositore esperienza basato su moduli.

>[!NOTE]
>
>Per sfruttare appieno la funzionalità AI e ML di Target, seleziona [Allocazione automatica](../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4) o [Personalizzazione automatizzata](../../c-activities/t-automated-personalization/automated-personalization.md#task_8AAF837796D74CF893CA2F88BA1491C9) durante la creazione di un test A/B.

**Per utilizzare frammenti di esperienza utilizzando il Compositore esperienza visivo:**

1. In Target, durante la creazione o la modifica di un’esperienza nel  [Compositore esperienza visivo](../../c-experiences/experiences.md#concept_A2E10F6AFB3D4AEAB6951EE14688848D), fai clic sulla posizione nella pagina in cui vuoi inserire il contenuto AEM, poi seleziona **[!UICONTROL Scambia con frammento esperienza]** per visualizzare l’elenco [!UICONTROL Scegli un frammento esperienza].

   >[!NOTE]
   >
   >L’opzione [!UICONTROL Scambia con frammento esperienza] non è disponibile per le immagini. Se vuoi utilizzare questa opzione con un’immagine, fai clic sull’elemento che la contiene.

   L’elenco [!UICONTROL Frammenti esperienza] presenta tutti i contenuti creati in AEM che ora sono disponibili in modo nativo in Target.

   ![](assets/experience_fragment_list.png)

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Salva]**.
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

1. In Target, durante la creazione o la modifica di un’esperienza nel  [Compositore esperienza basato su moduli](../../c-experiences/form-experience-composer.md#task_FAC842A6535045B68B4C1AD3E657E56E), seleziona il percorso nella pagina in cui desideri inserire il contenuto AEM, quindi seleziona **[!UICONTROL Cambia frammento esperienza]** per visualizzare l’elenco [!UICONTROL Scegli un frammento esperienza].

   ![](assets/experience_fragment_list.png)

   L’elenco [!UICONTROL Frammenti esperienza] presenta tutti i contenuti creati in AEM che ora sono disponibili in modo nativo in Target.

1. Seleziona il frammento di esperienza desiderato, quindi fai clic su **[!UICONTROL Salva]**.
1. Termina la configurazione dell’attività.

## Video di formazione: Utilizzo dei frammenti esperienza AEM con Adobe Target {#section_C0EDC54063464F41A182492D2045BC64}

Il seguente video illustra come impostare e utilizzare i frammenti di esperienza: [Uso dei frammenti di esperienza AEM con Adobe Target](https://helpx.adobe.com/experience-manager/kt/sites/using/experience-fragment-target-feature-video-use.html).
