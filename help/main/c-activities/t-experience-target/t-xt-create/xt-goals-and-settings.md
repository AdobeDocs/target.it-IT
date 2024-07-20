---
keywords: impostazioni attività;obiettivi e impostazioni di targeting esperienza;obiettivi e impostazioni XT;targeting esperienza;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo primario;metriche aggiuntive;finalità;priorità;durata;soluzione di reporting;obiettivo;pubblico per il reporting;quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;cosa succede dopo che un utente trova questa metrica di obiettivo;note
description: Scopri come utilizzare la pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] per specificare informazioni sugli obiettivi di un'attività [!UICONTROL Experience Targeting] (XT).
title: Come si specifica [!UICONTROL Goals & Settings] in un'attività [!UICONTROL Experience Targeting]?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 39%

---

# Obiettivi e impostazioni nelle attività [!UICONTROL Experience Targeting] (XT)

Nella pagina [!UICONTROL Goals & Settings] è possibile immettere informazioni sugli obiettivi del test:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

Le impostazioni disponibili dipendono dall&#39;utilizzo di [!DNL Target] o [!DNL Analytics] come origine per la generazione di rapporti.

## [!UICONTROL Activity Settings] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Objective]

Specifica una finalità facoltativa. La finalità può essere costituita da qualsiasi informazione che consenta a te e agli altri membri del gruppo di identificare la campagna.

### [!UICONTROL Priority]

A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priority] variano. È possibile utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High] oppure abilitare le priorità precise da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività sono assegnate alla posizione, viene visualizzata l’attività con la priorità più elevata.

Se questa opzione non è abilitata in [!UICONTROL Administration] (impostazione predefinita), specificare una priorità: [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High].

Per abilitare le priorità dettagliate, fare clic su **[!UICONTROL Administration]** > **[!UICONTROL Reporting]**, quindi attivare l&#39;opzione [!UICONTROL Enable Fine-Grained Priorities].

Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

* 0 = Bassa
* 999 = Alta

Per le attività create con le versioni precedenti di [!DNL Target], la priorità [!UICONTROL Low] viene convertita in 0, [!UICONTROL Medium] in 5 e [!UICONTROL High] in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

### [!UICONTROL Duration]

L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Allo stesso modo, l’attività può terminare quando viene disattivata oppure puoi impostare una data e un’ora di fine. Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## [!UICONTROL Reporting Settings] {#section_13119392051044FBA6387D9B3B1C43CF}

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Reporting Source]

Specifica da quali dati della soluzione vengono raccolti:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Se una soluzione di reporting è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata la soluzione specificata e questa impostazione non è visibile.

Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.

**[!DNL Adobe Analytics]**: consulta [[!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per informazioni sulle differenze tra le soluzioni per la generazione di rapporti e i vantaggi di ciascuna.

Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T), selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target]. Scegli innanzitutto una delle [!DNL Analytics] società a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Target]. Se la suite di rapporti prevista non è visibile, disconnettersi e accedere nuovamente a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell&#39;elenco, contatta l&#39;[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Nel campo [!UICONTROL Tracking Server] viene visualizzato un server di tracciamento predefinito. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Per ulteriori informazioni, vedere [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

**[!DNL Adobe Customer Journey Analytics]**: vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].

### [!UICONTROL Goal Metric]

Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversion], quindi imposta i parametri che determinano quando viene raggiunto il successo.

Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è [!UICONTROL Conversion]. Impossibile selezionare [!DNL Analytics] metriche come obiettivo.

Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.

Se attivato, il campo [!UICONTROL Estimated Value of the Conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. I dati sono di tipo valuta.

Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Questo comportamento è diverso da quello predefinito in [!DNL Target Classic], che ha conteggiato i visitatori come nuovi se visualizzassero nuovamente il test.

### [!UICONTROL Additional Metrics]

Consente di creare metriche di successo aggiuntive.

Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics].

### [!UICONTROL Audiences for Reporting]

Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per visualizzare solo le informazioni su tipi di pubblico specifici.

Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per la suite di rapporti [!DNL Analytics] è applicato.

## [!UICONTROL Other Meta Data]

Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro [!UICONTROL Notes] è ridimensionabile.

## [!UICONTROL Advanced Settings] {#section_E2FE441AFB324E498793ABB025ED9974}

Le impostazioni avanzate sono disponibili per [!UICONTROL Experience Targeting] metriche obiettivo.

![Impostazioni avanzate](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. Opzione [!UICONTROL Advanced Settings] non disponibile.

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Which success metric must be reached before incrementing this metric?]

Utilizza questa opzione per contare solo i visitatori che raggiungono la metrica di successo se in precedenza avevano raggiunto una metrica di successo diversa. Ad esempio, una conversione di test potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.

È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.

L&#39;opzione [!UICONTROL Add Dependency] consente di incrementare la metrica di successo nel caso in cui un&#39;altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto ulteriori metriche, fare clic su **[!UICONTROL Advanced Settings]**.
2. Fare clic su **[!UICONTROL Add Dependency]**:

   ![Collegamento Aggiungi dipendenza](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su **[!UICONTROL Reached]** per scegliere tra [!UICONTROL Reached] e [!UICONTROL Not Reached].

   ![Finestra di dialogo Aggiungi dipendenza metrica](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

### [!UICONTROL What will happen after a user encounters this goal metric?]

Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:

* Selezionare [!UICONTROL Increment Count & Keep User in Activity] per specificare la modalità di incremento del conteggio.
* Seleziona [!UICONTROL Increment Count, Release User & Allow Reentry] per specificare l&#39;esperienza che l&#39;utente vedrà se accede nuovamente all&#39;attività.
* Seleziona [!UICONTROL Increment Count, Release User & Bar from Reentry] per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Video di formazione: Impostazioni attività (03:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
