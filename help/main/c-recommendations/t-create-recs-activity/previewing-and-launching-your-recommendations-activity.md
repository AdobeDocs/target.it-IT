---
keywords: Consigli;offerta;anteprima;lancio;stato;criteri;algoritmo
description: Scopri come visualizzare in anteprima l’attività Consigli di Adobe [!DNL Target] per garantire che i risultati siano disponibili prima di avviare l’attività.
title: Come posso visualizzare in anteprima e avviare un’attività Consigli?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
TQID: 'https://experienceleague.adobe.com/21swhpZie0QN09m0LB7VwVO-9U6GWxQ0kbthPlnns18'
product_v2:
  - id: e43347a8-f2c5-4aa4-8623-6f13875d7e3a
    internal-label: Target
feature_v2:
  - id: f69bc5f1-ebdb-4306-a281-f2e77daf734c
    internal-label: Activities and tests
subfeature_v2:
  - id: ed58f4a1-16eb-4c8c-b505-be9da766a9ec
    internal-label: Recommendations
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c4147b6e-073b-4d3c-9ab1-d60f2f4434ef
    internal-label: Behavioral data
source-git-commit: 1ca30ccbd1acc115980ffe3780ba6c0dbb343806
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%
---
# Anteprima e avvio di un’attività Consigli {#preview-launch-recs-activity}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come controllare lo stato dell&#39;algoritmo, visualizzare in anteprima i consigli e attivare un&#39;attività [!DNL Recommendations].

>[!ENDSHADEBOX]

L’anteprima dei consigli prima di avviare un’attività conferma la disponibilità dei risultati. Ciò si applica alle [!UICONTROL attività Consigli], [!UICONTROL Test A/B] e [!UICONTROL Targeting esperienza] (XT) che contengono [Offerte Consigli](/help/main/c-recommendations/recommendations-as-an-offer.md). [!DNL Target Recommendations] offre diversi modi per visualizzare in anteprima i consigli.

## Controllare lo stato dell’algoritmo {#check-status}

Dopo la creazione di un&#39;attività, [!DNL Recommendations] esegue un algoritmo per generare i consigli. L’esecuzione di questo algoritmo potrebbe richiedere alcune ore.

Lo stato dell&#39;algoritmo è elencato con i criteri nel diagramma attività nella pagina **[!UICONTROL Panoramica]** dell&#39;attività [!DNL Recommendations].

![Pagina di panoramica dell&#39;attività Consigli](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview-new.png)

Lo stato può essere uno dei seguenti:

* **[!UICONTROL Risultati pronti]**: l&#39;algoritmo ha restituito dei risultati.
* **[!UICONTROL Risultati non pronti]**: l&#39;esecuzione dell&#39;algoritmo non è stata completata.
* **[!UICONTROL Errore di feed]**: impossibile recuperare il file di feed dei criteri personalizzato.

![Finestra di dialogo dei risultati](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Stimare il tempo di esecuzione dell’algoritmo {#algorithm-run-time}

Dopo il salvataggio di un&#39;attività che contiene un criterio, [!DNL Target] calcola i consigli in base alla raccolta, ai criteri, alla progettazione e alle promozioni selezionate. Il tempo necessario dipende dalla logica dei consigli, dall’intervallo di dati, dal numero di elementi nel catalogo, dalla quantità di dati comportamentali generati dai clienti e dall’origine dei dati comportamentali. L’origine dei dati comportamentali ha il maggiore impatto sul tempo di elaborazione.

### mbox

Quando le mbox sono l’origine dei dati comportamentali, i criteri vengono eseguiti subito dopo la creazione. A seconda della quantità di dati comportamentali e delle dimensioni del catalogo, l’esecuzione dell’algoritmo può richiedere fino a 12 ore.

Le modifiche alla configurazione dei criteri in genere causano la riesecuzione dell’algoritmo. A seconda della modifica, i consigli calcolati in precedenza potrebbero non essere disponibili fino al completamento della nuova esecuzione. Per modifiche di grandi dimensioni, è disponibile solo il contenuto di backup o predefinito fino al completamento della nuova esecuzione.

Un algoritmo non modificato viene rieseguito automaticamente da [!DNL Target] ogni 12-48 ore, a seconda dell&#39;intervallo di dati selezionato.

### [!DNL Adobe Analytics]

Quando [!DNL Adobe Analytics] è l&#39;origine dei dati comportamentali, il tempo fino a quando i criteri non sono disponibili dipende dal fatto che la suite di rapporti e l&#39;intervallo di lookback selezionati siano già stati utilizzati per altri criteri. La prima volta che una suite di rapporti viene utilizzata con un intervallo di lookback specificato, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare i dati comportamentali da [!DNL Analytics].

Per informazioni sulla tempistica dei criteri nuovi o modificati e delle esecuzioni in corso dell&#39;algoritmo, vedere il menu a discesa **Disponibilità dei criteri quando Analytics è l&#39;origine dati** in [Data Source](/help/main/c-recommendations/c-algorithms/create-new-algorithm.md#data-source).

>[!NOTE]
>
>**[!UICONTROL Gli elementi visualizzati di recente]** non richiedono l&#39;esecuzione di un algoritmo offline e i risultati sono immediatamente disponibili. Gli algoritmi **[!UICONTROL Più visualizzati]** e **[!UICONTROL Più venduti]** basati sui dati mbox generalmente producono risultati molto rapidamente perché il calcolo è più semplice. Questi algoritmi sono buone opzioni per visualizzare in anteprima una modifica alla progettazione o per confermare che i dati comportamentali vengono raccolti correttamente.

## Anteprima con un collegamento di controllo qualità {#preview-qa-link}

Quando i risultati dell&#39;algoritmo sono pronti, è possibile visualizzarli in anteprima con la funzionalità [Collegamento controllo qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) di [!DNL Adobe Target]. I collegamenti di controllo qualità sono disponibili nella sezione **[!UICONTROL Posizione attività]** della pagina di panoramica **[!UICONTROL Attività]** e consentono di visualizzare i consigli nella pagina.

![Prodotti in primo piano](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Target] aggiunge automaticamente l&#39;utente al pubblico richiesto per il collegamento di controllo qualità. Se questa impostazione è disattivata e l’attività dispone di regole di targeting, il profilo utente deve soddisfare tali regole di targeting per visualizzare l’esperienza che contiene i consigli.

La modalità di controllo qualità prevede i seguenti comportamenti:

* La modalità di controllo qualità di [!DNL Target] viene salvata in un cookie e persiste tra le pagine. Se non si esce dalla modalità di controllo qualità, i risultati del controllo qualità continuano a essere visualizzati in tutto il sito. Per uscire dalla modalità di controllo qualità, utilizzare [bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
* In modalità di controllo qualità, la navigazione nel sito non influisce sui **[!UICONTROL articoli visualizzati di recente]** o **[!UICONTROL articoli acquistati di recente]** del profilo. Questo comportamento è progettato per evitare un inquinamento involontario dei dati comportamentali di produzione. Per visualizzare in anteprima i risultati di un criterio di **[!UICONTROL Elementi visualizzati di recente]** o di **[!UICONTROL Consigli basati sull&#39;utente]**, esplorare prima il sito al di fuori della modalità di controllo qualità e quindi utilizzare la stessa sessione per aprire un collegamento alla modalità di controllo qualità.

## Anteprima con il file CSV scaricabile {#preview-csv}

Il download dei risultati consente di controllare gli elementi consigliati specifici. Questo è particolarmente utile per algoritmi come **[!UICONTROL Persone che hanno visualizzato questo/a, hanno visualizzato quel/a]**, in cui gli elementi consigliati dipendono dall&#39;elemento attualmente visualizzato dal visitatore e il catalogo può contenere migliaia o milioni di elementi diversi.

1. Attendi che venga visualizzato lo stato **[!UICONTROL Risultati pronti]** per almeno un algoritmo nell&#39;attività. I risultati non sono prima disponibili per il download.

1. Nella pagina della panoramica dell&#39;**[!UICONTROL Attività]**, fai clic sull&#39;icona del menu nell&#39;angolo superiore destro, quindi fai clic su **[!UICONTROL Scarica dati]**.

   ![Opzione per il download dei dati](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

1. Apri il file CSV scaricato per visualizzare gli elementi consigliati.

   ![File CSV elementi consigliati](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Nel file sono elencati gli elementi consigliati da sinistra a destra, in questo esempio quelli visualizzati più di frequente. I consigli sono separati per ambiente. In questo esempio, solo l’ambiente di produzione dispone di consigli.

Una riga che inizia con un asterisco (*) elenca [elementi di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md). Gli elementi di backup vengono visualizzati quando gli elementi consigliati dell’algoritmo (criteri) non possono riempire tutti gli slot di una progettazione.

Per gli algoritmi basati su un valore chiave, ad esempio **[!UICONTROL Persone che hanno visualizzato questo, hanno visualizzato quel]**, i valori chiave (gli elementi &quot;Questo&quot;) si trovano nella colonna più a sinistra. Gli elementi consigliati (gli elementi &quot;che&quot;) sono elencati da sinistra a destra nelle colonne Recommendation_X.

Per le attività con set di risultati molto grandi, l&#39;opzione **[!UICONTROL Scarica dati]** potrebbe non riuscire con l&#39;errore `Error while fetching recommendation data file.`. Ciò si verifica quando il CSV generato supera le dimensioni di risposta che l&#39;interfaccia utente può restituire in un singolo download.

>[!NOTE]
>
>I download dei risultati non sono disponibili per le attività che contengono un algoritmo di **[!UICONTROL Consigli basati sull&#39;utente]** o per i criteri che utilizzano la logica di **[!UICONTROL Articoli visualizzati di recente]** per i consigli.

### Formato di download CSV per algoritmi basati sulla popolarità e su chiavi {#format}

Il file CSV scaricabile riflette in modo coerente i risultati generati dopo l’esecuzione dei criteri di back-end.

* **Algoritmi basati sulla popolarità (non basati su chiave)**: il file include:

  * Una riga di consigli di backup con prefisso (*)
  * Una riga separata che elenca i consigli in base alle impostazioni dell’algoritmo

* **Algoritmi basati su chiavi**: il file include:

  * Una riga di backup, come per gli algoritmi basati sulla popolarità
  * Righe multiple in formato chiave-valore, dove la prima voce è l’ID prodotto della chiave, seguita da ID prodotto separati da virgole che rappresentano i candidati per i consigli

## Attivare l’attività {#activate-activity}

Quando si attiva l&#39;attività, questa viene avviata e il suo stato cambia in **[!UICONTROL Live]**.

Dalla scheda **[!UICONTROL Panoramica attività]**, fai clic sulla freccia a discesa **[!UICONTROL Stato]**, quindi seleziona **[!UICONTROL Attiva]**. Se l&#39;attività è attualmente nello stato **[!UICONTROL Inattivo]**, l&#39;elenco a discesa è etichettato come **[!UICONTROL Inattivo]**. Dopo alcuni secondi o pochi minuti, lo stato passa a **[!UICONTROL Live]**.

Lo stesso elenco a discesa può essere utilizzato anche per disattivare o archiviare l’attività.

## Evitare interruzioni durante la modifica delle impostazioni {#avoid-disruptions}

La modifica di [!DNL Recommendations] raccolte, criteri, promozioni o impostazioni di progettazione in un&#39;attività live potrebbe invalidare i risultati dell&#39;algoritmo e modificare lo stato di un algoritmo in **[!UICONTROL Risultati non pronti]**.

Per evitare di interrompere un’attività live, l’approccio consigliato consiste nel modificare una copia dell’attività e quindi sostituire l’originale:

1. Duplica l’attività originale (attività 1) e i criteri da modificare, per creare una nuova attività (attività 2).
1. Apporta le modifiche all’attività duplicata (attività 2) e ai relativi criteri, quindi attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima dell’attività modificata (attività 2) e conferma che i risultati siano quelli desiderati.
1. Attiva la nuova attività (attività 2).
1. Disattiva l’attività originale (attività 1).

Quando i risultati storici delle segnalazioni devono essere mantenuti nella stessa attività, è possibile un approccio alternativo. Questo approccio potrebbe causare un’interruzione temporanea della disponibilità dei consigli:

1. Duplica l’attività originale (attività 1) e i criteri da modificare, per creare una nuova attività (attività 2).
1. Apporta le modifiche all’attività duplicata (attività 2) e ai relativi criteri, quindi attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima dell’attività modificata (attività 2) e conferma che i risultati siano quelli desiderati.
1. Sospendi l’attività modificata (attività 2) e cambia le impostazioni e i criteri con l’attività originale (attività 1).
1. Visualizza l’anteprima dell’attività originale (attività 1) e conferma che i risultati siano quelli desiderati.
1. Riattiva l’attività originale (attività 1).
