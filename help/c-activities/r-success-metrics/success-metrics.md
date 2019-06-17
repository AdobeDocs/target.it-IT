---
description: In Target Standard, le metriche di successo sono preconfigurate e possono essere utilizzate per la generazione di rapporti e per il tracciamento.
keywords: Targeting;successo;metrica di conversione;metrica di punteggio pagina;metrica di visualizzazioni pagina;metriche di ricavi;metrica tempo sul sito;valore stimato;impostazioni avanzate
seo-description: In Target Standard, le metriche di successo sono preconfigurate e possono essere utilizzate per la generazione di rapporti e per il tracciamento.
seo-title: Metriche di successo
solution: Target
title: Metriche di successo
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: 2a400b05f3e5637465fe65a10285544793d67b47

---


# Metriche di successo{#success-metrics}

In Target Standard, le metriche di successo sono preconfigurate e possono essere utilizzate per la generazione di rapporti e per il tracciamento.

Le metriche di successo sono parametri utilizzati per misurare il successo di un&#39;attività. Le metriche di successo includono le misure aziendali chiave che consentono di determinare il successo di un&#39;esperienza o un&#39;offerta specifica in un&#39;attività Target. Ad esempio, potete determinare se una nuova offerta aumenta le entrate per visitatore o aggiungere un elemento a un carrello. Le metriche di successo possono essere utili per scoprire i problemi con la registrazione, l&#39;ordinazione o l&#39;acquisto di funnel, ma anche semplicemente con il coinvolgimento dei visitatori o del cliente.

In linea con il suo obiettivo di semplificare la creazione di test, [!DNL Target Standard] si occupa di alcune delle configurazioni che dovevano essere eseguite manualmente in [!DNL Target Classic]. Ad esempio, le metriche di successo sono preconfigurate con le opzioni ottimali.

Per impostazione predefinita, in [!DNL Target Standard] gli eventi di conversione sono impostati per essere conteggiati una volta e per mantenere il partecipante nell’attività. Le conversioni vengono conteggiate una sola volta, le conversioni ripetute non sono conteggiate e il visitatore vede sempre il contenuto del test.

Nelle metriche dei ricavi impostate su “Incrementa il conteggio e mantieni utente attivo” vengono riportati i dettagli solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non il valore di Ricavo per visita, Valore medio dell’ordine e Vendite, e non verranno inclusi nel rapporto Dettagli ordine.

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione si verifica quando un visitatore esegue sul tuo sito un’azione da te definita (clic su un pulsante, visualizzazione di una pagina, completamento di un sondaggio o acquisto). Una conversione può essere conteggiata una volta per ogni visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Tempo sul sito | Basato su coinvolgimento | Il tempo trascorso (in secondi) dal momento in cui il visitatore vede per la prima volta la prima mbox di visualizzazione dell&#39;attività fino al caricamento della pagina finale con una mbox nella sessione. |
| Punteggio personalizzato | Basato su coinvolgimento | Punteggio aggregato in base al valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima mbox di visualizzazione dell&#39;attività. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Di conseguenza, i risultati non vengono visualizzati immediatamente durante la verifica, tuttavia tutti i risultati della sessione sono disponibili entro pochi minuti dalla stessa.

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica di conversione, impostala per il conteggio una volta per ogni visitatore, quindi definisci se il successo viene ottenuto quando un visitatore visualizza una determinata pagina (o insieme di pagine), visualizza una determinata mbox o fa clic su un collegamento specifico.

Se attivato, il campo del Valore stimato di una conversione (non disponibile per la metrica Punteggio di pagina) fornisce un valore per l’obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche collegate ai ricavi (Ricavo per visitatore, Valore ordine medio, Vendite totali e Ordini), la stima utilizza Ricavo per visitatore. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](../../administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md#concept_32F875D8F91349CE86AF391F65BEAEEE) per maggiori informazioni.

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
| Incrementa il conteggio e mantieni l’utente nell’attività | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>Per ogni impression, escluso l’aggiornamento della pagina</li><li>Su ogni impression</li></ul> |
| Incrementa il conteggio, rilascia l’utente e consenti di accedere di nuovo all’attività | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| Incrementa il conteggio, rilascia l’utente e non consentire un nuovo accesso all’attività | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380?captions=ita)