---
keywords: personalizzazione automatizzata;ap
description: Scopri come creare un'attività [!UICONTROL Automated Personalization] (AP) utilizzando [!UICONTROL Visual Experience Composer].
title: Come si crea un'attività [!UICONTROL Automated Personalization]?
badgePremium: label="Premium" type="Positive" url="https://experienceleague.adobe.com/docs/target/using/introduction/intro.html?lang=en#premium newtab=true" tooltip="Scopri cosa è incluso in Target Premium."
feature: Automated Personalization
exl-id: eadc2bbc-310b-479f-b75b-253e8d7aa812
source-git-commit: 3a44c05bea24c622292dd0b774f88f0c93be1d88
workflow-type: tm+mt
source-wordcount: '1844'
ht-degree: 23%

---

# Crea un&#39;attività [!UICONTROL Automated Personalization]

Creare un&#39;attività [!UICONTROL Automated Personalization] (AP) in [!DNL Adobe Target] utilizzando [!UICONTROL Visual Experience Composer] (VEC).

Il flusso di lavoro dell&#39;attività [!UICONTROL Automated Personalization] (AP) in [!DNL Target] è diverso da quello degli altri tipi di attività.

1. Dall&#39;elenco [!DNL Target] [!UICONTROL Activities], fare clic su **[!UICONTROL Create Activity]** > **[!UICONTROL Automated Personalization]**.

1. Per utilizzare [!UICONTROL Visual Experience Composer] (VEC), fare clic su **[!UICONTROL Visual]**.

   Per utilizzare [!UICONTROL Form-Based Experience Composer], selezionare [!UICONTROL Form]. Per ulteriori informazioni, consulta [Compositore esperienza basato su moduli](/help/main/c-experiences/form-experience-composer.md).

   >[!NOTE]
   >
   >Oltre al Compositore esperienza visivo e a [!UICONTROL Form-Based Experience Composer], [!DNL Target] offre [!UICONTROL Single Page Application VEC]. Per ulteriori informazioni sui vari moduli di composizione, consulta [Esperienze e offerte](/help/main/c-experiences/experiences.md).
   >
   >Per informazioni sulla risoluzione dei problemi relativi al Compositore esperienza visivo, vedere [Risoluzione dei problemi relativi al Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md).

1. (Condizionale) [Scegliere un&#39;area di lavoro](/help/main/administrating-target/c-user-management/property-channel/property-channel.md).

1. Nella casella **[!UICONTROL Enter Activity URL]**, specifica l&#39;[URL attività](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-activity-url.md).

   Se l’account è [configurato con un URL predefinito](/help/main/administrating-target/visual-experience-composer-set-up.md), questo verrà visualizzato come impostazione predefinita. Se necessario, puoi passare dall’URL predefinito a un altro.

   [!DNL Target] non distingue tra protocolli URL ([!DNL https] e [!DNL http]). Di conseguenza, [!DNL `http://www.adobe.com`] e [!DNL `https://wwww.adobe.com`] corrispondono entrambi.

1. Fare clic su **[!UICONTROL Create]**.

   La pagina con l’URL specificato viene aperta nel Compositore esperienza visivo.

1. Fare clic sull&#39;icona **[!UICONTROL Rename]** ( ![icona Rinomina](/help/main/assets/icons/MoreSmallListVert.svg) ), fare clic su **[!UICONTROL Rename]**, specificare un nome per l&#39;attività, quindi fare clic su **[!UICONTROL Save]**.

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

1. Modifica gli elementi della pagina come descritto in [Opzioni del Compositore esperienza visivo](/help/main/c-experiences/c-visual-experience-composer/viztarget-options.md).

   È possibile selezionare più immagini contemporaneamente dal gestore delle risorse. Questo consente di visualizzare rapidamente la pagina con ciascuna delle immagini configurate per l’attività. Inoltre è possibile modificare facilmente gli elementi di testo nelle offerte. Quando si modifica un elemento, su tale elemento vengono visualizzate delle barre per indicare che è stato modificato.

1. Fai clic sull&#39;icona **[!UICONTROL Manage Content]** ( ![icona Gestisci contenuto](/help/main/assets/icons/Experience.svg) ) per configurare le combinazioni disponibili.

   Viene visualizzata una finestra di dialogo con due opzioni nella parte superiore dello schermo: [!UICONTROL Experiences] e [!UICONTROL Offers].

   >[!NOTE]
   >
   >Anche se è possibile creare fino a 30.000 esperienze in un’attività Personalizzazione automatizzata, l’attività fornisce prestazioni migliori quando si utilizzano meno di 5.000 esperienze. Lo stesso limite viene applicato anche quando l&#39;attività ha abilitato l&#39;opzione [!UICONTROL Disalow Duplicates].

   L&#39;elenco [!UICONTROL Experiences] mostra ogni elemento di contenuto selezionato per l&#39;attività e la posizione a cui è assegnato.

   È possibile escludere esperienze specifiche selezionando la casella di controllo accanto all&#39;esperienza desiderata e quindi facendo clic sull&#39;icona [!UICONTROL Exclude].

   È possibile escludere o includere esperienze in blocco selezionando la casella di controllo per le esperienze rilevanti e quindi facendo clic sull&#39;icona [!UICONTROL Exclude].

1. (Facoltativo) Fai clic su **[!UICONTROL Offers]** per selezionare parti di contenuto e assegnarle a gruppi di reporting o per consentire solo a determinati visitatori di visualizzare alcune offerte con targeting.

   Per ulteriori informazioni sui gruppi di reporting, vedi [Gruppi di reporting di offerte in Automated Personalization](/help/main/c-activities/t-automated-personalization/offer-reporting-groups-in-automated-personalization.md).

<!--
1. (Conditional) Click **[!UICONTROL Exclusion Groups]** to choose any combination of elements that you want to exclude from the activity.

   ![Exclusion Groups tab of Manage Content dialog box](/help/main/c-activities/t-automated-personalization/assets/exclusion_groups-new.png)

   Although you can create up to 30,000 experiences in an AP test, the algorithm performs its best when fewer than 10,000 distinct experiences are used. This same limit is applied even when the activity has enabled the [!UICONTROL Disalow Duplicates] option.

   If you do not currently have any exclusion groups included in your activity, click **Create Exclusion Group**. You can filter to create a list that shows only the combinations you want to exclude. Name your exclusion group, then click **Save**.

   To edit an existing exclusion group, hover over the group you want to edit, then click the pencil icon.-->

1. Fai clic su **[!UICONTROL Done]** una volta completata la configurazione del contenuto dell&#39;attività.

1. Fai clic su **[!UICONTROL Targeting]** nella parte superiore di [!UICONTROL Visual Experience Composer] per passare al passaggio successivo nel flusso di lavoro guidato in tre passaggi.

   Il passaggio **Targeting** ha un aspetto familiare se sono stati utilizzati altri tipi di attività [!DNL Target]. Qui puoi selezionare un pubblico e specificare la percentuale di visitatori che visualizzano ogni esperienza.

   Viene visualizzato il diagramma di flusso.

   ![Passaggio destinazione test AP](/help/main/c-activities/t-automated-personalization/assets/ap-traffic-flow.png)

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

1. Fare clic sul controllo **[!UICONTROL Traffic Allocation]** per scegliere tra le opzioni seguenti:

   ![Opzioni obiettivo di allocazione traffico](/help/main/c-activities/t-automated-personalization/assets/traffic-allocation-goal-ap-new.png)

   * **[!UICONTROL Evaluate Personalization Algorithm (50/50)]:** Se l&#39;obiettivo è quello di testare l&#39;algoritmo, utilizzare una suddivisione del 50% dei visitatori tra il controllo e l&#39;algoritmo di destinazione. Questa suddivisione fornisce la stima più accurata dell’incremento. Consigliato per l’utilizzo con &quot;esperienze casuali&quot; come controllo.
   * **[!UICONTROL Maximizing Personalization Traffic (90/10)]:** Se il tuo obiettivo è quello di creare un&#39;attività &quot;sempre attiva&quot;, inserisci il 10% dei visitatori nel controllo. Questa opzione assicura che siano presenti dati sufficienti per consentire agli algoritmi di continuare a imparare nel tempo. In questo caso, il compromesso è che, in cambio della personalizzazione di una proporzione maggiore del traffico, si ha meno precisione in cosa sia l’incremento esatto. Indipendentemente dall’obiettivo, questa opzione rappresenta la suddivisione del traffico consigliata quando si utilizza come controllo un’esperienza specifica.
   * **[!UICONTROL Custom Allocation]:** dividi manualmente la percentuale come desiderato.

1. (Condizionale) Dall&#39;elenco a discesa [!UICONTROL Control], [selezionare un&#39;esperienza specifica da utilizzare come controllo](/help/main/c-activities/t-automated-personalization/experience-as-control.md) oppure selezionare [!UICONTROL Random Experience.]

   L&#39;esperienza di controllo fornisce un confronto per determinare l&#39;incremento fornito dal test automatizzato.

   [!UICONTROL Automated Personalization] misura sempre le prestazioni rispetto a un gruppo di controllo. La migliore prassi è quella di collocare almeno il 10% dei partecipanti nel gruppo di controllo. Se l’obiettivo è quello di verificare se l’algoritmo di personalizzazione sui dati che ti vengono forniti funziona meglio dell’assenza di personalizzazione (ad esempio, il controllo fornito in modo casuale), il modo più veloce e preciso per raggiungere questo obiettivo è quello di suddividere il traffico del 50% tra il controllo e l’algoritmo di personalizzazione. Se desideri massimizzare la quantità di traffico personalizzato e non sei interessato a comprendere l’incremento esatto che l’attività sta generando, il modo più veloce e preciso per raggiungere questo obiettivo è quello di suddividere il traffico del 10% e del 90% tra il controllo e l’algoritmo di personalizzazione.

   >[!NOTE]
   >
   >Nelle attività [!UICONTROL Automated Personalization], i criteri di ingresso (targeting URL, regole modello e target di pubblico) vengono valutati per ogni richiesta. Nelle versioni precedenti, i criteri di ingresso venivano valutati una volta a sessione.

1. Fare clic su **[!UICONTROL Next]** per visualizzare la pagina **[!UICONTROL Goals & Settings]**.
1. Configura l&#39;attività con le impostazioni seguenti, quindi fai clic su **[!UICONTROL Save & Close]**.

   | Impostazione | Descrizione |
   |--- |--- |
   | [!UICONTROL Name] | Assegna un nome all’attività. Assegnare all&#39;attività un nome sufficientemente descrittivo da consentire ai membri del team di riconoscerla nell&#39;elenco [!UICONTROL Activities]. Consultate la tabella qui sopra per vedere quali caratteri non sono consentiti nel nome di un’attività. |
   | [!UICONTROL Objective] | (Facoltativo) Inserire la finalità del test. La finalità aiuta a ricordare lo scopo dell&#39;attività. |
   | [!UICONTROL Priority] | A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priority] variano. È possibile utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High] oppure abilitare le priorità precise da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Administration] > [!UICONTROL Reporting] (impostazione predefinita), specificare una priorità: [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High].<P>Per abilitare le priorità dettagliate, fare clic su [!UICONTROL Administration] > [!UICONTROL Reporting], quindi attivare l&#39;opzione [!UICONTROL Enable Fine-Grained Priorities].<P>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:<ul><li>0 = Bassa</li><li>999 = Alta</li></ul>Per le attività create con le versioni precedenti di [!DNL Target Standard/Premium], la priorità [!UICONTROL Low] viene convertita in 0, la priorità [!UICONTROL Medium] in 5 e la priorità [!UICONTROL High] in 10. Se necessario, è possibile modificare questi valori.<P>**Nota**: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
   | [!UICONTROL Duration] | Imposta le date di inizio e di fine dell’attività. È possibile selezionare [!UICONTROL When Activated] oppure specificare una data e un&#39;ora specifiche. |
   | [!UICONTROL Optimization Goal] | Specifica l&#39;obiettivo di ottimizzazione, costituito da due parametri:<ul><li>Ciò che desideri misurare con l&#39;attività</li><li>L&#39;azione intrapresa da un partecipante a un&#39;attività che dimostra che l&#39;obiettivo è stato raggiunto.</li></ul>È possibile scegliere di denominare l&#39;obiettivo di ottimizzazione selezionando i tre punti a destra di [!UICONTROL My Primary Goal]. [!UICONTROL Automated Personalization] attività possono misurare [!UICONTROL Conversion] o [!UICONTROL Revenue]. La conversione può essere ottenuta visualizzando una pagina o una mbox. È possibile inoltre il tracciamento dei clic.<P>L’obiettivo principale diventa anche la metrica di modellazione utilizzata dal sistema di modellazione per calcolare il successo dell’esperienza.<P>I visitatori possono essere mantenuti nell&#39;attività per scopi di tracciamento, dopo aver raggiunto l&#39;obiettivo di modellazione. Ad esempio, spesso viene utilizzata un&#39;attività [!UICONTROL Automated Personalization] per migliorare i click-rate e questa viene impostata come obiettivo di modellazione. Tuttavia è importante capire in che modo un maggior numero di clic porti alla conversione finale, perciò è essenziale effettuare il tracciamento fino alla conversione finale.<P>È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.<P>È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.<P>L&#39;opzione [!UICONTROL Add Dependency] consente di incrementare la metrica di successo nel caso in cui un&#39;altra metrica di successo venga raggiunta o meno.<P>Per aggiungere una dipendenza:<ol><li>Dopo aver aggiunto ulteriori metriche, fai clic su **[!UICONTROL Advanced Settings]** nel menu a tre punti a destra di [!UICONTROL Additional Goal].</li><li>Fare clic sull&#39;opzione **[!UICONTROL Add Dependency]** nella parte inferiore della sezione [!UICONTROL Reporting Settings].</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Reached] per scegliere tra [!UICONTROL Reached] e [!UICONTROL Not Reached].</li></ol>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte. |
   | [!UICONTROL Conversion Metric] | Per impostazione predefinita, la metrica di conversione è la stessa della metrica dell’obiettivo di ottimizzazione. Tuttavia, è possibile definire una metrica di conversione separata deselezionando l&#39;opzione [!UICONTROL Same as Optimization Goal]. |
   | [!UICONTROL Additional Metrics] | Aggiungi eventuali metriche di reporting aggiuntive da utilizzare. Puoi aggiungere metriche di conversione o ricavi.<P>**Nota**: la metrica [!UICONTROL Engagement] non è supportata come metrica aggiuntiva. L&#39;interfaccia utente di [!DNL Target] potrebbe consentire di selezionare la metrica [!UICONTROL Engagement], ma i dati non vengono visualizzati con precisione nei rapporti. |
   | [!UICONTROL Audiences for Reporting] | Aggiungi tipi di pubblico per poter filtrare i rapporti in base al pubblico. Per impostazione predefinita, il rapporto mostra risultati per tutti i visitatori idonei. Aggiungi dei tipi di pubblico per filtrare i risultati per sottoinsiemi più specifici di visitatori.<P>**Nota**: a differenza di altri tipi di attività, [!UICONTROL Automated Personalization] non può utilizzare [!UICONTROL Adobe Analytics] come origine per la generazione di rapporti (A4T). |
   | [!UICONTROL Notes] | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro [!UICONTROL Notes] è ridimensionabile. |

   Quando denomini o rinomini una metrica, i seguenti caratteri non sono consentiti:

   | Carattere | Descrizione |
   |--- |--- |
   | / | Barra |
   | ? | Punto interrogativo |
   | # | Cancelletto |
   | : | Due punti |
   | = | Uguale |
   | + | Più |
   | - | Meno |
   | @ | Chiocciola |

Dopo aver fatto clic su **[!UICONTROL Save & Close]**, viene visualizzata la pagina [!UICONTROL Overview] dell&#39;attività. Fai clic su **Anteprima esperienze** per visualizzare in anteprima l&#39;aspetto delle esperienze consegnate. Viene visualizzato un popup che è possibile utilizzare per visualizzare e condividere i collegamenti alle esperienze di Personalizzazione automatizzata sul sito per ottenere una &quot;anteprima fedele&quot; al di fuori del [!UICONTROL Target] [!UICONTROL Visual Experience Composer] (Compositore esperienza visivo). Per condividere l’anteprima, è necessario condividere i collegamenti dal messaggio. Non è possibile fare clic su un collegamento e quindi copiare l’URL direttamente dal browser. Copiare il collegamento fa sì che l’URL contenga un parametro che visualizza correttamente la pagina solo quando si accede alla pagina dal collegamento nel messaggio.

Per informazioni sul reporting, consulta [Rapporti di Automated Personalization](/help/main/c-reports/personalization-reports/reports-ap.md).
