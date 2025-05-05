---
keywords: creare targeting automatico;test A/B;targeting automatico;nuova attività A/B;targeting automatico;targeting automatico per esperienze personalizzate;personalizzato;ottimizzazione
description: Scopri come utilizzare il Compositore esperienza visivo di [!UICONTROL Visual Experience Composer] in  [!DNL Adobe Target]  per creare un'attività Test A/B di [!UICONTROL Auto-Target].
title: Come si crea un'attività [!UICONTROL Auto-Target]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=it#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Auto-Target
exl-id: 5521740c-eee2-4ba2-8931-cf56d56a4561
source-git-commit: 32a91a41cd182d3a55ded7dea8c1c6ea6f46aa71
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 43%

---

# Crea un&#39;attività [!UICONTROL Auto-Target]

Utilizzare il Compositore esperienza visivo [!UICONTROL Visual Experience Composer] in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL Auto-Target] [!UICONTROL A/B Test] direttamente in una pagina abilitata per [!DNL Target] e modificare parti della pagina in [!DNL Target].

>[!NOTE]
>
>[!UICONTROL Auto-Target] è disponibile nella soluzione [!DNL Target Premium]. Questa funzione non è disponibile in [!DNL Target Standard] senza una licenza [!DNL Target Premium]. Per ulteriori informazioni sulle funzioni avanzate fornite da questa licenza, consulta [Target Premium](/help/main/c-intro/intro.md).

Per creare un&#39;attività [!UICONTROL Auto-Target]:

1. Dall&#39;elenco **[!UICONTROL Activities]**, fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

   ![Elenco a discesa Crea attività](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell’elenco. [!UICONTROL Recommendations] è una [funzionalità di Target Premium](/help/main/c-intro/intro.md#premium). Per informazioni sui vari tipi di attività, consulta [Attività](/help/main/c-activities/activities.md) e la [guida alle attività di Target](/help/main/c-activities/target-activities-guide.md).

1. Selezionare **[!UICONTROL Visual]**, se necessario.

   Se preferisci utilizzare [!UICONTROL Form-Based Experience Composer], seleziona [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e a [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre anche il Compositore esperienza visivo per applicazione a pagina singola. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un cliente [Target Premium](/help/main/c-intro/intro.md#premium), scegli un’[area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md), quindi fai clic su **[!UICONTROL Next]**.

   Se l’account è configurato con un URL predefinito, questo verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto [!UICONTROL Visual Experience Composer], con la pagina specificata nell&#39;URL.

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

   [!UICONTROL Visual Experience Composer] visualizza due schede a sinistra dopo aver creato un&#39;attività: Esperienza A ed Esperienza B. Esperienza A è l&#39;esperienza di controllo. L&#39;attenzione è rivolta alla scheda Esperienza B, che puoi modificare in base alle tue esigenze. L’esperienza B è un’esperienza alternativa che puoi aggiungere al test. È possibile aggiungere più esperienze al test. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni sull&#39;aggiunta e la modifica delle esperienze in [!UICONTROL Visual Experience Composer], vedere [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md). Per modificare l&#39;Esperienza B, inizia con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore di [!UICONTROL Visual Experience Composer] per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e l’impostazione delle esperienze.

1. Nella casella [!UICONTROL Audience], fai clic sull&#39;icona di modifica (puntini di sospensione verticali), fai clic su **[!UICONTROL Replace Audience]**, quindi [seleziona il pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md) per l&#39;attività.

   Per impostazione predefinita, il pubblico è impostato su [!UICONTROL All Visitors].

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegli il metodo di allocazione del traffico desiderato. Per creare un&#39;attività [!UICONTROL Auto-Target], selezionare **[!UICONTROL Auto-Target for personalized experiences]**.

   Di seguito sono descritti i tre tipi di allocazione del traffico:

   * **[!UICONTROL Manual (Default)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%. Per ulteriori informazioni, vedere [Creare un test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/test-create-ab.md).

   * **[!UICONTROL Auto-Allocate to best experience]**: la maggior parte dei partecipanti all&#39;attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, vedere [Panoramica dell&#39;allocazione automatica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] utilizza l&#39;apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall&#39;addetto al marketing. Inoltre, indica l&#39;esperienza più adatta per i visitatori in base al loro profilo cliente individuale e ai comportamenti precedenti di visitatori simili.

   Puoi anche fare clic su **[!UICONTROL Add]** per aggiungere un&#39;altra esperienza all&#39;attività.

1. Quando si è soddisfatti del pubblico, delle scelte di esperienza e delle scelte di allocazione del traffico, fare clic su **[!UICONTROL Next]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   >[!NOTE]
   >
   >Se desideri utilizzare [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) con questa attività, consulta le informazioni importanti in [Supporto A4T per le attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Fare clic su **[!UICONTROL Save & Close]** o **[!UICONTROL Save]**.

Dopo aver creato l&#39;attività, nella scheda [!UICONTROL Overview] vengono visualizzate informazioni sull&#39;attività, incluso un diagramma dell&#39;attività.

## Video di formazione: Creazione di test A/B (08:36)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Crea un&#39;attività [!UICONTROL A/B Test] in [!DNL Adobe Target]
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/36325?captions=ita)
