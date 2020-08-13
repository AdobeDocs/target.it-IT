---
keywords: Targeting;success;conversion metric;page score metric;page views metric;revenue metrics;time on site metric;estimated value;advanced settings;success metrics;advanced settings
description: In  Adobe Target, le metriche di successo sono parametri utilizzati per misurare il successo di un'attività. Le metriche di successo includono misure aziendali chiave che consentono di determinare il successo di un’esperienza o un’offerta specifica in un’attività Target.
title: Metriche di successo in  Adobe Target
feature: success metrics
uuid: 24e9ae0f-099b-430b-b2bb-03b405f88929
translation-type: tm+mt
source-git-commit: b2f80c89ecceb6f88a176db7a90e71a162a24641
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 52%

---


# Metriche di successo{#success-metrics}

In [!DNL Adobe Target] success metrics are parameters used to measure the success of an activity. Success metrics include key business measures that enable you to determine the success of a given experience or offer in a [!DNL Target] activity.

Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti.

## Panoramica

In [!DNL Target]questo caso, le metriche di successo sono preconfigurate con le opzioni ottimali sia a scopo di reporting che di tracciamento.

Per impostazione predefinita, gli eventi di conversione sono impostati su &quot;[!UICONTROL Incremento conteggio e mantenimento dell&#39;utente nell&#39;attività]&quot;. Le conversioni vengono contate solo una volta, non vengono conteggiate conversioni ripetute e il visitatore visualizza sempre il contenuto dell&#39;attività.

Revenue metrics that are set to &quot;[!UICONTROL Increment count &amp; keep user in activity]&quot; log order details only for the first order made by the same visitor. All subsequent orders increase conversion count, but will not add revenue to RPV/AOV/Sales, and will not be included in the [!UICONTROL Order Details] report.

>[!NOTE]
>
>Il comportamento predefinito per le attività che utilizzano [Analytics come origine](/help/c-integrating-target-with-mac/a4t/a4t.md) di reporting (A4T) è &quot;[!UICONTROL Increment count &amp; keep user in activity]&quot; (Conteggio incrementi e mantieni l&#39;utente in attività[!UICONTROL ) con &quot;]Once per entrant&quot; (Una volta per partecipante).

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione è quando un visitatore esegue un’azione sul sito definita, come <ul><li>Clic su un pulsante</li><li>Visualizzazione di una pagina</li><li>Completamento di un sondaggio</li><li>Acquisto effettuato</li></ul>Una conversione può essere conteggiata una volta per ogni visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li><li>Ordini</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Punteggio personalizzato | Basato su coinvolgimento | Aggregated score based on the value assigned to pages visited on the site, from the point the visitor first sees the activity&#39;s first display [!DNL Target] request. |
| Tempo sul sito | Basato su coinvolgimento | Time spent in the visit (in seconds) from the point the visitor sees the activity&#39;s first display [!DNL Target] request to the load of the final page with a request in the session. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Pertanto, i risultati non verranno visualizzati immediatamente durante il test; tuttavia, tutti i risultati di tale sessione sono disponibili entro pochi minuti dalla fine della sessione.

## Metriche di successo personalizzate

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. For example, choose a [!UICONTROL Conversion] metric, set it to be counted once per visitor, then set whether success is achieved when a visitor views a certain page (or set of pages), views a specific [!DNL Target] request, or clicks a specific link.

If enabled, the [!UICONTROL Estimated Value of one conversion] field (not available for the [!UICONTROL Page Score] metrics) provides a value for your goal, but not for other metrics. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. For all revenue metrics ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales], and [!UICONTROL Orders]), the estimate uses [!UICONTROL Revenue per Visitor]. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](/help/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo selezionate per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Some metrics, such as [!UICONTROL Custom Scoring] and [!UICONTROL Revenue Per Visitor], require a customized implementation that passes in information such as order totals and order IDs.

## Impostazioni avanzate {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono il conteggio della metrica per impression o una volta per visitatore, e la possibilità di scegliere se mantenere o meno l’utente nell’attività.

Per accedere alle opzioni [!UICONTROL Impostazioni] avanzate, fate clic sulle ellissi **[!UICONTROL verticali]** > Impostazioni **[!UICONTROL avanzate]**.

![Menu Impostazioni avanzate](/help/c-activities/r-success-metrics/assets/advanced-settings.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. The [!UICONTROL Advanced Settings] option will not be available. For more information, see [Adobe Analytics as the reporting source for Adobe Target (A4T)](/help/c-integrating-target-with-mac/a4t/a4t.md).

Puoi inoltre utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore ha già raggiunto un’altra metrica.

![Aggiungi dipendenza](/help/c-activities/r-success-metrics/assets/UI_dep_success_metric.png)

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

Le metriche di successo dipendenti sono supportate nelle attività di test A/B, Personalizzazione automatizzata, Targeting esperienze e test multivariato. Al momento le attività Consigli non supportano le metriche di successo dipendenti.

>[!NOTE]
>
>Le metriche di successo dipendenti non verranno convertite nei seguenti casi:
>
>* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
>* Le attività di Personalizzazione automatizzata rilasciano gli utenti e riavviano l’attività una volta raggiunte le metriche di conversione, cosicché eventuali metriche dipendenti sulla conversione non vengono convertite.


Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono indicate le opzioni disponibili:

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| [!UICONTROL Incremento conteggio e mantenimento utente nell&#39;attività] | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| [!UICONTROL Numero incrementi, Rilascia utenti e Consenti rientro] | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| [!UICONTROL Incremento conteggio, rilascio utente e barra da rientro] | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

>[!NOTE]
>
>Se configurate una metrica con una delle opzioni [!UICONTROL Increment Count] (Conteggioincrementi) di cui sopra, il conteggio delle metriche incrementa correttamente una volta per partecipante solo a livello di visitatore. Il conteggio delle metriche incrementa una volta per visita per ogni nuova sessione a livello di visita.

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)