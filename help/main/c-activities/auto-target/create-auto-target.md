---
keywords: creare targeting automatico;test A/B;targeting automatico;nuova attività A/B;targeting automatico;targeting automatico per esperienze personalizzate;personalizzato;ottimizzazione
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare un [!UICONTROL Targeting automatico] Attività test A/B.
title: Come si crea un [!UICONTROL Targeting automatico] Attività?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Vedi cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 3e8c2d77f300bf0e2ca83a53d30e7b9eee48894e
workflow-type: tm+mt
source-wordcount: '874'
ht-degree: 50%

---

# Creare un [!UICONTROL Targeting automatico] attività

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare [!UICONTROL Targeting automatico] [!UICONTROL Test A/B] attività direttamente su un [!DNL Target]e per modificare parti della pagina in [!DNL Target].

>[!NOTE]
>
>La funzione di [!UICONTROL Targeting automatico] è disponibile come parte della soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md).

Per creare un [!UICONTROL Targeting automatico] attività:

1. Nell&#39;elenco **[!UICONTROL Attività]** fai clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. Ad esempio, [!UICONTROL Consigli] è una [funzione disponibile in Target Premium](/help/main/c-intro/intro.md#premium). Per informazioni sui vari tipi di attività, consulta [Attività](/help/main/c-activities/activities.md) e la [guida alle attività di Target](/help/main/c-activities/target-activities-guide.md).

1. Seleziona **[!UICONTROL Visivo]**, se necessario.

   Se preferisce utilizzare il [!UICONTROL Compositore esperienza basato su moduli], seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e [!UICONTROL Compositore esperienza basato su moduli], [!DNL Target] offre il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un cliente [Target Premium](/help/main/c-intro/intro.md#premium), scegli un’[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l’[URL di attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Successivo]**.

   Se l’account è configurato con un URL predefinito, questo verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

   ![Compositore esperienza visivo](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Digita un nome per l’attività nello spazio fornito.

   ![Campo Nome](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_newname-new.png)

   Il nome dell’attività non può iniziare con uno dei seguenti caratteri:

   | Carattere | Descrizione |
   |--- |--- |
   | `=` | Uguale |
   | `+` | Più |
   | `-` | Meno |
   | `@` | Chiocciola |

1. Crea le esperienze modificando gli elementi nella pagina.

   Il [!UICONTROL Compositore esperienza visivo] dopo aver creato un’attività di, visualizza due schede a sinistra: Esperienza A e Esperienza B. L’Esperienza A è l’esperienza di controllo. L&#39;attenzione è rivolta alla scheda Esperienza B, che puoi modificare in base alle tue esigenze. L’esperienza B è un’esperienza alternativa che puoi aggiungere al test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni su come aggiungere e modificare le esperienze nel [!UICONTROL Compositore esperienza visivo], vedi [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Per modificare l&#39;Esperienza B, inizia con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del [!UICONTROL Compositore esperienza visivo] per andare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. In [!UICONTROL Pubblico] fare clic sull&#39;icona di modifica (puntini di sospensione verticali), quindi fare clic su **[!UICONTROL Sostituisci pubblico]**, quindi [selezionare il pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per la tua attività.

   Per impostazione predefinita, il pubblico è impostato su [!UICONTROL Tutti i visitatori].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo desiderato per l’allocazione del traffico. Per creare un [!UICONTROL Targeting automatico] attività, seleziona **[!UICONTROL Targeting automatico per esperienze personalizzate]**.

   Di seguito sono descritti i tre tipi di allocazione del traffico:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%. Per ulteriori informazioni, consulta [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Allocazione automatica all’esperienza migliore]**: la maggior parte dei partecipanti all’attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, consulta [Panoramica dell’allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Targeting automatico per esperienze personalizzate]**: [!DNL Target] utilizza l’apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall’addetto al marketing. Inoltre, indica l’esperienza più adatta per ogni visitatore in base al suo profilo cliente individuale e ai comportamenti precedenti di visitatori simili.

   Potete inoltre fate clic su **[!UICONTROL Add  (Aggiungi esperienza)]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Quando sei soddisfatto delle scelte di pubblico, esperienza e allocazione del traffico, fai clic su **[!UICONTROL Successivo]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   >[!NOTE]
   >
   >Se si desidera utilizzare [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) con questa attività, consulta informazioni importanti in [Supporto A4T per attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Clic **[!UICONTROL Salva e chiudi]** o **[!UICONTROL Salva]**.

Dopo aver creato l’attività, il [!UICONTROL Panoramica] Questa scheda mostra informazioni sull’attività, incluso un diagramma dell’attività.

## Video di formazione: Creazione di test A/B (08:36)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Creare un [!UICONTROL Test A/B] attività in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
