---
keywords: Creare targeting automatico;test A/B;attività di targeting automatico;nuova attività A/B;targeting automatico;targeting automatico per esperienze personalizzate;personalizzato;ottimizzazione
description: Scopri come utilizzare il Compositore esperienza visivo in Adobe Target per creare l’attività di test A/B di targeting automatico direttamente su una pagina abilitata per Target.
title: Come si crea un'attività di Targeting automatico?
feature: Targeting automatico
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
translation-type: tm+mt
source-git-commit: 73053526e68e08136ab66b9d4c1aa17958cfc76e
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 51%

---

# ![](/help/assets/premium.png) PREMIUMC: creare un’attività di Targeting automatico

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL Targeting automatico] [!UICONTROL Test A/B] direttamente su una pagina abilitata [!DNL Target] e per modificare parti della pagina all&#39;interno di [!DNL Target].

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/c-intro/intro.md).
>
>Oltre all&#39;attività [!UICONTROL Targeting automatico] [!UICONTROL Test A/B] (discussa in questo articolo), [!DNL Target] fornisce altri due tipi di attività [!UICONTROL Test A/B]: [!UICONTROL Manuale (predefinito)] e [!UICONTROL Allocazione automatica].
>
>Consulta [Tipi di attività di test A/B](/help/c-activities/t-test-ab/test-ab.md#types) in *Panoramica sul test A/B*.

Per creare un&#39;attività [!UICONTROL Targeting automatico]:

1. Nell&#39;elenco **[!UICONTROL Attività]** fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Targeting automatico] e [!UICONTROL Recommendations] sono [Funzioni di Target Premium](/help/c-intro/intro.md#premium).
   >
   >Per informazioni sui vari tipi di attività, consulta [Attività](/help/c-activities/activities.md) e la [guida alle attività di Target](/help/c-activities/target-activities-guide.md).

1. Se necessario, seleziona **[!UICONTROL Visivo (impostazione predefinita)]**.

   ![Creare un’attività Test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

   Se preferisci utilizzare il [!UICONTROL Compositore esperienza basato su moduli], seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e al [!UICONTROL Compositore esperienza basato su moduli], [!DNL Target] offre anche il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >L’opzione [[!UICONTROL Choose Workplace]](/help/administrating-target/c-user-management/property-channel/property-channel.md) (Scegli luogo di lavoro) nell’illustrazione precedente è una funzione di [Target Premium](/help/c-intro/intro.md). Se non trovi questa opzione, la tua organizzazione dispone di una licenza [!UICONTROL Target Standard] .

1. Scegli un [workspace](/help/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l’[URL di attività](/help/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Successivo]**.

   Se l’account è configurato con un URL predefinito, questo verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

   ![Compositore esperienza visivo](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

1. Crea esperienze modificando gli elementi nella pagina.

   Dopo la creazione di un&#39;attività, nel [!UICONTROL Compositore esperienza visivo] vengono visualizzate due schede a sinistra: Esperienza A ed Esperienza B. L’esperienza A è l’esperienza di controllo. La tua attenzione è rivolta alla scheda Esperienza B, che puoi modificare come desiderato. Esperienza B è l&#39;esperienza alternativa che puoi aggiungere al tuo test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni su come aggiungere e modificare le esperienze nel [!UICONTROL Compositore esperienza visivo], vedi [Aggiungi esperienza](/help/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Per modificare l&#39;Esperienza B, inizia con il passaggio 3.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del [!UICONTROL Compositore esperienza visivo] per andare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. Nella casella [!UICONTROL Pubblico], fai clic sull&#39;icona di modifica (tre puntini di sospensione verticali), fai clic su **[!UICONTROL Sostituisci pubblico]**, quindi [seleziona il pubblico](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività.

   Per impostazione predefinita, il pubblico è impostato su [!UICONTROL Tutti i visitatori].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico. Per creare un&#39;attività [!UICONTROL Targeting automatico], seleziona **[!UICONTROL Targeting automatico per esperienze personalizzate]**.

   I tre tipi di ripartizione del traffico sono descritti di seguito:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%. Per ulteriori informazioni, consulta [Creare un test A/B](/help/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Allocazione automatica all’esperienza]** migliore: La maggior parte dei partecipanti all’attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, consulta [Panoramica dell’allocazione automatica](/help/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Targeting automatico per esperienze]** personalizzate:  [!DNL Target] utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. In seguito, indica l’esperienza più adatta per i visitatori in base ai loro profili cliente individuali e comportamenti passati di visitatori simili.
   Potete inoltre fate clic su **[!UICONTROL Add  (Aggiungi esperienza)]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Quando sei soddisfatto del pubblico, delle scelte di esperienza e delle scelte di allocazione del traffico, fai clic su **[!UICONTROL Avanti]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   ![Impostazioni per attività A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

   >[!NOTE]
   >
   >Se desideri utilizzare [Analytics for Target](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T) con questa attività, consulta informazioni importanti nel supporto [A4T per le attività di allocazione automatica e targeting automatico](/help/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Fai clic su **[!UICONTROL Salva e chiudi]** o **[!UICONTROL Salva]**.

Dopo aver creato l&#39;attività, la scheda [!UICONTROL Panoramica] mostra informazioni sull&#39;attività, incluso un diagramma.

## Video di formazione: Creazione di test A/B (8:36) ![Badge tutorial](/help/assets/tutorial.png)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Crea un&#39;attività [!UICONTROL Test A/B] in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
