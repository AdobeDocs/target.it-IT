---
keywords: creare allocazione automatica;test A/B;allocazione automatica attività;nuova attività A/B;allocazione automatica;allocazione automatica all'esperienza migliore;allocare;allocazione automatica
description: Scopri come utilizzare il [!UICONTROL Compositore esperienza visivo] (VEC) per creare [!UICONTROL attività di test A/B con allocazione automatica].
title: Come si crea un'attività [!UICONTROL Allocazione automatica]?
feature: Auto-Allocate
exl-id: 30bc95e0-4f5e-4d1f-bad2-7b20b8f3c7d2
TQID: https://experienceleague.adobe.com/dInypDH72qyoj5UygbEt-BWpq1gZkbxJiSXSheNPO54
product_v2: id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2: id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c1579802-ddd4-4214-8a91-97b2066abe11id: eb30f47f-d87a-400f-8f78-63ce7979ff56id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1060
ht-degree: 14%

---

# Crea un&#39;attività [!UICONTROL Allocazione automatica]

Utilizza il [!UICONTROL Compositore esperienza visivo] (VEC) in [!DNL Adobe Target] per creare l&#39;attività [!UICONTROL Allocazione automatica] [!UICONTROL Test A/B] direttamente su una pagina abilitata per [!DNL Target] e per modificare parti della pagina in [!DNL Target].

Oltre all&#39;attività [!UICONTROL Allocazione automatica] [!UICONTROL Test A/B] (discussa in questo articolo), [!DNL Target] fornisce due tipi aggiuntivi di attività [!UICONTROL Test A/B]: [!UICONTROL Manuale (predefinito)] e [!UICONTROL Targeting automatico]. Consulta [Tipi di attività test A/B](/help/main/c-activities/t-test-ab/test-ab.md#types) in *Panoramica test A/B*.

Per creare un&#39;attività [!UICONTROL Allocazione automatica]:

1. Dall&#39;elenco **[!UICONTROL Attività]**, fare clic su **[!UICONTROL Crea attività]** > **[!UICONTROL Test A/B]**.

1. Dalla finestra di dialogo [!UICONTROL Crea attività test A/B], seleziona **[!UICONTROL Visivo]**, se necessario.

   Se preferisci utilizzare il [!UICONTROL Compositore esperienza basato su moduli], seleziona [!UICONTROL Modulo]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e al Compositore esperienza basato su moduli [!UICONTROL 1}, [!DNL Target] offre il Compositore esperienza visivo [!UICONTROL Applicazione a pagina singola]. ]Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) Se sei un [cliente Target Premium](/help/main/c-intro/intro.md#premium), dall&#39;elenco a discesa **[!UICONTROL Scegli Workspace]** scegli un [area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

   L&#39;opzione [[!UICONTROL Scegli area di lavoro]](/help/main/administrating-target/c-user-management/property-channel/property-channel.md) è una funzionalità di [Target Premium](/help/main/c-intro/intro.md) e potrebbe non essere visualizzata se la tua organizzazione dispone di una licenza di [!UICONTROL Target Standard].

1. Nella casella **[!UICONTROL Immetti URL attività]**, specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

1. Fai clic su **[!UICONTROL Crea]**.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

1. Per assegnare un nome all&#39;attività, fare clic sull&#39;icona **[!UICONTROL Modifica]** ( ![Icona Modifica](/help/main/assets/icons/Edit.svg) ) accanto a &quot;[!UICONTROL Attività senza titolo]&quot;, specificare un nome descrittivo per l&#39;attività, quindi fare clic su **[!UICONTROL Salva]**.

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

   Il [!UICONTROL Compositore esperienza visivo] visualizza due schede sul lato sinistro dopo aver creato una nuova attività: [!UICONTROL Esperienza A] e [!UICONTROL Esperienza B]. [!UICONTROL Esperienza A] è l&#39;esperienza di controllo. Il tuo focus è sulla scheda [!UICONTROL Esperienza B], che puoi modificare come desideri. [!UICONTROL Esperienza B] è l&#39;esperienza alternativa che puoi aggiungere al test. Per aggiungere più esperienze al test, fai clic sull&#39;icona [!UICONTROL Aggiungi] ( ![Aggiungi icona](/help/main/assets/icons/Add.svg) ) nella parte superiore del riquadro [!UICONTROL Esperienze]. È inoltre possibile eliminare l&#39;Esperienza A dall&#39;attività se non si desidera includere un&#39;esperienza di sito predefinita come opzione.

   Per ulteriori informazioni sull&#39;aggiunta e la modifica delle esperienze nel [!UICONTROL Compositore esperienza visivo], vedere [Aggiungi esperienza](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Per modificare [!UICONTROL Esperienza B], iniziare con il passaggio 2.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore del [!UICONTROL Compositore esperienza visivo] per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting per Test A/B](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new-ui.png)

   Il diagramma di flusso ti guida attraverso i passaggi per assegnare un pubblico e la relativa percentuale di traffico, selezionare il metodo di allocazione del traffico e specificare l’allocazione del traffico per ogni esperienza nell’attività.

1. (Condizionale) Fai clic sul controllo **[!UICONTROL Tutti i visitatori]** per selezionare un altro pubblico per l&#39;attività.

   Il pubblico [!UICONTROL Tutti i visitatori] è impostato come predefinito. Se selezioni un altro pubblico, il suo nome viene visualizzato nel controllo più a sinistra.

   Viene visualizzato il frame a destra, che consente di aggiungere o eliminare un pubblico e di assegnare la percentuale di visitatori per l’attività.

   1. Per cambiare il pubblico, fai clic sull&#39;icona **[!UICONTROL Sostituisci]** ( ![Sostituisci icona](/help/main/assets/icons/Retweet.svg) ) nel riquadro a destra.
   1. Nella finestra di dialogo [!UICONTROL Aggiungi pubblico], [seleziona il pubblico desiderato](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), quindi fai clic su **[!UICONTROL Assegna pubblico]**.

      Puoi fare clic su **Combina tipi di pubblico** per [creare un pubblico che combini più tipi di pubblico](/help/main/c-target/combining-multiple-audiences.md).

      Se devi creare un nuovo pubblico che non sia già presente nella [!UICONTROL Libreria pubblico], fai clic su **Crea pubblico**. Durante il flusso di lavoro [create-audience](/help/main/c-target/c-audiences/audiences.md) puoi scegliere tra le seguenti opzioni:

      * **[!UICONTROL Libreria tipi di pubblico]**: crea un pubblico on-demand salvato nella [!UICONTROL Libreria tipi di pubblico] che può essere riutilizzato in altre attività
      * **Solo questa attività**: crea un [pubblico specifico per l&#39;attività](/help/main/c-target/creating-activity-only-audience.md) che non è salvato nella [!UICONTROL Libreria tipi di pubblico] e può essere utilizzato solo nell&#39;attività corrente

   1. Fai clic su **[!UICONTROL Percentuale visitatori]** nel frame a destra, quindi scegli la percentuale di visitatori idonei che desideri inserire nell&#39;attività.

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Fai clic sul controllo **[!UICONTROL Allocazione traffico]**, quindi scegli il metodo di allocazione del traffico desiderato nel riquadro a destra. In questo scenario, fai clic su **[!UICONTROL Allocazione automatica all&#39;esperienza migliore]**.

   ![Impostazioni del metodo di allocazione traffico](/help/main/c-activities/automated-traffic-allocation/assets/auto-allocate-to-best-exp.png)

   Sono disponibili i seguenti metodi di allocazione del traffico:

   * **[!UICONTROL Manuale (impostazione predefinita)]**: specifica la percentuale di partecipanti che dovranno visualizzare ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Allocazione automatica all&#39;esperienza migliore]**: la maggior parte dei partecipanti all&#39;attività viene automaticamente indirizzata alle esperienze con prestazioni migliori. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Per ulteriori informazioni, vedere [[!UICONTROL Cenni preliminari sull&#39;allocazione automatica]](/help/main/c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Targeting automatico per esperienze personalizzate]**: [!DNL Target] utilizza l&#39;apprendimento automatico avanzato per personalizzare i contenuti e favorire le conversioni identificando più esperienze ad alte prestazioni definite dall&#39;addetto al marketing e fornendo l&#39;esperienza più personalizzata ai visitatori in base ai loro profili cliente individuali e ai comportamenti passati di visitatori simili. Per ulteriori informazioni, consulta [Panoramica sul Targeting automatico](/help/main/c-activities/auto-target/auto-target-to-optimize.md).

1. Fai clic su **[!UICONTROL Esperienze]** nel riquadro a destra, quindi specifica l&#39;allocazione del traffico desiderata per ogni esperienza.

1. Quando sei soddisfatto delle scelte relative a pubblico, esperienza e allocazione del traffico, fai clic su **[!UICONTROL Avanti]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md) per l’attività.

   >[!NOTE]
   >
   >Se desideri utilizzare [Analytics for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T) con questa attività, consulta le informazioni importanti in [Supporto A4T per le attività di allocazione automatica e targeting automatico](/help/main/c-integrating-target-with-mac/a4t/a4t-at-aa.md).

1. Fai clic su **[!UICONTROL Salva e chiudi]** o **[!UICONTROL Salva]**.

Dopo aver creato l&#39;attività, nella scheda [!UICONTROL Panoramica] vengono visualizzate informazioni sull&#39;attività, incluso un diagramma.
