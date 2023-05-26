---
keywords: Recommendations;offerta;anteprima;lancio;stato;criteri;algoritmo
description: Scopri come visualizzare in anteprima il tuo Adobe [!DNL Target] Attività Recommendations per garantire la disponibilità dei risultati prima di avviare l’attività.
title: Come posso visualizzare in anteprima e avviare un’attività di Recommendations?
feature: Recommendations
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
source-git-commit: 7732f3af0fd995309035a8a214afd438ab7a1823
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 17%

---

# Anteprima e avvio di un’attività Consigli

Dopo aver creato il [!UICONTROL Recommendations], [!UICONTROL Test A/B], o [!UICONTROL Targeting esperienza] (XT) attività contenente [Offerte Recommendations](/help/main/c-recommendations/recommendations-as-an-offer.md), ti consigliamo di visualizzare in anteprima i consigli per assicurarti che i risultati siano disponibili prima di avviare l’attività. [!DNL Target Recommendations] offre diversi modi per visualizzare in anteprima i consigli.

## Verifica dello stato dell’algoritmo di Recommendations

Dopo aver creato un’attività, [!DNL Recommendations] esegue un algoritmo per generare i consigli. L’esecuzione di questo algoritmo potrebbe richiedere alcune ore.

Puoi verificare se l’algoritmo è stato eseguito correttamente nel [!UICONTROL Attività] diagramma di panoramica, in cui è elencato lo stato dei criteri. L’illustrazione seguente mostra lo stato nel diagramma dell’attività su un [!DNL Recommendations] dell&#39;attività [!UICONTROL Panoramica] pagina:

![Pagina Panoramica dell’attività Recommendations](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

Nella figura seguente viene illustrato lo stato di una [!UICONTROL Test A/B] o XT dell’attività [!UICONTROL Panoramica] pagina:

![Pagina Panoramica test A/B](/help/main/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

I risultati dello stato includono quanto segue, come illustrato di seguito:

* [!UICONTROL Risultati pronti]: indica che l’algoritmo ha restituito dei risultati
* [!UICONTROL Risultati non pronti]: indica che l’esecuzione dell’algoritmo non è stata completata.
* [!UICONTROL Errore di feed]: indica che non è stato possibile recuperare il file di feed dei criteri personalizzato.

![Finestra di dialogo Risultati](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Quanto tempo ci vorrà per eseguire l&#39;algoritmo?

Dopo aver salvato un’attività contenente un criterio, [!DNL Target] calcola i consigli in base alla raccolta, ai criteri, alla progettazione e alle promozioni selezionati. Il calcolo richiede un po’ di tempo, in base alla logica selezionata per i consigli, all’intervallo di dati, al numero di elementi nel catalogo, alla quantità di dati comportamentali generati dai clienti e all’origine selezionata per i dati comportamentali.

Quest’ultima influisce maggiormente sul tempo di elaborazione, come segue:

### mbox

Se come origini dei dati comportamentali sono selezionate delle mbox, i criteri creati vengono eseguiti subito. A seconda della quantità di dati comportamentali utilizzati e delle dimensioni del catalogo, l’esecuzione dell’algoritmo può richiedere fino a 12 ore. L’apporto di modifiche alla configurazione dei criteri comporta solitamente la riesecuzione dei criteri. A seconda della modifica apportata, i consigli calcolati in precedenza potrebbero non essere disponibili fino a quando non viene completata una nuova esecuzione oppure, per modifiche di maggiore entità, fino a quando non viene completata una nuova esecuzione potrebbero essere disponibili solo i contenuti di backup o predefiniti. Se un algoritmo non viene modificato, viene rieseguito automaticamente da [!DNL Target] ogni 12-48 ore, a seconda dell’intervallo di dati selezionato.

### Adobe Analytics

Se il criterio utilizza [!DNL Adobe Analytics] come origine dei dati comportamentali, l’eventuale utilizzo della suite di rapporti e dell’intervallo di lookback selezionati per altri criteri incide sul tempo che trascorre prima che il criterio creato diventi disponibile.

* **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. Il tempo necessario dipende dal caricamento del sistema [!DNL Analytics].
* **Criteri nuovi o modificati che utilizzano una suite di rapporti già disponibile**: quando crei un nuovo criterio o ne modifichi uno esistente, se la suite di rapporti selezionata è già stata utilizzata con [!DNL Target Recommendations], con un intervallo di dati uguale o inferiore a quello selezionato, i dati sono immediatamente disponibili e non è richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
* **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per un consiglio di tipo [!UICONTROL Affinità per articoli visualizzati], quando un utente visualizza un prodotto, a [!DNL Analytics] viene trasmessa una chiamata di tracciamento per visualizzazione prodotto quasi in tempo reale. Il [!DNL Analytics] i dati vengono inviati a [!DNL Target] all&#39;inizio del giorno successivo [!DNL Target] esegue l’algoritmo in meno di 12 ore.

>[!NOTE]
>
>[!UICONTROL Articoli visualizzati di recente] non richiede l’esecuzione di algoritmi offline e i risultati sono immediatamente disponibili. [!UICONTROL Più visualizzati] e [!UICONTROL Articoli più venduti] gli algoritmi basati sui dati mbox generalmente producono risultati molto rapidamente a causa del calcolo più semplice richiesto. Queste possono essere buone opzioni quando vuoi visualizzare in anteprima una modifica alla progettazione o confermare che i dati comportamentali vengono raccolti correttamente.

## Utilizzo dei collegamenti di controllo qualità per l’anteprima di Recommendations

Quando i risultati dell’algoritmo sono pronti, puoi visualizzarli in anteprima utilizzando [Collegamento Controllo di qualità](/help/main/c-activities/c-activity-qa/activity-qa.md) funzionalità di [!DNL Adobe Target]. I collegamenti di controllo qualità sono disponibili nella [!UICONTROL Controllo di qualità delle attività] sezione della pagina Panoramica attività:

![Collegamento Controllo di qualità attività](/help/main/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Target] ti aggiunge automaticamente al pubblico richiesto per il collegamento di controllo qualità. Se questa impostazione è disattivata e l&#39;attività dispone di regole di targeting, il profilo utente deve soddisfare tali regole di targeting per visualizzare l&#39;esperienza contenente i consigli.

L’utilizzo di un collegamento di controllo qualità consente di visualizzare in anteprima i consigli sulla pagina:

![Prodotti in evidenza](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* La modalità di controllo qualità di Target è &quot;permanente&quot; e viene salvata in un cookie. Se non esci dalla modalità di controllo qualità, continuerai a visualizzare i risultati del controllo qualità in tutto il sito. Per uscire dalla modalità di controllo qualità, utilizza [bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* In modalità di controllo qualità, la navigazione nel sito non influirà sui [!UICONTROL Articoli visualizzati di recente] o [!UICONTROL Articoli acquistati di recente]. Questo comportamento si verifica per progettazione per evitare un inquinamento involontario dei dati comportamentali di produzione. Per visualizzare in anteprima i risultati da un [!UICONTROL Articoli visualizzati di recente] o [!UICONTROL Recommendations basato su utente] criteri, esplora il sito all’esterno della modalità di controllo qualità, quindi utilizza la stessa sessione per aprire un collegamento alla modalità di controllo qualità.


## Utilizzo del file CSV scaricabile per visualizzare in anteprima i consigli

In alcuni casi, potrebbe essere utile controllare gli elementi specifici consigliati. Questa funzione è particolarmente utile quando si utilizzano algoritmi come [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello], in cui è consigliabile utilizzare un set di elementi diverso a seconda dell&#39;elemento attualmente visualizzato dall&#39;utente e nel catalogo potrebbero essere presenti migliaia o milioni di elementi diversi.

I risultati non sono disponibili per il download fino al [!UICONTROL Risultati pronti] Lo stato viene visualizzato per almeno un algoritmo nell’attività.

Per scaricare i risultati per l’anteprima, fai clic sull’icona del menu nell’angolo in alto a destra della pagina Panoramica attività, quindi fai clic su **[!UICONTROL Scarica dati]**.

![Opzione Scarica dati](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

È in corso il download di un file CSV. Aprilo per visualizzare gli articoli consigliati:

![File CSV di articoli consigliati](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Da sinistra a destra è un elenco di articoli consigliati, in questo caso quelli visualizzati più di frequente. I consigli sono separati per ambiente; in questo caso solo l’ambiente di produzione dispone di consigli. Per questo algoritmo, non sono state applicate restrizioni in base al valore chiave, pertanto la riga contrassegnata con un asterisco (*) contiene l’intero set di consigli. Per altri tipi di algoritmo basati su un valore chiave, ad esempio [!UICONTROL Chi ha visualizzato questo ha visualizzato anche quello], i valori chiave (ovvero gli elementi &quot;Questo&quot;) sono elencati nella colonna più a sinistra e gli elementi consigliati (ovvero gli elementi &quot;Che&quot;) sono elencati da sinistra a destra nelle colonne Recommendation_X.

>[!NOTE]
>
>I download dei risultati non sono disponibili per le attività che contengono [!UICONTROL Recommendations basato su utente] algoritmo. I download dei risultati non sono disponibili per i criteri che utilizzano [!UICONTROL Articoli visualizzati di recente] logica per i consigli.

## Attivazione dell’attività Recommendations

Dalla sezione [!UICONTROL Panoramica delle attività] , fai clic sulla freccia a discesa accanto allo stato, quindi seleziona **[!UICONTROL Attiva]**.

![Attiva, opzione](/help/main/c-recommendations/t-create-recs-activity/assets/activate.png)

Lo stato diventa [!UICONTROL Attivazione]:

![Attivazione](/help/main/c-recommendations/t-create-recs-activity/assets/activating.png)

Dopo alcuni secondi o un paio di minuti, lo stato passa a [!UICONTROL Live]:

![Live](/help/main/c-recommendations/t-create-recs-activity/assets/live.png)

Puoi anche disattivare o archiviare l’attività utilizzando lo stesso elenco a discesa.

## Evitare interruzioni durante la modifica delle impostazioni di Recommendations

Modifica [!DNL Recommendations] raccolte, criteri, promozioni o impostazioni di progettazione in un’attività live potrebbero impedire la validità dei risultati dell’algoritmo e modificare lo stato di un algoritmo in [!UICONTROL Risultati non pronti].

Per evitare di interrompere un’attività live, si consiglia di adottare il seguente approccio durante la modifica di un’attività live:

1. Duplica l’attività originale (attività 1) e i criteri che desideri modificare per creare una nuova attività (attività 2).
1. Modifica l’attività duplicata (attività 2) e i criteri, quindi attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima della nuova attività modificata (attività 2) e conferma che i risultati corrispondano alle tue esigenze.
1. Attiva la nuova attività (attività 2).
1. Disattiva l’attività originale (attività 1).

Se devi conservare i risultati dei rapporti storici nella stessa attività, è possibile un approccio alternativo che potrebbe causare un’interruzione temporanea della disponibilità dei consigli:

1. Duplica l’attività originale (attività 1) e i criteri che desideri modificare per creare una nuova attività (attività 2).
1. Modifica l’attività duplicata (attività 2) e i criteri, quindi attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima della nuova attività modificata (attività 2) e conferma che i risultati corrispondano alle tue esigenze.
1. Sospendi la nuova attività modificata (attività 2) e cambia le impostazioni/criteri con l’attività originale (attività 1).
1. Visualizza l’anteprima dell’attività originale (attività 1) e conferma che i risultati corrispondano alle tue esigenze.
1. Riattiva l’attività originale (attività 1).
