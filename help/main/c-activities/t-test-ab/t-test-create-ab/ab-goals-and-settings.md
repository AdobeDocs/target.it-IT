---
keywords: impostazioni attività;obiettivi e impostazioni A/B;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo principale;metriche aggiuntive;obiettivo;priorità;durata;soluzione di reporting;obiettivo;audience per rapporti;Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;Cosa succede dopo che un utente ha individuato questa metrica obiettivo;note
description: Scopri come utilizzare la pagina [!UICONTROL Goals and Settings] per specificare informazioni sugli obiettivi di un'attività A/B.
title: Come posso specificare obiettivi e impostazioni in un'attività A/B di  [!DNL Target] ?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: b5f508d283390c859085d4ee52c582312085addc
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 35%

---

# Obiettivi e impostazioni

Nella pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] è possibile specificare informazioni sugli obiettivi dell&#39;attività.

Le impostazioni disponibili dipendono dall&#39;utilizzo di Target o [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) come origine per la generazione di rapporti.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

La sezione [!UICONTROL Activity Settings] della pagina [!UICONTROL Goals & Settings] consente di configurare le opzioni seguenti:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Objective] | Specifica una finalità facoltativa. L’obiettivo può essere qualsiasi informazione che aiuti te e i membri del tuo team a identificare l’attività. |
| [!UICONTROL Priority] | A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priority] variano. È possibile utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High] oppure abilitare le priorità precise da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Administration] (impostazione predefinita), specificare una priorità: [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High].<P>Per abilitare [le priorità precise](/help/main/administrating-target/reporting.md), fai clic su [!UICONTROL Administration] > [!UICONTROL Reporting], quindi attiva l&#39;opzione [!UICONTROL Enable Fine-Grained Priorities]. <P>Se questa opzione è abilitata, specificare un valore compreso tra 0 e 999: 0 = [!UICONTROL Low] e 999 = [!UICONTROL High]. <P>Per le attività create con le versioni precedenti di [!DNL Target], la priorità [!UICONTROL Low] viene convertita in 0, [!UICONTROL Medium] in 5 e [!UICONTROL High] in 10. Se necessario, è possibile modificare questi valori.<P>Nota: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
| Durata | L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

La sezione [!UICONTROL Reporting Settings] della pagina [!UICONTROL Goals & Settings] consente di configurare le opzioni seguenti:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Reporting Source] | Specifica da quali dati della soluzione vengono raccolti:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Se un&#39;origine per la generazione di rapporti è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata l&#39;origine specificata e questa impostazione non è visibile.<P>Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.<P>**Adobe Analytics**: consulta [Adobe Analytics as the Reporting Source for Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per informazioni sulle differenze tra le soluzioni di reporting e i vantaggi di ciascuna. Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target].<P>Per specificare un&#39;origine per la generazione di rapporti, scegliere innanzitutto una delle [!DNL Analytics] società associate al proprio account, quindi selezionare la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Adobe Target]. Se le suite di rapporti previste non sono visualizzate, disconnettersi e accedere di nuovo a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.<P><P>**Adobe Customer Journey Analytics**: per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target], vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md).<P>Il reporting di [!DNL Target] in [!DNL Customer Journey Analytics] è supportato nelle attività A/B con suddivisione manuale del traffico. Le attività A/B [!UICONTROL Auto-Target] e [!UICONTROL Auto-Allocate] non possono utilizzare il reporting [!DNL Target] in [!DNL Customer Journey Analytics]. |
| [!UICONTROL Goal Metric] | Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversion], quindi imposta i parametri che determinano quando viene raggiunto il successo. Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Nota: se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è [!UICONTROL Conversion]. Impossibile selezionare [!DNL Analytics] metriche come obiettivo. Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.<P>Se attivato, il campo [!UICONTROL Estimated Value of the Conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. I dati sono di tipo valuta.<P>Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Si tratta di un comportamento diverso da quello predefinito in [!DNL Target Classic], che conta i visitatori come nuovi se visualizzano nuovamente l&#39;attività. |
| [!UICONTROL Additional Metrics] | Creare ulteriori metriche di successo. Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics]. |
| [!UICONTROL Audiences for Reporting] | Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per mostrare informazioni solo su tipi di pubblico specifici. Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per la suite di rapporti [!DNL Analytics] è applicato. |

## Impostazioni avanzate  {#section_E2FE441AFB324E498793ABB025ED9974}

La sezione [!UICONTROL Advanced Settings] della pagina [!UICONTROL Goals & Settings] consente di configurare le opzioni seguenti:

Per specificare le impostazioni avanzate, fare clic sull&#39;icona **[!UICONTROL More]** (puntini di sospensione verticali), quindi fare clic su **[!UICONTROL Advanced Settings]**, come illustrato nella figura seguente.

![Menu Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

![Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Impostazione | Descrizione |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di attività potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione. Puoi fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. L&#39;opzione [!UICONTROL Add Dependency] consente di incrementare la metrica di successo nel caso in cui un&#39;altra metrica di successo venga raggiunta o meno. Per aggiungere una dipendenza:<ul><li>Dopo aver aggiunto ulteriori metriche, fare clic su [!UICONTROL Advanced Settings].</li><li>Fare clic sull&#39;opzione [!UICONTROL Add Dependency]:</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Reached] per scegliere tra [!UICONTROL Reached] e [!UICONTROL  Not Reached].</li><li>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:<ul><li>Selezionare [!UICONTROL Increment Count & Keep User in Activity] per specificare la modalità di incremento del conteggio.</li><li>Seleziona [!UICONTROL Increment Count, Release User & Allow Reentry] per specificare l&#39;esperienza che l&#39;utente vedrà se accede nuovamente all&#39;attività.</li><li>Seleziona [!UICONTROL Increment Count, Release User & Bar from Reentry] per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Sono disponibili tre opzioni per l’incremento del conteggio:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

La sezione [!UICONTROL Other Metadata] della pagina [!UICONTROL Goals & Settings] consente di specificare qualsiasi informazione sull&#39;attività utile da tenere a portata di mano per te o per gli altri membri del team. Il riquadro Note è ridimensionabile.|

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Impostazioni attività (3:02) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

(https://video.tv.adobe.com/v/17381?captions=ita)

### Creazione di test A/B (8:36) ![Icona esercitazione](/help/main/assets/tutorial.png)

Questo video mostra le impostazioni di attività nel flusso di lavoro guidato in tre passaggi durante la creazione di un’attività. Obiettivi e impostazioni sono trattati a partire dal minuto 5:30.

* Creare un’attività A/B in Adobe Target
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
