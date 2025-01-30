---
keywords: Targeting;successo;metrica conversione;metrica punteggio pagina;metrica visualizzazioni pagina;metrica ricavi;metrica tempo sul sito;valore stimato;impostazioni avanzate;metriche successo;impostazioni avanzate;dipendenza;dipendente;Incrementa il conteggio e mantieni l'utente nell'attività;Incrementa il conteggio, rilascia l'utente e consenti il reinserimento;incrementa il conteggio, rilascia l'utente e impedisci reinserimento
description: Scopri le metriche di successo in Adobe [!DNL Target] che ti aiutano a determinare il successo di un'attività. Le metriche di successo includono Conversione, Entrate, Visualizzazioni pagina, Punteggio personalizzato e Tempo sul sito.
title: Cosa Sono Le Metriche Di Successo?
feature: Success Metrics
hide: true
hidefromtoc: true
source-git-commit: 99ea312405e397e97e64e32d2685e8a6966d8928
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 41%

---

# Metriche di successo

In [!DNL Adobe Target] le metriche di successo sono parametri utilizzati per misurare il successo di un&#39;attività. Le metriche di successo includono misure aziendali chiave che consentono di determinare il successo di un&#39;esperienza o un&#39;offerta specifica in un&#39;attività [!DNL Target].

Ad esempio, puoi determinare se una nuova offerta o l’aggiunta di un articolo al carrello può aumentare il tuo ricavo per visitatore. Le metriche di successo possono essere utili per individuare problemi a livello di registrazione, ordini o percorsi di acquisto, o anche semplicemente il livello di coinvolgimento di visitatori o clienti.

## Panoramica

In [!DNL Target], le metriche di successo sono preconfigurate con le opzioni ottimali a scopo di reporting e tracciamento.

Per impostazione predefinita, gli eventi di conversione sono impostati su &quot;[!UICONTROL Increment count & keep user in activity]&quot;. Le conversioni vengono conteggiate una sola volta, non vengono conteggiate conversioni ripetute e il visitatore visualizza sempre il contenuto dell’attività.

Le metriche dei ricavi impostate su &quot;[!UICONTROL Increment count & keep user in activity]&quot; registrano i dettagli solo per il primo ordine effettuato dallo stesso visitatore. Tutti gli ordini successivi aumentano il conteggio delle conversioni, ma non aggiungono ricavi a RPV/AOV/Sales e non verranno inclusi nel report [!UICONTROL Order Details].

>[!NOTE]
>
>Per le attività che utilizzano [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T), la metrica di obiettivo utilizzerà sempre le impostazioni &quot;[!UICONTROL Increment Count & Keep User in Activity]&quot; e &quot;[!UICONTROL On Every Impression]&quot;. *non* configurabile.

Sono disponibili le seguenti metriche di successo:

| Metrica di successo | Approccio di misurazione | Definizione |
|--- |--- |--- |
| Conversione | Basato su conversione | La conversione si verifica quando un visitatore esegue sul tuo sito un’azione da te definita, ad esempio <ul><li>Clic su un pulsante</li><li>Visualizzazione di una pagina</li><li>Completamento di un sondaggio</li><li>Acquisto effettuato</li></ul>Una conversione può essere conteggiata una volta per visitatore o ogni volta che un visitatore completa una conversione. |
| Ricavi | Basato su conversione | Ricavi generati dalla visita. Puoi scegliere tra le seguenti metriche collegate ai ricavi:<ul><li>Ricavo per visitatore (RPV)</li><li>Valore medio dell’ordine (AOV)</li><li>Vendite totali</li><li>Ordini</li></ul> |
| Visualizzazioni pagina | Basato su coinvolgimento | Ogni visita univoca viene conteggiata come conversione. |
| Punteggio personalizzato | Basato su coinvolgimento | Punteggio aggregato basato sul valore assegnato alle pagine visitate sul sito, dal momento in cui il visitatore vede per la prima volta la prima richiesta di visualizzazione dell&#39;attività [!DNL Target]. |
| Tempo sul sito | Basato su coinvolgimento | Tempo trascorso nella visita (in secondi) dal momento in cui il visitatore vede la prima richiesta di visualizzazione [!DNL Target] dell&#39;attività al caricamento della pagina finale con una richiesta nella sessione. |

Per le metriche basate su coinvolgimento (a differenza delle metriche basate su conversione e su ricavo), i visitatori devono riqualificarsi per l&#39;attività in ciascuna posizione per incrementare il conteggio per quella sessione. La metrica associata inizia ad aumentare dopo la riqualificazione e termina alla fine di ogni sessione del visitatore. Una visita termina dopo 30 minuti di inattività. Pertanto, non vedrai i risultati immediatamente durante il test; tuttavia, tutti i risultati di quella sessione sono disponibili entro pochi minuti dalla fine della sessione.

## Metriche di successo personalizzate

Inoltre puoi creare metriche di successo personalizzate.

Dopo aver selezionato la metrica di successo, seleziona l’azione eseguita da un visitatore per raggiungere l’obiettivo. Ad esempio, scegli una metrica [!UICONTROL Conversion], impostala per essere conteggiata una volta per visitatore, quindi imposta se viene raggiunto il successo quando un visitatore visualizza una determinata pagina (o set di pagine), visualizza una richiesta [!DNL Target] specifica o fa clic su un collegamento specifico.

Se attivato, il campo [!UICONTROL Estimated Value of one conversion] (non disponibile per le metriche [!UICONTROL Page Score]) fornisce un valore per l&#39;obiettivo, ma non per altre metriche. Questo valore consente a [!DNL Target] di calcolare un incremento stimato dei ricavi. Questo campo è facoltativo; tuttavia, i ricavi incrementali per eventuali metriche non collegate ai ricavi non possono essere calcolate senza di esso. Per tutte le metriche ricavi ([!UICONTROL Revenue per Visitor], [!UICONTROL Average Order Value], [!UICONTROL Total Sales] e [!UICONTROL Orders]), la stima utilizza [!UICONTROL Revenue per Visitor]. I dati sono di tipo valuta. Consulta [Stima dell’incremento dei ricavi](/help/main/administrating-target/r-target-account-preferences/estimating-lift-in-revenue.md) per maggiori informazioni.

Le metriche di successo selezionate per l’attività sono disponibili nelle impostazioni del rapporto quando si visualizza un rapporto per l’attività.

Alcune metriche, come [!UICONTROL Custom Scoring] e [!UICONTROL Revenue Per Visitor], richiedono un&#39;implementazione personalizzata che trasmette informazioni quali i totali degli ordini e gli ID degli ordini.

## Impostazioni avanzate  {#section_7CE95A2FA8F5438E936C365A6D43BC5B}

Con le impostazioni avanzate puoi gestire il modo in cui viene misurato il successo. Le opzioni includono l’aggiunta delle dipendenze, la scelta di mantenere l’utente nell’attività o rimuoverlo e se contare la metrica una volta per partecipante o su ogni impression.

Per accedere alle opzioni [!UICONTROL Advanced Settings], fai clic sull&#39;icona **[!UICONTROL More Actions]** ( ![Icona Altre azioni](/help/main/assets/icons/MoreSmallListVert.svg) ), quindi fai clic su **[!UICONTROL Advanced Settings]**.

![Menu Impostazioni avanzate](/help/main/c-activities/r-success-metrics/assets/advanced-settings-refresh.png)

>[!NOTE]
>
>Se utilizzi [!DNL Adobe Analytics] come origine per la generazione dei rapporti, le impostazioni vengono gestite dal server [!DNL Analytics]. L&#39;opzione [!UICONTROL Advanced Settings] non sarà disponibile. Per ulteriori informazioni, vedere [Adobe Analytics come origine per la generazione di rapporti per Adobe Target (A4T)](/help/main/c-integrating-target-with-mac/a4t/a4t.md).

### Aggiungi dipendenza

Puoi utilizzare le impostazioni avanzate per creare metriche di successo dipendenti, incrementando una metrica solo se un visitatore ha già raggiunto un’altra metrica.

Ad esempio, potresti rendere valida una conversione di test solo se un visitatore fa clic sull’offerta o raggiunge una determinata pagina prima della conversione.

La funzionalità di dipendenza *non* è supportata per:

* [!UICONTROL Recommendations] attività. Questa funzionalità è supportata da tutti gli altri tipi di attività.
* Se utilizzi [Analytics come origine per la generazione di rapporti](/help/main/c-integrating-target-with-mac/a4t/a4t.md) (A4T).
* Il tipo di metrica &quot;Visualizzazione di una pagina&quot;.
* Il tipo di metrica &quot;Clic su un elemento&quot; per le attività del Compositore esperienza visivo.

Le metriche di successo dipendenti non verranno convertite nei seguenti casi:

* Se crei una dipendenza circolare in cui metric1 dipende da metric2 e metric2 dipende da metric1, nessuna delle due metriche viene convertita.
* Le attività [!UICONTROL Automated Personalization] rilasciano gli utenti e riavviano l&#39;attività quando vengono raggiunte le metriche di conversione, pertanto le metriche dipendenti dalla metrica di conversione non verranno convertite.

### Cosa accade dopo che un utente incontra questa metrica per obiettivo?

Utilizza le impostazioni avanzate per determinare cosa succede dopo che un utente raggiunge la metrica obiettivo. Nella tabella seguente sono illustrate le opzioni disponibili:

| Quando un utente raggiunge la metrica obiettivo | Opzioni |
|--- |--- |
| [!UICONTROL Increment Count & Keep User in Activity] | Specifica come viene incrementato il conteggio:<ul><li>Una volta per partecipante (impostazione predefinita)</li><li>A ogni impression, escluso l’aggiornamento della pagina</li><li>A ogni impression</li></ul> |
| [!UICONTROL Increment Count, Release user, & Allow Reentry] | Seleziona l’esperienza che il visitatore vede se accede di nuovo all’attività:<ul><li>Stessa esperienza (impostazione predefinita)</li><li>Esperienza casuale</li><li>Esperienza non visualizzata</li></ul> |
| [!UICONTROL Increment Count, Release User, & Bar from Reentry] | Determina ciò che l’utente vede al posto del contenuto dell’attività:<ul><li>Stessa esperienza, senza tracciamento (impostazione predefinita)</li><li>Contenuto predefinito o contenuto di altra attività</li></ul> |

>[!NOTE]
>
>Se configuri una metrica in una delle opzioni [!UICONTROL Increment Count] (menzionate sopra), il conteggio delle metriche viene incrementato correttamente una volta per partecipante solo a livello di visitatore. Il conteggio delle metriche incrementa una volta per visita per ogni nuova sessione a livello di visita.

### Come verrà incrementato il conteggio:

Scegli il comportamento desiderato:

* Una volta per partecipante
* A ogni impression (esclusi aggiornamenti pagina)
* A ogni impression

## Problemi noti

* Le metriche di successo con l’opzione avanzata “Come verrà incrementato il conteggio?” impostata su “a ogni impression” o “a ogni impression (esclusi aggiornamenti pagina)” non possono essere utilizzate come metriche di successo da cui dipende un’altra metrica.

Quando una metrica di successo è impostata per essere incrementata a ogni impression, [!DNL Target] conta nuovamente il visitatore ogni volta che visita questa metrica di successo. [!DNL Target] reimposta quindi su 0 la metrica di successo &quot;appartenenza&quot; in modo che possa contare di nuovo sull&#39;impression successiva. Pertanto, se un&#39;altra metrica richiede che questa metrica sia stata vista per prima, [!DNL Target] non riconosce mai che l&#39;utente ha visto la prima metrica.

## Video di formazione: Metriche di attività

In questo video viene illustrato come utilizzare le metriche dell&#39;attività.

* Le metriche per “Obiettivo”
* Concetti e creazione di metriche per conversione, ricavi e coinvolgimento
* Creazione di una metrica di tracciamento dei clic

>[!VIDEO](https://video.tv.adobe.com/v/17380)
