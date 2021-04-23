---
keywords: Targeting;successo;metrica di conversione;metrica di punteggio pagina;metrica di visualizzazioni pagina;metriche di ricavi;metrica tempo sul sito;valore stimato;impostazioni avanzate;metriche di successo;impostazioni avanzate;dipendenza;dipendente;Incrementa il conteggio e mantieni l’utente nell’attività;Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso;incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso
description: Scopri le metriche di successo in Adobe [!DNL Target] che consentono di determinare il successo di un'attività. Le metriche di successo includono Conversione, Entrate, Visualizzazioni pagina, Punteggio personalizzato e Tempo sul sito.
title: Cosa sono le metriche di successo?
feature: Metriche di successo
exl-id: 38d5314d-4950-4106-a058-0d221faf5a24
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 43%

---

# Metriche di successo

In [!DNL Adobe Target] le metriche di successo sono parametri utilizzati per misurare il successo di un’attività. Le metriche di successo includono misure aziendali chiave che ti consentono di determinare il successo di una determinata esperienza o offerta in un’attività [!DNL Target].

Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti.

## Panoramica

In [!DNL Target], le metriche di successo sono preconfigurate con le opzioni ottimali sia a scopo di reporting che di tracciamento.

Per impostazione predefinita, gli eventi di conversione sono impostati su &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente in attività]&quot;. Le conversioni vengono conteggiate una sola volta, non vengono conteggiate conversioni ripetute e il visitatore visualizza sempre il contenuto dell’attività.

Le metriche dei ricavi impostate su &quot;[!UICONTROL Incrementa il conteggio e mantieni l&#39;utente in attività]&quot; dettagli dell&#39;ordine dei registri solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi incrementano il conteggio delle conversioni, ma non aggiungono ricavi a RPV/AOV/Vendite, e non saranno inclusi nel rapporto [!UICONTROL Dettagli ordine].

>[!NOTE]
>
>Per le attività che utilizzano [Analytics come origine per la generazione di rapporti](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T), la metrica obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Incrementa il conteggio e mantieni l’utente in attività]&quot; e &quot;[!UICONTROL Su ogni impression]&quot;. È *non* configurabile.

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione si verifica quando un visitatore esegue un&#39;azione sul sito definita, ad esempio <ul><li>Clic su un pulsante</li><li>Visualizzazione di una pagina</li><li>Completamento di un sondaggio</li><li>Acquisto effettuato</li></ul>Una conversione può essere conteggiata una volta per visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li><li>Ordini</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Punteggio personalizzato | Basato su coinvolgimento | Punteggio aggregato basato sul valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima richiesta di visualizzazione dell’attività [!DNL Target]. |
| Tempo sul sito | Basato su coinvolgimento | Il tempo trascorso nella visita (in secondi) dal momento in cui il visitatore vede la prima richiesta di visualizzazione dell’attività [!DNL Target] al caricamento della pagina finale con una richiesta nella sessione. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Pertanto, non vedrai i risultati immediatamente durante il test; tuttavia, tutti i risultati di tale sessione sono disponibili entro pochi minuti dalla fine della sessione.

## Metriche di successo personalizzate

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversione] , impostala per il conteggio una volta per visitatore, quindi imposta se il successo viene ottenuto quando un visitatore visualizza una determinata pagina (o insieme di pagine), visualizza una specifica richiesta [!DNL Target] o fa clic su un collegamento specifico.

Se attivato, il campo [!UICONTROL Valore stimato di una conversione] (non disponibile per le metriche [!UICONTROL Punteggio di pagina]) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche relative ai ricavi ([!UICONTROL Ricavo per visitatore], [!UICONTROL Valore medio dell&#39;ordine], [!UICONTROL Vendite totali] e [!UICONTROL Ordini]), la stima utilizza [!UICONTROL Ricavo per visitatore]. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo selezionate per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Alcune metriche, come [!UICONTROL Punteggio personalizzato] e [!UICONTROL Ricavo per visitatore], richiedono un’implementazione personalizzata che trasmette informazioni quali i totali degli ordini e gli ID ordine.

## Impostazioni avanzate {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono l’aggiunta di dipendenze, la scelta se mantenere o rimuovere l’utente nell’attività e se contare la metrica una volta per partecipante o su ogni impression.

Per accedere alle opzioni [!UICONTROL Impostazioni avanzate], fai clic sui **[!UICONTROL puntini di sospensione verticali]** > **[!UICONTROL Impostazioni avanzate]**.

![Menu Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione [!UICONTROL Impostazioni avanzate] non sarà disponibile. Per ulteriori informazioni, consulta [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md).

### Aggiungi dipendenza

Puoi utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore raggiunge prima un’altra metrica.

![Aggiungi dipendenza](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

La funzionalità di dipendenza è *non* supportata per i seguenti elementi:

* [!UICONTROL Attività di consigli. ] Questa funzionalità è supportata da tutti gli altri tipi di attività.
* Se utilizzi [Analytics come origine per la generazione di rapporti](/help/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Con il tipo di metrica “Visualizzazione di una pagina”.
* Con il tipo di metrica “Clic su un elemento” per le attività del Compositore esperienza visivo.

Le metriche di successo dipendenti non verranno convertite nei seguenti casi:

* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
* Le attività di Personalizzazione automatizzata rilasciano gli utenti e riavviano l’attività una volta raggiunte le metriche di conversione, cosicché eventuali metriche dipendenti sulla conversione non vengono convertite.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo?

Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono indicate le opzioni disponibili:

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| [!UICONTROL Incrementa il conteggio e mantieni l’utente nell’attività] | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| [!UICONTROL Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso] | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| [!UICONTROL Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso] | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

>[!NOTE]
>
>Se configuri una metrica in una delle opzioni [!UICONTROL Incrementa il conteggio] (come indicato sopra), il conteggio delle metriche incrementa correttamente una volta per partecipante solo a livello di visitatore. Il conteggio delle metriche incrementa una volta per visita per ogni nuova sessione a livello di visita.

### Come verrà incrementato il conteggio:

Scegli il comportamento desiderato:

* Una volta per partecipante
* A ogni impression (esclusi aggiornamenti pagina)
* A ogni impression

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
