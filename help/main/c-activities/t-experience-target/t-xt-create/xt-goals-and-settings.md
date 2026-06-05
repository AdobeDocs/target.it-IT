---
keywords: impostazioni attività;obiettivi e impostazioni di targeting esperienza;obiettivi e impostazioni XT;targeting esperienza;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo primario;metriche aggiuntive;finalità;priorità;durata;soluzione di reporting;obiettivo;pubblico per il reporting;quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;cosa succede dopo che un utente trova questa metrica di obiettivo;note
description: Scopri come utilizzare la pagina [!UICONTROL Obiettivi e impostazioni] in [!DNL Adobe Target] per specificare informazioni sugli obiettivi di un'attività [!UICONTROL Targeting esperienza] (XT).
title: Come posso specificare [!UICONTROL Obiettivi e impostazioni] in un'attività [!UICONTROL Targeting esperienza]?
feature: Experience Targeting
exl-id: 80cb7eff-4e9c-43d7-a3d8-7a9de79c91b9
TQID: https://experienceleague.adobe.com/vlpJSJ4Z6mxQI-D8UyUPEXHVWKfR54l89uoxULd2oD0
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 51d3993ca3daaae824b9c598529ff4038fdcdb77
workflow-type: tm+mt
source-wordcount: 1285
ht-degree: 41%

---

# Obiettivi e impostazioni nelle [!UICONTROL attività Targeting esperienza] (XT)

Nella pagina [!UICONTROL Obiettivi e impostazioni] è possibile immettere informazioni sugli obiettivi del test:

* [!UICONTROL Impostazioni attività]
* [!UICONTROL Impostazioni reporting]
* [!UICONTROL Altri metadati]

Le impostazioni disponibili dipendono dall&#39;utilizzo di [!DNL Target] o [!DNL Analytics] come origine per la generazione di rapporti.

## [!UICONTROL Impostazioni attività] {#section_DCBDC354261F420EBD4B43EA34947BAC}

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Obiettivo]

Specifica una finalità facoltativa. La finalità può essere costituita da qualsiasi informazione che consenta a te e agli altri membri del gruppo di identificare la campagna.

### [!UICONTROL Priorità]

A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priorità] variano. Puoi utilizzare le impostazioni legacy di [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta] oppure abilitare le priorità precise da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività sono assegnate alla posizione, viene visualizzata l’attività con la priorità più elevata.

Se questa opzione non è abilitata in [!UICONTROL Amministrazione] (impostazione predefinita), specificare una priorità: [!UICONTROL Bassa], [!UICONTROL Medium] o [!UICONTROL Alta].

Per abilitare le priorità dettagliate, fai clic su **[!UICONTROL Amministrazione]** > **[!UICONTROL Generazione rapporti]**, quindi attiva l&#39;opzione [!UICONTROL Abilita priorità precise].

Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

* 0 = Bassa
* 999 = Alta

Per le attività create con le versioni precedenti di [!DNL Target], la priorità [!UICONTROL Bassa] viene convertita in 0, [!UICONTROL Medium] in 5 e la priorità [!UICONTROL Alta] in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

### [!UICONTROL Durata]

L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Allo stesso modo, l’attività può terminare quando viene disattivata oppure puoi impostare una data e un’ora di fine. Il selettore dell&#39;ora utilizza un orologio di 24 ore, dove 00:00 corrisponde a mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## [!UICONTROL Impostazioni reporting] {#section_13119392051044FBA6387D9B3B1C43CF}

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Reporting di Source]

Specifica da quali dati della soluzione vengono raccolti:

* [!DNL Adobe Target]
* [!DNL Adobe Analytics]
* [!DNL Adobe Customer Journey Analytics]

Se una soluzione di reporting è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata la soluzione specificata e questa impostazione non è visibile.

Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.

**[!DNL Adobe Analytics]**: consulta [[!DNL Adobe Analytics] come origine per la generazione di rapporti per [!DNL Target]](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per informazioni sulle differenze tra le soluzioni per la generazione di rapporti e i vantaggi di ciascuna.

Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target] (A4T), selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target]. Scegli innanzitutto una delle [!DNL Analytics] società a cui è associato il tuo account, quindi seleziona la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Target]. Se la suite di rapporti prevista non è visibile, disconnettersi e accedere nuovamente a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell&#39;elenco, contatta l&#39;[Assistenza clienti](/help/main/cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C).

[!DNL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Nel campo [!UICONTROL Server di monitoraggio] viene visualizzato un server di monitoraggio predefinito. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Per ulteriori informazioni, vedere [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).

**[!DNL Adobe Customer Journey Analytics]**: vedere [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per ulteriori informazioni sull&#39;integrazione tra [!DNL Adobe Customer Journey Analytics] e [!DNL Target].

### [!UICONTROL Metrica per obiettivo]

Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversione], quindi imposta i parametri che determinano quando viene raggiunto il successo.

Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md#task_A04AB66007C1467DA1C21A519A5C7BEB).

>[!NOTE]
>
>Se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è [!UICONTROL Conversione]. Impossibile selezionare [!DNL Analytics] metriche come obiettivo.

Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.

Se attivato, il campo [!UICONTROL Valore stimato della conversione] (non disponibile per le metriche [!UICONTROL Punteggio di pagina]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche relative ai ricavi ([!UICONTROL Ricavi per visitatore], [!UICONTROL Valore medio ordine], [!UICONTROL Vendite totali] e [!UICONTROL Ordini]), la stima utilizza [!UICONTROL Ricavi per visitatore]. Il tipo di dati è valuta.

Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Questo comportamento è diverso da quello predefinito in [!DNL Target Classic], che ha conteggiato i visitatori come nuovi se visualizzassero nuovamente il test.

### [!UICONTROL Altre metriche]

Consente di creare metriche di successo aggiuntive.

Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics].

### [!UICONTROL Tipi di pubblico per reporting]

Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per visualizzare solo le informazioni su tipi di pubblico specifici.

Questa impostazione non è disponibile se si sceglie [!DNL Analytics] come soluzione di reporting. Il pubblico definito per la suite di rapporti [!DNL Analytics] è applicato.

## [!UICONTROL Altri dati Meta]

Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro [!UICONTROL Notes] è ridimensionabile.

## [!UICONTROL Impostazioni avanzate] {#section_E2FE441AFB324E498793ABB025ED9974}

Le impostazioni avanzate sono disponibili per [!UICONTROL Metriche obiettivo di Targeting esperienza].

![Impostazioni avanzate](/help/main/c-activities/t-experience-target/t-xt-create/assets/Menu_AdvancedSettings-new.png)

>[!NOTE]
>
>Se utilizzi [!DNL Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. Opzione [!UICONTROL Impostazioni avanzate] non disponibile.

Sono disponibili le seguenti impostazioni:

### [!UICONTROL Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica?]

Utilizza questa opzione per contare solo i visitatori che raggiungono la metrica di successo se in precedenza avevano raggiunto una metrica di successo diversa. Ad esempio, una conversione di test potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.

È necessario definire entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.

L’opzione [!UICONTROL Aggiungi dipendenza] consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto le metriche aggiuntive, fai clic su **[!UICONTROL Impostazioni avanzate]**.
2. Fai clic su **[!UICONTROL Aggiungi dipendenza]**:

   ![Collegamento Aggiungi dipendenza](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency-new.png)

3. Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su **[!UICONTROL Raggiunto]** per scegliere tra [!UICONTROL Raggiunto] e [!UICONTROL Non raggiunto].

   ![Finestra di dialogo Aggiungi dipendenza metrica](/help/main/c-activities/t-experience-target/t-xt-create/assets/add_dependency_reached-new.png)

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

### [!UICONTROL Cosa succede quando un utente incontra questa metrica per obiettivo?]

Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:

* Seleziona [!UICONTROL Incrementa il conteggio e mantieni utente attivo] per specificare la modalità di incremento del conteggio.
* Seleziona [!UICONTROL Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso] per specificare l’esperienza che l’utente vedrà se accede di nuovo all’attività.
* Seleziona [!UICONTROL Incrementa il conteggio, rilascia l&#39;utente e impedisci nuovo accesso] per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Video di formazione: Impostazioni attività (3:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)
