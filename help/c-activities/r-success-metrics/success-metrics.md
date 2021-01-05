---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings;dependency;dependant;Increment Count & Keep User in Activity;Increment Count, Release user, & Allow Reentry;increment Count, Release User, & Bar from Reentry
description: In  Adobe Target, le metriche di successo sono parametri utilizzati per misurare il successo di un'attività. Le metriche di successo includono misure aziendali chiave che consentono di determinare il successo di un’esperienza o un’offerta specifica in un’attività Target.
title: Metriche di successo in  Adobe Target
feature: Success Metrics
translation-type: tm+mt
source-git-commit: 4adade56529fb95e4400e06d04d3c6c69e120edc
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 47%

---


# Metriche di successo

In [!DNL Adobe Target] le metriche di successo sono parametri utilizzati per misurare il successo di un&#39;attività. Le metriche di successo includono misure aziendali chiave che consentono di determinare il successo di una determinata esperienza o offerta in un&#39;attività [!DNL Target].

Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti.

## Panoramica

In [!DNL Target], le metriche di successo sono pre-configurate con le opzioni ottimali sia a scopo di reporting che di tracciamento.

Per impostazione predefinita, gli eventi di conversione sono impostati su &quot;[!UICONTROL Incrementa conteggio e mantieni l&#39;utente in attività]&quot;. Le conversioni vengono contate solo una volta, non vengono conteggiate conversioni ripetute e il visitatore visualizza sempre il contenuto dell&#39;attività.

Metriche delle entrate impostate su &quot;[!UICONTROL Incrementa conteggio e mantieni utente in attività]&quot; dettagli dell&#39;ordine di registro solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il numero di conversioni, ma non aggiungono ricavi a RPV/AOV/Sales, e non saranno inclusi nel report [!UICONTROL Dettagli ordine].

>[!NOTE]
>
>Per le attività che utilizzano [Analytics come origine di reporting](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T), la metrica di obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Increment Count &amp; Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. È possibile configurare *not*.

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione è quando un visitatore esegue un’azione sul sito definita, come <ul><li>Clic su un pulsante</li><li>Visualizzazione di una pagina</li><li>Completamento di un sondaggio</li><li>Acquisto effettuato</li></ul>Una conversione può essere conteggiata una volta per ogni visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li><li>Ordini</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Punteggio personalizzato | Basato su coinvolgimento | Punteggio aggregato basato sul valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima richiesta di visualizzazione dell&#39;attività [!DNL Target]. |
| Tempo sul sito | Basato su coinvolgimento | Tempo trascorso nella visita (in secondi) dal momento in cui il visitatore vede la prima richiesta di visualizzazione dell&#39;attività [!DNL Target] al caricamento della pagina finale con una richiesta nella sessione. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Pertanto, i risultati non verranno visualizzati immediatamente durante il test; tuttavia, tutti i risultati di tale sessione sono disponibili entro pochi minuti dalla fine della sessione.

## Metriche di successo personalizzate

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegliete una metrica [!UICONTROL Conversione], impostatela per il conteggio una volta per ogni visitatore, quindi impostate se il successo viene ottenuto quando un visitatore visualizza una determinata pagina (o insieme di pagine), visualizza una specifica richiesta [!DNL Target] o fa clic su un collegamento specifico.

Se attivato, il campo [!UICONTROL Estimated Value of a conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche relative alle entrate ([!UICONTROL Entrate per visitatore], [!UICONTROL Valore ordine medio], [!UICONTROL Vendite totali] e [!UICONTROL Ordini]), la stima utilizza [!UICONTROL Entrate per visitatore]. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo selezionate per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Alcune metriche, come [!UICONTROL Custom Scoring] e [!UICONTROL Revenue per Visitor] (Entrate per visitatore), richiedono un&#39;implementazione personalizzata che trasmette informazioni come i totali degli ordini e gli ID ordine.

## Impostazioni avanzate {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono l&#39;aggiunta di dipendenze, la scelta se mantenere l&#39;utente nell&#39;attività o rimuoverli, e se contare la metrica una volta per partecipante o su ogni impressione.

Per accedere alle opzioni [!UICONTROL Impostazioni avanzate], fare clic sulle **[!UICONTROL ellissi verticali]** > **[!UICONTROL Impostazioni avanzate]**.

![Menu Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione [!UICONTROL Impostazioni avanzate] non sarà disponibile. Per ulteriori informazioni, vedere [ Adobe Analytics come origine di reporting per  Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md).

### Aggiungi dipendenza

Potete utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore raggiunge prima un&#39;altra metrica.

![Aggiungi dipendenza](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

La funzionalità di dipendenza è *not* supportata per i seguenti elementi:

* [!UICONTROL Attività di consigli. ] Questa funzionalità è supportata da tutti gli altri tipi di attività.
* Se utilizzate [Analytics come origine di reporting](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Con il tipo di metrica “Visualizzazione di una pagina”.
* Con il tipo di metrica “Clic su un elemento” per le attività del Compositore esperienza visivo.

Le metriche di successo dipendenti non verranno convertite nei seguenti casi:

* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
* Le attività di Personalizzazione automatizzata rilasciano gli utenti e riavviano l’attività una volta raggiunte le metriche di conversione, cosicché eventuali metriche dipendenti sulla conversione non vengono convertite.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo?

Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono indicate le opzioni disponibili:

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| [!UICONTROL Incremento conteggio e mantenimento utente nell&#39;attività] | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| [!UICONTROL Numero incrementi, Rilascia utenti e Consenti rientro] | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| [!UICONTROL Incremento conteggio, rilascio utente e barra da rientro] | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

>[!NOTE]
>
>Se configurate una metrica per una delle opzioni [!UICONTROL Incremento conteggio] (menzionate sopra), il conteggio delle metriche incrementa correttamente una volta per partecipante solo a livello di visitatore. Il conteggio delle metriche incrementa una volta per visita per ogni nuova sessione a livello di visita.

### Come verrà incrementato il conteggio:

Scegliete il comportamento desiderato:

* Una volta per partecipante
* Su ogni impressione (escludendo gli aggiornamenti di pagina)
* A ogni impression

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)