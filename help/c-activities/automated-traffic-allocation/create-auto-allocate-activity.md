---
keywords: creare l'allocazione automatica;test A/B;allocare automaticamente l'attività;nuova attività a/b;allocare automaticamente;allocare automaticamente per la migliore esperienza;allocare;allocare automaticamente
description: Scoprite come utilizzare Visual Experience Composer (VEC) in  Adobe Target per creare un'attività di test A/B allocata automaticamente direttamente su una pagina abilitata per Target.
title: Come si crea un'attività di allocazione automatica?
feature: Allocazione automatica
translation-type: tm+mt
source-git-commit: e87786f2df104d66d97cacd83921875dacd78afe
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 58%

---


# Creazione di un&#39;attività di allocazione automatica

Utilizzate [!UICONTROL Visual Experience Composer] (VEC) in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test] direttamente su una pagina [!DNL Target] abilitata e per modificare parti della pagina all&#39;interno di [!DNL Target].

>[!NOTE]
>
>Oltre all&#39;attività [!UICONTROL Auto-Allocate] [!UICONTROL A/B Test] (discussa in questo articolo), [!DNL Target] fornisce due tipi aggiuntivi di attività [!UICONTROL A/B Test]: [!UICONTROL Manuale (predefinito)] e [!UICONTROL Auto-Target].
>
>Vedere [Tipi di attività di test A/B](/help/c-activities/t-test-ab/test-ab.md#types) in *Panoramica test A/B*.

Per creare un&#39;attività [!UICONTROL Allocazione automatica]:

1. Nell&#39;elenco **[!UICONTROL Attività]** fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Consigli] è una [funzione disponibile in Target Premium](/help/c-intro/intro.md#premium).
   >
   >Per informazioni sui vari tipi di attività, consulta [Attività](/help/c-activities/activities.md) e la [guida alle attività di Target](/help/c-activities/target-activities-guide.md).

1. Se necessario, seleziona **[!UICONTROL Visivo (impostazione predefinita)]**.

   ![Crea attività test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   Se preferite utilizzare [!UICONTROL Form-Based Experience Composer], selezionate [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre a VEC e [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre VEC per l&#39;applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L’opzione [[!UICONTROL Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) (Scegli luogo di lavoro) nell’illustrazione precedente è una funzione di [Target Premium](/help/c-intro/intro.md). Se questa opzione non è disponibile, l&#39;organizzazione dispone di una licenza [!UICONTROL Target Standard].

1. (Condizionale) Se sei un cliente [Target Premium](/help/c-intro/intro.md#premium), scegli un’[area di lavoro](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l’[URL di attività](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Successivo]**.

   Se l’account è configurato con un URL predefinito, questo verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

   ![Compositore esperienza visivo](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Il nome dell&#39;attività non può iniziare con i seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
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

1. Nella casella [!UICONTROL Audience] fare clic sull&#39;icona di modifica (tre ellissi verticali), fare clic su **[!UICONTROL Replace Audience]**, quindi [selezionare l&#39;audience](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività.

   Per impostazione predefinita, l&#39;audience è impostata su [!UICONTROL Tutti i visitatori].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico. Per creare un&#39;attività [!UICONTROL Allocazione automatica], selezionare **[!UICONTROL Allocazione automatica per migliorare l&#39;esperienza]**.

   I tre tipi di assegnazione del traffico sono descritti di seguito:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%. Per ulteriori informazioni, vedere [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Allocazione automatica all’esperienza migliore]**: la maggior parte dei partecipanti all’attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali.

   * **[!UICONTROL Targeting automatico per esperienze]** personalizzate:  [!DNL Target] utilizza l&#39;machine learning avanzato per personalizzare i contenuti e stimolare le conversioni identificando più esperienze definite dall&#39;esperto di marketing ad alte prestazioni, e quindi fornendo ai visitatori l&#39;esperienza più personalizzata in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili. Per ulteriori informazioni, vedere [Auto-Target](/help/c-activities/auto-target/auto-target-to-optimize.md).
   Potete inoltre fate clic su **[!UICONTROL Add  (Aggiungi esperienza)]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Una volta soddisfatti il pubblico, le scelte relative all&#39;esperienza e le scelte relative all&#39;allocazione del traffico, fate clic su **[!UICONTROL Next]** per passare al terzo passaggio del flusso di lavoro guidato in tre fasi.

1. Specifica [obiettivi e impostazioni](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   ![Impostazioni per attività A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

   >[!NOTE]
   >
   >Se desiderate utilizzare [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) con questa attività, consultate informazioni importanti nel supporto [A4T per le attività di allocazione automatica e di destinazione automatica](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Fare clic su **[!UICONTROL Salva e chiudi]** o su **[!UICONTROL Salva]**.

Dopo aver creato l&#39;attività, la scheda [!UICONTROL Panoramica] mostra informazioni sull&#39;attività, incluso un diagramma dell&#39;attività.

## Video di formazione: Creazione di test A/B (8:36) ![Logo esercitazione](/help/assets/tutorial.png)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Creare un&#39;attività [!UICONTROL A/B Test] in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)