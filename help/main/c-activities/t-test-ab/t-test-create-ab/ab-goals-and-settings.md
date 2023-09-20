---
keywords: impostazioni attività;obiettivi e impostazioni A/B;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo principale;metriche aggiuntive;obiettivo;priorità;durata;soluzione di reporting;obiettivo;audience per rapporti;Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;Cosa succede dopo che un utente ha individuato questa metrica obiettivo;note
description: Scopri come utilizzare il [!UICONTROL Obiettivi e impostazioni] pagina in [!DNL Adobe Target] per specificare informazioni sugli obiettivi di un'attività A/B.
title: Come si specificano obiettivi e impostazioni in una [!DNL Target] Attività A/B?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
source-git-commit: 8682c24cf1740171dd2ce1862b3bdce1e2082869
workflow-type: tm+mt
source-wordcount: '1349'
ht-degree: 53%

---

# Obiettivi e impostazioni

Il [!UICONTROL Obiettivi e impostazioni] pagina in [!DNL Adobe Target] è dove si specificano informazioni sugli obiettivi dell’attività.

Le impostazioni disponibili dipendono dall’utilizzo di Target o [Analytics](/help/main/c-integrating-target-with-mac/a4t/a4t.md) come origine per la generazione di rapporti.

## [!UICONTROL Impostazioni attività] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Il [!UICONTROL Impostazioni delle attività] sezione del [!UICONTROL Obiettivi e impostazioni] pagina consente di configurare le seguenti opzioni:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Finalità] | Specifica una finalità facoltativa. L’obiettivo può essere qualsiasi informazione che aiuti te e i membri del tuo team a identificare l’attività. |
| [!UICONTROL Priorità] | A seconda delle impostazioni, il [!DNL Target] Interfaccia utente e opzioni per [!UICONTROL Priorità] variare. Puoi utilizzare le impostazioni legacy di [!UICONTROL Basso], [!UICONTROL Medio], o [!UICONTROL Alta], oppure puoi abilitare le priorità dettagliate da 0 a 999.<P>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<P>Se questa opzione non è abilitata in [!UICONTROL Amministrazione] (impostazione predefinita), specifica una priorità: [!UICONTROL Basso], [!UICONTROL Medio], o [!UICONTROL Alta].<P>Per abilitare [priorità precise](/help/main/administrating-target/reporting.md), fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Generazione rapporti], quindi attiva/disattiva [!UICONTROL Abilita priorità precise] nella posizione &quot;On&quot;. <P>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999: 0 = [!UICONTROL Basso] e 999 = [!UICONTROL Alta]. <P>Per le attività create con le versioni precedenti di [!DNL Target], [!UICONTROL Basso] la priorità è convertita in 0, [!UICONTROL Medio] è convertito in 5, e [!UICONTROL Alta] viene convertito in 10. Se necessario, è possibile modificare questi valori.<P>Nota: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
| Durata | L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser. |

## [!UICONTROL Impostazioni reporting] {#section_13119392051044FBA6387D9B3B1C43CF}

Il [!UICONTROL Impostazioni di reporting] sezione del [!UICONTROL Obiettivi e impostazioni] pagina consente di configurare le seguenti opzioni:

| Impostazioni | Descrizione |
|--- |--- |
| [!UICONTROL Origine per i rapporti] | Specifica se i dati vengono raccolti da [!DNL Adobe Target] o da [!DNL Adobe Analytics]. Consulta [Adobe Analytics come origine per la generazione di rapporti per Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna. Durante la selezione [!DNL Analytics] come origine di reporting per [!DNL Target], si seleziona un [!DNL Analytics] suite di rapporti da ricevere [!DNL Target] dati attività.<P>Per specificare un&#39;origine per la generazione di rapporti, scegliere una delle opzioni disponibili [!DNL Analytics] aziende a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l’attività. Solo le suite di rapporti per le quali è stato eseguito il provisioning [!DNL Adobe Target] sono disponibili per la selezione. Se non trovi le suite di rapporti previste, disconnettiti e accedi di nuovo al [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.<P>Se un’origine per la generazione di rapporti è specificata nelle impostazioni del tuo account, viene utilizzata l’origine specificata e questa impostazione non è visibile.<P>Nota: al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva. |
| [!UICONTROL Metrica per obiettivo] | Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli un [!UICONTROL Conversione] metrica, quindi imposta i parametri che determinano quando viene raggiunto il successo. Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<P>Nota: se la soluzione di reporting è impostata su [!DNL Analytics], l’unica metrica di obiettivo disponibile è [!UICONTROL Conversione]. [!DNL Analytics]Le metriche di non possono essere selezionate come obiettivo. Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.<P>Se l&#39;opzione è abilitata, [!UICONTROL Valore stimato della conversione] (non disponibile per il [!UICONTROL Punteggio pagina] metriche) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Ricavo per visitatore], [!UICONTROL Valore medio ordine], [!UICONTROL Vendite totali], e [!UICONTROL Ordini]), la stima utilizza [!UICONTROL Ricavo per visitatore]. I dati sono di tipo valuta.<P>Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Questo comportamento è diverso da quello predefinito in [!DNL Target Classic], che conta i visitatori come nuovi se visualizzano nuovamente l’attività. |
| [!UICONTROL Altre metriche] | Consente di creare metriche di successo aggiuntive. Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, le metriche definite per [!DNL Analytics] suite di rapporti. |
| [!UICONTROL Tipi di pubblico per i rapporti] | Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per mostrare informazioni solo su tipi di pubblico specifici. Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per [!DNL Analytics] suite di rapporti applicata. |

## Impostazioni avanzate  {#section_E2FE441AFB324E498793ABB025ED9974}

Il [!UICONTROL Impostazioni avanzate] sezione del [!UICONTROL Obiettivi e impostazioni] pagina consente di configurare le seguenti opzioni:

Per specificare le impostazioni avanzate, fare clic su **[!UICONTROL Altro]** (puntini di sospensione verticali), quindi fai clic su **[!UICONTROL Impostazioni avanzate]**, come illustrato nella figura seguente.

![Menu Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

![Impostazioni avanzate](/help/main/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Impostazione | Descrizione |
|--- |--- |
| [!UICONTROL Quali sono le metriche di successo da raggiungere prima di incrementare questa metrica?] | Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di attività potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione. È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. L’opzione [!UICONTROL Aggiungi dipendenza] consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno. Per aggiungere una dipendenza:<ul><li>Dopo aver aggiunto le metriche aggiuntive, fai clic su [!UICONTROL Impostazioni avanzate].</li><li>Fai clic sull’opzione [!UICONTROL Aggiungi dipendenza]:</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su [!UICONTROL Raggiunto] per scegliere tra [!UICONTROL Raggiunto] e [!UICONTROL Non raggiunto].</li><li>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.</li></ul> |
| [!UICONTROL Cosa accade dopo che un utente incontra questa metrica per obiettivo?] | Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:<ul><li>Seleziona [!UICONTROL Incrementa il conteggio e mantieni utente attivo] per specificare la modalità di incremento del conteggio.</li><li>Seleziona [!UICONTROL Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso] per specificare l’esperienza che l’utente vedrà se accede di nuovo all’attività.</li><li>Seleziona [!UICONTROL Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso] per specificare cosa vedrà l’utente al posto del contenuto dell’attività.</li></ul> |
| [!UICONTROL Come verrà incrementato il conteggio?] | Sono disponibili tre opzioni per l’incremento del conteggio:<ul><li>[!UICONTROL Una volta per partecipante]</li><li>[!UICONTROL A ogni impression (esclusi aggiornamenti pagina)]</li><li>[!UICONTROL A ogni impression]</li></ul> |

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

Il [!UICONTROL Altri metadati] sezione del [!UICONTROL Obiettivi e impostazioni] Questa pagina consente di specificare tutte le informazioni sull’attività, utili per te o per altri membri del gruppo. Il riquadro Note può essere ridimensionato.|

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
