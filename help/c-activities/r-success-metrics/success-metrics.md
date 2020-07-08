---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics
description: In  Adobe Target, le metriche di successo sono preconfigurate a scopo di reporting e tracciamento.
title: Metriche di successo in  Adobe Target
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: c7664f9674234565a3657f453541095811fa5aa6
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 83%

---


# Metriche di successo{#success-metrics}

In  Adobe Target, le metriche di successo sono preconfigurate a scopo di reporting e tracciamento.

Le metriche di successo sono parametri utilizzati per misurare il successo di un’attività. Le metriche di successo includono misure aziendali chiave che consentono di determinare il successo di un’esperienza o un’offerta specifica in un’attività Target. Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti.

In linea con il suo obiettivo di semplificare la creazione di test, [!DNL Target Standard] si occupa di alcune delle configurazioni che dovevano essere eseguite manualmente in [!DNL Target Classic]. Ad esempio, le metriche di successo sono preconfigurate con le opzioni ottimali.

By default, conversion events are set to &quot;Count once and keep the entrant in the activity&quot; in [!DNL Target Standard]. Le conversioni vengono conteggiate una sola volta, le conversioni ripetute non sono conteggiate e il visitatore vede sempre il contenuto del test.

Nelle metriche dei ricavi impostate su “Incrementa il conteggio e mantieni utente attivo” vengono riportati i dettagli solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non il valore di Ricavo per visita, Valore medio dell’ordine e Vendite, e non verranno inclusi nel rapporto Dettagli ordine.

>[!NOTE]
>
>Il comportamento predefinito per le attività che utilizzano [Analytics come origine](/help/c-integrating-target-with-mac/a4t/a4t.md) di reporting (A4T) è &quot;Increment count and keep the user in activity&quot; (Conteggio incrementi e mantenimento dell&#39;utente nell&#39;attività) con &quot;Once per entrant&quot; (Una volta per partecipante).

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione si verifica quando un visitatore esegue sul tuo sito un’azione da te definita (clic su un pulsante, visualizzazione di una pagina, completamento di un sondaggio o acquisto). Una conversione può essere conteggiata una volta per ogni visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Tempo sul sito | Basato su coinvolgimento | Tempo trascorso nella visita (in secondi) dal momento in cui il visitatore vede la prima richiesta Target di visualizzazione dell&#39;attività al caricamento della pagina finale con una richiesta nella sessione. |
| Punteggio personalizzato | Basato su coinvolgimento | Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity&#39;s first display [!DNL Target] request. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Di conseguenza, i risultati non vengono visualizzati immediatamente durante la verifica, tuttavia tutti i risultati della sessione sono disponibili entro pochi minuti dalla stessa.

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. For example, choose a Conversion metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

Se attivato, il campo del Valore stimato di una conversione (non disponibile per la metrica Punteggio di pagina) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche collegate ai ricavi (Ricavo per visitatore, Valore ordine medio, Vendite totali e Ordini), la stima utilizza Ricavo per visitatore. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo selezionate per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Alcune metriche, quali Punteggio personalizzato e Ricavo per visitatore, richiedono un’implementazione personalizzata che trasmette informazioni quali i totali degli ordini e gli ID ordine.

## Impostazioni avanzate {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono il conteggio della metrica per impression o una volta per visitatore, e la possibilità di scegliere se mantenere o meno l’utente nell’attività.

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L’opzione Impostazioni avanzate non sarà disponibile.

![Menu a discesa Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/Menu_AdvancedSettings.png)

Puoi inoltre utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore ha già raggiunto un’altra metrica.

![Aggiungi dipendenza](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

Le metriche di successo dipendenti sono supportate nelle attività di test A/B, Personalizzazione automatizzata, Targeting esperienze e test multivariato. Al momento le attività Consigli non supportano le metriche di successo dipendenti.

>[!NOTE]
>
>Le metriche di successo dipendenti non verranno convertite nei seguenti casi:

* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
* Le attività di Personalizzazione automatizzata rilasciano gli utenti e riavviano l’attività una volta raggiunte le metriche di conversione, cosicché eventuali metriche dipendenti sulla conversione non vengono convertite.

Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono indicate le opzioni disponibili.

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| Incrementa il conteggio e mantieni l’utente nell’attività | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| Incrementa il conteggio, rilascia l’utente e consenti nuovo accesso | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| Incrementa il conteggio, rilascia l’utente e impedisci nuovo accesso | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)