---
keywords: Recommendations;offerta;anteprima;lancio;stato;criteri;algoritmo
description: 'Scopri come visualizzare in anteprima l’attività Adobe [!DNL Target] Recommendations per garantire che i risultati siano disponibili prima di avviare l’attività. '
title: Come posso visualizzare in anteprima e avviare un'attività Recommendations?
feature: Consigli
exl-id: 60391778-4d48-4c41-a7c5-fedcfabf2530
translation-type: tm+mt
source-git-commit: a92e88b46c72971d5d3c752593d651d8290b674e
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 17%

---

# Anteprima e avvio di un’attività Consigli

Dopo aver creato l&#39;attività [!UICONTROL Recommendations], [!UICONTROL Test A/B] o [!UICONTROL Targeting esperienza] (XT) contenente [offerte Recommendations](/help/c-recommendations/recommendations-as-an-offer.md), è necessario visualizzare in anteprima i consigli per garantire che i risultati siano disponibili prima di avviare l&#39;attività. [!DNL Target Recommendations] offre diversi modi per visualizzare in anteprima i consigli.

## Verifica dello stato dell’algoritmo Recommendations

Dopo aver creato un&#39;attività, [!DNL Recommendations] esegue un algoritmo per generare consigli. L&#39;esecuzione di questo algoritmo potrebbe richiedere alcune ore.

Puoi verificare se l&#39;algoritmo ha terminato l&#39;esecuzione nel diagramma di panoramica [!UICONTROL Attività], dove è elencato lo stato dei criteri. L&#39;illustrazione seguente mostra lo stato nel diagramma attività in una pagina [!DNL Recommendations] dell&#39;attività [!UICONTROL Panoramica]:

![Pagina Panoramica dell’attività Recommendations](/help/c-recommendations/t-create-recs-activity/assets/recs-overview.png)

La figura seguente illustra lo stato di una pagina [!UICONTROL Test A/B] o dell&#39;attività XT [!UICONTROL Panoramica]:

![Pagina Panoramica del test A/B](/help/c-recommendations/t-create-recs-activity/assets/ab-overview.png)

I risultati dello stato includono quanto segue, come illustrato di seguito:

* [!UICONTROL Risultati pronti]: Indica che l’algoritmo ha restituito i risultati
* [!UICONTROL Risultati non pronti]: Indica che l&#39;algoritmo non è stato completato.
* [!UICONTROL Errore] feed: Indica che non è stato possibile recuperare il file di feed dei criteri personalizzati.

![Finestra di dialogo Risultati](/help/c-recommendations/c-algorithms/assets/criteria_status_multi.png)

## Quanto tempo ci vorrà per l&#39;esecuzione dell&#39;algoritmo?

Dopo aver salvato un&#39;attività contenente un criterio, [!DNL Target] calcola i consigli in base alla raccolta, ai criteri, alla progettazione e alle promozioni selezionate. Questo calcolo richiede un po&#39; di tempo e il periodo di tempo varia in base alla logica selezionata per le raccomandazioni, all&#39;intervallo di dati, al numero di elementi nel catalogo, alla quantità di dati comportamentali generati dai clienti e all&#39;origine selezionata per i dati comportamentali.

Quest’ultima influisce maggiormente sul tempo di elaborazione, come segue:

### mbox

Se come origini dei dati comportamentali sono selezionate delle mbox, i criteri creati vengono eseguiti subito. A seconda della quantità di dati comportamentali utilizzati e delle dimensioni del catalogo, l’esecuzione dell’algoritmo può richiedere fino a 12 ore. L’apporto di modifiche alla configurazione dei criteri comporta solitamente la riesecuzione dei criteri. A seconda della modifica apportata, i consigli calcolati in precedenza potrebbero non essere disponibili fino al completamento di una nuova esecuzione; in caso di modifiche di dimensioni maggiori, fino al completamento della nuova esecuzione sarà disponibile solo il contenuto di backup o predefinito. Se un algoritmo non viene modificato, viene rieseguito automaticamente da [!DNL Target] ogni 12-48 ore, a seconda dell’intervallo di dati selezionato.

### Adobe Analytics

Se il criterio utilizza [!DNL Adobe Analytics] come origine dei dati comportamentali, l’eventuale utilizzo della suite di rapporti e dell’intervallo di lookback selezionati per altri criteri incide sul tempo che trascorre prima che il criterio creato diventi disponibile.

* **Configurazione una tantum della suite di rapporti**: la prima volta che una suite di rapporti viene utilizzata con una specifica finestra di lookback dei dati, [!DNL Target Recommendations] può richiedere da due a sette giorni per scaricare completamente i dati comportamentali della suite di rapporti selezionata da [!DNL Analytics]. Il tempo necessario dipende dal caricamento del sistema [!DNL Analytics].
* **Criteri nuovi o modificati che utilizzano una suite** di rapporti già disponibile: Quando crei un nuovo criterio o modifichi un criterio esistente, se la suite di rapporti selezionata è già stata utilizzata con  [!DNL Target Recommendations], con un intervallo di dati uguale o inferiore a quello selezionato, i dati sono immediatamente disponibili e non è richiesta alcuna configurazione una tantum. In questo caso, oppure se le impostazioni di un algoritmo vengono modificate senza che si modifichi la suite di rapporti o l’intervallo di dati selezionato, l’algoritmo viene eseguito o rieseguito entro 12 ore.
* **Viene eseguito un algoritmo continuo**: i dati scorrono da [!DNL Analytics] a [!DNL Target Recommendations] su base giornaliera. Ad esempio, per un consiglio di tipo [!UICONTROL Affinità per articoli visualizzati], quando un utente visualizza un prodotto, a [!DNL Analytics] viene trasmessa una chiamata di tracciamento per visualizzazione prodotto quasi in tempo reale. I dati [!DNL Analytics] vengono inviati a [!DNL Target] all’inizio del giorno successivo e [!DNL Target] esegue l’algoritmo in meno di 12 ore.

>[!NOTE]
>
>[!UICONTROL Gli ] elementi visualizzati di recente non richiedono l’esecuzione di algoritmi offline e i risultati sono immediatamente disponibili. [!UICONTROL Gli algoritmi ] più visualizzati e  [!UICONTROL più ] avanzati basati sui dati mbox generalmente producono risultati molto rapidamente a causa del calcolo più semplice richiesto. Queste possono essere buone opzioni quando desideri visualizzare in anteprima una modifica della progettazione o confermare che i dati comportamentali vengono raccolti correttamente.

## Utilizzo di collegamenti QA per l’anteprima di Recommendations

Una volta che l&#39;algoritmo ha i risultati pronti, è possibile visualizzare in anteprima tali risultati utilizzando la funzionalità [QA link](/help/c-activities/c-activity-qa/activity-qa.md) di [!DNL Adobe Target]. I collegamenti QA sono disponibili nella sezione [!UICONTROL Controllo qualità delle attività] della pagina di panoramica Attività :

![Collegamento Controllo di qualità attività](/help/c-recommendations/t-create-recs-activity/assets/qa-link.png)

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Target] ti aggiunge automaticamente al pubblico richiesto per il collegamento Controllo qualità. Se questa impostazione è disattivata e l’attività dispone di regole di targeting, il profilo utente deve soddisfare tali regole di targeting per visualizzare l’esperienza contenente i consigli.

L’utilizzo di un collegamento di controllo qualità consente di visualizzare in anteprima i consigli sulla pagina:

![Prodotti consigliati](/help/c-recommendations/t-create-recs-activity/assets/featured-products.png)

>[!NOTE]
>
>* La modalità di controllo qualità di Target è &quot;persistente&quot; e viene salvata in un cookie. Se non esci dalla modalità di controllo qualità, continuerai a visualizzare i risultati del controllo qualità in tutto il sito. Per uscire dalla modalità di controllo qualità, utilizza il [bookmarklet](/help/c-activities/c-activity-qa/activity-qa-bookmark.md).
   >
   >
* In modalità Controllo qualità, la navigazione nel sito non influirà sugli [!UICONTROL Articoli visualizzati di recente] o [!UICONTROL Articoli acquistati di recente] del tuo profilo.&quot; Questo comportamento si verifica per progettazione per evitare l’inquinamento involontario dei dati comportamentali di produzione. Per visualizzare in anteprima i risultati di un criterio [!UICONTROL Articoli visualizzati di recente] o [!UICONTROL Recommendations basato su utente], sfoglia prima il sito al di fuori della modalità di controllo qualità, quindi utilizza la stessa sessione per aprire un collegamento alla modalità di controllo qualità.


## Utilizzo del download CSV per visualizzare in anteprima le raccomandazioni

In alcuni casi, potrebbe essere utile controllare gli elementi specifici consigliati. Questa funzione è particolarmente utile quando si utilizzano algoritmi come [!UICONTROL Persone che hanno visualizzato questo, hanno visualizzato che], in cui viene consigliato un diverso set di elementi a seconda dell&#39;elemento attualmente visualizzato dall&#39;utente e si potrebbero avere migliaia o milioni di elementi diversi nel catalogo.

I risultati non sono disponibili per il download finché non viene mostrato uno stato [!UICONTROL Risultati pronti] per almeno un algoritmo nell&#39;attività.

Per scaricare i risultati per l&#39;anteprima, fai clic sull&#39;icona del menu nell&#39;angolo in alto a destra della pagina Panoramica attività, quindi fai clic su **[!UICONTROL Scarica dati]**.

![Opzione Scarica dati](/help/c-recommendations/t-create-recs-activity/assets/download-data.png)

È in corso il download di un file CSV. Apri per visualizzare gli elementi consigliati:

![File CSV degli elementi consigliati](/help/c-recommendations/t-create-recs-activity/assets/recommended-items.png)

Da sinistra a destra è riportato un elenco di elementi consigliati, in questo caso quelli visualizzati più frequentemente. Le raccomandazioni sono separate da ambiente, in questo caso solo l’ambiente di produzione dispone di raccomandazioni. Per questo algoritmo, non sono state applicate restrizioni basate sul valore chiave, pertanto la riga etichettata con un asterisco (*) contiene il set completo di raccomandazioni. Per altri tipi di algoritmi basati su un valore chiave, ad esempio [!UICONTROL Persone che hanno visualizzato questo, hanno visualizzato che], i valori chiave (ovvero gli elementi &quot;This&quot;) sono elencati nella colonna più a sinistra e gli elementi consigliati (ovvero gli elementi &quot;That&quot;) sono elencati da sinistra a destra nelle colonne Recommendation_X.

>[!NOTE]
>
>I download dei risultati non sono disponibili per le attività contenenti un algoritmo [!UICONTROL Recommendations basato su utente]. I download dei risultati non sono disponibili per i criteri che utilizzano la logica per i consigli [!UICONTROL Articoli visualizzati di recente].

## Attivazione dell’attività Recommendations

Dalla scheda [!UICONTROL Panoramica attività], fai clic sulla freccia a discesa accanto allo stato, quindi seleziona **[!UICONTROL Attiva]**.

![Opzione Attiva](/help/c-recommendations/t-create-recs-activity/assets/activate.png)

Lo stato diventa [!UICONTROL Attivazione]:

![Attivazione](/help/c-recommendations/t-create-recs-activity/assets/activating.png)

Dopo alcuni secondi a un paio di minuti, lo stato passa a [!UICONTROL Live]:

![Live](/help/c-recommendations/t-create-recs-activity/assets/live.png)

Puoi anche disattivare o archiviare l’attività utilizzando lo stesso elenco a discesa.

## Evitare interruzioni durante la modifica delle impostazioni di Recommendations

La modifica delle raccolte [!DNL Recommendations], dei criteri, delle promozioni o delle impostazioni di progettazione in un&#39;attività live potrebbe comportare la mancata validità dei risultati dell&#39;algoritmo e la modifica dello stato di un algoritmo in [!UICONTROL Risultati non pronti].

Per evitare di interrompere un’attività live, è consigliabile adottare il seguente approccio quando modifichi un’attività live:

1. Duplica l’attività e i criteri da modificare.
1. Apporta modifiche all’attività e ai criteri duplicati e attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima della nuova attività modificata e verifica che i risultati siano come desiderato.
1. Attiva la nuova attività.
1. Disattiva la vecchia attività.

Se è necessario mantenere i risultati storici dei rapporti nella stessa attività, è possibile adottare un approccio alternativo che potrebbe causare un’interruzione temporanea della disponibilità dei consigli:

1. Duplica l’attività e i criteri da modificare.
1. Apporta modifiche all’attività e ai criteri duplicati e attendi che l’algoritmo generi risultati.
1. Visualizza l’anteprima della nuova attività modificata e verifica che i risultati siano come desiderato.
1. Sospendi l’attività esistente e scambia le impostazioni/i criteri con i nuovi criteri.
1. Visualizza l’anteprima dell’attività esistente e verifica che i risultati siano come desiderato.
1. Riattiva l’attività.
