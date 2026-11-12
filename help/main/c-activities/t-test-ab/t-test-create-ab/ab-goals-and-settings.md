---
keywords: impostazioni attività;obiettivi e impostazioni A/B;impostazioni di reporting;metriche obiettivo;metriche di successo;metriche di successo dipendenti;impostazioni avanzate;obiettivo principale;metriche aggiuntive;obiettivo;priorità;durata;soluzione di reporting;obiettivo;pubblico per rapporti;Quale metrica di successo deve essere raggiunta prima di incrementare questa metrica;Cosa succede dopo che un utente ha individuato questa metrica obiettivo;note
description: Scopri come utilizzare la pagina [!UICONTROL Obiettivi e impostazioni] per definire gli obiettivi dell'attività A/B.
title: Come si specificano obiettivi e impostazioni in un'attività A/B [!DNL Target]?
feature: A/B Tests
exl-id: 6c970289-a897-46bc-a8d2-ba8c045abe12
TQID: 'https://experienceleague.adobe.com/X3JDvfXDHM2rAOodEY5N9TVO-tBpz4vNDUvhOpC0XZ4'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: adee20bd-51f4-461d-b9db-d215f8756eeb
    internal-label: Audiences
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ab2570eb-4844-49aa-8334-e91a345525e5
    internal-label: A/B Tests
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: abab6b3e464bb9f294e9c3c455dca1f57bb0d458
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 24%
---
# Obiettivi e impostazioni {#ab-goals-and-settings}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri cosa è possibile impostare nella pagina **[!UICONTROL Obiettivi e impostazioni]** di un&#39;attività A/B, Targeting esperienza (XT) o Test multivariato (MVT): le impostazioni dell&#39;attività, le impostazioni del reporting, le impostazioni avanzate e le note.

>[!ENDSHADEBOX]

Nella pagina **[!UICONTROL Obiettivi e impostazioni]** di [!DNL Adobe Target] è possibile specificare informazioni sugli obiettivi dell&#39;attività.

Le impostazioni disponibili dipendono dall&#39;utilizzo di Target o [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

Le stesse impostazioni si applicano alle attività [!UICONTROL Targeting esperienza] (XT) e [!UICONTROL Test multivariato] (MVT), ad eccezione di [Metodologia statistica](#section_statistical-methodology), che è disponibile solo per le attività A/B.

* [Impostazioni attività](#section_DCBDC354261F420EBD4B43EA34947BAC): finalità, priorità e durata
* [Impostazioni reporting](#section_13119392051044FBA6387D9B3B1C43CF): origine per la generazione di rapporti, metrica obiettivo, metriche aggiuntive e pubblico
* [Impostazioni avanzate](#section_E2FE441AFB324E498793ABB025ED9974): dipendenze e cosa accade dopo che un visitatore ha raggiunto l&#39;obiettivo
* [Metodologia statistica](#section_statistical-methodology): analisi dei risultati
* [Altri metadati](#section_2E8917BEFB954480A4206B9E9E917F80): note

## [!UICONTROL Impostazioni attività] {#section_DCBDC354261F420EBD4B43EA34947BAC}

La sezione **[!UICONTROL Impostazioni attività]** della pagina **[!UICONTROL Obiettivi e impostazioni]** consente di configurare le opzioni seguenti.

![](../../assets/goals-ab-1.png)

### Finalità {#objective}

Specifica una finalità facoltativa. L’obiettivo può essere qualsiasi informazione che aiuti te e i membri del tuo team a identificare l’attività.

### Priorità {#priority}

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per **[!UICONTROL Priorità]** variano:

* **Priorità legacy (predefinita):** Se questa opzione non è abilitata in **[!UICONTROL Amministrazione]** (predefinita), specifica una priorità di **[!UICONTROL Bassa]**, **[!UICONTROL Medium]** o **[!UICONTROL Alta]**.
* **Priorità precise:** Specificare un valore compreso tra 0 e 999, dove 0 = **[!UICONTROL Bassa]** e 999 = **[!UICONTROL Alta]**.

  Per abilitare [priorità precise](/help/main/administrating-target/reporting.md), accedi a **[!UICONTROL Amministrazione]** > **[!UICONTROL Generazione rapporti]**, quindi attiva l&#39;opzione **[!UICONTROL Abilita priorità precise]**.

Per le attività create con le versioni precedenti di [!DNL Target], la priorità **[!UICONTROL Bassa]** viene convertita in 0, **[!UICONTROL Medium]** in 5 e la priorità **[!UICONTROL Alta]** in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare le priorità dettagliate dopo averle utilizzate, tutte le priorità devono essere impostate su 0, 5 o 10.

### Durata {#duration}

L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche.

Il selettore dell’ora è nel formato 24 ore e la mezzanotte è indicata come 00:00. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## [!UICONTROL Impostazioni reporting] {#section_13119392051044FBA6387D9B3B1C43CF}

La sezione **[!UICONTROL Impostazioni reporting]** della pagina **[!UICONTROL Obiettivi e impostazioni]** consente di configurare le opzioni seguenti.

![](../../assets/goals-ab-2.png)

### Origine per i rapporti {#reporting-source}

Specifica da quali dati della soluzione vengono raccolti:

* [!DNL Adobe Target]

* [!DNL Adobe Analytics]

  +++ Ulteriori informazioni su Analytics come origine per la generazione di rapporti

  Consulta [Adobe Analytics come origine per la generazione di rapporti per Target](/help/main/c-integrating-target-with-mac/a4t/a4t.md) per scoprire le differenze tra le soluzioni di reporting e i vantaggi di ciascuna. Quando selezioni [!DNL Analytics] come origine per la generazione di rapporti per [!DNL Target], selezioni una suite di rapporti [!DNL Analytics] per ricevere i dati dell&#39;attività [!DNL Target].

  Per specificare un&#39;origine per la generazione di rapporti, scegliere innanzitutto una delle [!DNL Analytics] società associate al proprio account, quindi selezionare la suite di rapporti appropriata per l&#39;attività. È possibile selezionare solo le suite di rapporti predisposte per la connessione a [!DNL Adobe Target]. Se le suite di rapporti previste non sono visualizzate, disconnettersi e accedere di nuovo a [!DNL Adobe Experience Cloud] per riprovare. Se la suite di rapporti non è ancora presente nell’elenco, contatta l’Assistenza clienti.

  [!DNL Analytics for Target] (A4T) richiede un server di tracciamento per riportare correttamente i risultati. Nel campo **[!UICONTROL Server di monitoraggio]** viene visualizzato un server di monitoraggio predefinito. Se utilizzi più server di tracciamento, assicurati di includere in questo campo il server di tracciamento corretto. Per ulteriori informazioni, vedere [Utilizzo di un server di tracciamento di Analytics](/help/main/c-integrating-target-with-mac/a4t/analytics-tracking-server.md#task_72077BA7E93C4A65A715A18F32228823).
  +++

* [!DNL Adobe Customer Journey Analytics]

  +++ Ulteriori informazioni su Customer Journey Analytics come origine per la generazione di rapporti

  Consulta [[!DNL Target] creazione di rapporti in [!DNL Adobe Customer Journey Analytics]](/help/main/c-integrating-target-with-mac/cja/target-reporting-in-cja.md) per i tipi di attività supportati, selezione di sandbox e visualizzazioni dati, metriche obiettivo e impostazione di reporting in [!DNL Customer Journey Analytics].
  +++

Se un&#39;origine per la generazione di rapporti è specificata nelle [impostazioni account](/help/main/administrating-target/reporting.md), viene utilizzata l&#39;origine specificata e questa impostazione non è visibile.

Al fine di mantenere coerenza dei rapporti, non è possibile modificare l’origine per i rapporti una volta che l’attività è diventata attiva.

### Metrica per obiettivo {#goal-metric}

>[!NOTE]
>
>Se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è **[!UICONTROL Conversione]**. Impossibile selezionare [!DNL Analytics] metriche come obiettivo.

Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica **[!UICONTROL Conversione]**, quindi imposta i parametri che determinano quando viene raggiunto il successo.

Per ulteriori informazioni sull’impostazione delle metriche, consulta [Impostare le metriche](/help/main/c-activities/t-test-ab/t-test-create-ab/ab-set-metrics.md).

Per altre opzioni, fai clic sull&#39;icona **[!UICONTROL Altro]** accanto alla metrica obiettivo, quindi fai clic su **[!UICONTROL Impostazioni avanzate]**. Consulta [Impostazioni avanzate](#section_E2FE441AFB324E498793ABB025ED9974).

![](../../assets/goals-ab-3.png)

Se attivato, il campo **[!UICONTROL Valore stimato della conversione]** fornisce un valore per l&#39;obiettivo, ma non per altre metriche. A questo campo si applicano i seguenti punti:

* Il valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi.
* Il campo è facoltativo; tuttavia, i ricavi incrementali per qualsiasi metrica non relativa ai ricavi non possono essere calcolati senza di esso.
* Il campo non è disponibile per le metriche **[!UICONTROL Punteggio di pagina]**.
* Per tutte le metriche relative ai ricavi (**[!UICONTROL Ricavi per visitatore]**, **[!UICONTROL Valore medio ordine]**, **[!UICONTROL Vendite totali]** e **[!UICONTROL Ordini]**), la stima utilizza **[!UICONTROL Ricavi per visitatore]**. Il tipo di dati è valuta.

### Additional Metrics (Metriche aggiuntive) {#additional-metrics}

Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics].

### Tipi di pubblico per i rapporti {#audiences-for-reporting}

![](../../assets/goals-ab-4.png)

Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per mostrare informazioni solo su tipi di pubblico specifici.

Tieni presente che questa impostazione non è disponibile se scegli [!DNL Analytics] come soluzione per la generazione di rapporti. Il pubblico definito per la suite di rapporti [!DNL Analytics] è applicato.

## Impostazioni avanzate {#section_E2FE441AFB324E498793ABB025ED9974}

La sezione **[!UICONTROL Impostazioni avanzate]** della pagina **[!UICONTROL Obiettivi e impostazioni]** consente di configurare le opzioni avanzate.

Per specificare le impostazioni avanzate, fai clic sull&#39;icona **[!UICONTROL Altro]** ( ![Altro icona](/help/main/assets/icons/MoreSmallList.svg) ) nella sezione **[!UICONTROL Obiettivo primario]**, quindi fai clic su **[!UICONTROL Impostazioni avanzate]**.

![](../../assets/goals-ab-3.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

### Quali sono le metriche di successo da raggiungere prima di incrementare questa metrica? {#dependencies}

Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di attività potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione.

È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio. Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro. L’opzione **[!UICONTROL Aggiungi dipendenza]** consente di incrementare la metrica di successo nel caso in cui un’altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto le metriche aggiuntive, fai clic su **[!UICONTROL Impostazioni avanzate]**.

1. Fai clic sull&#39;opzione **[!UICONTROL Aggiungi dipendenza]**.

1. Trascina e rilascia le metriche desiderate, quindi fai clic su **[!UICONTROL Raggiunto]** per scegliere tra **[!UICONTROL Raggiunto]** e **[!UICONTROL Non raggiunto]**.

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo? {#after-goal}

Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Si tratta di un comportamento diverso da quello predefinito in [!DNL Target Classic], che ha conteggiato i visitatori come nuovi se visualizzavano nuovamente l&#39;attività.

Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:

* **[!UICONTROL Incrementa il conteggio e mantieni utente attivo]** per specificare come viene incrementato il conteggio.
* **[!UICONTROL Incrementa il conteggio, rilascia l&#39;utente e consenti nuovo accesso]** per specificare l&#39;esperienza che l&#39;utente vedrà se accede di nuovo all&#39;attività.
* **[!UICONTROL Incrementa il conteggio, rilascia l&#39;utente e impedisci nuovo accesso]** per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.

### Come verrà incrementato il conteggio? {#count-increment}

Sono disponibili tre opzioni per l’incremento del conteggio:

* **[!UICONTROL Una volta per partecipante]**
* **[!UICONTROL Su ogni impression (esclusi aggiornamenti pagina)]**
* **[!UICONTROL Su ogni impression]**

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#overview) per ulteriori informazioni sulle impostazioni avanzate.

## Metodologia statistica {#section_statistical-methodology}

La sezione **[!UICONTROL Metodologia statistica]** della pagina **[!UICONTROL Obiettivi e impostazioni]** consente di scegliere come analizzare i risultati dell&#39;esperimento.

### Opzioni di metodologia {#methodology-options}

Questa scelta determina il framework statistico, le metriche dei risultati e i criteri di decisione utilizzati per la metrica dell&#39;obiettivo **[!UICONTROL Conversione]** di questa attività:

* **[!UICONTROL Bayesiano]:** decisioning basato sulle probabilità che aggiorna le credenze con l&#39;arrivo dei dati e supporta il monitoraggio continuo e dimensioni di campione inferiori. I risultati sono espressi come probabilità che una variante sia migliore di un&#39;altra, ad esempio &quot;92% di probabilità che la variante B batta Control&quot;.
  * Ideale per campioni di dimensioni più piccole, monitoraggio continuo, stakeholder che preferiscono le probabilità o quando si ha una conoscenza pregressa da test passati da applicare.
  * Non è ideale quando hai bisogno di un accordo rigoroso sulle normative o sulla conformità, o di valori p tradizionali.
  * I report mostrano **[!UICONTROL possibilità di controllo battute]** e un intervallo credibile invece della colonna **[!UICONTROL Affidabilità]**.
* **[!UICONTROL Test t di Welch (Frequentist)]:** La metodologia tradizionale di testing delle ipotesi esistente. Utilizza valori p e richiede una dimensione campione fissa. I rapporti mostrano una percentuale di **[!UICONTROL affidabilità]** e un intervallo di affidabilità.

Questa impostazione è disponibile solo per le attività la cui metrica obiettivo principale è **[!UICONTROL Conversione]**. Le attività con obiettivo primario **[!UICONTROL Ricavi]** o **[!UICONTROL Coinvolgimento]** utilizzano sempre il test t di **[!UICONTROL Welch]**.

Per ulteriori informazioni su come viene calcolata e segnalata ogni metodologia, vedere [Calcoli statistici nei test A/Bn](/help/main/c-reports/statistical-methodology/statistical-calculations.md).

### Configurazione bayesiana {#bayesian-configuration}

Questa impostazione viene visualizzata solo quando **[!UICONTROL Bayesiano]** è selezionato come **[!UICONTROL Metodologia statistica]**. Configura le seguenti opzioni:

* **[!UICONTROL Intervallo credibile]**: imposta l&#39;intervallo entro il quale è previsto che l&#39;effetto reale rientri.
* **[!UICONTROL Soglia di decisione]**: imposta la probabilità minima che una variante deve raggiungere, rispetto a **[!UICONTROL Controllo]**, prima di poter essere dichiarata vincitrice.
* **[!UICONTROL Utilizzare le conoscenze precedenti dei test passati?]**: attivare questa opzione per fornire le conoscenze precedenti sulle prestazioni passate per informare il calcolo **[!UICONTROL bayesiano]**.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

La sezione **[!UICONTROL Altri metadati]** della pagina **[!UICONTROL Obiettivi e impostazioni]** consente di specificare qualsiasi informazione sull&#39;attività utile da tenere a portata di mano per se stessi o per altri membri del team.
