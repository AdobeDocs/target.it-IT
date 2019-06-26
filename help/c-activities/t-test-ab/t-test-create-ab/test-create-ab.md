---
description: Utilizza il Compositore esperienza visivo in Target per creare il test direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.
keywords: Crea A/B;test A/B;attività A/B;nuova attività A/B
seo-description: Utilizza il Compositore esperienza visivo in Target per creare il test direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.
seo-title: Creare un test A/B
solution: Target
title: Creare un test A/B
topic: Advanced,Standard,Classic
uuid: 2a255cf9-91c7-4710-bfd7-a4d8797ef24c
translation-type: tm+mt
source-git-commit: 8bd57fb3bb467d8dae50535b6c367995f2acabac

---


# Creare un test A/B{#create-an-a-b-test}

Utilizza il Compositore esperienza visivo in Target per creare il test direttamente su una pagina abilitata per Target e modificare parti della pagina in Target.

1. Nell’elenco [!UICONTROL Attività] fai clic su **[!UICONTROL Crea attività]** &gt; **[!UICONTROL Test A/B]**.

   ![Elenco a discesa Crea attività](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_select-new.png)

   >[!NOTE]
   >
   >I tipi di attività disponibili dipendono dall’account [!DNL Target]. Alcuni tipi di attività potrebbero non essere visualizzati nell&#39;elenco. For example, [!UICONTROL Recommendations] is a [Target Premium feature](/help/c-intro/intro.md#premium).
   >
   >For information about the various activity types, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) and the [Target activities guide](/help/c-activities/target-activities-guide.md).

   ![Creare un test di test A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/create-ab.png)

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   Se preferisci utilizzare il Compositore esperienza basato su moduli, seleziona [!UICONTROL Modulo]. See [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) for more information.

   >[!NOTE]
   >
   >Oltre a VEC e Experience Composer basato su modulo, Target offre il VEC applicazione singola e il VEC per le app mobili. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, consulta [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).
   >
   >The [!UICONTROL [Choose Workplace](/help/administrating-target/c-user-management/property-channel/property-channel.md) option in the preceding illustration is a [Target Premium](/help/c-intro/intro.md) feature. Se l&#39;opzione non è visualizzata, l&#39;organizzazione dispone di una licenza di Target Standard.]

1. (Condizionale) Se siete clienti Target Premium, scegliete un&#39;area di lavoro.

1. Specify your [activity URL](../../../c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click **[!UICONTROL Next]**.

   Se l&#39;account è configurato con un URL predefinito, tale URL verrà visualizzato come impostazione predefinita. È possibile passare dall’URL predefinito a un altro.

   Verrà aperto il [!UICONTROL Compositore esperienza visivo], con la pagina specificata nell&#39;URL.

   ![VEC](/help/c-activities/t-test-ab/t-test-create-ab/assets/vec-new.png)

1. Digita un nome per l&#39;attività nello spazio fornito.

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

   Per ulteriori informazioni su come aggiungere e modificare le esperienze nel [!UICONTROL Compositore esperienza visivo], vedi [Aggiungi esperienza](../../../c-activities/t-test-ab/t-test-create-ab/ab-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00). Per modificare l&#39;Esperienza B, inizia con il passaggio 3.

1. Click **[!UICONTROL Targeting]** at the top of the [!UICONTROL Visual Experience Composer] to move to the next step in the three-step guided workflow.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio Targeting A/B Test](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_flow-new.png)

   Il diagramma di flusso ti guida attraverso le fasi di selezione del pubblico per l’attività e creazione di esperienze.
1. Nella casella [!UICONTROL Pubblico], fai clic sull¡icona di modifica, quindi [seleziona il pubblico](../../../c-activities/t-test-ab/t-test-create-ab/ab-audience.md#concept_A268236C1224451DB7844BF67F41A087) per la tua attività.

   Per impostazione predefinita, il pubblico è impostato su Tutti i visitatori.

1. Scegli la percentuale di visitatori qualificati che dovranno accedere all’attività.

   ![Percentuale di pubblico](/help/c-activities/t-test-ab/t-test-create-ab/assets/audperc-new.png)

   Ad esempio, puoi limitare l’accesso al 50% di tutti i visitatori o 45% del pubblico “Californians”.

1. Imposta l&#39;allocazione del traffico.

   Puoi mostrare più esperienze allo stesso pubblico. Viene visualizzato un diagramma che mostra il pubblico selezionato e le esperienze aggiunte all’attività.

   Scegliete il metodo desiderato per l&#39;allocazione del traffico:

   * **[!UICONTROL Manuale (predefinito)]**: Specificate la percentuale di partecipanti che desiderate vedere ogni esperienza. Puoi suddividere le percentuali in modo uniforme tra tutte le esperienze, oppure specificare percentuali maggiori o minori per ogni esperienza. Il totale per tutte le esperienze deve essere uguale al 100%.

   * **[!UICONTROL Allocazione automatica all&#39;esperienza ottimale]**: La maggior parte dei partecipanti all&#39;attività vengono indirizzati automaticamente a esperienze più performanti. Alcuni visitatori sono assegnati a tutte le esperienze, per mantenere l’esplorazione delle esperienze e riconoscere eventuali cambiamenti nelle tendenze prestazionali. Consulta [Allocazione automatizzata del traffico](../../../c-activities/automated-traffic-allocation/automated-traffic-allocation.md#concept_A1407678796B4C569E94CBA8A9F7F5D4).

   * **[!UICONTROL Targeting automatico per esperienze personalizzate]**: In Target sono utilizzati algoritmi di machine learning avanzati per eseguire automaticamente il targeting dei visitatori con la migliore esperienza per massimizzare gli obiettivi. Per ulteriori informazioni, consulta [Targeting automatico per ottimizzare](../../../c-activities/auto-target-to-optimize.md#concept_67779E5B7F67427A97D7EA2A6FB919B3).
   Puoi inoltre fare clic su **[!UICONTROL Aggiungi esperienza]** per aggiungere un’altra esperienza all’attività.

1. Quando hai effettuato le scelte di pubblico ed esperienza desiderate, fai clic su **[!UICONTROL Avanti]** per passare al terzo passaggio del flusso di lavoro guidato in tre passaggi.

1. Specifica [obiettivi e impostazioni](../../../c-activities/t-test-ab/t-test-create-ab/ab-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) per l&#39;attività.

   ![Impostazioni attività A/B](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

1. Fai clic su **[!UICONTROL Salva]**.

Dopo la creazione dell&#39;attività, nella scheda Panoramica sono visualizzate informazioni riguardanti l&#39;attività, compreso un diagramma.

## Video di formazione: Creazione di test A/B (08:36)

In questo video viene illustrato come creare un test A/B utilizzando il flusso di lavoro guidato in tre fasi di [!DNL Target].

* Creare un’attività A/B in Adobe Target
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391?captions=ita)
