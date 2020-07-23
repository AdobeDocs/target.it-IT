---
keywords: activity settings;A/B goals and settings;reporting settings;goal metrics;success metrics;dependent success metrics;advanced settings;primary goal;additional metrics;objective;priority;duration;reporting solution;goal;audiences for reporting;Which success metric must be reached before incrementing this metric;What will happen after a user encounters this goal metric;notes
description: Nella pagina Obiettivi e impostazioni è possibile inserire le informazioni sugli obiettivi del test.
title: Obiettivi e impostazioni
uuid: 46d02e39-0c19-4da8-bdd8-48acb708831b
snippet: y
translation-type: tm+mt
source-git-commit: 3edb13b196240bb1918fc66edcc653936e32d3ef
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 96%

---


# Obiettivi e impostazioni {#goals-and-settings}

Nella pagina Obiettivi e impostazioni è possibile inserire le informazioni sugli obiettivi del test.

Le impostazioni disponibili dipendono dall’utilizzo di Target o [Analytics](/help/c-integrating-target-with-mac/a4t/a4t.md) come origine di dati.

![Finestra di dialogo Impostazioni attività](/help/c-activities/t-test-ab/t-test-create-ab/assets/ab_settings-new.png)

## Impostazioni delle attività {#section_DCBDC354261F420EBD4B43EA34947BAC}

| Impostazioni | Descrizione |
|--- |--- |
| Finalità | Specifica una finalità facoltativa. La finalità può essere costituita da qualsiasi informazione che consenta a te e agli altri membri del gruppo di identificare la campagna. |
| Priorità | L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.<br>La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.<br>Se questa opzione non è abilitata in [!UICONTROL Amministrazione] (impostazione predefinita), specificate una priorità: Bassa, Media o Alta. <br>Per abilitare le priorità con granulometria fine, fai clic su [!UICONTROL Amministrazione] > [!UICONTROL Reporting (Generazione rapporti]), quindi seleziona l’opzione Attiva priorità con granulosità fine nella posizione &quot;Attiva&quot;. <br>Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999: 0 = bassa e 999 = alta. <br>Per le attività create con le versioni precedenti di Target Standard/Premium, la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.<br>Nota: prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10. |
| Durata | L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser. |

## Impostazioni reporting {#section_13119392051044FBA6387D9B3B1C43CF}

| Impostazioni | Descrizione |
|--- |--- |
| Origine per i rapporti | Specifica se i dati vengono raccolti da Adobe Target o da Adobe Analytics. Consulta [Adobe Analytics come origine per la generazione di rapporti per Target](/help/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna.  Quando si seleziona Analytics come origine per la generazione di rapporti per Target, si seleziona la suite di rapporti di Analytics che dovrà ricevere i dati relativi all’attività di Target.<br>Scegli innanzitutto una delle società Analytics associate al tuo account, quindi, seleziona la suite di rapporti idonea all’attività. Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova. Se la suite di rapporti continua a non essere elencata, contatta l’Assistenza clienti.<br>Se un’origine per la generazione di rapporti è specificata nelle impostazioni del tuo account, viene utilizzata l’origine specificata e questa impostazione non è visibile.<br>Nota: al fine di mantenere coerenza dei rapporti, non è possibile cambiare l’origine per i rapporti una volta che l’attività è diventata attiva. |
| Obiettivo | Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica di conversione, quindi imposta i parametri che determinano il raggiungimento del successo.  Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](../../../c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).<br>Nota: se la soluzione di reporting è impostata su Analytics, l’unica metrica di obiettivo disponibile è Conversione. Le metriche di Analytics non possono essere selezionate come obiettivo.   Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.<br>Se attivato, il campo del Valore stimato di una conversione (non disponibile per la metrica Punteggio di pagina) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a Target di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche collegate ai ricavi (Ricavo per visitatore, Valore ordine medio, Vendite totali e Ordini), la stima utilizza Ricavo per visitatore. I dati sono di tipo valuta.<br>Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità maggiore. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Nota: questo è diverso dal comportamento predefinito in Target Classic, in cui i visitatori sono conteggiati come nuovi se vedono il test di nuovo. |
| Altre metriche | Consente di creare metriche di successo aggiuntive.  Questa impostazione non è disponibile se la soluzione di reporting è impostata su Analytics. In questo caso, si applicano le metriche definite per la suite di rapporti di Analytics. |
| Tipi di pubblico per i rapporti | Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per visualizzare solo le informazioni su tipi di pubblico specifici.  Questa impostazione non è disponibile se si sceglie Analytics come soluzione di reporting. Vengono applicati i tipi di pubblico definiti per la suite di rapporti di Analytics. |

## Impostazioni avanzate {#section_E2FE441AFB324E498793ABB025ED9974}

Per le metriche dell’obiettivo di Test A/B sono disponibili impostazioni avanzate.

![Menu Impostazioni avanzate](/help/c-activities/t-test-ab/t-test-create-ab/assets/menu-advanced-settings-new.png)

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server Analytics. L’opzione Impostazioni avanzate non sarà disponibile.

![Impostazioni avanzate](/help/c-activities/t-test-ab/t-test-create-ab/assets/advanced-settings.png)

| Impostazione | Descrizione |
|--- |--- |
| Quali sono le metriche di successo da raggiungere prima di incrementare questa metrica? | Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.  È possibile fornire una dipendenza da più metriche e decidere se, per incrementare il conteggio, la metrica deve essere raggiunta o non raggiunta.  È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.  L’opzione Aggiungi dipendenza consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.  Per aggiungere una dipendenza:<ul><li>Dopo aver aggiunto le metriche aggiuntive, fai clic su Impostazioni avanzate.</li><li>Fai clic sull’opzione Aggiungi dipendenza:</li><li>Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su Raggiunto per scegliere tra Raggiunto e Non raggiunto.</li><li>È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.</li></ul> |
| Cosa accade dopo che un utente incontra questa metrica per obiettivo? | Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:<ul><li>Seleziona Incrementa il conteggio e mantieni utente attivo per specificare la modalità di incremento del conteggio.</li><li>Seleziona Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso per specificare l’esperienza che l’utente vedrà se accede di nuovo all’attività.</li><li>Seleziona Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso per specificare cosa vedrà l’utente al posto del contenuto dell’attività.</li></ul> |
| Come verrà incrementato il conteggio? | Sono disponibili tre opzioni per l’incremento del conteggio:<ul><li>Una volta per partecipante</li><li>A ogni impression (esclusi aggiornamenti pagina)</li><li>A ogni impression</li></ul> |

Consulta [Metriche di successo](../../../c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

| Impostazioni | Descrizione |
|---|---|
| Note | Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro Note può essere ridimensionato. |

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Etichetta ![Esercitazione impostazioni attività (3:02)](/help/assets/tutorial.png)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

(https://video.tv.adobe.com/v/17381?captions=ita)

### Creazione di un contrassegno ![Esercitazione per test A/B (8:36)](/help/assets/tutorial.png)

Questo video mostra le impostazioni di attività nel flusso di lavoro guidato in tre passaggi durante la creazione di un’attività. Obiettivi e impostazioni sono trattati a partire dal minuto 5:30.

* Creare un’attività A/B in Adobe Target
* Allocare il traffico con suddivisione manuale o automatica del traffico

>[!VIDEO](https://video.tv.adobe.com/v/17391)
