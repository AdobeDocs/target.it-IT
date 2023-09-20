---
keywords: Creare test A/B;attività A/B;nuova attività A/B;creare test A/B
description: Scopri come utilizzare il Compositore esperienza visivo in Adobe [!DNL Target] per creare l’attività Test A/B direttamente su un [!DNL Target]pagina abilitata.
title: Come si crea un test A/B?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: ec1041fd1823d1ab7f1af147af5825c3ae8662b5
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 45%

---

# Creare un test A/B

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare [!UICONTROL Test A/B] attività direttamente su un [!DNL Target]e per modificare parti della pagina in [!DNL Target].

>[!NOTE]
>
>Oltre al manuale (impostazione predefinita) [!UICONTROL Test A/B] attività (discussa in questo articolo), [!DNL Target] fornisce due tipi aggiuntivi di [!UICONTROL Test A/B] attività: [!UICONTROL Allocazione automatica] e [!UICONTROL Targeting automatico].
>
>Consulta [Tipi di attività di test A/B](/help/main/c-activities/t-test-ab/test-ab.md#types) in *Panoramica sui test A/B*.

Per creare un manuale [!UICONTROL Test A/B] attività:

1. Nell&#39;elenco **[!UICONTROL Attività]** fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Consigli] è una [funzione disponibile in Target Premium](/help/main/c-intro/intro.md#premium).
   >
   >Per informazioni sui vari tipi di attività, consulta [Attività](/help/main/c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) e la [guida alle attività di Target](/help/main/c-activities/target-activities-guide.md).

1. Dalla finestra di dialogo Crea attività di test A/B, seleziona **[!UICONTROL Visivo (predefinito)]**, se necessario.

   Se preferisce utilizzare il [!UICONTROL Compositore esperienza basato su moduli], seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e [!UICONTROL Compositore esperienza basato su moduli], [!DNL Target] offre il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un [Cliente Target Premium](/help/main/c-intro/intro.md#premium), dalla **[!UICONTROL Scegli area di lavoro]** , scegli un [workspace](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   Il [[!UICONTROL Scegli area di lavoro]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) nell&#39;illustrazione precedente è un&#39;opzione [Target Premium](/help/main/c-intro/intro.md) e potrebbero non essere visualizzati se l’organizzazione dispone di un [!UICONTROL Target Standard] licenza.

1. In **[!UICONTROL Inserisci l’URL dell’attività]** , specificare [URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Crea]**.

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

1. Clic **[!UICONTROL Attività senza titolo]** nella parte superiore del Compositore esperienza visivo, specifica un nome per l’attività nello spazio fornito.

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

   Sopo aver creato una nuova attività, il [!UICONTROL Compositore esperienza visivo] presenta due schede a sinistra: Esperienza A ed Esperienza B. L&#39;Esperienza A è l&#39;esperienza di controllo. L&#39;attenzione è rivolta alla scheda Esperienza B, che puoi modificare in base alle tue esigenze. L’esperienza B è un’esperienza alternativa che puoi aggiungere al test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni su come aggiungere e modificare le esperienze nel [!UICONTROL Compositore esperienza visivo], vedi [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Per modificare l&#39;Esperienza B, inizia con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del [!UICONTROL Compositore esperienza visivo] per andare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. In **[!UICONTROL Pubblico]** fare clic sull&#39;icona di modifica (puntini di sospensione verticali), quindi fare clic su **[!UICONTROL Sostituisci pubblico]**, quindi [selezionare il pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per la tua attività.

   Per impostazione predefinita, il pubblico è impostato su [!UICONTROL Tutti i visitatori].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Allocazione automatica all’esperienza migliore]**: la maggior parte dei partecipanti all’attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, consulta [[!UICONTROL Allocazione automatica] panoramica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Targeting automatico per esperienze personalizzate]**: [!DNL Target] utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e ai comportamenti precedenti di visitatori simili. Per ulteriori informazioni, consulta [Panoramica del Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

   Potete inoltre fate clic su **[!UICONTROL Add  (Aggiungi esperienza)]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Quando sei soddisfatto delle scelte di pubblico, esperienza e allocazione del traffico, fai clic su **[!UICONTROL Successivo]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

1. Clic **[!UICONTROL Salva e chiudi]** o **[!UICONTROL Salva]**.

Dopo aver creato l’attività, il [!UICONTROL Panoramica] Questa scheda mostra informazioni sull’attività, incluso un diagramma dell’attività.

## Video di formazione: Creazione di test A/B (08:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Creare un [!UICONTROL Test A/B] attività in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
