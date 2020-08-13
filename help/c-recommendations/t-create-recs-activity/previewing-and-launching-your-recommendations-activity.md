---
keywords: Recommendations;offer;preview;launch
description: 'Dopo aver creato l''attività Recommendations, A/B Test o Experience Targeting (XT) contenente  offerte Adobe Target Recommendations, desiderate visualizzarla in anteprima per verificare che i risultati siano disponibili prima di avviare l''attività. In Target Recommendations sono disponibili diversi modi per visualizzare l''anteprima delle raccomandazioni. '
title: 'Dopo aver creato l''attività Recommendations, A/B Test o Experience Targeting (XT) contenente  offerte Adobe Target Recommendations, desiderate visualizzarla in anteprima per verificare che i risultati siano disponibili prima di avviare l''attività. In Target Recommendations sono disponibili diversi modi per visualizzare l''anteprima delle raccomandazioni. '
feature: recs creation
subtopic: Recommendations
translation-type: tm+mt
source-git-commit: 3cf1f4fa56f86c106dccdc2c97c080c17c3982b4
workflow-type: tm+mt
source-wordcount: '1398'
ht-degree: 19%

---


# Anteprima e avvio di un’attività Consigli

Dopo aver creato l&#39;attività [!UICONTROL Recommendations], Test A/B o Targeting  esperienza (XT) contenente le offerte [](/help/c-recommendations/recommendations-as-an-offer.md)Recommendations, desiderate visualizzare l&#39;anteprima delle raccomandazioni per assicurarvi che i risultati siano disponibili prima di avviare l&#39;attività. [!DNL Target Recommendations] offre diversi modi per visualizzare l&#39;anteprima delle raccomandazioni.

## Verifica dello stato dell’algoritmo Recommendations

Dopo aver creato un&#39;attività, [!DNL Recommendations] esegue un algoritmo per generare le raccomandazioni. L&#39;esecuzione di questo algoritmo potrebbe richiedere alcune ore.

Potete verificare se l&#39;algoritmo è stato completato nel diagramma di panoramica [!UICONTROL Attività] , in cui è elencato lo stato dei criteri. L&#39;illustrazione seguente mostra lo stato nel diagramma dell&#39;attività nella pagina [!DNL Recommendations] Panoramica  di un&#39;attività:

![Pagina Panoramica dell&#39;attività Recommendations](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

L&#39;illustrazione seguente illustra lo stato in una pagina [!UICONTROL A/B Test] o XT activity&#39;s [!UICONTROL Overview (Panoramica] dell&#39;attività XT):

![Pagina Panoramica test A/B](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

I risultati dello stato includono quanto segue:

* [!UICONTROL Risultati pronti]: Indica che l&#39;algoritmo ha restituito dei risultati
* [!UICONTROL Risultati non pronti]: Indica che l&#39;algoritmo non è stato completato.
* [!UICONTROL Errore]feed: Indica che non è stato possibile recuperare il file di feed dei criteri personalizzati.

![Risultati, finestra di dialogo](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Quanto tempo sarà necessario per l&#39;esecuzione dell&#39;algoritmo?

Dopo aver salvato un&#39;attività contenente un criterio, [!DNL Target] calcola le raccomandazioni in base alla raccolta, ai criteri, alla progettazione e alle promozioni selezionate. Il calcolo richiede un po’ di tempo, in base alla logica selezionata per la generazione dei consigli, all’intervallo di dati, alla quantità di elementi nel catalogo, alla quantità di dati comportamentali generati dai clienti e all’origine selezionata per i dati comportamentali.

Quest’ultima influisce maggiormente sul tempo di elaborazione, come segue:

### mbox

Se come origini dei dati comportamentali sono selezionate delle mbox, i criteri creati vengono eseguiti subito. A seconda della quantità di dati comportamentali utilizzati e delle dimensioni del catalogo, l’esecuzione dell’algoritmo può richiedere fino a 12 ore. L’apporto di modifiche alla configurazione dei criteri comporta solitamente la riesecuzione dei criteri. A seconda delle modifiche apportate, le raccomandazioni calcolate in precedenza potrebbero essere disponibili solo al termine di una nuova esecuzione, oppure, per modifiche di dimensioni maggiori, solo il contenuto di backup o predefinito sarà disponibile fino al completamento di una nuova esecuzione. Se un algoritmo non viene modificato, viene rieseguito automaticamente da [!DNL Target] ogni 12-48 ore, a seconda dell’intervallo di dati selezionato.

### Adobe Analytics

Se il criterio utilizza [!DNL Adobe Analytics] come origine dei dati comportamentali, l’eventuale utilizzo della suite di rapporti e dell’intervallo di lookback selezionati per altri criteri incide sul tempo che trascorre prima che il criterio creato diventi disponibile.

* **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. Il tempo necessario dipende dal caricamento del sistema [!DNL Analytics].
* **Criteri nuovi o modificati utilizzando una suite** di rapporti già disponibile: Quando si crea un nuovo criterio o si modifica un criterio esistente, se la suite di rapporti selezionata è già stata utilizzata con [!DNL Target Recommendations], con un intervallo di dati uguale o inferiore all&#39;intervallo di dati selezionato, i dati sono immediatamente disponibili e non è richiesta alcuna impostazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
* **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per un consiglio di tipo [!UICONTROL Affinità per articoli visualizzati], quando un utente visualizza un prodotto, a [!DNL Analytics] viene trasmessa una chiamata di tracciamento per visualizzazione prodotto quasi in tempo reale. The [!DNL Analytics] data is pushed to [!DNL Target] early the next day and [!DNL Target] runs the algorithm in fewer than 12 hours.

>[!NOTE]
>
>[!UICONTROL Gli elementi] visualizzati di recente non richiedono l&#39;esecuzione di un algoritmo offline e i risultati sono immediatamente disponibili. [!UICONTROL Gli algoritmi Top View] e [!UICONTROL Top Sellers] basati su dati mbox generalmente producono risultati molto rapidamente a causa del calcolo più semplice richiesto. Queste possono essere buone opzioni quando si desidera visualizzare l&#39;anteprima di una modifica di progettazione o confermare che i dati comportamentali vengono raccolti correttamente.

## Utilizzo dei collegamenti QA per l&#39;anteprima di Recommendations

Una volta pronti i risultati per l&#39;algoritmo, potete visualizzare l&#39;anteprima dei risultati utilizzando la funzionalità di collegamento [](/help/c-activities/c-activity-qa/activity-qa.md) QA di [!DNL Adobe Target]. I collegamenti QA sono disponibili nella sezione [!UICONTROL Activity QA] della pagina di panoramica dell&#39;attività:

![Collegamento Controllo di qualità attività](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Per impostazione predefinita, ti aggiunge [!DNL Target] automaticamente al pubblico richiesto per il collegamento QA. Se questa impostazione è disattivata e l&#39;attività ha regole di targeting, il profilo utente deve rispettare tali regole di targeting per visualizzare l&#39;esperienza che contiene le raccomandazioni.

L&#39;utilizzo di un collegamento di controllo qualità consente di visualizzare in anteprima le raccomandazioni sulla pagina:

![Prodotti](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>La modalità QA di destinazione è &quot;appiccicosa&quot; e salvata in un cookie. Se non uscite dalla modalità di controllo qualità, continuerete a visualizzare i risultati di tale controllo in tutto il sito. Per uscire dalla modalità QA, utilizzare il [bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).

>[!NOTE]
>
>In modalità QA, la navigazione sul sito non influirà sugli articoli [!UICONTROL visualizzati di] recente o sugli articoli [!UICONTROL acquistati]di recente del profilo.&quot; Questo comportamento si verifica in base alla progettazione per evitare l&#39;inquinamento accidentale dei dati comportamentali di produzione. Per visualizzare in anteprima i risultati di un [!UICONTROL visualizzatore recente di elementi] o criteri Recommendations [!UICONTROL basati su] utente, prima sfogliate il sito al di fuori della modalità QA, quindi utilizzate la stessa sessione per aprire un collegamento in modalità QA.

## Utilizzo del download CSV per visualizzare in anteprima le raccomandazioni

In alcuni casi, potrebbe essere utile controllare gli elementi specifici consigliati. Questo è particolarmente utile quando si utilizzano algoritmi come [!UICONTROL Persone che hanno visualizzato questo, Visualizzato che], dove viene consigliato un diverso set di elementi a seconda dell&#39;elemento che l&#39;utente sta visualizzando attualmente, e si potrebbero avere migliaia o milioni di elementi diversi nel catalogo.

I risultati non sono disponibili per il download fino a quando non viene visualizzato uno stato Pronto [!UICONTROL per i] risultati per almeno un algoritmo nell&#39;attività.

Per scaricare i risultati per l&#39;anteprima, fate clic sull&#39;icona del menu nell&#39;angolo superiore destro della pagina Panoramica dell&#39;attività, quindi fate clic su **[!UICONTROL Scarica dati]**.

![Opzione di download dei dati](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

È in corso il download di un file CSV. Aprirlo per visualizzare gli elementi consigliati:

![Elementi consigliati, file CSV](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Da sinistra a destra è riportato un elenco degli elementi consigliati, in questo caso quelli visualizzati più di frequente. Le raccomandazioni sono separate per ambiente, in questo caso solo l&#39;ambiente di produzione ha raccomandazioni. Per questo algoritmo, non sono state applicate restrizioni basate sul valore chiave, pertanto la riga con un asterisco (*) contiene l&#39;intero set di raccomandazioni. Per altri tipi di algoritmo basati su un valore chiave, come [!UICONTROL Persone che hanno visualizzato questo, che]i valori chiave (cioè gli elementi &quot;This&quot;) sono elencati nella colonna più a sinistra e gli elementi consigliati (cioè gli elementi &quot;That&quot;) sono elencati da sinistra a destra nelle colonne Recommendation_X.

>[!NOTE]
>
>I download dei risultati non sono disponibili per le attività contenenti un algoritmo Recommendations [!UICONTROL basato su] utente. I download dei risultati non sono disponibili per i criteri che utilizzano la logica di raccomandazione Elementi [!UICONTROL visualizzati di] recente.

## Attivazione dell&#39;attività Recommendations

Dalla scheda Panoramica  attività, fare clic sulla freccia a discesa accanto allo stato, quindi selezionare **[!UICONTROL Attiva]**.

![Attiva, opzione](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Lo stato diventa [!UICONTROL Attivazione]:

![Attivazione](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Dopo alcuni secondi o due minuti, lo stato passa a [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Potete anche disattivare o archiviare l&#39;attività utilizzando lo stesso elenco a discesa.

## Evitare interruzioni durante la modifica delle impostazioni di Recommendations

La modifica delle [!DNL Recommendations] raccolte, dei criteri, delle promozioni o delle impostazioni di progettazione in un&#39;attività live potrebbe causare la mancata validità dei risultati dell&#39;algoritmo e la modifica dello stato di un algoritmo in [!UICONTROL Risultati non pronti].

Per evitare di interrompere un&#39;attività live, è consigliabile adottare il seguente approccio quando si modifica un&#39;attività live:

1. Duplicate l&#39;attività e i criteri da modificare.
1. Apportate modifiche all&#39;attività e ai criteri duplicati e attendete che l&#39;algoritmo generi risultati.
1. Visualizzate l&#39;anteprima della nuova attività modificata e verificate che i risultati siano quelli desiderati.
1. Attiva la nuova attività.
1. Disattivate la vecchia attività.

Se è necessario mantenere i risultati storici dei report nella stessa attività, è possibile adottare un approccio alternativo, che potrebbe causare un&#39;interruzione temporanea della disponibilità delle raccomandazioni:

1. Duplicate l&#39;attività e i criteri da modificare.
1. Apportate modifiche all&#39;attività e ai criteri duplicati e attendete che l&#39;algoritmo generi risultati.
1. Visualizzate l&#39;anteprima della nuova attività modificata e verificate che i risultati siano quelli desiderati.
1. Metti in pausa l&#39;attività esistente e sostituisci le impostazioni/i criteri con i nuovi criteri.
1. Visualizzate l&#39;anteprima dell&#39;attività esistente e confermate che i risultati siano quelli desiderati.
1. Riattivate l&#39;attività.
