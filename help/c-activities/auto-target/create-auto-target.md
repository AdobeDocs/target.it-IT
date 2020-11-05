---
keywords: Create auto-target;A/B test;auto-target activity;new a/b activity;auto target;auto-target for personalized experiences;personalized
description: Utilizzate Visual Experience Composer (Compositore esperienza visivo) in  Adobe Target per creare l'attività di allocazione automatica del test A/B direttamente su una pagina compatibile con Target e per modificare parti della pagina all'interno di Target.
title: Creazione di un'attività di targeting automatico
feature: ab
topic: Advanced,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: fb4f43eef067a24f58ab8b53a7c8aa9c09392c9e
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 61%

---


# ![PREMIUM](/help/assets/premium.png) Creazione di un&#39;attività di targeting automatico

Utilizzate [!UICONTROL Visual Experience Composer (VEC, Compositore] esperienza visivo) in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL Auto-Target] Test [!UICONTROL A/B direttamente su una pagina] abilitata e per modificare parti della pagina all&#39;interno [!DNL Target][!DNL Target].

>[!NOTE]
>
>Oltre all&#39;attività [!UICONTROL Auto-Target] Test [!UICONTROL A/B (descritta in questo articolo),] fornisce due tipi aggiuntivi di attività Test [!DNL Target]  A/B: [!UICONTROL Manuale (predefinito)] e [!UICONTROL Allocazione]automatica.
>
>Consultate [Tipi di attività](/help/c-activities/t-test-ab/test-ab.md#types) di test A/B nella panoramica ** dei test A/B.

Per creare un&#39;attività [!UICONTROL di targeting] automatico:

1. Nell&#39;elenco **[!UICONTROL Attività]** fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Auto-Target] e [!UICONTROL Recommendations] sono funzioni [](/help/c-intro/intro.md#premium)Target Premium.
   >
   >Per informazioni sui vari tipi di attività, consulta [Attività](/help/c-activities/activities.md) e la [guida alle attività di Target](/help/c-activities/target-activities-guide.md).

1. Se necessario, seleziona **[!UICONTROL Visivo (impostazione predefinita)]**.

   ![Crea attività test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   If you prefer to use the [!UICONTROL Form-Based Experience Composer], select [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre a VEC e [!UICONTROL Form-Based Experience Composer (Compositore esperienza basato su moduli)], [!DNL Target] offre il VEC per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L’opzione [[!UICONTROL Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) (Scegli luogo di lavoro) nell’illustrazione precedente è una funzione di [Target Premium](/help/c-intro/intro.md). Your organization has a [!UICONTROL Target Standard] license if you do not see this option.

1. Scegliete un’ [area di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l’[URL di attività](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Successivo]**.

   Se l’account è configurato con un URL predefinito, questo verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

   ![Compositore esperienza visivo](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   I seguenti caratteri non sono consentiti nel nome di un’attività:

   | Carattere | Descrizione |
   |--- |--- |
   | `/` | Barra |
   | `?` | Punto interrogativo |
   | `#` | Cancelletto |
   | `:` | Due punti |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

1. Crea nuove esperienze modificando gli elementi nella pagina.

   Sopo aver creato una nuova attività, il [!UICONTROL Compositore esperienza visivo] presenta due schede a sinistra: Esperienza A ed Esperienza B. L&#39;Esperienza A è l&#39;esperienza di controllo. La tua attenzione sarà rivolta alla scheda Esperienza B, che è possibile modificare a piacimento. Esperienza B è l&#39;esperienza alternativa che puoi aggiungere al tuo test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni su come aggiungere e modificare le esperienze nel [!UICONTROL Compositore esperienza visivo], vedi [Aggiungi esperienza](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Per modificare l&#39;Esperienza B, inizia con il passaggio 3.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del [!UICONTROL Compositore esperienza visivo] per andare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. Nella casella [!UICONTROL Pubblico] , fate clic sull&#39;icona di modifica (tre ellissi verticali), fate clic su **[!UICONTROL Sostituisci pubblico]**, quindi [selezionate l&#39;audience](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività.

   By default, the audience is set to [!UICONTROL All Visitors].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico. Per creare un&#39;attività [!UICONTROL Auto-Target] , selezionate **[!UICONTROL Auto-Target per esperienze]** personalizzate.

   I tre tipi di assegnazione del traffico sono descritti di seguito:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%. For more information, see [Create an A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Allocazione automatica all’esperienza migliore]**: la maggior parte dei partecipanti all’attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. For more information, see [Auto-Allocate overview](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Targeting automatico per esperienze]** personalizzate: [!DNL Target] utilizza l&#39;machine learning avanzato per personalizzare i contenuti e stimolare le conversioni identificando più esperienze definite dall&#39;esperto di marketing ad alte prestazioni, e quindi fornendo ai visitatori l&#39;esperienza più personalizzata in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili.
   Potete inoltre fate clic su **[!UICONTROL Add  (Aggiungi esperienza)]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. When you are satisfied with your audience, experience choices, and traffic allocation choices, click **[!UICONTROL Next]** to move to the third step of the three-step guided workflow.

1. Specifica [obiettivi e impostazioni](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   ![Impostazioni per attività A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. Fate clic su **[!UICONTROL Salva e chiudi]** o **[!UICONTROL Salva]**.

After you create the activity, the [!UICONTROL Overview] tab shows information about the activity, including a diagram of your activity.

## Training video: Creating A/B Tests (8:36) ![Tutorial badge](/help/assets/tutorial.png)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Crea un&#39;attività di test  A/B in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)