---
keywords: Creare test A/B;attività A/B;nuova attività A/B;creare test A/B
description: Utilizzare il Compositore esperienza visivo [!UICONTROL Visual Experience Composer] per creare attività Test A/B direttamente su una pagina abilitata per  [!DNL Target].
title: Come si crea un test A/B?
feature: A/B Tests
exl-id: 76002873-0b7c-44a8-8e89-8ad28b63eccb
source-git-commit: 9cc1eb4c5c95ea51bc0a1fc9e89b245a18c9914b
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 17%

---

# Creare un’attività di test A/B

Sfrutta il Compositore esperienza visivo di [!UICONTROL Visual Experience Composer] in [!DNL Adobe Target] per creare [!UICONTROL A/B Test] attività direttamente su una pagina abilitata per [!DNL Target] e modificare le sezioni della pagina in [!DNL Target].

>[!NOTE]
>
>Oltre all&#39;attività [!UICONTROL Manual] (predefinita) [!UICONTROL A/B Test] (discussa in questo articolo), [!DNL Target] fornisce altri due tipi di attività [!UICONTROL A/B Test]: [!UICONTROL Auto-Allocate] e [!UICONTROL Auto-Target].
>
>Consulta [Tipi di attività test A/B](/help/main/c-activities/t-test-ab/test-ab.md#types) in *Panoramica test A/B*.

Per creare un&#39;attività [!UICONTROL A/B Test] manuale:

1. Dall&#39;elenco **[!UICONTROL Activities]**, fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL A/B Test]**.

1. Dalla finestra di dialogo [!UICONTROL Create A/B Test Activity], selezionare **[!UICONTROL Visual]**, se necessario.

   Se preferisci utilizzare [!UICONTROL Form-Based Experience Composer], seleziona [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e a [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre il Compositore esperienza visivo [!UICONTROL Single Page Application]. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un cliente di [Target Premium](/help/main/c-intro/intro.md#premium), scegli un **[!UICONTROL Choose Workspace]** area di lavoro[ dall&#39;elenco a discesa ](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   L&#39;opzione [[!UICONTROL Choose Workplace]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) è una funzionalità di [Target Premium](/help/main/c-intro/intro.md) e potrebbe non essere visualizzata se la tua organizzazione dispone di una licenza di [!UICONTROL Target Standard].

1. Nella casella **[!UICONTROL Enter Activity URL]**, specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

1. Fare clic su **[!UICONTROL Create]**.

   Verrà aperto [!UICONTROL Visual Experience Composer], con la pagina specificata nell&#39;URL.

1. Per assegnare un nome all&#39;attività, fare clic sull&#39;icona **[!UICONTROL Edit]** ( ![icona Modifica](/help/main/assets/icons/Edit.svg) ) accanto a &quot;[!UICONTROL Untitled Activity]&quot;, specificare un nome descrittivo per l&#39;attività e quindi fare clic su **[!UICONTROL Save]**.

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

   [!UICONTROL Visual Experience Composer] visualizza due schede a sinistra dopo aver creato una nuova attività: Esperienza A ed Esperienza B. L&#39;Esperienza A è l&#39;esperienza di controllo. L&#39;attenzione è rivolta alla scheda Esperienza B, che puoi modificare in base alle tue esigenze. L’esperienza B è un’esperienza alternativa che puoi aggiungere al test. È possibile aggiungere più esperienze al test facendo clic sull&#39;icona [!UICONTROL Add] ( ![Icona Aggiungi](/help/main/assets/icons/Add.svg) ) nella parte superiore del riquadro [!UICONTROL Experiences]. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni sull&#39;aggiunta e la modifica delle esperienze in [!UICONTROL Visual Experience Composer], vedere [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Per modificare l&#39;Esperienza B, inizia con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore di [!UICONTROL Visual Experience Composer] per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Il diagramma di flusso ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l’allocazione del traffico per ogni esperienza nell’attività.

1. (Condizionale) Fare clic sul controllo **[!UICONTROL All Visitors]** per selezionare un altro pubblico per l&#39;attività.

   Il pubblico [!UICONTROL All Visitors] è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra.

   Viene visualizzato il frame a destra, che consente di aggiungere o eliminare un pubblico e di assegnare la percentuale di visitatori per l’attività.

   1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Replace]** ( ![Icona Sostituisci](/help/main/assets/icons/Retweet.svg) ) nel frame a destra.
   1. Nella finestra di dialogo [!UICONTROL Add Audience], [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assign Audience]**.

      Puoi fare clic su **Combina tipi di pubblico** per [creare un pubblico che combini più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

      Se devi creare un nuovo pubblico che non sia già presente in [!UICONTROL Audience Library], fai clic su **Crea pubblico**. Durante il flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md) puoi scegliere tra le seguenti opzioni:

      * **[!UICONTROL Audience Library]**: crea un pubblico su richiesta salvato in [!UICONTROL Audience Library] che può essere riutilizzato in altre attività.
      * **[!UICONTROL This activity only]**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non è salvato in [!UICONTROL Audience Library] e può essere utilizzato solo nell&#39;attività corrente.

   1. Fai clic su **[!UICONTROL Visitor Percentage]** nel frame a destra, quindi scegli la percentuale di visitatori idonei che dovranno accedere all&#39;attività.

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Fare clic sul controllo **[!UICONTROL Traffic Allocation]**, quindi scegliere il metodo di allocazione del traffico desiderato nel riquadro di destra, come illustrato di seguito:

   ![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/traffic-allocation-method-new.png)

   Scegli il metodo desiderato per l’allocazione del traffico:

   * **[!UICONTROL Manual (Default)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Auto-Allocate to best experience]**: la maggior parte dei partecipanti all&#39;attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, vedere [[!UICONTROL Auto-Allocate] panoramica](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Auto-Target for personalized experiences]**: [!DNL Target] utilizza l&#39;apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall&#39;addetto al marketing. Inoltre, indica l&#39;esperienza più adatta per i visitatori in base al loro profilo cliente individuale e ai comportamenti precedenti di visitatori simili. Per ulteriori informazioni, consulta [Panoramica sul Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Fai clic su **[!UICONTROL Experiences]** nel riquadro a destra, quindi specifica l&#39;allocazione del traffico desiderata per ogni esperienza.

1. Quando si è soddisfatti del pubblico, delle scelte di esperienza e delle scelte di allocazione del traffico, fare clic su **[!UICONTROL Next]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

1. Fare clic su **[!UICONTROL Save & Close]** o **[!UICONTROL Save]**.

Dopo aver creato l&#39;attività, nella scheda [!UICONTROL Overview] vengono visualizzate informazioni sull&#39;attività, incluso un diagramma dell&#39;attività.
