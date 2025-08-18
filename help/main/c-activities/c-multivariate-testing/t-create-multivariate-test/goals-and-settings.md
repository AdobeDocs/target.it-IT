---
keywords: impostazioni attività;obiettivi e impostazioni;multivariato;mvt
description: Scopri come utilizzare la pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] per specificare informazioni sugli obiettivi di un'attività [!UICONTROL Multivariate Test] (MVT).
title: Come è possibile specificare obiettivi e impostazioni in un'attività [!UICONTROL Multivariate Test] (MVT)?
feature: Multivariate Tests
exl-id: 823a1435-ccb9-4357-9c33-a0968d704b7a
source-git-commit: af8291a27e62a588046f66f20f8d3a47c8af0a18
workflow-type: tm+mt
source-wordcount: '1164'
ht-degree: 38%

---

# Obiettivi e impostazioni ([!UICONTROL Multivariate Test])

Nella pagina [!UICONTROL Goals & Settings] in [!DNL Adobe Target] è possibile immettere informazioni sugli obiettivi delle attività di [!UICONTROL Multivariate Test] (MVT).

Sono disponibili le seguenti sezioni:

* [!UICONTROL Activity Settings]
* [!UICONTROL Reporting Settings]
* [!UICONTROL Other Metadata]

Le impostazioni disponibili in ogni sezione dipendono dall&#39;utilizzo di [!DNL Target] o [!DNL Analytics] come origine per la generazione di rapporti.

## Impostazioni attività {#section_DCBDC354261F420EBD4B43EA34947BAC}

Sono disponibili le seguenti opzioni:

### Finalità

Specifica una finalità facoltativa. La finalità può essere costituita da qualsiasi informazione che consenta a te e agli altri membri del gruppo di identificare la campagna.

### Priorità

A seconda delle impostazioni, l&#39;interfaccia utente di [!DNL Target] e le opzioni per [!UICONTROL Priority] variano. È possibile utilizzare le impostazioni legacy di [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High] oppure abilitare le priorità precise da 0 a 999.

La priorità è utilizzata se più attività vengono assegnate alla stessa posizione con lo stesso pubblico. Se due o più attività vengono assegnate alla posizione, viene visualizzata l’attività con priorità maggiore.

Se questa opzione non è abilitata in [!UICONTROL Administration] > [!UICONTROL Reporting] (impostazione predefinita), specificare una priorità: [!UICONTROL Low], [!UICONTROL Medium] o [!UICONTROL High].

Per abilitare le priorità dettagliate, fare clic su [!UICONTROL Administration] > [!UICONTROL Reporting], quindi attivare l&#39;opzione [!UICONTROL Enable Fine-Grained Priorities].

Se questa opzione è abilitata, specifica un valore compreso tra 0 e 999:

* 0 = Bassa
* 999 = Alta

Per le attività create con le versioni precedenti di [!DNL Target], la priorità [!UICONTROL Low] viene convertita in 0, la priorità [!UICONTROL Medium] in 5 e la priorità [!UICONTROL High] in 10. Se necessario, è possibile modificare questi valori.

>[!NOTE]
>
>Prima di poter disabilitare questa opzione dopo aver utilizzato le priorità precise, tutte le priorità devono essere impostate su 0, 5 o 10.

### Durata

L’attività può iniziare dopo l’approvazione, oppure è possibile impostare una data e un’ora specifiche. Analogamente, l’attività può terminare quando viene disattivata, oppure è possibile impostare una data e un’ora specifiche. Il selettore dell&#39;ora utilizza un orologio di 24 ore, dove 00:00 corrisponde a mezzanotte. Il fuso orario è impostato sul fuso configurato nel browser. Per utilizzare un fuso orario diverso, imposta il browser su un altro fuso orario e riavvia il browser.

## Impostazioni reporting {#section_13119392051044FBA6387D9B3B1C43CF}

Sono disponibili le seguenti impostazioni:

### Origine per i rapporti

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

### Metrica per obiettivo

Seleziona l’azione che deve essere eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversion], quindi imposta i parametri che determinano quando viene raggiunto il successo.

>[!NOTE]
>
>Se la soluzione di reporting è impostata su [!DNL Analytics], l&#39;unica metrica di obiettivo disponibile è [!UICONTROL Conversion]. Impossibile selezionare [!DNL Analytics] metriche come obiettivo.

Quando si seleziona la metrica di successo, viene visualizzato un selettore. Utilizza questo selettore per scegliere le specifiche per la metrica di successo.

Se attivato, il campo [!UICONTROL Estimated Value of the Conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. Il tipo di dati è valuta.

Dopo aver raggiunto l’obiettivo dell’attività, un visitatore continua a vedere il contenuto dell’attività, a meno che il visitatore non sia idoneo per un’attività di priorità più elevata. Se il visitatore raggiunge nuovamente l’obiettivo, viene conteggiato come un’altra conversione. Questo comportamento è diverso da quello predefinito in [!DNL Target Classic], che conta i visitatori come nuovi se visualizzano nuovamente il test.

### Altre metriche

Consente di creare metriche di successo aggiuntive.

Questa impostazione non è disponibile se la soluzione di reporting è impostata su [!DNL Analytics]. In questo caso, vengono applicate le metriche definite per la suite di rapporti [!DNL Analytics].

### Tipi di pubblico per i rapporti

Per impostazione predefinita, nei rapporti sono mostrati i risultati per tutti i visitatori idonei. È possibile aggiungere tipi di pubblico per i rapporti per visualizzare solo le informazioni su tipi di pubblico specifici.

### Impostazioni avanzate  {#section_E2FE441AFB324E498793ABB025ED9974}

Le impostazioni avanzate sono disponibili per [!UICONTROL Multivariate Test] metriche obiettivo.

![Menu Impostazioni avanzate](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/Menu_AdvancedSettings.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione Impostazioni avanzate non è disponibile.

#### Quali sono le metriche di successo da raggiungere prima di incrementare questa metrica?

Utilizza questa opzione per contare solo chi raggiunge la metrica di successo se in precedenza aveva raggiunto una metrica di successo diversa. Ad esempio, una conversione di test potrebbe essere valida solo se il visitatore fa clic sull’offerta o raggiunge una pagina particolare prima della conversione.

È possibile fornire la dipendenza su più metriche insieme alla flessibilità necessaria, per scegliere se la metrica debba essere raggiunta o meno per incrementare il conteggio.

Definisci entrambe le metriche (o più metriche) di successo prima di renderle interdipendenti tra loro.

L&#39;opzione [!UICONTROL Add Dependency] consente di incrementare la metrica di successo nel caso in cui un&#39;altra metrica di successo venga raggiunta o meno.

Per aggiungere una dipendenza:

1. Dopo aver aggiunto ulteriori metriche, fare clic su **[!UICONTROL Advanced Settings]**.
2. Fare clic sull&#39;opzione **[!UICONTROL Add Dependency]**:

   ![Aggiungi dipendenza](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency.png)

3. Trascina e rilascia le metriche desiderate dal riquadro di sinistra a quello di destra, quindi fai clic su **[!UICONTROL Reached]** per scegliere tra Raggiunto e Non raggiunto.

   ![Dipendenza raggiunta](/help/main/c-activities/c-multivariate-testing/t-create-multivariate-test/assets/add_dependency_reached.png)

È possibile modificare o rimuovere le dipendenze dopo averle aggiunte.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo?

Dopo che un visitatore raggiunge la metrica obiettivo, sono disponibili tre opzioni:

* [!UICONTROL Select Increment Count & Keep User in Activity] per specificare la modalità di incremento del conteggio.
* [!UICONTROL Select Increment Count, Release User & Allow Reentry] per specificare l&#39;esperienza che l&#39;utente vedrà se accede nuovamente all&#39;attività.
* [!UICONTROL Select Increment Count, Release User & Bar from Reentry] per specificare cosa vedrà l&#39;utente al posto del contenuto dell&#39;attività.

Consulta [Metriche di successo](/help/main/c-activities/r-success-metrics/success-metrics.md#reference_D011575C85DA48E989A244593D9B9924) per ulteriori informazioni sulle impostazioni avanzate.

## Altri metadati {#section_2E8917BEFB954480A4206B9E9E917F80}

Sono disponibili le seguenti impostazioni:

### Note

Inserisci informazioni sull’attività, utili per te o per gli altri membri del gruppo. Il riquadro [!UICONTROL Notes] è ridimensionabile.

## Video di formazione

I video seguenti contengono ulteriori informazioni sui concetti descritti in questo articolo.

### Impostazioni attività (3:02)

Questo video include informazioni sulle impostazioni delle attività.

* Inserire una finalità per l’attività
* Impostare il livello di priorità delle attività
* Orari di inizio e fine dell’attività
* Aggiungere tipi di pubblico da usare come filtri nella generazione di rapporti
* Inserire delle note per le attività

>[!VIDEO](https://video.tv.adobe.com/v/17381)

### Creazione di test multivariati (9:25)

Questo video illustra come creare un test multivariato utilizzando il flusso di lavoro guidato in tre passaggi di [!DNL Target]. Obiettivi e impostazioni sono discussi a partire dal 7:00.

* Definizione e progettazione di un test multivariato
* Creazione di un test multivariato

>[!VIDEO](https://video.tv.adobe.com/v/36329?captions=ita)
