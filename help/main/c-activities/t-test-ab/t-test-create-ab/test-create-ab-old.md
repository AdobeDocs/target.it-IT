---
keywords: Creare test A/B;attività A/B;nuova attività A/B;creare test A/B
description: Scopri come utilizzare il Compositore esperienza visivo in Adobe [!DNL Target] per creare l'attività Test A/B direttamente su una pagina abilitata per  [!DNL Target].
title: Come si crea un test A/B?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: eb7e892a85fa3952ffc22172085d421756d0dfb5
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 35%

---

# Creare un test A/B

Utilizzare il Compositore esperienza visivo [!UICONTROL Visual Experience Composer] in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL A/B Test] direttamente in una pagina abilitata per [!DNL Target] e modificare parti della pagina in [!DNL Target].

>[!NOTE]
>
>Oltre all&#39;attività Manuale (predefinita) [!UICONTROL A/B Test] (descritta in questo articolo), [!DNL Target] fornisce due tipi aggiuntivi di attività [!UICONTROL A/B Test]: [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].
>
>Consulta [Tipi di attività test A/B](/help/main/c-activities/t-test-ab/test-ab.md#types) in *Panoramica test A/B*.

Per creare un&#39;attività [!UICONTROL A/B Test] manuale:

1. Dall&#39;elenco **[!UICONTROL Activities]**, fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Elenco a discesa Crea attività](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. [!UICONTROL Recommendations] è una [funzionalità di Target Premium](/help/main/c-intro/intro.md#premium).
   >
   >Per informazioni sui vari tipi di attività, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) e la [guida alle attività di Target](/help/main/c-activities/target-activities-guide.md).

1. Dalla finestra di dialogo Crea attività test A/B, seleziona **[!UICONTROL Visual (Default)]**, se necessario.

   Se preferisci utilizzare [!UICONTROL Form-Based Experience Composer], seleziona [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e a [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre anche il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un cliente di [Target Premium](/help/main/c-intro/intro.md#premium), scegli un **[!UICONTROL Choose Workspace]** area di lavoro[ dall&#39;elenco a discesa ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   L&#39;opzione [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) nell&#39;illustrazione precedente è una funzionalità di [Target Premium](/help/main/c-intro/intro.md) e potrebbe non essere visualizzata se la tua organizzazione dispone di una licenza di [!UICONTROL Target Standard].

1. Nella casella **[!UICONTROL Enter Activity URL]**, specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Create]**.

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

   Verrà aperto [!UICONTROL Visual Experience Composer], con la pagina specificata nell&#39;URL.

1. Fai clic su **[!UICONTROL Untitled Activity]** nella parte superiore del Compositore esperienza visivo, quindi specifica un nome per l&#39;attività nello spazio fornito.

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

   Il nome dell’attività non può contenere nessuna delle seguenti sequenze di caratteri:

   | Sequenza di caratteri | Descrizione |
   |--- |--- |
   | ;= | Punto e virgola, uguale a |
   | ;+ | Punto e virgola, segno più |
   | ;- | Punto e virgola, meno |
   | ;@ | Punto e virgola, segno A |
   | ,= | Virgola, uguale a |
   | ,+ | Virgola più |
   | ,- | Virgola meno |
   | ,@ | Virgola, segno A |
   | `[`&quot; | Parentesi quadra aperta, virgolette doppie |
   | &quot;`]` | Virgolette doppie, parentesi quadra chiusa |

1. Crea nuove esperienze modificando gli elementi nella pagina.

   [!UICONTROL Visual Experience Composer] visualizza due schede a sinistra dopo aver creato una nuova attività: Esperienza A ed Esperienza B. L&#39;Esperienza A è l&#39;esperienza di controllo. L&#39;attenzione è rivolta alla scheda Esperienza B, che puoi modificare in base alle tue esigenze. L’esperienza B è un’esperienza alternativa che puoi aggiungere al test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni sull&#39;aggiunta e la modifica delle esperienze in [!UICONTROL Visual Experience Composer], vedere [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Per modificare l&#39;Esperienza B, inizia con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore di [!UICONTROL Visual Experience Composer] per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. Nella casella **[!UICONTROL Audience]**, fai clic sull&#39;icona di modifica (puntini di sospensione verticali), fai clic su **[!UICONTROL Replace Audience]**, quindi [seleziona il pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività.

   Per impostazione predefinita, il pubblico è impostato su [!UICONTROL All Visitors].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico:

   * **[!UICONTROL Manual (Default)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Auto-allocate to best experience]**: la maggior parte dei partecipanti all&#39;attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, vedere [[!UICONTROL Auto-Allocate] panoramica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-target for personalized experiences]**: [!DNL Target] utilizza l&#39;apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall&#39;addetto al marketing. Inoltre, indica l&#39;esperienza più adatta per i visitatori in base al loro profilo cliente individuale e ai comportamenti precedenti di visitatori simili. Per ulteriori informazioni, consulta [Panoramica sul Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Puoi anche fare clic su **[!UICONTROL Add]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Quando si è soddisfatti del pubblico, delle scelte di esperienza e delle scelte di allocazione del traffico, fare clic su **[!UICONTROL Next]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

1. Fare clic su **[!UICONTROL Save & Close]** o **[!UICONTROL Save]**.

Dopo aver creato l&#39;attività, nella scheda [!UICONTROL Overview] vengono visualizzate informazioni sull&#39;attività, incluso un diagramma dell&#39;attività.

## Video di formazione: Creazione di test A/B (8:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Crea un&#39;attività [!UICONTROL A/B Test] in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
