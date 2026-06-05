---
keywords: Consigli;offerta;anteprima;lancio;stato;criteri;algoritmo
description: Scopri come visualizzare in anteprima la tua attività Adobe [!DNL Target] Recommendations per assicurarti che i risultati siano disponibili prima di avviare l'attività.
title: Come posso visualizzare in anteprima e avviare un’attività Consigli?
feature: Recommendations
hide: true
hidefromtoc: true
source-git-commit: 1be09adbab3db2c0cf4447b8abba06ca26cf5571
workflow-type: tm+mt
source-wordcount: '1444'
ht-degree: 14%

---

# Anteprima e avvio di un’attività Consigli

Dopo aver creato l&#39;attività [!UICONTROL Consigli], [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] (XT) contenente [Offerte Consigli](/help/main/c-recommendations/recommendations-as-an-offer.md), è necessario visualizzare in anteprima i consigli per assicurarsi che siano disponibili i risultati prima di avviare l&#39;attività. [!DNL Target Recommendations] offre diversi modi per visualizzare in anteprima i consigli.

## Verifica dello stato dell’algoritmo di Recommendations

Dopo aver creato un&#39;attività, [!DNL Recommendations] esegue un algoritmo per generare i consigli. L’esecuzione di questo algoritmo potrebbe richiedere alcune ore.

Puoi verificare se l&#39;algoritmo ha terminato l&#39;esecuzione nel diagramma di panoramica [!UICONTROL Attività], in cui è elencato lo stato dei criteri. La figura seguente mostra lo stato nel diagramma attività nella pagina [!UICONTROL Panoramica] di un&#39;attività [!DNL Recommendations]:

![Pagina di panoramica dell&#39;attività Consigli](/help/main/c-recommendations/t-create-recs-activity/assets/recs-overview-new.png)

I risultati dello stato includono quanto segue, come illustrato di seguito:

* [!UICONTROL Risultati pronti]: indica che l&#39;algoritmo ha restituito dei risultati
* [!UICONTROL Risultati non pronti]: indica che l&#39;esecuzione dell&#39;algoritmo non è stata completata.
* [!UICONTROL Errore di feed]: indica che non è stato possibile recuperare il file di feed dei criteri personalizzato.

![Finestra di dialogo dei risultati](/help/main/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Quanto tempo ci vorrà per eseguire l&#39;algoritmo?

Dopo aver salvato un&#39;attività contenente un criterio, [!DNL Target] calcola i consigli in base alla raccolta, ai criteri, alla progettazione e alle promozioni selezionati. Il calcolo richiede un po’ di tempo, in base alla logica selezionata per i consigli, all’intervallo di dati, al numero di elementi nel catalogo, alla quantità di dati comportamentali generati dai clienti e all’origine selezionata per i dati comportamentali.

Quest’ultima influisce maggiormente sul tempo di elaborazione, come segue:

### mbox

Se come origini dei dati comportamentali sono selezionate delle mbox, i criteri creati vengono eseguiti subito. A seconda della quantità di dati comportamentali utilizzati e delle dimensioni del catalogo, l’esecuzione dell’algoritmo può richiedere fino a 12 ore. L’apporto di modifiche alla configurazione dei criteri comporta solitamente la riesecuzione dei criteri. A seconda della modifica apportata, i consigli calcolati in precedenza potrebbero non essere disponibili fino a quando non viene completata una nuova esecuzione oppure, per modifiche di maggiore entità, fino a quando non viene completata una nuova esecuzione potrebbero essere disponibili solo i contenuti di backup o predefiniti. Se un algoritmo non viene modificato, viene rieseguito automaticamente da [!DNL Target] ogni 12-48 ore, a seconda dell’intervallo di dati selezionato.

### [!DNL Adobe Analytics]

Se il criterio utilizza [!DNL Adobe Analytics] come origine dei dati comportamentali, l’eventuale utilizzo della suite di rapporti e dell’intervallo di lookback selezionati per altri criteri incide sul tempo che trascorre prima che il criterio creato diventi disponibile.

* **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. L’arco temporale dipende dal caricamento del sistema [!DNL Analytics].
* **Criteri nuovi o modificati che utilizzano una suite di rapporti già disponibile**: se crei un nuovo criterio o ne modifichi uno esistente e la suite di rapporti selezionata è già utilizzata per [!DNL Target Recommendations], con un intervallo di dati uguale o inferiore a quello selezionato, i dati saranno immediatamente disponibili e non sarà richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
* **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per il consiglio [!UICONTROL Affinità visualizzata], quando un utente visualizza un prodotto, a [!DNL Analytics] viene passata una chiamata di tracciamento per la visualizzazione del prodotto quasi in tempo reale. I dati di [!DNL Analytics] vengono inviati a [!DNL Target] all&#39;inizio del giorno successivo e [!DNL Target] esegue l&#39;algoritmo in meno di 12 ore.

>[!NOTE]
>
>[!UICONTROL Gli elementi visualizzati di recente] non richiedono l&#39;esecuzione di algoritmi offline e i risultati sono immediatamente disponibili. Gli algoritmi [!UICONTROL Più visualizzati] e [!UICONTROL Più venduti] basati sui dati mbox producono in genere risultati molto rapidamente grazie al calcolo più semplice richiesto. Queste possono essere buone opzioni quando vuoi visualizzare in anteprima una modifica alla progettazione o confermare che i dati comportamentali vengono raccolti correttamente.

## Utilizzo dei collegamenti di controllo qualità per visualizzare in anteprima i consigli

Quando i risultati dell&#39;algoritmo sono pronti, è possibile visualizzarli in anteprima utilizzando la funzionalità [Collegamento QA](/help/main/c-activities/c-activity-qa/activity-qa.md) di [!DNL Adobe Target]. I collegamenti di controllo qualità sono disponibili nella sezione [!UICONTROL Posizione attività] della pagina di panoramica [!UICONTROL Attività]:

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Target] ti aggiunge automaticamente al pubblico richiesto per il collegamento di controllo qualità. Se questa impostazione è disattivata e l&#39;attività dispone di regole di targeting, il profilo utente deve soddisfare tali regole di targeting per visualizzare l&#39;esperienza contenente i consigli.

L’utilizzo di un collegamento di controllo qualità consente di visualizzare in anteprima i consigli sulla pagina:

![Prodotti in primo piano](/help/main/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* La modalità di controllo qualità di Target è &quot;permanente&quot; e viene salvata in un cookie. Se non esci dalla modalità di controllo qualità, continuerai a visualizzare i risultati del controllo qualità in tutto il sito. Per uscire dalla modalità di controllo qualità, utilizzare [bookmarklet](/help/main/c-activities/c-activity-qa/activity-qa-bookmark.md).
>
>* In modalità di controllo qualità, l&#39;esplorazione del sito non influirà sui [!UICONTROL articoli visualizzati di recente] o [!UICONTROL articoli acquistati di recente] del profilo. Questo comportamento si verifica per progettazione per evitare un inquinamento involontario dei dati comportamentali di produzione. Per visualizzare in anteprima i risultati di un criterio di [!UICONTROL Elementi visualizzati di recente] o di [!UICONTROL Consigli basati sull&#39;utente], esplorare prima il sito al di fuori della modalità di controllo qualità e quindi utilizzare la stessa sessione per aprire un collegamento alla modalità di controllo qualità.

## Utilizzo del file CSV scaricabile per visualizzare in anteprima i consigli

In alcuni casi, potrebbe essere utile controllare gli elementi specifici consigliati. Questa funzione è particolarmente utile quando si utilizzano algoritmi come [!UICONTROL Persone che hanno visualizzato questo/a, hanno visualizzato quel/a], in cui si consiglia un diverso set di elementi a seconda dell&#39;elemento che l&#39;utente sta visualizzando e si potrebbero avere migliaia o milioni di elementi diversi nel catalogo.

I risultati non sono disponibili per il download finché non viene visualizzato uno stato [!UICONTROL Risultati pronti] per almeno un algoritmo nell&#39;attività.

Per scaricare i risultati per l&#39;anteprima, fai clic sull&#39;icona del menu nell&#39;angolo superiore destro della pagina Panoramica attività, quindi fai clic su **[!UICONTROL Scarica dati]**.

![Opzione per il download dei dati](/help/main/c-recommendations/t-create-recs-activity/assets/download-data.png)

È in corso il download di un file CSV. Aprilo per visualizzare gli articoli consigliati:

![File CSV elementi consigliati](/help/main/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Da sinistra a destra è un elenco di articoli consigliati, in questo caso quelli visualizzati più di frequente. I consigli sono separati per ambiente; in questo caso solo l’ambiente di produzione dispone di consigli.

Se un asterisco (*) è il primo valore di una riga, indica [elementi di backup](/help/main/c-recommendations/c-algorithms/backup-recs.md). Gli elementi di backup vengono visualizzati se non tutti gli slot di una progettazione possono essere riempiti dagli elementi consigliati dell’algoritmo (criteri).

Per altri tipi di algoritmo basati su un valore chiave, ad esempio [!UICONTROL Persone che hanno visualizzato questo/a, hanno visualizzato questo/a], i valori chiave (ovvero gli elementi &quot;Questo&quot;) sono elencati nella colonna più a sinistra e gli elementi consigliati (ovvero gli elementi &quot;Che&quot;) sono elencati da sinistra a destra nelle colonne Recommendation_X.

Tieni presente che per le attività con set di risultati molto grandi, l&#39;opzione **[!UICONTROL Scarica dati]** potrebbe non riuscire con l&#39;errore `Error while fetching recommendation data file.`. Ciò si verifica quando il CSV generato supera la dimensione della risposta che può essere restituita tramite l&#39;interfaccia utente in un singolo download.

>[!NOTE]
>
>I download dei risultati non sono disponibili per le attività contenenti un algoritmo di [!UICONTROL Consigli basati sull&#39;utente]. I download dei risultati non sono disponibili per i criteri che utilizzano la logica per i consigli [!UICONTROL Articoli visualizzati di recente].

## Attivazione dell’attività Consigli

Dalla scheda [!UICONTROL Panoramica attività], fai clic sulla freccia a discesa Stato, quindi seleziona **[!UICONTROL Attiva]**.

Se l&#39;attività [!UICONTROL Recommendations] è attualmente nello stato [!UICONTROL Inactive], l&#39;elenco a discesa è etichettato come [!UICONTROL Inactive].

Dopo alcuni secondi o pochi minuti, lo stato passa a [!UICONTROL Live].

Puoi anche disattivare o archiviare l’attività utilizzando lo stesso elenco a discesa.

## Evitare interruzioni durante la modifica delle impostazioni di Recommendations

La modifica di [!DNL Recommendations] raccolte, criteri, promozioni o impostazioni di progettazione in un&#39;attività live potrebbe causare la mancata validità dei risultati dell&#39;algoritmo e la modifica dello stato di un algoritmo in [!UICONTROL Risultati non pronti].

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
