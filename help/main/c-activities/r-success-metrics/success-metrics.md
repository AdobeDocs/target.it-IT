---
keywords: Targeting;successo;metrica conversione;metrica punteggio pagina;metrica visualizzazioni pagina;metrica ricavi;metrica tempo sul sito;valore stimato;impostazioni avanzate;metriche successo;impostazioni avanzate;dipendenza;dipendente;Incrementa il conteggio e mantieni l'utente nell'attività;Incrementa il conteggio, rilascia l'utente e consenti il reinserimento;incrementa il conteggio, rilascia l'utente e impedisci reinserimento
description: Scopri le metriche di successo che ti aiutano a determinare il successo di un’attività. Le metriche di successo includono Conversione, Entrate, Visualizzazioni pagina, Punteggio personalizzato e Tempo sul sito.
title: Cosa Sono Le Metriche Di Successo?
feature: Success Metrics
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
source-git-commit: a34d40bef584bfa941731df718cb402c658f5d28
workflow-type: tm+mt
source-wordcount: '1362'
ht-degree: 22%

---

# [!UICONTROL Success metrics]

Le metriche di successo in [!DNL Adobe Target] sono indicatori chiave che consentono di misurare le prestazioni delle attività. Queste metriche acquisiscono risultati di business importanti, come conversioni, ricavi per visitatore e coinvolgimento dei clienti, consentendoti di valutare l’impatto di esperienze o offerte specifiche.

Ad esempio, puoi tenere traccia se una nuova promozione aumenta i ricavi per visitatore o porta a più articoli aggiunti ai carrelli. Le metriche di successo consentono inoltre di identificare i problemi nei flussi di utenti, come la registrazione, il pagamento o i processi di acquisto, fornendo nel contempo informazioni sul comportamento complessivo dei visitatori.

## Panoramica

In [!DNL Target], le metriche di successo sono preconfigurate con le impostazioni consigliate per garantire un reporting accurato e un tracciamento efficace.

Per impostazione predefinita, gli eventi di conversione utilizzano l&#39;impostazione **[!UICONTROL Increment count & keep user in activity].** Questa impostazione significa che ogni visitatore viene conteggiato come conversione una sola volta. Non vengono conteggiate conversioni ripetute. Questi visitatori continuano a visualizzare il contenuto dell’attività per tutta la sessione.

Per le metriche dei ricavi che utilizzano la stessa impostazione, solo il primo ordine di un visitatore registra i dettagli dell’ordine. Anche se gli ordini successivi aumentano il conteggio delle conversioni, non contribuiscono alle metriche basate sui ricavi come [!UICONTROL Revenue per Visitor (RPV)], [!UICONTROL Average Order Value (AOV)] o [!DNL Total Sales]. Anche questi ordini aggiuntivi sono esclusi dal report [!UICONTROL Order Details].

>[!NOTE]
>
>Per le attività che utilizzano [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), la metrica di obiettivo utilizza sempre le impostazioni &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. Queste impostazioni sono *non* configurabili.

Le metriche di successo seguenti possono essere configurate nella sezione [!UICONTROL Reporting Settings] di [!UICONTROL Activity Settings page], nel passaggio [!UICONTROL Goals & Settings]:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| [!UICONTROL Conversion] | Basato su conversione | La conversione si verifica quando un visitatore esegue sul tuo sito un’azione da te definita, ad esempio <ul><li>Visualizzazione di una pagina</li><li>Visualizzazione di una mbox</li><li>Clic su un elemento</li></ul>Una conversione può essere conteggiata una volta per visitatore o ogni volta che un visitatore completa una conversione. |
| [!UICONTROL Revenue] | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere una sola metrica di ricavo:<ul><li>Visualizzazione di una mbox</li></ul>Per ulteriori informazioni sulle modifiche apportate all&#39;interfaccia utente aggiornata di [!DNL Target] in relazione alle metriche di successo per le entrate, vedi [Aggiornato [!DNL Target] Modifiche all&#39;interfaccia utente](#changes) di seguito. |
| [!UICONTROL Engagement] | Basato su coinvolgimento | Coinvolgimento generato dalla visita. Puoi scegliere una delle metriche di coinvolgimento seguenti:<UL><li>Visualizzazioni di pagina: ogni visita univoca viene conteggiata come conversione.</li><li>[!UICONTROL Custom Scoring]: Punteggio aggregato basato sul valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima richiesta [!DNL Target] di visualizzazione dell&#39;attività.</li>[!DNL Time on Site]: tempo trascorso nella visita (in secondi) dal momento in cui il visitatore vede la prima richiesta di visualizzazione [!DNL Target] dell&#39;attività al caricamento della pagina finale con una richiesta nella sessione.</UL> |

Per le metriche basate sul coinvolgimento (a differenza delle metriche basate sulla conversione e sui ricavi), i visitatori devono riqualificarsi per l’attività in ogni visita per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Pertanto, non vedrai immediatamente i risultati durante il test; tuttavia, tutti i risultati di quella sessione sono disponibili entro pochi minuti dalla fine della sessione.

## Metriche di successo personalizzate

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversion], impostala per essere conteggiata una volta per visitatore, quindi imposta se viene raggiunto il successo quando un visitatore visualizza una determinata pagina (o set di pagine), visualizza una richiesta [!DNL Target] specifica o fa clic su un collegamento specifico.

Se attivato, il campo [!UICONTROL Estimated Value of one conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. Il tipo di dati è valuta. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo scelte per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Alcune metriche, come [!UICONTROL Custom Scoring] e [!UICONTROL Revenue Per Visitor], richiedono un&#39;implementazione personalizzata che trasmette informazioni, come i totali degli ordini e gli ID degli ordini.

## Impostazioni avanzate  {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono l’aggiunta delle dipendenze, la scelta di mantenere l’utente nell’attività o rimuoverlo e se contare la metrica una volta per partecipante o su ogni impression.

Per accedere alle opzioni [!UICONTROL Advanced Settings], fai clic sull&#39;icona **[!UICONTROL More Actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallListVert.svg) ), quindi fai clic su **[!UICONTROL Advanced Settings]**.

![Menu Impostazioni avanzate](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

Per ulteriori informazioni sulle opzioni [!UICONTROL Advanced Settings] (&quot;[!UICONTROL What will happen after a user encounters this goal]&quot; e &quot;[!UICONTROL How will the count be incremented]&quot;) vedere [Cosa succede dopo che un utente rileva questa metrica obiettivo](#what-happens)?

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. Opzione [!UICONTROL Advanced Settings] non disponibile. Per ulteriori informazioni, vedere [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Aggiungi dipendenza

Puoi utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore ha già raggiunto un’altra metrica.

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

La funzionalità di dipendenza *non* è supportata per:

* [!UICONTROL Recommendations] attività. Questa funzionalità è supportata da tutti gli altri tipi di attività.
* Se utilizzi [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Il tipo di metrica &quot;Visualizzazione di una pagina&quot;.
* Il tipo di metrica &quot;Clic su un elemento&quot; per le attività del Compositore esperienza visivo.

Le metriche di successo dipendenti non vengono convertite nei casi seguenti:

* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
* Le attività [!UICONTROL Automated Personalization] rilasciano gli utenti e riavviano l&#39;attività quando vengono raggiunte le metriche di conversione, pertanto le metriche dipendenti dalla metrica di conversione non vengono convertite.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo? {#what-happens}

Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono illustrate le opzioni disponibili:

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Seleziona l’esperienza che il visitatore vede se accede nuovamente all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

>[!NOTE]
>
>Se configuri una metrica in una delle opzioni [!UICONTROL Increment Count] (menzionate sopra), il conteggio delle metriche viene incrementato correttamente una volta per partecipante solo a livello di visitatore. Il conteggio delle metriche incrementa una volta per visita per ogni nuova sessione a livello di visita.

### Come viene incrementato il conteggio:

Scegli il comportamento desiderato:

* Una volta per partecipante
* A ogni impression (esclusi aggiornamenti pagina)
* A ogni impression

## Problemi noti

* Le metriche di successo con l’opzione avanzata “Come verrà incrementato il conteggio?” impostata su “a ogni impression” o “a ogni impression (esclusi aggiornamenti pagina)” non possono essere utilizzate come metriche di successo da cui dipende un’altra metrica.

  Quando una metrica di successo è impostata per essere incrementata a ogni impression, [!DNL Target] conta nuovamente il visitatore ogni volta che visita questa metrica di successo. [!DNL Target] reimposta quindi su 0 la metrica di successo &quot;appartenenza&quot; in modo che possa contare di nuovo sull&#39;impression successiva. Pertanto, se un&#39;altra metrica richiede che questa metrica sia stata vista per prima, [!DNL Target] non riconosce mai che l&#39;utente ha visto la prima metrica.

## [!DNL Target] modifiche all&#39;interfaccia utente aggiornate {#changes}

La versione [[!DNL Target Standard/Premium] 25.2.1](/help/main/r-release-notes/release-notes-for-previous-releases.md#ui-update-2), avviata il 17 febbraio 2015, ha introdotto [!DNL Target] e [!UICONTROL Visual Experience Composer] UI (VEC) aggiornate. Questa sezione illustra le differenze chiave tra l’interfaccia utente legacy e quella aggiornata, in particolare per quanto riguarda la configurazione e la gestione delle metriche di successo.

### Modifiche all&#39;interfaccia utente relative a [!UICONTROL Revenue] metriche di successo

Nell&#39;interfaccia [!DNL Target] aggiornata, il menu a discesa [!UICONTROL Default View for Reporting] è stato rimosso. Questo campo era ridondante, in quanto in precedenza salvava la visualizzazione di reporting predefinita in [!DNL Overview] > [!UICONTROL Reports] nell&#39;interfaccia utente legacy.

Con l&#39;interfaccia utente aggiornata, la metrica di reporting predefinita ora è sempre impostata su [!UICONTROL Revenue per Visitor (RPV)]. È comunque possibile personalizzare la visualizzazione nella sezione [!UICONTROL Reports] per visualizzare le metriche più rilevanti per l&#39;analisi.

Questa modifica non influisce sulle metriche di consegna. Questa modifica influisce solo sul filtro predefinito visualizzato nella visualizzazione di reporting. Poiché RPV è la metrica più comunemente utilizzata dai clienti, questa impostazione predefinita è stata selezionata per semplificare i flussi di lavoro di reporting. È possibile passare ad altre metriche in qualsiasi momento nella sezione [!UICONTROL Reports].