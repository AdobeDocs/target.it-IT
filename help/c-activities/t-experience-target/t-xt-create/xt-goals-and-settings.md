---
keywords: impostazioni attività;obiettivi e impostazioni di targeting esperienza;obiettivi e impostazioni XT;targeting esperienza;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo primario;metriche aggiuntive;finalità;priorità;durata;soluzione di reporting;obiettivo;pubblico per il reporting;quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;cosa succede dopo che un utente trova questa metrica di obiettivo;note
description: Scopri come utilizzare la pagina Goals and Settings (Obiettivi e impostazioni) in  Adobe Target per specificare le informazioni sugli obiettivi di un'attività Experience Targeting (XT).
title: Come si specificano gli obiettivi e le impostazioni in un'attività di targeting delle esperienze?
feature: Experience Targeting
translation-type: tm+mt
source-git-commit: bb27f6e540998f7dbe7642551f7a5013f2fd25b4
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 93%

---


# Obiettivi e impostazioni nelle attività Experience Targeting (XT)

Nella pagina Obiettivi e impostazioni è possibile inserire le informazioni sugli obiettivi del test.

* Impostazioni attività
* Impostazioni reporting
* Altri metadati

Le impostazioni disponibili dipendono dall’utilizzo di [!DNL Target] o [!DNL Analytics] come origine di dati.

![Pagina Impostazioni attività](/help/c-activities/t-experience-target/t-xt-create/assets/ab_settings-new.png)

## Impostazioni delle attività {#section_DCBDC354261F420EBD4B43EA34947BAC}

Sono disponibili le seguenti opzioni

### Finalità

Specifica una finalità facoltativa. La finalità può essere costituita da qualsiasi informazione che consenta a te e agli altri membri del gruppo di identificare la campagna.

### Priorità

L’interfaccia utente e le opzioni per Priorità variano a seconda delle impostazioni. È possibile utilizzare le impostazioni legacy Bassa, Media o Alta, oppure attivare la priorità precisa da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

Se questa opzione non è abilitata in Amministrazione (impostazione predefinita), specificate una priorità: Bassa, Media o Alta.

Per abilitare le priorità con granulosità fine, fare clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Reporting]**, quindi attivare l&#39;opzione Attiva priorità con granulosità fine nella posizione &quot;Attiva&quot;.

Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

* 0 = Bassa
* 999 = Alta

Per le attività create con le versioni precedenti di Target Standard/Premium, la priorità Bassa viene convertita in 0, la priorità Media in 5 e la priorità Alta in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

### Durata

L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## Impostazioni reporting {#section_13119392051044FBA6387D9B3B1C43CF}

Sono disponibili le seguenti opzioni:

### Soluzione di reporting

Specifica se i dati vengono raccolti da Adobe Target o da Adobe Analytics. Consulta [Adobe Analytics come origine per la generazione di rapporti per Target](/help/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna.

Quando si seleziona Analytics come origine per la generazione di rapporti per Target, si seleziona la suite di rapporti di Analytics che dovrà ricevere i dati relativi all’attività di Target. Scegli innanzitutto una delle società Analytics associate al tuo account, quindi, seleziona la suite di rapporti idonea all’attività. Puoi selezionare solo le suite di rapporti impostate per la connessione ad Adobe Target. Se non visualizzi la suite di rapporti desiderata, disconnettiti, accedi di nuovo ad Adobe Experience Cloud e riprova. Se la suite di rapporti continua a non essere elencata, contatta l’Assistenza clienti.

Analytics for Target richiede un server di tracciamento per riportare correttamente i risultati. Un server di tracciamento predefinito verrà visualizzato nel campo Server di tracciamento. Se si utilizzano più server di tracciamento, è necessario verificare di aver inserito in questo campo quello corretto. Consulta [Utilizzo di un server di tracciamento di Analytics](/help/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823) per ulteriori informazioni.

Se una soluzione di reporting è specificata nelle impostazioni del tuo account, viene utilizzata tale soluzione e questa impostazione non è visibile.

>[!NOTE]
>
>Al fine di mantenere coerenza dei rapporti, non è possibile cambiare l’origine per i rapporti una volta che l’attività è diventata attiva.

### Metrica per obiettivo

Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica di conversione, quindi imposta i parametri che determinano il raggiungimento del successo.

Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Se la soluzione di reporting è impostata su Analytics, l’unica metrica di obiettivo disponibile è Conversione. Le metriche di Analytics non possono essere selezionate come obiettivo.

Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.

Se attivato, il campo del Valore stimato di una conversione (non disponibile per la metrica Punteggio di pagina) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a Target di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche collegate ai ricavi (Ricavo per visitatore, Valore ordine medio, Vendite totali e Ordini), la stima utilizza Ricavo per visitatore. I dati sono di tipo valuta.

Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità maggiore. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Nota: questo è diverso dal comportamento predefinito in Target Classic, in cui i visitatori sono conteggiati come nuovi se vedono il test di nuovo.

### Altre metriche

Consente di creare metriche di successo aggiuntive.

Questa impostazione non è disponibile se la soluzione di reporting è impostata su Analytics. In questo caso, si applicano le metriche definite per la suite di rapporti di Analytics.

### Tipi di pubblico per i rapporti

Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per visualizzare solo le informazioni su tipi di pubblico specifici.

Questa impostazione non è disponibile se si sceglie Analytics come soluzione di reporting. Vengono applicati i tipi di pubblico definiti per la suite di rapporti di Analytics.

## Altri metadati

Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro Note può essere ridimensionato.

## Impostazioni avanzate {#section_E2FE441AFB324E498793ABB025ED9974}

Per le metriche dell’obiettivo di Targeting esperienza sono disponibili impostazioni avanzate.

![Impostazioni avanzate](/help/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Se utilizzi Adobe Analytics come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server Analytics. L’opzione Impostazioni avanzate non sarà disponibile.

Sono disponibili le seguenti opzioni:

### Quali sono le metriche di successo da raggiungere prima di incrementare questa metrica?

Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio una conversione di test potrebbe risultare valida solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

È possibile fornire una dipendenza da più metriche e decidere se, per incrementare il conteggio, la metrica deve essere raggiunta o non raggiunta.

È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.

L’opzione Aggiungi dipendenza consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto le metriche aggiuntive, fai clic su **[!UICONTROL Impostazioni avanzate]**.
2. Fai clic su **[!UICONTROL Aggiungi dipendenza]**:

   ![Collegamento Aggiungi dipendenza](/help/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su Raggiunto per scegliere tra Raggiunto e Non raggiunto.

   ![Finestra di dialogo Aggiungi dipendenza metrica](/help/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo?

Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:

* Seleziona Incrementa il conteggio e mantieni utente attivo per specificare la modalità di incremento del conteggio.
* Seleziona Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso per specificare l’esperienza che l’utente vedrà se accede di nuovo all’attività.
* Seleziona Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso per specificare cosa vedrà l’utente al posto del contenuto dell’attività.

Consulta [Metriche di successo](/help/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Video di formazione: Impostazioni attività (03:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)