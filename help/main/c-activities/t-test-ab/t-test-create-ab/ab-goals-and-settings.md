---
keywords: impostazioni attività;obiettivi e impostazioni A/B;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo principale;metriche aggiuntive;obiettivo;priorità;durata;soluzione di reporting;obiettivo;audience per rapporti;Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;Cosa succede dopo che un utente ha individuato questa metrica obiettivo;note
description: Scopri come utilizzare il [!UICONTROL Goals and Settings] per specificare informazioni sugli obiettivi di un'attività A/B.
title: Come si specificano obiettivi e impostazioni in una [!DNL Target] Attività A/B?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: b5f508d283390c859085d4ee52c582312085addc
workflow-type: tm+mt
source-wordcount: '1252'
ht-degree: 35%

---

# Obiettivi e impostazioni

Il [!UICONTROL Goals & Settings] pagina in [!DNL Adobe Target] è dove si specificano informazioni sugli obiettivi dell’attività.

Le impostazioni disponibili dipendono dall’utilizzo di Target o [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) come origine per la generazione di rapporti.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Il [!UICONTROL Activity Settings] sezione del [!UICONTROL Goals & Settings] pagina consente di configurare le seguenti opzioni:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Objective] | Specifica una finalità facoltativa. L’obiettivo può essere qualsiasi informazione che aiuti te e i membri del tuo team a identificare l’attività. |
| [!UICONTROL Priority] | A seconda delle impostazioni, il [!DNL Target] Interfaccia utente e opzioni per [!UICONTROL Priority] variare. Puoi utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium], o [!UICONTROL High], oppure puoi abilitare le priorità dettagliate da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Administration] (impostazione predefinita), specifica una priorità: [!UICONTROL Low], [!UICONTROL Medium], o [!UICONTROL High].<P>Per abilitare [priorità precise](/help/main/administrating-target/reporting.md), fai clic su [!UICONTROL Administration] > [!UICONTROL Reporting], quindi attiva/disattiva [!UICONTROL Enable Fine-Grained Priorities] nella posizione &quot;On&quot;. <P>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999: 0 = [!UICONTROL Low] e 999 = [!UICONTROL High]. <P>Per le attività create con le versioni precedenti di [!DNL Target], [!UICONTROL Low] la priorità è convertita in 0, [!UICONTROL Medium] è convertito in 5, e [!UICONTROL High] viene convertito in 10. Se necessario, è possibile modificare questi valori.<P>Nota: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
| Durata | L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser. |

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

Il [!UICONTROL Reporting Settings] sezione del [!UICONTROL Goals & Settings] pagina consente di configurare le seguenti opzioni:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Reporting Source] | Specifica da quali dati della soluzione vengono raccolti:<ul><li>[!DNL Adobe Target]</li><li>[!DNL Adobe Analytics]</li><li>[!DNL Adobe Customer Journey Analytics]</li></ul>Se un’origine per la generazione di rapporti è specificata nel [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata l’origine specificata e questa impostazione non è visibile.<P>Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.<P>**Adobe Analytics**: vedi [Adobe Analytics come origine per la generazione di rapporti per Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna. Durante la selezione [!DNL Analytics] come origine di reporting per [!DNL Target], si seleziona un [!DNL Analytics] suite di rapporti da ricevere [!DNL Target] dati attività.<P>Per specificare un&#39;origine per la generazione di rapporti, scegliere una delle opzioni disponibili [!DNL Analytics] aziende a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l’attività. Solo le suite di rapporti per le quali è stato eseguito il provisioning [!DNL Adobe Target] sono disponibili per la selezione. Se non trovi le suite di rapporti previste, disconnettiti e accedi di nuovo al [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.<P><P>**Adobe Customer Journey Analytics**: vedi [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull’integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].<P>[!DNL Target] creazione di rapporti in [!DNL Customer Journey Analytics] è supportato nelle attività A/B con suddivisione manuale del traffico. [!UICONTROL Auto-Target] e [!UICONTROL Auto-Allocate] Le attività A/B non possono utilizzare [!DNL Target] creazione di rapporti in [!DNL Customer Journey Analytics]. |
| [!UICONTROL Goal Metric] | Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli un [!UICONTROL Conversion] metrica, quindi imposta i parametri che determinano quando viene raggiunto il successo. Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Nota: se la soluzione di reporting è impostata su [!DNL Analytics], l’unica metrica di obiettivo disponibile è [!UICONTROL Conversion]. [!DNL Analytics] Le metriche non possono essere selezionate come obiettivo. Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.<P>Se l&#39;opzione è abilitata, [!UICONTROL Estimated Value of the Conversion] (non disponibile per il [!UICONTROL Page Score] metriche) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. I dati sono di tipo valuta.<P>Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Questo comportamento è diverso da quello predefinito in [!DNL Target Classic], che conta i visitatori come nuovi se visualizzano nuovamente l’attività. |
| [!UICONTROL Additional Metrics] | Creare ulteriori metriche di successo. Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, le metriche definite per [!DNL Analytics] suite di rapporti. |
| [!UICONTROL Audiences for Reporting] | Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per mostrare informazioni solo su tipi di pubblico specifici. Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per [!DNL Analytics] suite di rapporti applicata. |

## Impostazioni avanzate  {#section_E2FE441AFB324E498793ABB025ED9974}

Il [!UICONTROL Advanced Settings] sezione del [!UICONTROL Goals & Settings] pagina consente di configurare le seguenti opzioni:

Per specificare le impostazioni avanzate, fare clic su **[!UICONTROL More]** (puntini di sospensione verticali), quindi fai clic su **[!UICONTROL Advanced Settings]**, come illustrato nella figura seguente.

![Menu Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

![Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Impostazione | Descrizione |
|--- |--- |
| [!UICONTROL Which success metric must be reached before incrementing this metric?] | Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di attività potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione. Puoi fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. Il [!UICONTROL Add Dependency] consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno. Per aggiungere una dipendenza:<ul><li>Dopo aver aggiunto ulteriori metriche, fai clic su [!UICONTROL Advanced Settings].</li><li>Fai clic su [!UICONTROL Add Dependency] opzione:</li><li>Trascina le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Reached] per alternare l&#39;impostazione tra [!UICONTROL Reached] e[!UICONTROL  Not Reached].</li><li>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.</li></ul> |
| [!UICONTROL What will happen after a user encounters this goal metric?] | Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:<ul><li>Seleziona [!UICONTROL Increment Count & Keep User in Activity] per specificare come incrementare il conteggio.</li><li>Seleziona [!UICONTROL Increment Count, Release User & Allow Reentry] per specificare l’esperienza che l’utente vedrà se accede nuovamente all’attività.</li><li>Seleziona [!UICONTROL Increment Count, Release User & Bar from Reentry] per specificare cosa vede l’utente al posto del contenuto dell’attività.</li></ul> |
| [!UICONTROL How will the count be incremented?] | Sono disponibili tre opzioni per l’incremento del conteggio:<ul><li>[!UICONTROL Once per Entrant]</li><li>[!UICONTROL On Every Impression (Excluding page refreshes)]</li><li>[!UICONTROL On Every Impression]</li></ul> |

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

Il [!UICONTROL Other Metadata] sezione del [!UICONTROL Goals & Settings] Questa pagina consente di specificare tutte le informazioni sull’attività, utili per te o per altri membri del gruppo. Il riquadro Note è ridimensionabile.|

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
